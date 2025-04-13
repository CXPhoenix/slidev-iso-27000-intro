---
theme: "@cxphoenix/slidev-theme-isip.hs"
class: "text-center"
transition: slide-left
title: ISO 27000系列介紹：資訊安全管理與稽核基礎
mdc: true
---

::title::

# ISO 27000系列介紹

::subtitle::

## 資訊安全管理與稽核基礎 <small>高中資安CTF技術實務教學</small>

---

::title::

# 課程目標

::default::

<div class="flex flex-col gap-4 h-full p-2 justify-center">
<div class="grid grid-cols-3 gap-8">
  <OutlineBlock v-click icon="/security-concept-icon.svg">
    理解資訊安全管理基本概念
    
    與重要性
  </OutlineBlock>
  
  <OutlineBlock v-click icon="/standard-icon.svg">
    認識ISO 27000系列標準架構
    
    與主要內容
  </OutlineBlock>
  
  <OutlineBlock v-click icon="/book-icon.svg">
    掌握三個核心ISO標準的要點
  </OutlineBlock>
</div>

<div class="grid grid-cols-2 gap-4 px-12"> 
  <OutlineBlock v-click icon="/audit-icon.svg">
    了解資安稽核的基本方法與流程
  </OutlineBlock>
  
  <OutlineBlock v-click icon="/link-icon.svg">
    連結ISO標準與CTF技術實務
  </OutlineBlock>
</div>
</div>

<style>
.slidev-vclick-target {
  transition: all 400ms ease;
}

.slidev-vclick-hidden {
  transform: scale(0);
}
</style>

---

::title::

# 為什麼學習這個主題？

::default::

- 建立系統性的思維方式，不只處理技術細節
- 從組織與管理的角度理解資安問題
- 為後續學習CTF技術打下管理層面的基礎
- 培養跨領域的資安能力，提升就業競爭力

---

::title::

# 資訊安全基礎概念

::default::

## ![question-icon](/question-icon.svg){.inline .w-12 .h-12} 什麼是資訊安全？

<div class="flex h-[20dvh] items-center px-9 mt-4">
  <p class="text-2xl bg-orange/20 rounded-lg py-2 line-height-[3.2rem]">
  資訊安全主要指的是保護資訊及資訊系統的<mark class="bg-yellow-200 font-semibold rounded-md">機密性</mark>、<mark class="bg-yellow-200 font-semibold rounded-md">完整性</mark>和<mark class="bg-yellow-200 font-semibold rounded-md">可用性</mark>，<mark class="px-2 bg-yellow-200 font-semibold text-3xl rounded-md text-red-600">防止</mark>未經授權的存取 (Access)、使用 (Misuse)、揭露 (Disclosure)、中斷 (Disruption)、修改 (Modification) 或破壞 (Destruction)。
  </p>
</div>

---

::title::

# 資訊安全三要素（CIA三角）

::default::

<div class="relative mx-auto w-140 h-82 mt-10">
  <h3 class="absolute top-[15.2dvh] left-[9.2dvw] text-lg font-bold bg-yellow/60 rounded-md">Cybersecurity Triangle</h3>
  <!-- 手繪三角形 SVG -->
  <img src="/triangle.svg" class="w-full h-full" />
  
  <!-- 三個節點 - 使用手繪風格圓形 -->
  <div v-click class="absolute w-40 h-40 rounded-full bg-white shadow-md border-2 border-orange-400 -top-[3dvh] left-[10.3dvw] flex flex-col items-center justify-center pb-4" style="box-shadow: 3px 3px 5px rgba(0,0,0,0.1);">
    <img src="/confidentiality-icon.svg" class="w-16 h-16 -mb-2" />
    <p class="font-bold text-lg text-center">機密性<br/>Confidentiality</p>
  </div>
  
  <div v-click class="absolute w-40 h-40 rounded-full bg-white shadow-md border-2 border-orange-400 bottom-3 left-7 flex flex-col items-center justify-center pb-3" style="box-shadow: 3px 3px 5px rgba(0,0,0,0.1);">
    <img src="/integrity-icon.svg" class="w-16 h-16 -mb-2" />
    <p class="font-bold text-lg text-center">完整性<br/>Integrity</p>
  </div>
  
  <div v-click class="absolute w-40 h-40 rounded-full bg-white shadow-md border-2 border-orange-400 bottom-3 right-6 flex flex-col items-center justify-center pb-3" style="box-shadow: 3px 3px 5px rgba(0,0,0,0.1);">
    <img src="/availability-icon.svg" class="w-16 h-16 -mb-2" />
    <p class="font-bold text-lg text-center">可用性<br/>Availability</p>
  </div>
</div>

<style>
.slidev-vclick-target {
  transition: all 500ms ease;
}

.slidev-vclick-hidden {
  transform: scale(0);
}
</style>

---

::title::

# CIA 三要素完整說明

::default::

<div class="h-full flex flex-col justify-center gap-5 pr-4">
  <div class="ml-4 border-l-4 border-yellow-400 pl-4 py-2 bg-yellow-50 rounded-r-lg">
    <div class="font-bold flex items-center gap-2 mb-2">
      <img src="/confidentiality-icon.svg" class="w-8 h-8" />
      <span class="relative">
        <span class="px-1">機密性 Confidentiality</span>
        <img src="/highlight-yellow.svg" class="absolute -bottom-1 left-0 w-full h-3" style="z-index: -1" />
      </span>
    </div>
    <div class="text-gray-600 italic">你知、我知，但其他人不知。</div>
    <div class="text-xs text-gray-400 pt-1"><mark class="text-gray-400 bg-yellow-200 rounded-md px-1">ISO/IEC 27000:2018 3.10</mark> property that information is not made available or disclosed to unauthorized individuals, entities, or processes.</div>
  </div>
  
  <div class="ml-4 border-l-4 border-yellow-400 pl-4 py-2 bg-yellow-50 rounded-r-lg">
    <div class="font-bold flex items-center gap-2 mb-2">
      <img src="/integrity-icon.svg" class="w-8 h-8" />
      <span class="relative">
        <span class="px-1">完整性 Integrity</span>
        <img src="/highlight-yellow.svg" class="absolute -bottom-1 left-0 w-full h-3" style="z-index: -1" />
      </span>
    </div>
    <div class="text-gray-600 italic">一個資訊，我擁有的，跟你擁有的是一樣的；我傳給你的，跟你收到的是一樣的。</div>
    <div class="text-xs text-gray-400 pt-1"><mark class="text-gray-400 bg-yellow-200 rounded-md px-1">ISO/IEC 27000:2018 3.36</mark> property of accuracy and completeness.</div>
  </div>
  
  <div class="ml-4 border-l-4 border-yellow-400 pl-4 py-2 bg-yellow-50 rounded-r-lg">
    <div class="font-bold flex items-center gap-2 mb-2">
      <img src="/availability-icon.svg" class="w-8 h-8" />
      <span class="relative">
        <span class="px-1">可用性 Availability</span>
        <img src="/highlight-yellow.svg" class="absolute -bottom-1 left-0 w-full h-3" style="z-index: -1" />
      </span>
    </div>
    <div class="text-gray-600 italic">你要用的時候，系統正常運作；我需要資料時，隨時都能取得。</div>
    <div class="text-xs text-gray-400 pt-1"><mark class="text-gray-400 bg-yellow-200 rounded-md px-1">ISO/IEC 27000:2018 3.7</mark> property of being accessible and usable on demand by an authorized entity.</div>
  </div>
</div>

---

::title::

# 資訊安全風險與威脅

::default::

<div class="mt-6 p-6 bg-white rounded-xl shadow-md">
  <h3 class="text-xl font-bold text-orange-500 mb-4 border-b-2 border-yellow-400 pb-2 flex items-center">
    <img src="/warning-icon.svg" class="w-6 h-6 mr-2" />
    資訊安全風險與威脅
  </h3>
  
  <div class="flex justify-center flex-wrap gap-8 my-4">
  <div class="flex flex-col items-center w-28">
    <div class="rounded-full bg-red-100 w-16 h-16 flex items-center justify-center mb-2 border border-red-200 transform rotate-3 shadow-sm">
      <img src="/hacker-icon.svg" class="w-10 h-10" />
    </div>
    <div class="text-center font-medium">駭客攻擊</div>
  </div>
  
  <div class="flex flex-col items-center w-28">
    <div class="rounded-full bg-red-100 w-16 h-16 flex items-center justify-center mb-2 border border-red-200 transform -rotate-3 shadow-sm">
      <img src="/data-leak-icon.svg" class="w-10 h-10" />
    </div>
    <div class="text-center font-medium">資料外洩</div>
  </div>
  
  <div class="flex flex-col items-center w-28">
    <div class="rounded-full bg-red-100 w-16 h-16 flex items-center justify-center mb-2 border border-red-200 transform rotate-3 shadow-sm">
      <img src="/phishing-icon.svg" class="w-10 h-10" />
    </div>
    <div class="text-center font-medium">社交工程</div>
  </div>
  
  <div class="flex flex-col items-center w-28">
    <div class="rounded-full bg-red-100 w-16 h-16 flex items-center justify-center mb-2 border border-red-200 transform -rotate-3 shadow-sm">
      <img src="/insider-threat-icon.svg" class="w-10 h-10" />
    </div>
    <div class="text-center font-medium">內部威脅</div>
  </div>
  
  <div class="flex flex-col items-center w-28">
    <div class="rounded-full bg-red-100 w-16 h-16 flex items-center justify-center mb-2 border border-red-200 transform rotate-3 shadow-sm">
      <img src="/disaster-icon.svg" class="w-10 h-10" />
    </div>
    <div class="text-center font-medium">自然災害</div>
  </div>
</div>

<div class="mt-8 p-5 bg-white rounded-lg shadow-md relative border-2 border-gray-100">
  <h3 class="font-bold text-orange-500 mb-2 flex items-center">
    <img src="/chat-icon.svg" class="w-6 h-6 mr-2" />
    思考問題
  </h3>
  <p>你能想到哪些近期的資安事件？這些事件可能對組織造成什麼影響？</p>
  <div class="absolute w-5 h-5 bg-white transform rotate-45 -bottom-2.5 left-8 border-r-2 border-b-2 border-gray-100"></div>
</div>
</div>
