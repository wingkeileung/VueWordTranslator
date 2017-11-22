<template>
  <div class="row" id="translateForm">
    <div class="col-md-2 mx-auto">
      <form id="transForm" class="well" v-on:submit="formSubmit">
        <input class="form-control" type="text" v-model="textToTranslate" placeholder="Enter a word...">
        <select class="form-control" v-model="language">
          <option value="ru">Russian</option>
          <option value="es">Spanish</option>
          <option value="fr">French</option>
          <option value="zh">Chinese</option>
          <option value="de">German</option>
          <option value="ko">Korean</option>
          <option value="vi">Vietnamese</option>
          <option value="th">Thai</option>
          <option value="tr">Turkish</option>
          <option value="fi">Finnish</option>
          <option value="cs">Czech</option>
          <option value="ja">Japanese</option>
        </select>
        <input class="btn btn-primary" type="submit" value="Translate">
      </form>
    </div>
  </div>
</template>

<script>

export default {
  name: 'translateForm',
  data() {
    return {
      textToTranslate:'',
      language:''
    }
  },
  created() {
    this.language = 'ru';
  },
  methods: {
    formSubmit (e) {
      this.$emit('formSubmit', this.textToTranslate, this.language);
      e.preventDefault();
    }
  }
}
</script>

<style>
  #transForm{
    border-radius: 10px;
    border: 1px #ccc solid;
  }
</style>