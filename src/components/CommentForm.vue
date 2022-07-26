<template>
  <form class="comment-form" @submit.prevent="handleComment">
    <div class="form-control">
      <label for="name">Name</label>
      <input id="name" name="name" v-model="comment.name" />
    </div>

    <div class="form-control">
      <label for="message">Message</label>
      <textarea id="message" name="message" v-model="comment.message" rows="4"></textarea>
    </div>

    <button type="submit">Send Message</button>
  </form>
</template>

<script>
export default {
  props: ['postId'],
  data() {
    return {
      comment: {
        name: '',
        message: '',
      },
    };
  },
  methods: {
    async handleComment() {
      //console.log({ ...this.comment, url: this.$props.postId });
      await fetch(`https:/niicoe.co/v3/entry/github/shecodez/niicoe.co/master/comments`, {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({ fields: this.comment, options: { slug: this.$props.postId } }),
      });
    },
  },
};
</script>

<style scoped lang="scss">
.comment-form {
  .form-control {
    display: flex;
    flex-direction: column;

    label {
      font-size: medium;
      font-weight: bold;
    }

    input,
    textarea {
      padding: 1.2em;
      margin: 0.5em 0;
      background-color: var(--bg-code);
      border: transparent;
      border-radius: var(--radius);
      color: var(--body-color);
    }
  }

  button {
    padding: 0.5em 1.5em;
    margin: 1em 0;
    border-color: transparent;
    border-radius: var(--radius);
    font-size: large;
    font-weight: bold;
    text-transform: uppercase;
    background-color: var(--link-color);
  }
}
</style>
