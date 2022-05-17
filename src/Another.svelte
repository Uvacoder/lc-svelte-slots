<script>
  export let name = "default";
</script>

<div>
  Hello
  <slot name="firstName">
    <div>Default firstName goes here</div>
  </slot>
  <slot name="lastName">
    <div>Default lastName goes here</div>
  </slot>
</div>
