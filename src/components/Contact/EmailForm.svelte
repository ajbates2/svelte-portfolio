<script>
  import { PUBLIC_EMAIL_KEY } from "$env/static/public";

  let contact = {
    name: "",
    email: "",
    subject: "",
    honeypot: "",
    message: "",
    accessKey: PUBLIC_EMAIL_KEY,
  };

  /**@type boolean*/
  let isMessageSent = false;

  const handleChange = (e) => {
    contact = { ...contact, [e.target.name]: e.target.value };
  };

  const handleSubmit = async (e) => {
    e.preventDefault();
    try {
      const res = await fetch("https://api.staticforms.xyz/submit", {
        method: "POST",
        body: JSON.stringify(contact),
        headers: { "Content-Type": "application/json" },
      });

      const json = await res.json();

      if (json.success) {
        isMessageSent = true;
      } else {
        alert(json.message);
      }
    } catch (e) {
      console.log("An error occurred", e);
      alert(e);
    }
  };
</script>

<div>
  {#if isMessageSent}
    <p>Thank you {contact.name} for reaching out!</p>
  {:else}
    <form
      action="https://api.staticforms.xyz/submit"
      method="post"
      on:submit={handleSubmit}
    >
      <span>Name</span>
      <input type="text" name="name" required on:change={handleChange} />
      <span>Subject</span>
      <input type="text" name="subject" required on:change={handleChange} />
      <span>Email</span>
      <input type="email" name="email" required on:change={handleChange} />
      <span>Message</span>
      <textarea name="message" required on:change={handleChange} />
      <button type="submit"> Say Hello! </button>
      <input type="text" name="honeypot" style="display: none;" />
    </form>
  {/if}
</div>

<style>
  div {
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: var(--red);
    width: 600px;
    height: 422px;
    padding: 2em;
    border-radius: 10px;
    box-shadow: -4px 20px 36px 8px var(--background);
    transition: all 0.2s ease-out;
  }

  form {
    width: 100%;
    display: flex;
    align-items: flex-start;
    justify-content: space-evenly;
    flex-direction: column;
  }

  form input {
    width: 100%;
    border: none;
    border-radius: 4px;
    height: 2lh;
    background-color: var(--foreground);
    box-shadow: 2px 2px 10px var(--glass-background);
    margin-bottom: 12px;
  }

  form textarea {
    width: 100%;
    height: 6lh;
    border: none;
    border-radius: 4px;
    background-color: var(--foreground);
    box-shadow: 2px 2px 10px var(--glass-background);
    resize: none;
    margin-bottom: 12px;
  }

  form span {
    color: var(--foreground);
    margin-bottom: 4px;
    font-size: 0.8rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
  }

  button {
    width: 100%;
    background-size: 220%;
    border: none;
    box-shadow: 2px 2px 10px var(--glass-background);
    color: var(--red);
    background-position: 100%;
    text-transform: uppercase;
    padding: 15px 20px;
    border-radius: 4px;
    transition: all 0.2s ease-out;
    font-weight: 400;
    cursor: pointer;
    letter-spacing: 2px;
    background-image: linear-gradient(
      110deg,
      var(--pink) 0%,
      var(--red) 50%,
      transparent 50%,
      transparent 100%
    );
    font-size: 14px;
    background-color: var(--background);
    margin-top: 8px;
  }

  button:hover {
    transform: translateY(-2px);
    box-shadow: 4px 4px 10px var(--glass-background);
    background-position: 0;
    color: var(--foreground);
  }

  @media only screen and (max-width: 620px) {
    div {
      width: 90vw;
    }
  }
</style>
