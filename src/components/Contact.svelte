<style>
  #contact {
    margin: 0 20px 80px 20px;

    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
  }

  .contact-text {
    margin: 10px;

    font-family: "Times New Roman", Times, serif;
    font-size: 24px;
    font-weight: 400;
    word-spacing: 2px;
    line-height: 36px;
  }

  p {
    margin-bottom: 20px;
  }

  .contact-form {
    width: 100%;
  }

  textarea,
  input {
    width: 100%;
    padding: 10px;
    border: solid #494949 3px;
    resize: none;
    font-family: "Times New Roman", Times, serif;
    font-size: 24px;
    font-weight: 400;
    word-spacing: 2px;
    line-height: 36px;
  }

  textarea {
    min-height: 200px;
  }

  input {
    min-height: 40px;
  }

  button {
    color: #494949;
    text-transform: uppercase;
    background: #ffffff;
    padding: 10px;
    border: 3px solid #494949;
    display: inline-block;
    transition: all 0.3s ease 0s;
    cursor: pointer;
  }

  button:hover {
    color: #c9ebfc;
    border-radius: 50px;
    border-color: #c9ebfc;
    transition: all 0.3s ease 0s;
  }

  @media screen and (min-width: 800px) {
    .contact-text {
      box-sizing: border-box;
      margin: 0;
      padding: 10px;
      width: 50%;
    }

    .contact-form {
      box-sizing: border-box;
      margin: 0;
      padding: 10px;
      width: 50%;
    }
  }
</style>

<div id="contact">
  <div class="contact-text">
    <p>Schicken sie uns gerne eine persönliche Nachricht.  </p>
    <p>
      Wir freuen uns auf Sie und wünschen Ihnen einen angenehmen Aufenthalt!
    </p>
  </div>
  <div class="contact-form">
    <form name="contact" method="POST" data-netlify="true">
      <p>
        <textarea name="message" placeholder="Ihre Nachricht..." />
      </p>
      <p>
        <input type="text" name="name" placeholder="Name" />
      </p>
      <p>
        <input type="email" name="email" placeholder="Email" />
      </p>
      <p>
        <button type="submit">Anfragen</button>
      </p>
    </form>
  </div>
</div>
