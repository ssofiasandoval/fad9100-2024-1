# 2024-04-19: encargo hacer formulario que me contacte a mi gmail.

## Investigación

Comencé buscando tutoriales de como hacerlo y aprendi que mi formulario debia tener un servidor, y hay servidores online, además que al codigo debía añadir las siguintes lineas que "activan el formulario"

```HTML
<form action="https://formspree.io/f/xvoevygz" method="POST">
  esta linea es nueva, pero no me resulto, incluso al presionar me
  lleva al php
  <input
    type="text"
    name="name"
    id="name"
    class="name"
    placeholder="NOMBRE"
  />
  <input
    type="text"
    name="mail"
    id="mail"
    class="email"
    placeholder="CORREO"
  />
  <input
    type="text"
    name="phone"
    id="subject"
    class="subject"
    placeholder="TELÉFONO"
  />
  <textarea
    name="message"
    class="message"
    placeholder="MENSAJE ... "
    id="message"
  ></textarea>
  <div class="clear"></div>
  <div class="col-md-8">
    <button type="submit" class="btn btn-primary">ENVIAR</button>
    <label>
      Your email:
      <input type="email" name="email" />
    </label>
    <label>
      Your message:
      <textarea name="message"></textarea>
    </label>
    <button type="submit">Send</button>
  </div>
</form>
```

Tambien aprendi a hacer un php

```PHP
<?php
$name = $_POST['name'];
$mail = $_POST['mail'];
$phone = $_POST['phone'];
$message = $_POST['message'];

$header = 'From: ' . $mail . " \r\n";
$header .= "X-Mailer: PHP/" . phpversion() . " \r\n";
$header .= "Mime-Version: 1.0 \r\n";
$header .= "Content-Type: text/plain";

$message = "Este mensaje fue enviado por: " . $name . " \r\n";
$message .= "Su e-mail es: " . $mail . " \r\n";
$message .= "Teléfono de contacto: " . $phone . " \r\n";
$message .= "Mensaje: " . $_POST['message'] . " \r\n";
$message .= "Enviado el: " . date('d/m/Y', time());

$para = 'sofia.sandoval@mail.udp.cl';
$asunto = 'Mensaje de... (Escribe como quieres que se vea el remitente de tu correo)';

mail($para, $asunto, utf8_decode($message), $header);

?>
```

y por lo que entendi hay que pagar entonces busque otra alternativa
link referido : <https://www.youtube.com/watch?v=FGJNC4bSztM>

Buscar referente portafolio, de como muestran su email Y me guie por
<https://itssharl.ee/fr/contact>
<img
  width="912"
  alt="Captura de pantalla 2024-04-18 a la(s) 10 46 29 p  m"
  src="https://github.com/ssofiasandoval/fad9100-2024-1/assets/128400293/564e6427-eda3-4864-af0f-b58f2bc7c9d3"
/>

y busque como hacerlo referido de:
<https://www.w3schools.com/html/tryit.asp?filename=tryhtml_links_email>
<img
  width="718"
  alt="Captura de pantalla 2024-04-18 a la(s) 11 23 07 p  m"
  src="https://github.com/ssofiasandoval/fad9100-2024-1/assets/128400293/0e869f22-f4a2-446f-a98f-081c3021debc"
/>

y lo logre jejeje y da el link mi correo
<img
  width="704"
  alt="Captura de pantalla 2024-04-18 a la(s) 11 23 44 p  m"
  src="https://github.com/ssofiasandoval/fad9100-2024-1/assets/128400293/eecac486-63be-4bbc-b99d-4c64d424a9e5"
/>
