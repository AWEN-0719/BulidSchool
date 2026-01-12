# 練習 Bootstrap 的 container / row / col 排版
- 排版先想 container → row → col
- 互動元件一定要 JS
- 圖片要加 img-fluid
- data-bs-target 和 id 需要一致

## Bootstrap 基本設定
### Bootstrap 響應式的基本條件 viewport
```
<meta name="viewport" content="width=device-width, initial-scale=1">
```
- 沒有這行手機版會壞掉

### 載入 Bootstrap CSS 與 JS
```
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet">
```
```
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js"></script>
```
- JS 沒載入，畫面會出來，但「按了沒反應」，如 Dropdown、Accordion、Navbar 折疊選單

## Navbar（導覽列）
### Navbar 基本結構
```
<nav class="navbar navbar-expand-md navbar-light bg-light">
```
- navbar；啟用導覽列
- navbar-expand-md；md 以下折疊
- navbar-light；淺色字體配置
- bg-light；淺色背景

### Collapse（漢堡選單）
```
<button class="navbar-toggler" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent">
```
```
<div class="collapse navbar-collapse" id="navbarSupportedContent">
```
- button 負責「按」
- div 負責「收合內容」
- ```data-bs-target``` 一定要對到 ```id```

### Navbar 元件
選單
```
<ul class="navbar-nav me-auto">
```
- ```me-auto```：把後面的搜尋欄推到右邊
Dropdown 下拉選單
```
<li class="nav-item dropdown">
<a class="nav-link dropdown-toggle" data-bs-toggle="dropdown">
```
需要 Bootstrap JS，dropdown-menu 是下拉內容

## 排版
### container / row / col
```
<div class="container">
  <div class="row">
    <div class="col">...</div>
    <div class="col">...</div>
  </div>
</div>
```
- container：整個版面的外框
- row：一排
- col：欄位（Bootstrap 會自動平分）

### gutter（欄距）
```
<div class="row gx-6">
```
- gx-*：控制左右欄距，數字越大，間距越大

## 圖片
```
<img src="..." class="img-fluid">
```
- img-fluid：圖片自動縮放，不超出欄位

## Accordion（手風琴）
用 Accordion的目的是顯示「可收合的說明」與節省版面空間
### Accordion 基本結構
```
<div class="accordion" id="accordionExample">
<div class="accordion-item">
<button class="accordion-button" data-bs-toggle="collapse"
```
- 每個項目都是 ```.accordion-item```
- ```data-bs-parent``` 控制「一次只開一個」
- ```show```預設展開
- ```collapsed```預設收起

## Table（表格）
```
<table class="table">
```
- ```table```Bootstrap 表格樣式
- ```align-middle```垂直置中
### 響應式表格
```
<div class="table-responsive">
```
- 小螢幕時會出現橫向捲軸，不會破版
### 表格對齊
```
<tr class="align-bottom">
<td class="align-top">
```
- ```align-top```上對齊
- ```align-middle```置中
- ```align-bottom```下對齊

## Bootstrap 需要 JS 的互動元件
- Navbar collapse
- Dropdown
- Accordion

