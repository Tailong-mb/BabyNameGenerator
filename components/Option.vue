<div class="option-container">
    <h4>1) Choose a gender</h4>
    <div class="option-buttons">
      <button
        :class="options.gender === Gender.BOY && 'option-active'"
        class="option option-left"
        @click="options.gender = Gender.BOY"
      >
        Boy
      </button>
      <button
        class="option"
        :class="options.gender === Gender.UNISEX && 'option-active'"
        @click="options.gender = Gender.UNISEX"
      >
        Unisex
      </button>
      <button
        :class="options.gender === Gender.GIRL && 'option-active'"
        class="option option-right"
        @click="options.gender = Gender.GIRL"
      >
        Girl
      </button>
    </div>
