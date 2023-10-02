<script>
  import EmailForm from "../../components/Contact/EmailForm.svelte";
  import ContactInfo from "../../components/Contact/ContactInfo.svelte";
</script>

<section class="container">
  <EmailForm />
  <ContactInfo />
</section>

<style>
  .container {
    height: 100vh;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
  }

  @media only screen and (max-width: 620px) {
    .container {
      flex-direction: column;
      justify-content: space-evenly;
    }
  }
</style>
