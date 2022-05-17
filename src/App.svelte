<script>
  import Another from "./Another.svelte";
  import ContactCard from "./ContactCard.svelte";

  export let name;
</script>

<main>
  <h1>Hello {name}!</h1>
  <div class="flex">
    <ContactCard>
      <h2 slot="name" class="custom-name">Andre Madarang</h2>
      <div slot="title" class="custom-title">Web Developer</div>
      <div slot="address">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="custom-svg h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          stroke-width="2"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"
          />
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"
          />
        </svg>
        <span>123 Address St.</span>
      </div>
      <div slot="phone">(123) 456-7890</div>
      <div slot="email">andre@andre.com</div>
    </ContactCard>

    <ContactCard>
      <h2 slot="name" class="custom-name-2">Elon Musk</h2>
      <div slot="title" class="custom-title-2">Tesla CEO</div>
      <div slot="address">321 Address St.</div>
      <div slot="phone">(321) 456-7890</div>
      <div slot="email">elon@musk.com</div>
    </ContactCard>
    <!-- <ContactCard
      name="Elon Musk"
      title="Tesla CEO"
      address="123 Address st."
      phone="(123) 123-1231"
      email="elon@musk.com"
    />
    <ContactCard
      name="Andre"
      title="Web Developer"
      address="123 Webdev st."
      phone="(123) 345-67890"
      email="andre@andre.com"
    /> -->
  </div>
  <!-- <Another>
    <h1 slot="firstName">Andre</h1>
    <h3 slot="lastName">Madarang</h3>
  </Another> -->
  <p>
    Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn
    how to build Svelte apps.
  </p>
</main>

<style>
  .custom-svg {
    height: 16px;
    width: 16px;
  }
  h2 {
    margin: 0;
  }
  .custom-name {
    color: red;
  }

  .custom-title {
    color: green;
  }
  .flex {
    display: flex;
    gap: 50px;
  }
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
