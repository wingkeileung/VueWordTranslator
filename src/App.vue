<template>
  <div class="text-center" id="app">
    <h1>Word Translator</h1>
    <h5>Powered by Vue.js</h5>
    <TranslateForm v-on:formSubmit="translateText" id="form"></TranslateForm>
    <TranslateOutput v-text="translatedText"></TranslateOutput>
  </div>
</template>

<script>
import TranslateForm from './components/TranslateForm'
import TranslateOutput from './components/TranslateOutput';

export default {
  name: 'app',
  components:{
    TranslateForm,
    TranslateOutput
  },
  data: function () {
    return {
      translatedText: ''
    }
  },
  methods: {
    translateText:function(text, language){
      this.$http.get('https://translate.yandex.net/api/v1.5/tr.json/translate?key=trnsl.1.1.20171122T065659Z.36fc5a2cdbe57cb5.8dbf3517353d7ea706ca71a4dbe0792622382a4d&lang='+language+'&text='+text)
      .then((response) => {
        this.translatedText = response.body.text[0];
      });
    }
  }
}
</script>

<style>
  #form {
  background: #fefefe;
}
</style>
