<template>
<div class="col-sm-6 col-md-4 col-lg-3">
    <div class="panel panel-default">
        <div class="panel-body quote">
            <slot></slot>
        </div>
    </div>
</div>


</template>

<script>
export default {};
</script>

<style scoped>
div {
  margin: 30px auto;
}

.panel-body {
  font-family: 'Arizonia', cursive;
  font-size: 24px;
  color: #6e6e6e;
  border: 0.5px solid #ccc;
  text-align: center;
  word-wrap: break-word;
  padding: 10px;
  font-style: italic;
}

.quote {
  cursor: pointer;
}

.quote:hover {
  background-color: #ffe2e2;
}
</style>
