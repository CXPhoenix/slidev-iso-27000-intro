---
theme: '@cxphoenix/slidev-theme-isip.hs'
class: 'text-center'
transition: slide-left
title: ISO 27000系列介紹：資訊安全管理與稽核基礎
mdc: true
---

::title::
# ISO 27000系列介紹

::subtitle::
## 資訊安全管理與稽核基礎 <small>高中資安CTF技術實務教學</small>

---
layout: default
---

::title::
# 課程目標

::default::

<div class="grid grid-cols-3 gap-8 mt-8">
  <OutlineBlock icon="/security-concept-icon.svg">
    理解資訊安全管理基本概念與重要性
  </OutlineBlock>
  
  <OutlineBlock icon="/standard-icon.svg">
    認識ISO 27000系列標準架構與主要內容
  </OutlineBlock>
  
  <OutlineBlock icon="/book-icon.svg">
    掌握三個核心ISO標準的要點
  </OutlineBlock>
</div>

<div class="grid grid-cols-2 gap-8 mt-8">
  <OutlineBlock icon="/audit-icon.svg">
    了解資安稽核的基本方法與流程
  </OutlineBlock>
  
  <OutlineBlock icon="/link-icon.svg">
    連結ISO標準與CTF技術實務
  </OutlineBlock>
</div>

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

<div class="p-6 bg-white rounded-xl shadow-md">
  <h3 class="text-xl font-bold text-blue-800 mb-4 border-b-2 border-yellow-400 pb-2 flex items-center">
    <img src="/question-icon.svg" class="w-6 h-6 mr-2" />
    什麼是資訊安全？
  </h3>
  
  <p class="text-lg">
    資訊安全是<mark class="px-1 bg-yellow-200 font-semibold">保護資訊及其系統</mark>不被未經授權的存取、使用、揭露、破壞、修改或破壞的<mark class="px-1 bg-yellow-200 font-semibold">狀態或過程</mark>。
  </p>

  <div class="mt-8 text-center">
    <h3 class="text-xl text-blue-800 mb-6 font-bold">資訊安全三要素（CIA三角）</h3>
    
    <div class="relative mx-auto w-96 h-80">
      <!-- 手繪三角形 SVG -->
      <img src="/triangle.svg" class="w-full h-full" />
      
      <!-- 三個節點 - 使用手繪風格圓形 -->
      <div class="absolute w-36 h-36 rounded-full bg-white shadow-md border-2 border-orange-400 -top-4 left-1/2 transform -translate-x-1/2 flex flex-col items-center justify-center text-center" style="box-shadow: 3px 3px 5px rgba(0,0,0,0.1);">
        <img src="/confidentiality-icon.svg" class="w-12 h-12 mb-2" />
        <span class="font-bold">機密性<br/>Confidentiality</span>
      </div>
      
      <div class="absolute w-36 h-36 rounded-full bg-white shadow-md border-2 border-orange-400 bottom-4 left-8 flex flex-col items-center justify-center text-center" style="box-shadow: 3px 3px 5px rgba(0,0,0,0.1);">
        <img src="/integrity-icon.svg" class="w-12 h-12 mb-2" />
        <span class="font-bold">完整性<br/>Integrity</span>
      </div>
      
      <div class="absolute w-36 h-36 rounded-full bg-white shadow-md border-2 border-orange-400 bottom-4 right-8 flex flex-col items-center justify-center text-center" style="box-shadow: 3px 3px 5px rgba(0,0,0,0.1);">
        <img src="/availability-icon.svg" class="w-12 h-12 mb-2" />
        <span class="font-bold">可用性<br/>Availability</span>
      </div>
    </div>
  </div>
</div>

---

::title::
# CIA三要素完整說明

::default::

<div class="p-6 bg-white/90 rounded-xl shadow-md border-2 border-dashed border-orange-400 transform -rotate-1">
  <div class="space-y-6">
    <div class="ml-4 border-l-4 border-yellow-400 pl-4 py-2 bg-yellow-50 rounded-r-lg transform rotate-1">
      <div class="font-bold flex items-center gap-2 mb-2">
        <img src="/confidentiality-icon.svg" class="w-8 h-8" />
        <span class="relative">
          <span class="px-1">機密性 (Confidentiality)</span>
          <img src="/highlight-yellow.svg" class="absolute -bottom-1 left-0 w-full h-3" style="z-index: -1" />
        </span>
      </div>
      <div class="text-gray-600 italic">你知、我知，但其他人不知。</div>
    </div>
    
    <div class="ml-4 border-l-4 border-yellow-400 pl-4 py-2 bg-yellow-50 rounded-r-lg transform -rotate-1">
      <div class="font-bold flex items-center gap-2 mb-2">
        <img src="/integrity-icon.svg" class="w-8 h-8" />
        <span class="relative">
          <span class="px-1">完整性 (Integrity)</span>
          <img src="/highlight-yellow.svg" class="absolute -bottom-1 left-0 w-full h-3" style="z-index: -1" />
        </span>
      </div>
      <div class="text-gray-600 italic">一個資訊，我擁有的，跟你擁有的是一樣的；我傳給你的，跟你收到的是一樣的。</div>
    </div>
    
    <div class="ml-4 border-l-4 border-yellow-400 pl-4 py-2 bg-yellow-50 rounded-r-lg transform rotate-1">
      <div class="font-bold flex items-center gap-2 mb-2">
        <img src="/availability-icon.svg" class="w-8 h-8" />
        <span class="relative">
          <span class="px-1">可用性 (Availability)</span>
          <img src="/highlight-yellow.svg" class="absolute -bottom-1 left-0 w-full h-3" style="z-index: -1" />
        </span>
      </div>
      <div class="text-gray-600 italic">你要用的時候，系統正常運作；我需要資料時，隨時都能取得。</div>
    </div>
  </div>
</div>

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

---
layout: section
---

::title::
# 為什麼需要資安管理標準？

::subtitle::
## 從單點防護到系統性管理

---

::title::
# 從單點防護到系統性管理

::default::

<div class="flex items-center justify-between my-8">
  <div class="text-center w-1/3">
    <div class="border-2 border-dashed border-orange-400 rounded-xl p-4 transform -rotate-2 bg-white/90 shadow-md">
      <img src="/single-point-icon.svg" class="w-16 h-16 mx-auto mb-3" />
      <p class="font-bold">單點安全措施</p>
      <p class="text-sm">各自為政，缺乏整合</p>
    </div>
  </div>
  
  <div class="text-center">
    <img src="/hand-drawn-arrow.svg" class="w-16 h-10" />
  </div>
  
  <div class="text-center w-1/3">
    <div class="border-2 border-dashed border-orange-400 rounded-xl p-4 transform rotate-2 bg-white/90 shadow-md">
      <img src="/process-icon.svg" class="w-16 h-16 mx-auto mb-3" />
      <p class="font-bold">流程與程序</p>
      <p class="text-sm">有序但不完整</p>
    </div>
  </div>
  
  <div class="text-center">
    <img src="/hand-drawn-arrow.svg" class="w-16 h-10" />
  </div>
  
  <div class="text-center w-1/3">
    <div class="border-2 border-dashed border-orange-400 rounded-xl p-4 transform -rotate-2 bg-white/90 shadow-md">
      <img src="/management-system-icon.svg" class="w-16 h-16 mx-auto mb-3" />
      <p class="font-bold">管理系統</p>
      <p class="text-sm">全面且持續改進</p>
    </div>
  </div>
</div>

<div class="mt-12 p-6 bg-white/90 rounded-xl shadow-md">
  <h3 class="text-xl font-bold text-blue-800 mb-4 border-b-2 border-yellow-400 pb-2 flex items-center">
    <img src="/maturity-icon.svg" class="w-6 h-6 mr-2" />
    資安治理成熟度模型
  </h3>
  
  <div class="relative pl-10 flex flex-col gap-4 mt-8">
    <!-- 手繪垂直進度線 -->
    <img src="/vertical-progress.svg" class="absolute left-6 top-0 bottom-0 h-full" style="z-index: 0" />
    
    <!-- 成熟度級別 -->
    <div class="flex items-center gap-4 min-h-16 relative z-10">
      <div class="w-10 h-10 rounded-full bg-white border-2 border-orange-500 flex items-center justify-center font-bold text-orange-500 transform -translate-x-1/2 shadow-md">5</div>
      <div class="flex-grow border-2 border-dashed border-orange-300 rounded-lg p-3 bg-white/90 transform rotate-1">
        <div class="font-bold">最佳化級</div>
        <div class="text-sm text-gray-600">持續改進，主動調適</div>
      </div>
      <div class="text-sm italic bg-red-50 px-3 py-1 rounded-md border border-red-100 transform -rotate-1">ISO 27001持續改進階段</div>
    </div>
    
    <div class="flex items-center gap-4 min-h-16 relative z-10">
      <div class="w-10 h-10 rounded-full bg-white border-2 border-orange-400 flex items-center justify-center font-bold text-orange-400 transform -translate-x-1/2 shadow-md">4</div>
      <div class="flex-grow border-2 border-dashed border-orange-300 rounded-lg p-3 bg-white/90 transform -rotate-1">
        <div class="font-bold">量化管理級</div>
        <div class="text-sm text-gray-600">量化管理與分析</div>
      </div>
      <div class="text-sm italic bg-orange-50 px-3 py-1 rounded-md border border-orange-100 transform rotate-1">ISO 27004稽核與量測</div>
    </div>
    
    <div class="flex items-center gap-4 min-h-16 relative z-10">
      <div class="w-10 h-10 rounded-full bg-white border-2 border-yellow-500 flex items-center justify-center font-bold text-yellow-500 transform -translate-x-1/2 shadow-md">3</div>
      <div class="flex-grow border-2 border-dashed border-orange-300 rounded-lg p-3 bg-white/90 transform rotate-1">
        <div class="font-bold">規則級</div>
        <div class="text-sm text-gray-600">標準流程與政策</div>
      </div>
      <div class="text-sm italic bg-yellow-50 px-3 py-1 rounded-md border border-yellow-100 transform -rotate-1">ISO 27001基本實施</div>
    </div>
    
    <div class="flex items-center gap-4 min-h-16 relative z-10">
      <div class="w-10 h-10 rounded-full bg-white border-2 border-yellow-300 flex items-center justify-center font-bold text-yellow-600 transform -translate-x-1/2 shadow-md">2</div>
      <div class="flex-grow border-2 border-dashed border-orange-300 rounded-lg p-3 bg-white/90 transform -rotate-1">
        <div class="font-bold">管理級</div>
        <div class="text-sm text-gray-600">可重複但未標準化</div>
      </div>
      <div class="text-sm italic bg-yellow-50 px-3 py-1 rounded-md border border-yellow-100 transform rotate-1">部分ISO 27002控制措施</div>
    </div>
    
    <div class="flex items-center gap-4 min-h-16 relative z-10">
      <div class="w-10 h-10 rounded-full bg-white border-2 border-gray-400 flex items-center justify-center font-bold text-gray-500 transform -translate-x-1/2 shadow-md">1</div>
      <div class="flex-grow border-2 border-dashed border-orange-300 rounded-lg p-3 bg-white/90 transform rotate-1">
        <div class="font-bold">初始級</div>
        <div class="text-sm text-gray-600">臨時性、反應式</div>
      </div>
      <div class="text-sm italic bg-gray-50 px-3 py-1 rounded-md border border-gray-100 transform -rotate-1">無ISO標準實施</div>
    </div>
  </div>
</div>

---

::title::
# 單點安全措施的問題

::default::

<div class="p-6 bg-white/90 rounded-xl shadow-md border-2 border-dashed border-orange-400 transform -rotate-1">
  <div class="grid grid-cols-2 gap-8 my-6">
    <div class="flex items-start gap-4">
      <div class="rounded-full bg-red-100 w-16 h-16 flex items-center justify-center border border-red-200 transform rotate-3 shadow-sm">
        <img src="/scattered-icon.svg" class="w-10 h-10" />
      </div>
      <div class="flex-grow">
        <div class="font-bold text-lg mb-1">零散性</div>
        <div>各部門各自實施，缺乏整合與協調</div>
      </div>
    </div>
    
    <div class="flex items-start gap-4">
      <div class="rounded-full bg-red-100 w-16 h-16 flex items-center justify-center border border-red-200 transform -rotate-3 shadow-sm">
        <img src="/measurement-icon.svg" class="w-10 h-10" />
      </div>
      <div class="flex-grow">
        <div class="font-bold text-lg mb-1">難以衡量</div>
        <div>缺乏統一指標評估安全措施成效</div>
      </div>
    </div>
    
    <div class="flex items-start gap-4">
      <div class="rounded-full bg-red-100 w-16 h-16 flex items-center justify-center border border-red-200 transform -rotate-3 shadow-sm">
        <img src="/unclear-role-icon.svg" class="w-10 h-10" />
      </div>
      <div class="flex-grow">
        <div class="font-bold text-lg mb-1">職責不明</div>
        <div>責任劃分不清，無法確保全面執行</div>
      </div>
    </div>
    
    <div class="flex items-start gap-4">
      <div class="rounded-full bg-red-100 w-16 h-16 flex items-center justify-center border border-red-200 transform rotate-3 shadow-sm">
        <img src="/inconsistent-icon.svg" class="w-10 h-10" />
      </div>
      <div class="flex-grow">
        <div class="font-bold text-lg mb-1">缺乏持續性</div>
        <div>一次性實施後不再更新，無法應對新威脅</div>
      </div>
    </div>
  </div>
</div>

<div class="mt-8 p-6 bg-gray-50 border-l-4 border-orange-500 rounded-r-lg shadow-md">
  <div class="font-bold text-orange-500 flex items-center gap-2 mb-2">
    <img src="/case-study-icon.svg" class="w-6 h-6" />
    案例思考
  </div>
  <p>想像一家公司：</p>
  <ul class="mt-2 ml-6 space-y-1">
    ❖ IT部門安裝了防火牆和防毒軟體
    ❖ 人資部門制定了密碼政策
    ❖ 行政部門負責監視攝影機和門禁
  </ul>
  <p class="mt-4">
    <span class="relative inline-block">
      <span class="px-1">問題在於</span>
      <img src="/highlight-yellow.svg" class="absolute -bottom-1 left-0 w-full h-3" style="z-index: -1" />
    </span>：這些措施彼此之間沒有協調，缺乏整體規劃和持續改進機制。
  </p>
  <p class="mt-2">
    這就是為什麼我們需要
    <span class="relative inline-block">
      <span class="px-1">標準化的資安管理系統</span>
      <img src="/highlight-yellow.svg" class="absolute -bottom-1 left-0 w-full h-3" style="z-index: -1" />
    </span>。
  </p>
</div>

---
layout: section
---

::title::
# ISO 27000系列概述

::subtitle::
## 國際資訊安全管理標準

---

::title::
# ISO 27000系列概述

::default::

<div class="p-6 bg-white/90 rounded-xl shadow-md">
  <h3 class="text-xl font-bold text-blue-800 mb-4 border-b-2 border-yellow-400 pb-2 flex items-center">
    <img src="/iso-organization-icon.svg" class="w-6 h-6 mr-2" />
    ISO是什麼？
  </h3>
  <p class="text-lg">
    國際標準化組織（International Organization for Standardization, ISO）是一個<mark class="px-1 bg-yellow-200 font-semibold">非政府組織</mark>，負責制定國際標準，促進全球貿易和合作。
  </p>

  <h3 class="text-xl font-bold text-blue-800 mt-8 mb-4 border-b-2 border-yellow-400 pb-2 flex items-center">
    <img src="/iso-27000-icon.svg" class="w-6 h-6 mr-2" />
    ISO 27000系列簡介
  </h3>
  <p class="text-lg">
    ISO 27000系列是專門針對<mark class="px-1 bg-yellow-200 font-semibold">資訊安全管理系統</mark>（ISMS）所制定的國際標準系列，提供組織建立、實施、維護和持續改進資訊安全管理的架構。
  </p>

  <div class="border-2 border-dashed border-orange-400 p-6 mt-6 rounded-lg bg-white/70 transform rotate-1">
    <table class="w-full border-collapse">
      <thead>
        <tr>
          <th class="border border-slate-200 px-4 py-3 bg-slate-50 text-left rounded-tl-lg">標準編號</th>
          <th class="border border-slate-200 px-4 py-3 bg-slate-50 text-left">標準名稱</th>
          <th class="border border-slate-200 px-4 py-3 bg-slate-50 text-left rounded-tr-lg">主要內容</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td class="border border-slate-200 px-4 py-3 bg-white"><strong>ISO 27000</strong></td>
          <td class="border border-slate-200 px-4 py-3 bg-white">概述與詞彙</td>
          <td class="border border-slate-200 px-4 py-3 bg-white">定義ISMS相關術語與基本概念</td>
        </tr>
        <tr>
          <td class="border border-slate-200 px-4 py-3 bg-white"><strong>ISO 27001</strong></td>
          <td class="border border-slate-200 px-4 py-3 bg-white">要求事項</td>
          <td class="border border-slate-200 px-4 py-3 bg-white">規定ISMS的要求，可進行驗證</td>
        </tr>
        <tr>
          <td class="border border-slate-200 px-4 py-3 bg-white"><strong>ISO 27002</strong></td>
          <td class="border border-slate-200 px-4 py-3 bg-white">實作指引</td>
          <td class="border border-slate-200 px-4 py-3 bg-white">提供安全控制措施的最佳實務</td>
        </tr>
        <tr>
          <td class="border border-slate-200 px-4 py-3 bg-white"><strong>ISO 27005</strong></td>
          <td class="border border-slate-200 px-4 py-3 bg-white">風險管理</td>
          <td class="border border-slate-200 px-4 py-3 bg-white">提供資訊安全風險管理指引</td>
        </tr>
        <tr>
          <td class="border border-slate-200 px-4 py-3 bg-white rounded-bl-lg"><strong>ISO 27032</strong></td>
          <td class="border border-slate-200 px-4 py-3 bg-white">網路安全</td>
          <td class="border border-slate-200 px-4 py-3 bg-white rounded-br-lg">專注於網際網路安全指引</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

<div class="mt-6 p-4 bg-gray-50 border-l-4 border-yellow-500 rounded-r-lg shadow-md flex items-center">
  <img src="/note-icon.svg" class="w-10 h-10 mr-4" />
  <p>
    <strong>重要提示：</strong>在本課程中，我們將重點關注ISO 27001、ISO 27002及ISO 27032三個標準，因為它們與CTF技術實務的關聯性最高。
  </p>
</div>

---
layout: section
---

::title::
# ISO 27001安全管理系統

::subtitle::
## 資訊安全管理系統的核心標準

---

::title::
# ISO 27001安全管理系統

::default::

<div class="p-6 bg-white/90 rounded-xl shadow-md">
  <h3 class="text-xl font-bold text-blue-800 mb-4 border-b-2 border-yellow-400 pb-2 flex items-center">
    <img src="/core-concept-icon.svg" class="w-6 h-6 mr-2" />
    ISO 27001核心概念
  </h3>
  <p class="text-lg">
    ISO 27001是ISO 27000系列的<mark class="px-1 bg-yellow-200 font-semibold">核心標準</mark>，規定了建立、實施、維護和持續改進資訊安全管理系統（ISMS）的要求。
  </p>

  <div class="grid grid-cols-4 gap-6 my-8">
    <div class="flex flex-col items-center">
      <div class="rounded-full bg-yellow-200 w-16 h-16 flex items-center justify-center mb-4 shadow-sm border-2 border-dashed border-yellow-400 transform rotate-3">
        <img src="/certificate-icon.svg" class="w-10 h-10" />
      </div>
      <div class="text-center font-medium">唯一可認證的標準</div>
    </div>
    
    <div class="flex flex-col items-center">
      <div class="rounded-full bg-yellow-200 w-16 h-16 flex items-center justify-center mb-4 shadow-sm border-2 border-dashed border-yellow-400 transform -rotate-3">
        <img src="/process-method-icon.svg" class="w-10 h-10" />
      </div>
      <div class="text-center font-medium">採用「過程方法」</div>
    </div>
    
    <div class="flex flex-col items-center">
      <div class="rounded-full bg-yellow-200 w-16 h-16 flex items-center justify-center mb-4 shadow-sm border-2 border-dashed border-yellow-400 transform rotate-3">
        <img src="/pdca-icon.svg" class="w-10 h-10" />
      </div>
      <div class="text-center font-medium">基於PDCA循環模型</div>
    </div>
    
    <div class="flex flex-col items-center">
      <div class="rounded-full bg-yellow-200 w-16 h-16 flex items-center justify-center mb-4 shadow-sm border-2 border-dashed border-yellow-400 transform -rotate-3">
        <img src="/risk-icon.svg" class="w-10 h-10" />
      </div>
      <div class="text-center font-medium">以風險為基礎</div>
    </div>
  </div>
</div>

<div class="mt-8 p-6 bg-white/90 rounded-xl shadow-md">
  <h3 class="text-xl font-bold text-blue-800 mb-6 border-b-2 border-yellow-400 pb-2 flex items-center">
    <img src="/pdca-cycle-icon.svg" class="w-6 h-6 mr-2" />
    PDCA循環模型
  </h3>
  
  <div class="relative py-6">
    <!-- 手繪連接線 -->
    <img src="/pdca-circle.svg" class="w-5/6 h-auto mx-auto absolute inset-0 z-0" />
    
    <div class="grid grid-cols-4 gap-6 relative z-10">
      <!-- 計劃 (Plan) -->
      <div class="flex flex-col items-center">
        <div class="w-20 h-20 rounded-full bg-white border-2 border-orange-500 flex items-center justify-center text-3xl font-bold text-orange-500 mx-auto mb-4 shadow-md transform rotate-3">P</div>
        <div class="text-center">
          <div class="font-bold text-lg mb-1">計劃 (Plan)</div>
          <p class="text-sm">確立ISMS政策、<br/>目標、過程和程序</p>
        </div>
      </div>
      
      <!-- 執行 (Do) -->
      <div class="flex flex-col items-center">
        <div class="w-20 h-20 rounded-full bg-white border-2 border-orange-500 flex items-center justify-center text-3xl font-bold text-orange-500 mx-auto mb-4 shadow-md transform -rotate-3">D</div>
        <div class="text-center">
          <div class="font-bold text-lg mb-1">執行 (Do)</div>
          <p class="text-sm">實施和運行ISMS<br/>政策、控制、過程</p>
        </div>
      </div>
      
      <!-- 檢查 (Check) -->
      <div class="flex flex-col items-center">
        <div class="w-20 h-20 rounded-full bg-white border-2 border-orange-500 flex items-center justify-center text-3xl font-bold text-orange-500 mx-auto mb-4 shadow-md transform rotate-3">C</div>
        <div class="text-center">
          <div class="font-bold text-lg mb-1">檢查 (Check)</div>
          <p class="text-sm">評估並測量過程<br/>績效，報告結果</p>
        </div>
      </div>
      
      <!-- 行動 (Act) -->
      <div class="flex flex-col items-center">
        <div class="w-20 h-20 rounded-full bg-white border-2 border-orange-500 flex items-center justify-center text-3xl font-bold text-orange-500 mx-auto mb-4 shadow-md transform -rotate-3">A</div>
        <div class="text-center">
          <div class="font-bold text-lg mb-1">行動 (Act)</div>
          <p class="text-sm">採取改進行動，<br/>持續提升ISMS</p>
        </div>
      </div>
    </div>
  </div>
</div>

<div class="mt-6 p-5 bg-gray-50 border-l-4 border-orange-500 rounded-r-lg shadow-md">
  <div class="font-bold text-orange-500 flex items-center gap-2 mb-2">
    <img src="/case-discussion-icon.svg" class="w-6 h-6" />
    案例討論
  </div>
  <p>某電子商務公司如何應用ISO 27001來保護客戶資料？考慮以下方面：</p>
  <ul class="mt-2 ml-6 space-y-1">
    ❖ 如何規劃資安管理體系？
    ❖ 需要實施哪些安全控制？
    ❖ 如何評估資安措施的有效性？
    ❖ 發現問題後如何持續改進？
  </ul>
</div>

---
layout: section
---

::title::
# ISO 27002安全控制

::subtitle::
## 資訊安全控制措施實施指引

---

::title::
# ISO 27002安全控制

::default::

<div class="p-6 bg-white/90 rounded-xl shadow-md">
  <h3 class="text-xl font-bold text-blue-800 mb-4 border-b-2 border-yellow-400 pb-2 flex items-center">
    <img src="/info-icon.svg" class="w-6 h-6 mr-2" />
    ISO 27002概述
  </h3>
  <p class="text-lg">
    ISO 27002提供了<mark class="px-1 bg-yellow-200 font-semibold">資訊安全控制措施</mark>的實施指引，是ISO 27001附錄A控制項的詳細說明。
  </p>

  <div class="grid grid-cols-3 gap-8 my-8">
    <div class="flex flex-col items-center">
      <div class="rounded-full bg-yellow-200 w-16 h-16 flex items-center justify-center mb-4 shadow-sm border-2 border-dashed border-yellow-400 transform rotate-3">
        <img src="/best-practice-icon.svg" class="w-10 h-10" />
      </div>
      <div class="text-center font-medium">提供安全控制措施的最佳實務</div>
    </div>
    
    <div class="flex flex-col items-center">
      <div class="rounded-full bg-yellow-200 w-16 h-16 flex items-center justify-center mb-4 shadow-sm border-2 border-dashed border-yellow-400 transform -rotate-3">
        <img src="/selection-icon.svg" class="w-10 h-10" />
      </div>
      <div class="text-center font-medium">協助選擇適當的安全控制措施</div>
    </div>
    
    <div class="flex flex-col items-center">
      <div class="rounded-full bg-yellow-200 w-16 h-16 flex items-center justify-center mb-4 shadow-sm border-2 border-dashed border-yellow-400 transform rotate-3">
        <img src="/guidance-icon.svg" class="w-10 h-10" />
      </div>
      <div class="text-center font-medium">非強制性，但提供實用指導</div>
    </div>
  </div>
</div>

<div class="mt-8 p-6 bg-white/90 rounded-xl shadow-md">
  <h3 class="text-xl font-bold text-blue-800 mb-4 border-b-2 border-yellow-400 pb-2 flex items-center">
    <img src="/controls-icon.svg" class="w-6 h-6 mr-2" />
    ISO 27002控制領域
  </h3>
  <p class="mb-4">ISO 27002:2022版本包含4個主要類別，涵蓋93個控制項：</p>

  <div class="border-2 border-dashed border-orange-400 p-6 rounded-lg bg-white/70 transform -rotate-1">
    <div class="grid grid-cols-2 gap-8 my-6">
      <div class="flex items-start gap-4">
        <div class="rounded-full bg-green-100 w-16 h-16 flex items-center justify-center border border-green-200 shadow-sm">
          <img src="/organization-control-icon.svg" class="w-10 h-10" />
        </div>
        <div class="flex-grow">
          <div class="font-bold text-lg mb-1">組織控制</div>
          <div>安全政策、角色與責任等</div>
        </div>
      </div>
      
      <div class="flex items-start gap-4">
        <div class="rounded-full bg-cyan-100 w-16 h-16 flex items-center justify-center border border-cyan-200 shadow-sm">
          <img src="/people-control-icon.svg" class="w-10 h-10" />
        </div>
        <div class="flex-grow">
          <div class="font-bold text-lg mb-1">人員控制</div>
          <div>安全意識與培訓、行為準則等</div>
        </div>
      </div>
      
      <div class="flex items-start gap-4">
        <div class="rounded-full bg-purple-100 w-16 h-16 flex items-center justify-center border border-purple-200 shadow-sm">
          <img src="/physical-control-icon.svg" class="w-10 h-10" />
        </div>
        <div class="flex-grow">
          <div class="font-bold text-lg mb-1">物理控制</div>
          <div>物理存取控制、設備安全等</div>
        </div>
      </div>
      
      <div class="flex items-start gap-4">
        <div class="rounded-full bg-yellow-100 w-16 h-16 flex items-center justify-center border border-yellow-200 shadow-sm">
          <img src="/technical-control-icon.svg" class="w-10 h-10" />
        </div>
        <div class="flex-grow">
          <div class="font-bold text-lg mb-1">技術控制</div>
          <div>存取控制、密碼學、網路安全等</div>
        </div>
      </div>
    </div>
  </div>
</div>

<div class="mt-6 p-5 bg-gray-50 border-l-4 border-yellow-500 rounded-r-lg shadow-md">
  <h3 class="font-bold text-lg flex items-center gap-2 mb-2">
    <img src="/connect-icon.svg" class="w-6 h-6" />
    與CTF關聯的控制項
  </h3>
  <ul class="ml-6 space-y-1">
    ❖ <strong>存取控制</strong> - 與OWASP A01:2021（<span class="relative inline-block">
      <span class="px-1">權限控制失效</span>
      <img src="/highlight-yellow.svg" class="absolute -bottom-1 left-0 w-full h-3" style="z-index: -1" />
    </span>）相關
    
    ❖ <strong>應用程式安全</strong> - 與OWASP A04:2021（<span class="relative inline-block">
      <span class="px-1">不安全設計</span>
      <img src="/highlight-yellow.svg" class="absolute -bottom-1 left-0 w-full h-3" style="z-index: -1" />
    </span>）相關
    
    ❖ <strong>系統與網路安全</strong> - 與OWASP A03:2021（<span class="relative inline-block">
      <span class="px-1">注入攻擊</span>
      <img src="/highlight-yellow.svg" class="absolute -bottom-1 left-0 w-full h-3" style="z-index: -1" />
    </span>）相關
  </ul>
</div>

<div class="mt-6 p-5 bg-white rounded-lg shadow-md relative border-2 border-gray-100">
  <h3 class="font-bold text-orange-500 mb-2 flex items-center">
    <img src="/group-activity-icon.svg" class="w-6 h-6 mr-2" />
    小組活動
  </h3>
  <p>請討論在日常生活中，你可能已經遇到的資訊安全控制措施有哪些？考慮學校、購物網站、銀行App等場景。</p>
  <div class="absolute w-5 h-5 bg-white transform rotate-45 -bottom-2.5 left-8 border-r-2 border-b-2 border-gray-100"></div>
</div>

---
layout: section
---

::title::
# ISO 27032網路安全

::subtitle::
## 網路空間安全指引

---

::title::
# ISO 27032網路安全

::default::

<div class="p-6 bg-white/90 rounded-xl shadow-md">
  <h3 class="text-xl font-bold text-blue-800 mb-4 border-b-2 border-yellow-400 pb-2 flex items-center">
    <img src="/info-icon.svg" class="w-6 h-6 mr-2" />
    ISO 27032概述
  </h3>
  <p class="text-lg">
    ISO 27032專注於<mark class="px-1 bg-yellow-200 font-semibold">網路安全</mark>（Cybersecurity），提供改善網路空間安全狀態的指引。
  </p>

  <div class="grid grid-cols-3 gap-8 my-8">
    <div class="flex flex-col items-center">
      <div class="rounded-full bg-yellow-200 w-16 h-16 flex items-center justify-center mb-4 shadow-sm border-2 border-dashed border-yellow-400 transform rotate-3">
        <img src="/internet-security-icon.svg" class="w-10 h-10" />
      </div>
      <div class="text-center font-medium">專注於網際網路環境的安全</div>
    </div>
    
    <div class="flex flex-col items-center">
      <div class="rounded-full bg-yellow-200 w-16 h-16 flex items-center justify-center mb-4 shadow-sm border-2 border-dashed border-yellow-400 transform -rotate-3">
        <img src="/cross-domain-icon.svg" class="w-10 h-10" />
      </div>
      <div class="text-center font-medium">處理不同安全領域的交叉部分</div>
    </div>
    
    <div class="flex flex-col items-center">
      <div class="rounded-full bg-yellow-200 w-16 h-16 flex items-center justify-center mb-4 shadow-sm border-2 border-dashed border-yellow-400 transform rotate-3">
        <img src="/stakeholder-icon.svg" class="w-10 h-10" />
      </div>
      <div class="text-center font-medium">提供與利害關係者協作的架構</div>
    </div>
  </div>
</div>

<div class="mt-8 p-6 bg-white/90 rounded-xl shadow-md">
  <h3 class="text-xl font-bold text-blue-800 mb-4 border-b-2 border-yellow-400 pb-2 flex items-center">
    <img src="/cyber-security-icon.svg" class="w-6 h-6 mr-2" />
    ISO 27032主要內容
  </h3>

  <div class="border-2 border-dashed border-orange-400 p-5 rounded-lg bg-white/70 transform rotate-1 mb-6">
    <h3 class="mb-4 text-lg font-bold text-orange-500 flex items-center">
      <img src="/cyber-attack-icon.svg" class="w-6 h-6 mr-2" />
      網路攻擊技術與常見威脅
    </h3>
    
    <div class="flex justify-center flex-wrap gap-6">
      <div class="flex flex-col items-center w-28">
        <div class="rounded-full bg-red-100 w-16 h-16 flex items-center justify-center mb-2 border border-red-200 transform -rotate-3 shadow-sm">
          <img src="/social-engineering-icon.svg" class="w-10 h-10" />
        </div>
        <div class="text-center font-medium">社交工程</div>
      </div>
      
      <div class="flex flex-col items-center w-28">
        <div class="rounded-full bg-red-100 w-16 h-16 flex items-center justify-center mb-2 border border-red-200 transform rotate-3 shadow-sm">
          <img src="/hacking-icon.svg" class="w-10 h-10" />
        </div>
        <div class="text-center font-medium">駭客入侵</div>
      </div>
      
      <div class="flex flex-col items-center w-28">
        <div class="rounded-full bg-red-100 w-16 h-16 flex items-center justify-center mb-2 border border-red-200 transform -rotate-3 shadow-sm">
          <img src="/malware-icon.svg" class="w-10 h-10" />
        </div>
        <div class="text-center font-medium">惡意軟體</div>
      </div>
      
      <div class="flex flex-col items-center w-28">
        <div class="rounded-full bg-red-100 w-16 h-16 flex items-center justify-center mb-2 border border-red-200 transform rotate-3 shadow-sm">
          <img src="/fraud-icon.svg" class="w-10 h-10" />
        </div>
        <div class="text-center font-medium">網路詐欺</div>
      </div>
    </div>
  </div>
  
  <div class="border-2 border-dashed border-orange-400 p-5 rounded-lg bg-white/70 transform -rotate-1">
    <h3 class="mb-4 text-lg font-bold text-orange-500 flex items-center">
      <img src="/security-measures-icon.svg" class="w-6 h-6 mr-2" />
      網路安全控制與防護措施
    </h3>
    
    <div class="grid grid-cols-3 gap-6">
      <div>
        <div class="font-bold mb-2 text-orange-500 flex items-center">
          <img src="/technical-icon.svg" class="w-5 h-5 mr-2" />
          技術層面
        </div>
        <ul class="ml-6 space-y-1">
          ➢ 防火牆
          ➢ 入侵偵測系統
          ➢ 加密技術
          ➢ 存取控制
        </ul>
      </div>
      
      <div>
        <div class="font-bold mb-2 text-orange-500 flex items-center">
          <img src="/process-icon-small.svg" class="w-5 h-5 mr-2" />
          程序層面
        </div>
        <ul class="ml-6 space-y-1">
          ➢ 安全政策
          ➢ 事件處理流程
          ➢ 業務持續計畫
          ➢ 稽核機制
        </ul>
      </div>
      
      <div>
        <div class="font-bold mb-2 text-orange-500 flex items-center">
          <img src="/people-icon-small.svg" class="w-5 h-5 mr-2" />
          人員層面
        </div>
        <ul class="ml-6 space-y-1">
          ➢ 安全意識
          ➢ 培訓與教育
          ➢ 責任與權限
          ➢ 行為規範
        </ul>
      </div>
    </div>
  </div>
</div>

<div class="mt-6 p-5 bg-gray-50 border-l-4 border-yellow-500 rounded-r-lg shadow-md">
  <h3 class="font-bold text-lg flex items-center gap-2 mb-2">
    <img src="/connect-icon.svg" class="w-6 h-6" />
    ISO 27032與CTF的關聯
  </h3>
  <ul class="ml-6 space-y-1">
    ❖ 了解攻擊技術有助於進行CTF解題
    ❖ 網路安全控制措施是CTF題目的常見情境
    ❖ 安全弱點分析是ISO 27032與CTF的共同關注點
  </ul>
</div>

<div class="mt-6 p-5 bg-gray-50 border-l-4 border-orange-500 rounded-r-lg shadow-md">
  <div class="font-bold text-orange-500 flex items-center gap-2 mb-2">
    <img src="/case-analysis-icon.svg" class="w-6 h-6" />
    案例分析
  </div>
  <p>某公司網站遭受SQL注入攻擊，從ISO 27032的角度，應如何預防？思考技術、程序和人員三個層面。</p>
</div>

---
layout: section
---

::title::
# 資安稽核方法概述

::subtitle::
## 系統性評估與改進流程

---

::title::
# 資安稽核方法概述

::default::

<div class="p-6 bg-white/90 rounded-xl shadow-md">
  <h3 class="text-xl font-bold text-blue-800 mb-4 border-b-2 border-yellow-400 pb-2 flex items-center">
    <img src="/question-icon.svg" class="w-6 h-6 mr-2" />
    什麼是資安稽核？
  </h3>
  <p class="text-lg">
    資安稽核是<mark class="px-1 bg-yellow-200 font-semibold">系統性評估</mark>組織資訊安全控制措施的過程，目的是確認這些措施是否有效實施、是否符合標準要求，並找出可能的弱點與改進空間。
  </p>

  <div class="border-2 border-dashed border-orange-400 p-6 mt-6 rounded-lg bg-white/70 transform rotate-1">
    <h3 class="text-lg font-bold text-orange-500 mb-4 flex items-center">
      <img src="/audit-types-icon.svg" class="w-6 h-6 mr-2" />
      資安稽核的類型
    </h3>
    
    <div class="grid grid-cols-4 gap-6">
      <div class="flex flex-col items-center">
        <div class="rounded-full bg-yellow-200 w-16 h-16 flex items-center justify-center mb-4 shadow-sm border-2 border-dashed border-yellow-400 transform rotate-3">
          <img src="/internal-audit-icon.svg" class="w-10 h-10" />
        </div>
        <div class="text-center">
          <div class="font-bold mb-1">內部稽核</div>
          <p class="text-sm">由組織內部人員執行</p>
        </div>
      </div>
      
      <div class="flex flex-col items-center">
        <div class="rounded-full bg-yellow-200 w-16 h-16 flex items-center justify-center mb-4 shadow-sm border-2 border-dashed border-yellow-400 transform -rotate-3">
          <img src="/external-audit-icon.svg" class="w-10 h-10" />
        </div>
        <div class="text-center">
          <div class="font-bold mb-1">外部稽核</div>
          <p class="text-sm">由第三方獨立機構執行</p>
        </div>
      </div>
      
      <div class="flex flex-col items-center">
        <div class="rounded-full bg-yellow-200 w-16 h-16 flex items-center justify-center mb-4 shadow-sm border-2 border-dashed border-yellow-400 transform rotate-3">
          <img src="/compliance-audit-icon.svg" class="w-10 h-10" />
        </div>
        <div class="text-center">
          <div class="font-bold mb-1">合規性稽核</div>
          <p class="text-sm">檢查是否符合標準或法規</p>
        </div>
      </div>
      
      <div class="flex flex-col items-center">
        <div class="rounded-full bg-yellow-200 w-16 h-16 flex items-center justify-center mb-4 shadow-sm border-2 border-dashed border-yellow-400 transform -rotate-3">
          <img src="/technical-audit-icon.svg" class="w-10 h-10" />
        </div>
        <div class="text-center">
          <div class="font-bold mb-1">技術性稽核</div>
          <p class="text-sm">針對技術控制措施評估</p>
        </div>
      </div>
    </div>
  </div>
</div>

<div class="mt-8 p-6 bg-white/90 rounded-xl shadow-md">
  <h3 class="text-xl font-bold text-blue-800 mb-6 border-b-2 border-yellow-400 pb-2 flex items-center">
    <img src="/audit-process-icon.svg" class="w-6 h-6 mr-2" />
    資安稽核流程
  </h3>
  
  <div class="relative py-6">
    <!-- 手繪流程線 -->
    <img src="/audit-process-flow.svg" class="w-5/6 h-16 mx-auto absolute top-10 left-0 right-0" style="z-index: 0" />
    
    <div class="grid grid-cols-4 gap-6 relative z-10">
      <!-- 稽核規劃 -->
      <div class="flex flex-col items-center">
        <div class="w-16 h-16 rounded-full bg-white border-2 border-orange-500 flex items-center justify-center text-xl font-bold text-orange-500 mx-auto mb-4 shadow-md transform rotate-3">1</div>
        <div class="text-center">
          <div class="font-bold text-lg mb-1">稽核規劃</div>
          <p class="text-sm">確定目標與範圍<br/>準備稽核計畫與檢查表</p>
        </div>
      </div>
      
      <!-- 稽核執行 -->
      <div class="flex flex-col items-center">
        <div class="w-16 h-16 rounded-full bg-white border-2 border-orange-500 flex items-center justify-center text-xl font-bold text-orange-500 mx-auto mb-4 shadow-md transform -rotate-3">2</div>
        <div class="text-center">
          <div class="font-bold text-lg mb-1">稽核執行</div>
          <p class="text-sm">收集證據<br/>記錄發現項目</p>
        </div>
      </div>
      
      <!-- 稽核報告 -->
      <div class="flex flex-col items-center">
        <div class="w-16 h-16 rounded-full bg-white border-2 border-orange-500 flex items-center justify-center text-xl font-bold text-orange-500 mx-auto mb-4 shadow-md transform rotate-3">3</div>
        <div class="text-center">
          <div class="font-bold text-lg mb-1">稽核報告</div>
          <p class="text-sm">分析發現項目<br/>評估風險與提出建議</p>
        </div>
      </div>
      
      <!-- 後續追蹤 -->
      <div class="flex flex-col items-center">
        <div class="w-16 h-16 rounded-full bg-white border-2 border-orange-500 flex items-center justify-center text-xl font-bold text-orange-500 mx-auto mb-4 shadow-md transform -rotate-3">4</div>
        <div class="text-center">
          <div class="font-bold text-lg mb-1">後續追蹤</div>
          <p class="text-sm">改善措施實施<br/>驗證改善效果</p>
        </div>
      </div>
    </div>
  </div>
</div>

<div class="mt-6 p-5 bg-gray-50 border-l-4 border-yellow-500 rounded-r-lg shadow-md">
  <h3 class="font-bold text-lg flex items-center gap-2 mb-2">
    <img src="/connect-icon.svg" class="w-6 h-6" />
    資安稽核與CTF的關聯
  </h3>
  <p>資安稽核與CTF解題有許多相似之處：</p>
  <ul class="ml-6 space-y-1 mt-2">
    ❖ 都需要<span class="relative inline-block">
      <span class="px-1">系統性的方法</span>
      <img src="/highlight-yellow.svg" class="absolute -bottom-1 left-0 w-full h-3" style="z-index: -1" />
    </span>來識別弱點
    
    ❖ 都需要依據<span class="relative inline-block">
      <span class="px-1">標準或最佳實務</span>
      <img src="/highlight-yellow.svg" class="absolute -bottom-1 left-0 w-full h-3" style="z-index: -1" />
    </span>進行評估
    
    ❖ 都需要撰寫清晰的<span class="relative inline-block">
      <span class="px-1">報告</span>
      <img src="/highlight-yellow.svg" class="absolute -bottom-1 left-0 w-full h-3" style="z-index: -1" />
    </span>說明發現項目
  </ul>
  <p class="mt-4">
    <strong>未來課程連結：</strong>我們將學習如何將CTF解題過程轉化為專業的資安稽核報告。
  </p>
</div>

---
layout: section
---

::title::
# 實際案例分析

::subtitle::
## 從資安事件學習標準應用

---

::title::
# 實際案例分析

::default::

<div class="p-6 bg-white/90 rounded-xl shadow-md mb-6">
  <h3 class="text-xl font-bold text-blue-800 mb-4 border-b-2 border-yellow-400 pb-2 flex items-center">
    <img src="/data-breach-icon.svg" class="w-6 h-6 mr-2" />
    案例一：個人資料外洩事件
  </h3>
  <p class="mb-4">
    <strong class="border-b-2 border-orange-300">情境：</strong>某購物網站因資料庫安全控制不足，導致大量客戶資料外洩。
  </p>

  <div class="mt-6">
    <div class="font-bold text-orange-500 mb-3 flex items-center">
      <img src="/analysis-icon.svg" class="w-6 h-6 mr-2" />
      從ISO角度分析
    </div>
    <div class="grid grid-cols-3 gap-6 border-2 border-dashed border-gray-200 p-4 rounded-lg bg-white/80 transform rotate-1">
      <div>
        <div class="font-bold mb-2 flex items-center">
          <img src="/iso-27001-icon-small.svg" class="w-5 h-5 mr-2" />
          ISO 27001
        </div>
        <ul class="ml-6 space-y-1">
          ➢ 缺乏適當的風險評估
          ➢ 未實施必要的控制措施
          ➢ 監控機制不足
        </ul>
      </div>
      <div>
        <div class="font-bold mb-2 flex items-center">
          <img src="/iso-27002-icon-small.svg" class="w-5 h-5 mr-2" />
          ISO 27002
        </div>
        <ul class="ml-6 space-y-1">
          ➢ 未實施適當的存取控制
          ➢ 密碼保護措施不足
          ➢ 資料加密缺失
        </ul>
      </div>
      <div>
        <div class="font-bold mb-2 flex items-center">
          <img src="/iso-27032-icon-small.svg" class="w-5 h-5 mr-2" />
          ISO 27032
        </div>
        <ul class="ml-6 space-y-1">
          ➢ 未能及時偵測網路入侵
          ➢ 缺乏應變計畫
          ➢ 未定期進行滲透測試
        </ul>
      </div>
    </div>
  </div>

  <div class="mt-6">
    <div class="font-bold text-orange-500 mb-3 flex items-center">
      <img src="/ctf-icon.svg" class="w-6 h-6 mr-2" />
      CTF技術關聯
    </div>
    <ul class="ml-6 space-y-1 border-2 border-dashed border-gray-200 p-4 rounded-lg bg-white/80 transform -rotate-1">
      ❖ 可能涉及SQL注入（A03:2021）
      ❖ 可能涉及權限控制失效（A01:2021）
    </ul>
  </div>
</div>

<div class="p-6 bg-white/90 rounded-xl shadow-md">
  <h3 class="text-xl font-bold text-blue-800 mb-4 border-b-2 border-yellow-400 pb-2 flex items-center">
    <img src="/ransomware-icon.svg" class="w-6 h-6 mr-2" />
    案例二：勒索軟體攻擊
  </h3>
  <p class="mb-4">
    <strong class="border-b-2 border-orange-300">情境：</strong>某醫院系統遭勒索軟體攻擊，導致系統癱瘓。
  </p>

  <div class="mt-6">
    <div class="font-bold text-orange-500 mb-3 flex items-center">
      <img src="/analysis-icon.svg" class="w-6 h-6 mr-2" />
      從ISO角度分析
    </div>
    <div class="grid grid-cols-3 gap-6 border-2 border-dashed border-gray-200 p-4 rounded-lg bg-white/80 transform -rotate-1">
      <div>
        <div class="font-bold mb-2 flex items-center">
          <img src="/iso-27001-icon-small.svg" class="w-5 h-5 mr-2" />
          ISO 27001
        </div>
        <ul class="ml-6 space-y-1">
          ➢ 缺乏完善的業務持續性計畫
          ➢ 事件處理程序不足
        </ul>
      </div>
      <div>
        <div class="font-bold mb-2 flex items-center">
          <img src="/iso-27002-icon-small.svg" class="w-5 h-5 mr-2" />
          ISO 27002
        </div>
        <ul class="ml-6 space-y-1">
          ➢ 備份策略不足
          ➢ 安全更新管理不當
        </ul>
      </div>
      <div>
        <div class="font-bold mb-2 flex items-center">
          <img src="/iso-27032-icon-small.svg" class="w-5 h-5 mr-2" />
          ISO 27032
        </div>
        <ul class="ml-6 space-y-1">
          ➢ 員工安全意識不足
          ➢ 易受社交工程攻擊
        </ul>
      </div>
    </div>
  </div>

  <div class="mt-6">
    <div class="font-bold text-orange-500 mb-3 flex items-center">
      <img src="/ctf-icon.svg" class="w-6 h-6 mr-2" />
      CTF技術關聯
    </div>
    <ul class="ml-6 space-y-1 border-2 border-dashed border-gray-200 p-4 rounded-lg bg-white/80 transform rotate-1">
      ❖ 可能涉及不安全設計（A04:2021）
      ❖ 可能涉及權限提升攻擊
    </ul>
  </div>
</div>

<div class="mt-6 p-5 bg-white rounded-lg shadow-md relative border-2 border-gray-100">
  <h3 class="font-bold text-orange-500 mb-2 flex items-center">
    <img src="/group-discussion-icon.svg" class="w-6 h-6 mr-2" />
    小組討論
  </h3>
  <p>請分析一則近期的資安事件，從ISO標準角度提出可能的防範措施。</p>
  <div class="absolute w-5 h-5 bg-white transform rotate-45 -bottom-2.5 left-8 border-r-2 border-b-2 border-gray-100"></div>
</div>

---
layout: section
---

::title::
# 延伸討論與閱讀

::subtitle::
## 思考資安標準與實務的關係

---

::title::
# 延伸討論與閱讀

::default::

<div class="p-6 bg-white/90 rounded-xl shadow-md mb-8">
  <h3 class="text-xl font-bold text-blue-800 mb-4 border-b-2 border-yellow-400 pb-2 flex items-center">
    <img src="/discussion-icon.svg" class="w-6 h-6 mr-2" />
    延伸討論：資安標準與實務的關係
  </h3>
  <p class="mb-4">
    資訊安全管理標準提供了框架，但實際執行時常需要根據組織特性進行調整。討論以下問題：
  </p>

  <div class="border-2 border-dashed border-orange-400 p-6 rounded-lg bg-white/70 transform -rotate-1">
    <ol class="ml-6 space-y-3 list-decimal">
      <li>為什麼不同組織需要不同的安全控制措施？</li>
      <li>標準化的優點與限制是什麼？</li>
      <li>台灣企業實施ISO 27001可能面臨哪些挑戰？</li>
    </ol>
  </div>
</div>

<div class="p-6 bg-white/90 rounded-xl shadow-md">
  <h3 class="text-xl font-bold text-blue-800 mb-4 border-b-2 border-yellow-400 pb-2 flex items-center">
    <img src="/balance-icon.svg" class="w-6 h-6 mr-2" />
    延伸思考：技術與管理的平衡
  </h3>

  <div class="border-2 border-dashed border-orange-400 p-6 rounded-lg bg-white/70 transform rotate-1">
    <div class="flex items-center justify-center mb-8">
      <div class="text-center w-1/3">
        <div class="rounded-full bg-yellow-200 w-20 h-20 flex items-center justify-center mb-4 shadow-sm border-2 border-dashed border-yellow-400 transform rotate-3 mx-auto">
          <img src="/technical-aspect-icon.svg" class="w-12 h-12" />
        </div>
        <div class="font-bold text-lg">技術面</div>
      </div>
      
      <div class="text-center mx-6">
        <img src="/balance-scale-icon.svg" class="w-20 h-20" />
      </div>
      
      <div class="text-center w-1/3">
        <div class="rounded-full bg-yellow-200 w-20 h-20 flex items-center justify-center mb-4 shadow-sm border-2 border-dashed border-yellow-400 transform -rotate-3 mx-auto">
          <img src="/management-aspect-icon.svg" class="w-12 h-12" />
        </div>
        <div class="font-bold text-lg">管理面</div>
      </div>
    </div>

    <ol class="ml-6 space-y-3 list-decimal">
      <li>若只有技術防護但缺乏管理流程，可能產生哪些問題？</li>
      <li>若只有管理制度但缺乏技術實作，又會有哪些風險？</li>
      <li>在資安防護中，如何取得技術與管理的最佳平衡？</li>
    </ol>
  </div>
</div>

<div class="mt-6 p-5 bg-gray-50 border-l-4 border-yellow-500 rounded-r-lg shadow-md">
  <p class="flex">
    <img src="/note-thinking-icon.svg" class="w-10 h-10 mr-4 flex-shrink-0" />
    <span>
      <strong>思考提示：</strong>在我們接下來的CTF技術實務課程中，將著重於技術面的學習，但需要記住，真實世界的資安防護必須結合技術與管理兩個面向才能有效。
    </span>
  </p>
</div>

---
layout: section
---

::title::
# 課程總結

::subtitle::
## 本週重點回顧與未來展望

---

::title::
# 課程總結

::default::

<div class="p-6 bg-white/90 rounded-xl shadow-md">
  <h3 class="text-xl font-bold text-blue-800 mb-6 border-b-2 border-yellow-400 pb-2 flex items-center">
    <img src="/summary-icon.svg" class="w-6 h-6 mr-2" />
    本週重點回顧
  </h3>

  <div class="border-2 border-dashed border-orange-400 p-6 rounded-lg bg-white/70 transform -rotate-1">
    <div class="grid grid-cols-3 gap-8">
      <div class="flex flex-col items-center">
        <div class="rounded-full bg-yellow-200 w-16 h-16 flex items-center justify-center mb-4 shadow-sm border-2 border-dashed border-yellow-400 transform rotate-3">
          <img src="/security-concept-icon.svg" class="w-10 h-10" />
        </div>
        <div class="text-center font-medium">資訊安全的基本概念與CIA三角</div>
      </div>
      
      <div class="flex flex-col items-center">
        <div class="rounded-full bg-yellow-200 w-16 h-16 flex items-center justify-center mb-4 shadow-sm border-2 border-dashed border-yellow-400 transform -rotate-3">
          <img src="/standards-icon.svg" class="w-10 h-10" />
        </div>
        <div class="text-center font-medium">ISO 27000系列標準的架構與主要內容</div>
      </div>
      
      <div class="flex flex-col items-center">
        <div class="rounded-full bg-yellow-200 w-16 h-16 flex items-center justify-center mb-4 shadow-sm border-2 border-dashed border-yellow-400 transform rotate-3">
          <img src="/management-system-small-icon.svg" class="w-10 h-10" />
        </div>
        <div class="text-center font-medium">ISO 27001安全管理系統的核心要求</div>
      </div>
    </div>

    <div class="grid grid-cols-3 gap-8 mt-8">
      <div class="flex flex-col items-center">
        <div class="rounded-full bg-yellow-200 w-16 h-16 flex items-center justify-center mb-4 shadow-sm border-2 border-dashed border-yellow-400 transform -rotate-3">
          <img src="/controls-small-icon.svg" class="w-10 h-10" />
        </div>
        <div class="text-center font-medium">ISO 27002安全控制措施的分類與實施</div>
      </div>
      
      <div class="flex flex-col items-center">
        <div class="rounded-full bg-yellow-200 w-16 h-16 flex items-center justify-center mb-4 shadow-sm border-2 border-dashed border-yellow-400 transform rotate-3">
          <img src="/cyber-security-small-icon.svg" class="w-10 h-10" />
        </div>
        <div class="text-center font-medium">ISO 27032網路安全的重點內容</div>
      </div>
      
      <div class="flex flex-col items-center">
        <div class="rounded-full bg-yellow-200 w-16 h-16 flex items-center justify-center mb-4 shadow-sm border-2 border-dashed border-yellow-400 transform -rotate-3">
          <img src="/audit-small-icon.svg" class="w-10 h-10" />
        </div>
        <div class="text-center font-medium">資安稽核的類型、流程與方法</div>
      </div>
    </div>
  </div>
</div>

<div class="mt-6 p-5 bg-gray-50 border-l-4 border-yellow-500 rounded-r-lg shadow-md">
  <p class="flex">
    <img src="/integration-icon.svg" class="w-10 h-10 mr-4 flex-shrink-0" />
    <span>
      <strong>整合與應用：</strong>本週課程介紹的ISO標準與資安管理框架，將在後續的CTF技術實務課程中持續作為重要的參考依據。我們將實際操作安全弱點分析工具與技術，同時結合ISO標準的架構來整理與表達發現的問題。
    </span>
  </p>
</div>

<div class="mt-6 p-5 bg-white rounded-lg shadow-md relative border-2 border-gray-100">
  <h3 class="font-bold text-orange-500 mb-2 flex items-center">
    <img src="/thinking-question-icon.svg" class="w-6 h-6 mr-2" />
    思考問題
  </h3>
  <p>你認為資訊安全管理最重要的目標是什麼？在實施資訊安全控制措施時，應該優先考慮什麼因素？</p>
  <img src="/hand-drawn-arrow-down.svg" class="absolute -bottom-10 right-8 w-10 h-10" />
</div>