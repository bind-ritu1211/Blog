<template>
  <div class="w">
    <div class="home-intro__wrapper-img">
      <div>
          <div v-if="is_maincontent== true" class="row">
      <div class="home-intro__content m-90">
        <ul class="link">
          <li>
            <div class="header5">
              <h1> Lorem Ipsum is simply dummy text of the printing</h1>
              </div>
            </li>
            <li>
              <div class="header l">
                <h1> Lorem Ipsum is simply dummy text of the printing</h1>
                  <div class="text-justify m3">
                    <p>industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
                  </div>
              </div>
            </li>
        </ul>
        </div>
    </div>
    <div class="home-intro__content s head">
    <div class="head">
            <div v-if="is_maincontent== true" class="submit">
      <button type="submit" class="btn" @click="alertDisplay">
        Submit
      </button>
    </div>
    </div>
    <div v-if="is_popup==true">
      <div class="popup">
        <div class="j">
          <div class="c">
        <p>Your content has been submitted. </p>
          </div>
        </div>
        <div class="button">
          <button type="submit" class="btn ok-button" @click="closePopup">
            Ok
          </button>
        </div>
    </div>
    </div>
    </div>
    </div>
    </div>
      </div>
</template>

<script>
export default {
  data () {
    return {
      is_popup: false,
      is_maincontent: true
    }
  },
  methods: {
    alertDisplay () {
      this.is_popup = true
      this.is_maincontent = false
    },
    closePopup () {
      this.is_popup = false
      this.is_maincontent = true
    }
  }
}
</script>

      
<style>
 
.l{
  height: 56vh;
}

 .c{
padding: 4em;
margin: auto;
 }
.m-90{
  top: 50%;
}

.header5 {
    background: #C2EFEF;
    border-radius: 22px;
    margin-top: 3em;
    padding-top: 2px;
    height: 13vh;
}
.button-ok{
background: #C2EFEF;
border-radius: 4px;
border: none;
margin-top: 4em;
width: 10%;
height: 42px;
}

.s{
  top: 100%;
    }

.btn{
  border: none;
  background: #C2EFEF;
  width: 10%;
  margin: 3em;
padding: 16px;

}

.j{
  background: #C2EFEF;
    border-radius: 22px;
  width: 50%;
    height: 25vh;
    margin: auto;
    margin-top: -25em;
}
</style>