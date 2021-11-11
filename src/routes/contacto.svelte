<script>
  import Header from '../components/Header.svelte';
  import Button from '../components/Button.svelte'

  let name = ''
  let email = ''
  let tel = ''
  let comment = ''
  let msg = ''
  let showLoading = false
  const url = process.env.API_URL

  function validateEmail(email) {
    const re = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
    return re.test(String(email).toLowerCase());
  }

  async function sendEmail(data) {
    const response = await fetch(url, {
      method: 'POST',
      mode: 'cors',
      cache: 'no-cache',
      credentials: 'same-origin',
      headers: {
        'Content-Type': 'application/json'
      },
      redirect: 'follow',
      referrerPolicy: 'no-referrer',
      body: JSON.stringify(data),
    });

    return response.json();
  }

  async function formHandler(event) {
    event.preventDefault()
    msg = ''
    showLoading = false

    if (!name || !email || !tel || !comment) {
      msg = "Favor de llenar todos los campos"
      return null
    }
    if (!validateEmail(email)) {
      msg = "Favor de proporcionar un correo válido"
      return null
    }

    const emailData = {
      from: email, 
      subject: 'Website Form: Hotel México',
      message: `
        <strong>name:</strong> ${name}<br />
        <strong>email:</strong> ${email}<br />
        <strong>tel:</strong> ${tel}<br />
        <strong>comment:</strong> ${comment}
      `,
    }

    try {
      showLoading = true
      const response = await sendEmail(emailData)

      if (response && response.response && response.response.body && Array.isArray(response.response.body.errors) && response.response.body.errors.length) {
        msg = response.response.body.errors[0].message
      } else {
        msg = "Mensaje enviado."
        
        name = ''
        email = ''
        tel = ''
        comment = ''
      }
    } catch(error) {
      msg = "Error, favor de intentar más tarde."
    }
    showLoading = false
  }
</script>

<style> 
  section {
    font-family: gotham;
  }

  .block-1 {
    max-width: 1000px;
    margin: 0 auto;
    display: flex;
    padding: 100px 0;
  }
  strong {
    text-transform: uppercase;
    display: block;
    font-weight: 100;
    font-size: 18px;
    padding-bottom: 10px;
  }
  .location {
    width: 589px;
  }
  .location-icon {
    width: 28px;
  }
  .facebook-icon {
    width: 11px;
  }
  .instagram-icon {
    width: 22px;
    padding-left: 6px;
  }
  .email-icon {
    width: 30px;
  }
  .gmaps-link {
    position: relative;
    left: 175px;
    text-decoration: none;
    border-bottom: 1px solid;
    padding-bottom: 3px;
    color: var(--color-almendra)
  }
  .location p {
    display: flex;
    align-items: center;
    margin-bottom: 40px;
  }
  span {
    padding-left: 10px;
  }

  form {
    width: 414px;
  }
  input, textarea {
    border: 2px solid var(--color-almendra);
    width: 100%;
    font-size: 20px;
    box-sizing: border-box;
  }
  textarea {
    height: 180px;
  }
  input {
    height: 40px;
  }
  .loader {
    border: 6px solid var(--color-hueso);
    border-top: 6px solid var(--color-almendra);
    border-radius: 50%;
    width: 20px;
    height: 20px;
    animation: spin 1.5s linear infinite;
  }
  @keyframes spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
  }

  .separator {
    border-bottom: 5px dashed var(--color-almendra);
    height: 10px;
    max-width: 1280px;
    margin: 0 auto;
    padding: 0 50px;
    position: relative;
    top: 3px;
  }

  .block-2 {
    padding: 100px 0;
    background-color: var(--color-background);
    width: 100%;
    text-align: center;
  }
  .xx {
    padding: 60px 0;
    width: 30px;
  }
  .yelp-icon {
    height: 35px;
    margin-right: 20px;
  }
  .tripadvisor-icon {
    height: 35px;
  }
  .reserva {
    display: inline-flex;
    align-items: center;
    height: 50px;
    text-transform: uppercase;
    font-family: gotham;
    font-size: 25px;
    padding: 8px 180px 0;
    text-decoration: none;
    background-color: var(--color-almendra);
    color: white;
  }

  .note {
    color: var(--color-almendra);
    font-size: 14px;
  }

  iframe {
    width: 500px;
    height: 300px;
  }

  @media (max-width: 480px) {
    .block-1 {
      padding-top: 40px;
    }
    iframe {
      width: 100%;
    }
    .block-1 {
      display: block;
    }
    .location {
      width: auto;
    }
    form {
      width: auto;
    }
    .gmaps-link {
      position: absolute;
      left: auto;
      right: 12px;
    }
    .reserva {
      padding: 8px 0;
      width: 100%;
      text-align: center;
      display: inline-block;
      line-height: 57px;
    }
    .content {
      padding: 0 12px;
    }
  }
</style>

<Header
  backgroundImage="/contacto/header.jpg"
  bannerHeight="500"
/>

<div class="content">
  <section class="block-1">
    <div class="location">
      <strong>ubicación</strong>
      <iframe title="ubicación" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3383.031220398899!2d-116.6290347843266!3d32.01426798120903!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x80d8efce960d5019%3A0x7366b9aeb37f8db7!2sM%C3%A9xico%20en%20la%20piel!5e0!3m2!1sen!2smx!4v1636645438067!5m2!1sen!2smx" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
      <p>
        <img class="location-icon" src="/support/pin-location.svg" alt="">
        <span>Vallle de Guadalupe, <br />
          22766 Ensenada, BC, México</span>
        <a class="gmaps-link" href="https://goo.gl/maps/RTzByVDUc2jHMF178" target="_blank">Google Maps</a>
      </p>
      <p>
        <a href="https://www.facebook.com/hotelmexicoenlapiel" target="_blank">
          <img class="facebook-icon" src="/support/facebook-small.svg" alt="">
        </a>
        <a href="https://www.instagram.com/hotelmexicoenlapiel/?hl=en" target="_blank">
          <img class="instagram-icon" src="/support/instagram-small.svg" alt="">
        </a>
        <span>/ hotelmexicoenlapiel</span>
      </p>
      <p>
        <img class="email-icon" src="/support/email.svg" alt="">
        <span>hola@hotelmexicoenlapiel.com</span>
      </p>
    </div>

    <form action="">
      <p>
        <strong>nombre y apellido</strong>
        <input type="text" bind:value={name}>
      </p>
      <p>
        <strong>correo electrónico</strong>
        <input type="text" bind:value={email}>
      </p>
      <p>
        <strong>teléfono</strong>
        <input type="text" bind:value={tel}>
      </p>
      <p>
        <strong>interés/comentario</strong>
        <textarea name="" id="" cols="30" rows="10" bind:value={comment}></textarea>
      </p>
      <p>
        <Button onclick={formHandler} href="/" className="small-arrow-almendra color-almendra">enviar</Button>
      </p>
      <p class="error">
        {msg}
      </p>
      {#if showLoading}
        <div class="loader"></div>
      {/if}
    </form>
  </section>
</div>

<div class="separator"></div>

<section class="block-2">
  <div class="content">
    <a class="reserva" href="http://www.airbnb.com/p/hotelmexicoenlapiel" target="_blank">reserva ahora</a>

    <p class="note">
      *Reservaciones deben de hacerse con 15 días <br /> de anticipación para confirmar y procesar.
    </p>

    <p>
      <img class="xx" src="/support/xx.svg" alt="">
    </p>

    <p>
      <a href="https://www.yelp.com/" target="_blank">
        <img class="yelp-icon" src="/support/yelp-large.svg" alt="">
      </a>
      <a href="https://www.tripadvisor.com/Hotel_Review-g150770-d23673959-Reviews-Mexico_en_la_Piel-Ensenada_Ensenada_Municipality_Baja_California.html" target="_blank">
        <img class="tripadvisor-icon" src="/support/tripadvisor-large.svg" alt="">
      </a>
    </p>
  </div>
</section>
