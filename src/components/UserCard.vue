<template>
  <div
    class="bg-white q-pa-lg column"
    style="
      border-radius: 12px;
      gap: 36px;
      box-shadow: 0px 15px 24px 0px rgba(0, 0, 0, 0.12);
    "
  >
    <div class="column items-center" style="gap: 16px">
      <div style="position: relative">
        <q-avatar size="120px">
          <img src="~/assets/avatar.png" />
        </q-avatar>
        <img
          src="~/assets/flag.png"
          style="position: absolute; bottom: 0; right: 14px"
        />
      </div>
      <div class="column items-center">
        <div class="text-color-2f" style="font-size: 24px">Abhishek Gupta</div>
        <div class="text-color-ff" style="font-size: 16px">마케팅 · 2y+</div>
      </div>
    </div>

    <div class="text-color-f column" style="gap: 4px; font-size: 16px">
      <div class="column items-center" style="gap: 4px">
        <div
          class="q-py-xs q-px-sm"
          style="
            border: solid;
            width: fit-content;
            border-radius: 6px;
            border-color: #c1c5cf;
          "
        >
          마케팅 콘텐츠 제작
        </div>
        <div
          class="q-py-xs q-px-sm"
          style="
            border: solid;
            width: fit-content;
            border-radius: 6px;
            border-color: #c1c5cf;
          "
        >
          인스타그램 관리
        </div>
      </div>
      <div class="row justify-center" style="gap: 4px">
        <div
          class="q-py-xs q-px-sm"
          style="
            border: solid;
            width: fit-content;
            border-radius: 6px;
            border-color: #c1c5cf;
          "
        >
          트위터 관리
        </div>
        <div
          class="q-py-xs q-px-sm"
          style="
            border: solid;
            width: fit-content;
            border-radius: 6px;
            border-color: #c1c5cf;
          "
        >
          블로그 글 작성
        </div>
      </div>
    </div>
  </div>
</template>
