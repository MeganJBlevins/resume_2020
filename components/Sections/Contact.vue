<template>
  <section id="contact">
    <div class="container">
      <div class="section-title">
        <h1>Contact Me</h1>
      </div>
    </div>
    <div class="container">
      <form>
        
          <fieldset>
            <label for='name'>Name</label>
            <input type="text" name="name" />
          </fieldset>
          <div class="columns">
            <div class="column is-one-half">
              <fieldset class="">
                <label for='email'>Email</label>
                <input type="email" name="email" required/>
              </fieldset>
            </div>
            <div class="column is-one-half">
              <fieldset>
                <label for='tel'>Telephone</label>
                <input type="tel" name="tel" />
              </fieldset>
            </div>
          </div>
          <fieldset>
            <label for='message'>Message</label>
            <input type="textarea" name="message" />
          </fieldset>
        <button type="submit" class="button is-primary">Send Message</button>
      </form>
    </div>
  </section>
</template>
<script>
export default {
  name: "Contact"
}
</script>