# 数字谱扩展集，语法计划

## 声明调式速度拍号

默认为 **C** 大调 每分钟 **120** 拍 **4/4** 拍

### 方式一

```
@C120: Number Sheet @G: Number Sheet ; 不改变部分可以省略不写
```

### 方式二 √

```
NMSBEGIN
    1=C
    BPM=120
    4/4
NMSEND

Number Sheet

NMSBEGIN
    BPM=140
NMSEND

Number Sheet
```

## 声明音轨
```
$1: Number Sheet 
$2: Number Sheet 
$3: Number Sheet 
.
.
.
```
**三和弦示范**
```
$1: 1 6 4 5 1 ---
$2: 0 0 0 0(5)---
$3:(3)0 0 0(3)---
```
; 有可能出现某一轨大多时候都是0的沙雕情况，想一个可以在任意位置加入另一个音轨的语法

## 音符时值

默认数字为四分音符<br>
```
四分音符   :  note1 note2 ...
八分音符   : 'note1 note2 ...'
十六分音符 : "note1 note2 ..."
二分音符   :  note1-note2-
全音符     :  note1---note2---
附点音符   :  note1`- 'note2`'
连续音     : /'note1' note2-\
三连音     : |3|'note1 note2 note3'|
休止符     :  0
```

## 音符音区

同之前的数字谱语法

## 其他语法

### 乐谱注释

以 `;` 开头之后的字符会被解释器忽略
```
; some text
```
可以用来写一些注解

### 琶音

暂且先放置<br />
预计语法
```
$1:  a5---
$2:   3---
$3:   1---
```
