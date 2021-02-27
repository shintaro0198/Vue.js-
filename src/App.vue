<template>
  <div id="App">
    <div class="tab">
      <input type="radio" id="menu1" value="1" v-model="isActive">
      <label for="menu1">タブメニュー１</label>
      <input type="radio" id="menu2" value="2" v-model="isActive">
      <label for="menu2">タブメニュー２</label>
      <input type="radio" id="menu3" value="3" v-model="isActive">
      <label for="menu3">タブメニュー３</label>
    </div>
    <ul>
      <li v-if="isActive==='1'">
        コンテンツ１コンテンツ１コンテンツ１コンテンツ１コンテンツ１コンテンツ１コンテンツ１コンテンツ１コンテンツ１
      </li>
      <li v-else-if="isActive==='2'">
        コンテンツ２コンテンツ２コンテンツ２コンテンツ２コンテンツ２コンテンツ２コンテンツ２コンテンツ２コンテンツ２
      </li>
      <li v-else-if="isActive==='3'">
        コンテンツ３コンテンツ３コンテンツ３コンテンツ３コンテンツ３コンテンツ３コンテンツ３コンテンツ３コンテンツ３
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data(){
    return{
      isActive:'1'
    }
  }
}
</script>
<style scoped>

label{
  padding: 20px;
  height: 25px;
  line-height: 25px;
}
input :checked + label{
  background-color: black;
  color:white}
ul{
  padding: 20px;
  border:gray solid 1px;
  list-style: none;
}
</style>