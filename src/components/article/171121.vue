<template>
  <o-card class="card171121 dark" :lang="['html', 'css']" title="RadioGroupSkin" :author="author" :date="1511232639328">
    <div class="line">缘 <o-radio-group :data="data1" v-model="radio1" class="kuro"></o-radio-group> {{radio1}}</div>
    <div class="line s">🍎 <o-radio-group :data="data2" v-model="radio2" class="kuro s"></o-radio-group> {{radio2}}</div>
  </o-card>
</template>

<script>
  import oRadioGroup from '@/components/base/radioGroup';
  import oCard from '@/components/ui/card';
  import author from '@/libs/author';

  export default {
    components: {
      oRadioGroup,
      oCard
    },
    data() {
      return {
        author: author.shiro,
        radio1: '',
        data1: [
          {name: '妙', value: 'miao', disabled: false},
          {name: '不', value: 'bu', disabled: false},
          {name: '可', value: 'ke', disabled: true},
          {name: '言', value: 'yan', disabled: false}
        ],
        radio2: '🍊',
        data2: [
          {name: '西瓜🍉', value: '🍉'},
          {name: '橘子🍊', value: '🍊'},
          {name: '草莓🍓', value: '🍓'}
        ]
      };
    }
  };
</script>

<style lang="scss">
  .card171121 {
    .line {
      font-size: .14rem;
      text-align: left;
      margin-bottom: .5em;
      color: #fff;
      &.s {
        font-size: 12px;
      }
    }
  }
</style>