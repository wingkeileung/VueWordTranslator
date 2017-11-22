<template>
  <div class="row" id="translateForm">
    <div class="col-md-2 mx-auto">
      <form id="transForm" class="well" v-on:submit="formSubmit">
        <input class="form-control" type="text" v-model="textToTranslate" placeholder="Enter a word...">
        <select class="form-control" v-model="language">
          <option value="en">English</option>
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
          <option value="el">Greek</option>
          <option value="ja">Japanese</option>
          <option value="az">Azerbaijan</option>
          <option value="sq">Albanian</option>
          <option value="am">Amharic</option>
          <option value="ar">Arabic</option>
          <option value="hy">Armenian</option>
          <option value="af">Afrikaans</option>
          <option value="eu">Basque</option>
          <option value="ba">Bashkir</option>
          <option value="be">Belarusian</option>
          <option value="bn">Bengali</option>
          <option value="my">Burmese</option>
          <option value="bg">Bulgarian</option>
          <option value="bs">Bosnian</option>
          <option value="cy">Welsh</option>
          <option value="hu">Hungarian</option>
          <option value="ht">Haitian (Creole)	</option>
          <option value="gl">Galician</option>
          <option value="mrj">Hill Mari	</option>
          <option value="ka">Georgian</option>
          <option value="gu">Gujarati</option>
          <option value="ru">Russian</option>
          <option value="da">Danish</option>
          <option value="he">Hebrew</option>
          <option value="id">Indonesian</option>
          <option value="ga">Irish</option>
          <option value="it">Italian</option>
          <option value="is">Icelandic</option>
          <option value="kk">Kazakh</option>
          <option value="kn">Kannada</option>
          <option value="ca">Catalan</option>
          <option value="ky">Kyrgyz</option>
          <option value="xh">Xhosa</option>
          <option value="km">Khmer</option>
          <option value="lo">Laotian</option>
          <option value="la">Latin</option>
          <option value="lv">Latvian</option>
          <option value="lt">Lithuanian</option>
          <option value="lb">Luxembourgish</option>
          <option value="mg">Malagasy</option>
          <option value="ms">Malay</option>
          <option value="ml">Malayalam</option>
          <option value="mt">Maltese	</option>
          <option value="mk">Macedonian</option>
          <option value="mi">Maori</option>
          <option value="mr">Marathi</option>
          <option value="mhr">Mari</option>
          <option value="mn">Mongolian</option>
          <option value="ne">Nepali</option>
          <option value="no">Norwegian</option>
          <option value="pa">Punjabi</option>
          <option value="pap">Papiamento</option>
          <option value="fa">Persian</option>
          <option value="pl">Polish</option>
          <option value="pt">Portuguese</option>
          <option value="ro">Romanian</option>
          <option value="ceb">Cebuano</option>
          <option value="sr">Serbian</option>
          <option value="si">Sinhala</option>
          <option value="sk">Slovakian</option>
          <option value="sl">Slovenian</option>
          <option value="sw">Swahili</option>
          <option value="su">Sundanese</option>
          <option value="tl">Tajik</option>
          <option value="ta">Tamil</option>
          <option value="tt">Tatar</option>
          <option value="te">Telugu</option>
          <option value="tr">Turkish</option>
          <option value="udm">Udmurt</option>
          <option value="uz">Uzbek</option>
          <option value="uk">Ukrainian</option>
          <option value="ur">Urdu</option>
          <option value="hi">Hindi</option>
          <option value="hr">Croatian</option>
          <option value="sv">Swedish</option>
          <option value="gd">Scottish</option>
          <option value="et">Estonian</option>
          <option value="eo">Esperanto</option>
          <option value="jv">Javanese</option>
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
    this.language = 'en';
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