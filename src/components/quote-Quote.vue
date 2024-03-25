<template>
  <section class="quote">
    <div class="quote-content">{{quote.content}}</div>
    <div class="quote-info">
    <div class="quote-anime">{{quote.anime}}</div>
    <div class="quote-author">{{quote.character}}</div>
    </div>
  </section>
</template>

<script>
export default {
props:['quote']
}
</script>

<style lang='scss' scoped>
.quote{
    position: relative ;
    margin: 0 auto;
    padding: 32px;
    max-width: 720px;

}
.quote-content{
    position: relative;
    font-size: 1.5rem;
    font-weight: 600;
    background-color: rgb(49, 49, 49);
    color: rgb(222, 230, 233);
    padding: 48px 32px;
    border-radius: 16px;
    &::before , &::after{
      content: '"';
      margin: 8px 8px ;
    }
}
.quote-info{
  position: relative;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  padding: 32px;
}
.quote-author , .quote-anime{
  position: absolute;
  padding: 12px 16px;
  font-size: 24px;
  font-weight: 700;
  border-radius: 99px;
  color: rgb(217, 225, 227);
  text-align: center;
// top: -200%;
// right: 88%;
// background-color: rgb(122, 130, 132);
// border-radius: 8px;
}
.quote-author{
  transform: translateY(-50%);
background-color: rgb(195, 96, 96);
  // top:calc(100% - 32px);
right:-5%;
top:0%


}
.quote-anime{
left: 0%;
top: -230%;
left: -5%;
background-color: aqua;
color: rgb(58, 67, 98);
}
</style>