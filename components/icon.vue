<template>
  <svg
    class="icon"
    v-if="name === 'search'"
    width="20"
    height="20"
    viewBox="0 0 24 24"
    fill="white"
  >
    <path
      d="M15.5 14h-.79l-.28-.27C15.41 12.59 16 11.11 16 9.5 16 5.91 13.09 3 9.5 3S3 5.91 3 9.5 5.91 16 9.5 16c1.61 0 3.09-.59 4.23-1.57l.27.28v.79l5 4.99L20.49 19l-4.99-5zm-6 0C7.01 14 5 11.99 5 9.5S7.01 5 9.5 5 14 7.01 14 9.5 11.99 14 9.5 14z"
    />
  </svg>
  <svg
    class="icon"
    v-else-if="name === 'arrow_down'"
    width="24"
    height="24"
    viewBox="0 0 24 24"
    fill="white"
  >
    <path d="M7.41 7.84L12 12.42l4.59-4.58L18 9.25l-6 6-6-6z" />
  </svg>
  <svg
    class="icon"
    v-else-if="name === 'play_button'"
    viewBox="0 0 24 24"
    width="34"
    height="30"
    fill="#fd6060"
  >
    <path d="M8 5v14l11-7z" />
  </svg>

  <!-- keyboard_arrow_up -->
  <svg
    v-else-if="name === 'arrow_up'"
    class="icon"
    width="24"
    height="24"
    viewBox="0 0 24 24"
    fill="white"
  >
    <path d="M7.41 15.41L12 10.83l4.59 4.58L18 14l-6-6-6 6z" />
  </svg>
  <!-- person -->
  <svg
    v-else-if="name === 'person'"
    class="icon"
    width="24"
    height="24"
    viewBox="0 0 24 24"
    fill="white"
  >
    <path
      d="M12 12c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm0 2c-2.67 0-8 1.34-8 4v2h16v-2c0-2.66-5.33-4-8-4z"
    />
  </svg>

  <!-- settings -->
  <svg
    v-else-if="name === 'setting'"
    class="icon"
    width="24"
    height="24"
    viewBox="0 0 24 24"
    fill="white"
  >
    <path
      d="M19.43 12.98c.04-.32.07-.64.07-.98s-.03-.66-.07-.98l2.11-1.65c.19-.15.24-.42.12-.64l-2-3.46c-.12-.22-.39-.3-.61-.22l-2.49 1c-.52-.4-1.08-.73-1.69-.98l-.38-2.65C14.46 2.18 14.25 2 14 2h-4c-.25 0-.46.18-.49.42l-.38 2.65c-.61.25-1.17.59-1.69.98l-2.49-1c-.23-.09-.49 0-.61.22l-2 3.46c-.13.22-.07.49.12.64l2.11 1.65c-.04.32-.07.65-.07.98s.03.66.07.98l-2.11 1.65c-.19.15-.24.42-.12.64l2 3.46c.12.22.39.3.61.22l2.49-1c.52.4 1.08.73 1.69.98l.38 2.65c.03.24.24.42.49.42h4c.25 0 .46-.18.49-.42l.38-2.65c.61-.25 1.17-.59 1.69-.98l2.49 1c.23.09.49 0 .61-.22l2-3.46c.12-.22.07-.49-.12-.64l-2.11-1.65zM12 15.5c-1.93 0-3.5-1.57-3.5-3.5s1.57-3.5 3.5-3.5 3.5 1.57 3.5 3.5-1.57 3.5-3.5 3.5z"
    />
  </svg>
  <!-- star -->
  <svg
    v-else-if="name === 'star'"
    class="icon"
    width="24"
    height="24"
    viewBox="0 0 24 24"
    fill="white"
  >
    <path
      d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"
    />
  </svg>
  <!-- sign-out -->
  <svg
    v-else-if="name === 'sign_out'"
    class="icon"
    width="24"
    height="24"
    viewBox="0 0 24 24"
    fill="white"
  >
    <path d="M7 7v10h5v3H4V4h8v3H7z" />
    <path d="M15 10h-5v4h5v2l5-4-5-4v2z" />
  </svg>
</template>

<script>
export default {
  props: ["name"]
};
</script>

<style>
.icon {
  z-index: 10;
}
</style>
