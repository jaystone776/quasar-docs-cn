<template>
  <div class="q-px-xl q-py-md" style="max-width: 500px">
    <p>.q-col-gutter 将样式设置在子元素上</p>
    <div class="row">
      <div class="col bg-red-4 q-mt-lg">
        <div class="row q-col-gutter-lg">
          <div class="semi-transparent col-6 q-pa-md text-center" :class="`bg-green-${n+1}`" v-for="n in 5" :key="n">
            Child
          </div>
        </div>
      </div>
    </div>

    <q-separator class="q-my-md" />

    <p>.q-col-gutter 将样式设置在子元素内的元素中</p>
    <div class="row">
      <div class="col bg-red-4">
        <div class="row q-col-gutter-lg">
          <div class="col-6" v-for="n in 5" :key="n">
            <div class="q-pa-md text-center" :class="`bg-green-${n+1}`">
              Child
            </div>
          </div>
        </div>
      </div>
    </div>

    <q-separator class="q-my-md" />

    <p>.q-col-gutter 直接使用 QBtn 作为子元素</p>
    <div class="row">
      <div class="col bg-red-4 q-mt-lg">
        <div class="row q-col-gutter-lg">
          <q-btn class="semi-transparent col-6" color="primary" label="Button" v-for="n in 5" :key="`md-${n}`" />
        </div>
      </div>
    </div>

    <q-separator class="q-my-md" />

    <p>.q-col-gutter 将 QBtn 放在子元素中作为子元素的子元素</p>
    <div class="row">
      <div class="col bg-red-4">
        <div class="row q-col-gutter-lg">
          <div class="col-6" v-for="n in 5" :key="n">
            <q-btn class="full-width" color="primary" label="Button" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="sass">
.semi-transparent
  opacity: .7
</style>
