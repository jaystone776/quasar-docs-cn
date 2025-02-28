---
title: Scroll Fire Directive
desc: 当用户滚动页面导致组件进入视口时触发一个函数的 Vue 指令。
keys: scroll-fire
related:
  - /vue-directives/scroll
  - /vue-directives/intersection
---
Scroll Fire 是一个指令，当用户滚动当前页面时，应用它的目标 DOM 元素(或组件)进入视口中，该指令允许调用一个方法(一次且仅一次)。

::: tip
还有一个[Scroll](/vue-directives/scroll)指令，每当用户滚动页面时就会触发。
:::

## ScrollFire API

<doc-api file="ScrollFire" />

## 用法

::: tip 滚动容器
请阅读 [这里](/vue-components/scroll-observer#确定滚动的容器) 了解 Quasar 如何 确定要附加滚动事件的容器。
:::

<doc-example title="Basic" file="ScrollFire/Basic" scrollable />

::: warning  重要
出于性能的考虑，注入的滚动侦听器函数在默认情况下将防抖 50ms。
:::
