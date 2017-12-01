# canvas-barrage

基于canvas的弹幕发射器

[![Build Status](https://travis-ci.org/zhaofinger/canvas-barrage.svg?branch=master)](https://travis-ci.org/zhaofinger/canvas-barrage)

## Usage

```html
<canvas width='700' height='400'></canvas>
<script src="../lib/index.js"></script>
<script>
    let canvasEle = document.querySelector('canvas')
    let barrage = new Barrage(canvasEle)
    barrage.pushMessage({text: '弹幕发射，biu'})
</script>
```

## APIS

- `new Barrage(options)` - 构造函数，初始化

    | # | name | type | default | desc |
    | :--- | :--- |:--- | :--- | :--- |
    | 1 | `canvasDom` | `object` | `null` | 必填，`canvas` dom对象 |
    | 2 | `msgStackLength` | `number` | `300` | 最多弹幕数 |
    | 3 | `quality` | `number` | `20` | `canvas` 绘制频率, 每 `quality` 毫秒绘制一次，绘制频率越高越流畅同时对性能消耗也越高 |

- `.pushMessage(options)` - 发送弹幕

    | # | name | type | default | desc |
    | :--- | :--- |:--- | :--- | :--- |
    | 1 | `text` | `string` | '' | 必填，弹幕文字内容 |
    | 2 | `color` | `string` | 随机色 | 弹幕颜色，非指定的情况下随机取色 |
    | 3 | `speed` | `number` | 2到4的随机色 | 弹幕移动速度 |

- `.clear()` - 清除