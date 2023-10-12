<script>
  import GitHubIcon from "~icons/ion/logo-github";
  import MailIcon from "~icons/ion/mail";
  import ResumeIcon from "~icons/ion/document-text";
  import LinkedInIcon from "~icons/ion/logo-linkedin";
</script>

<address>
  <div>
    <a
      href="mailto:aj.bates2.92@gmail.com"
      target="_blank"
      rel="noreferrer"
      title="Email"
    >
      <MailIcon />
    </a>
    <aside>Email</aside>
  </div>
  <div>
    <a
      href="https://www.linkedin.com/in/ajbates2/"
      target="_blank"
      rel="noreferrer"
      title="LinkedIn Profile"
    >
      <LinkedInIcon />
    </a>
    <aside>LinkedIn</aside>
  </div>
  <div>
    <a
      href="https://github.com/ajbates2"
      target="_blank"
      rel="noreferrer"
      title="GitHub Profile"
    >
      <GitHubIcon />
    </a>
    <aside>GitHub</aside>
  </div>
  <div>
    <a
      href="/AJ_Bates_Resume.pdf"
      type="resume/pdf"
      title="Resume"
      target="_blank"
    >
      <ResumeIcon />
    </a>
    <aside>Resume</aside>
  </div>
</address>

<style>
  address {
    width: 400px;
    height: 400px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
  }

  div {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  div a {
    font-size: 2.5rem;
    filter: drop-shadow(2px 2px 3px var(--background));
    transition: all 0.2s ease-out;
  }

  div a:hover {
    transform: translateY(-2px);
    filter: drop-shadow(2px 4px 3px var(--charcoal));
    color: var(--red);
  }

  div aside {
    font-size: 12px;
    font-weight: 100;
    font-style: italic;
  }

  @media only screen and (max-width: 620px) {
    address {
      flex-direction: row;
      height: 100px;
    }
  }
</style>
