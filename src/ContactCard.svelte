<script>
  export let name = "No Name";
  export let title = "Job Title";
  export let address = "Default address";
  export let phone = "(111) 111-1111";
  export let email = "email@email.com";
</script>

<div class="contact-card">
  <slot name="name"><h2>No Name</h2></slot>
  <slot name="title"><div>No Title</div></slot>
  <hr />
  <div class="info">
    <slot name="address"><div>No Address</div></slot>
    <slot name="phone"><div>No Phone</div></slot>
    <slot name="email"><div>No Email</div></slot>
  </div>
  <!-- <h2>{name}</h2>
  <div>{title}</div>
  <hr />
  <div class="info">
    <div>{address}</div>
    <div>{phone}</div>
    <div>{email}</div>
  </div> -->
</div>

<style>
  .contact-card .name {
    color: red;
  }
  .contact-card {
    box-shadow: 2px 2px 8px rgba(0, 0, 0, 0.2);
    max-width: 300px;
    width: 300px;
    padding: 30px 20px;
    text-align-last: left;
    line-height: 1.5;
  }

  .contact-card h2 {
    margin: 0;
  }

  .contact-card .info {
    margin-top: 16px;
  }
</style>
