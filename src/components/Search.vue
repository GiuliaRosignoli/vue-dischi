<template>
  <div class="search">
      <input type="text" placeholder="Search Album"  v-model="searchText">
      <span class="frame">
          <button class="mg custom-btn btn-8" @click.prevent="$emit('performSearch', searchText)">Search</button>
          <button class="custom-btn btn-8" @click="resetSearch">Reset</button>
      </span>
      
  </div>
</template>

<script>
export default {
    name: "Search",
    data(){
        return {
             searchText: "",

        };
    },
    methods: {
        resetSearch() {
            this.searchText= "",
            this.$emit('performSearch', this.searchText)
        }
    }

}
</script>

<style lang="scss" scoped>
@import "../assets/styles/general.scss"; 
@import "../assets/styles/vars.scss";
@import "../assets/styles/utilities.scss";

.search {
    padding-top: 30px;
    text-align: center;
    input {
        width: 18rem;
        height: 1.9rem;
        padding: 10px;
    }
}

/* Buttons */

.frame {
  width: 70%;
  margin: 30px auto;
  text-align: center;
}
button {
  margin: 12px;
}

.custom-btn {
  width: 110px;
  height: 40px;
  color: #fff;
  border-radius: 50px;
  padding: 8px 18px;
  font-family: 'Lato', sans-serif;
  font-weight: 500;
  font-size: 14px;
  background: transparent;
  cursor: pointer;
  transition: all 0.3s ease;
  position: relative;
  display: inline-block;
   box-shadow: inset 2px 2px 2px 0px rgba(255,255,255,.5),
    inset -7px -7px 10px 0px rgba(0,0,0,.1),7px 7px 20px 0px rgba(0,0,0,.1),
   4px 4px 5px 0px rgba(0,0,0,.1);
  text-shadow:  2px 2px 3px rgba(255,255,255,.5),
              -4px -4px 6px rgba(116, 125, 136, .2);
  outline: none;
}

.btn-8 {
  background-color: #5537b1;
  color: #e8e8e9;
  line-height: 42px;
  padding: 0;
  border: none;
}
.btn-8 span {
  position: relative;
  display: block;
  width: 100%;
  height: 100%;
}
.btn-8:before,
.btn-8:after {
  position: absolute;
  content: "";
  right: 0;
  bottom: 0;
  background: #c797eb;
  transition: all 0.3s ease;
}
.btn-8:before{
   height: 0%;
   width: 2px;
}
.btn-8:after {
  width: 0%;
  height: 2px;
}
.btn-8:hover:before {
  height: 100%;
}
.btn-8:hover:after {
  width: 100%;
}
.btn-8:hover{
  background: transparent;
}
.btn-8 span:hover{
  color: #c797eb;
}
.btn-8 span:before,
.btn-8 span:after {
  position: absolute;
  content: "";
  left: 0;
  top: 0;
  background: #c797eb;
  transition: all 0.3s ease;
}
.btn-8 span:before {
  width: 2px;
  height: 0%;
}
.btn-8 span:after {
  height: 2px;
  width: 0%;
}
.btn-8 span:hover:before {
  height: 100%;
}
.btn-8 span:hover:after {
  width: 100%;
}

</style>