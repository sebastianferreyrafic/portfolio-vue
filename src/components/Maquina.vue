<template>
    <div class="container ml-5">
      <h1>
        Hola soy Sebastian, 
        <span class="typed-text">{{ typeValue }}</span>
        <span class="blinking-cursor">|</span>
        <span class="cursor" :class="{ typing: typeStatus }">&nbsp;</span>
      </h1>
      
    </div>
    
  </template>
  
  <script>
  export default {
    name: "typeWriter",
    data: () => {
      return {
        typeValue: "",
        typeStatus: false,
        displayTextArray: ["Desarrollador 👨‍💻", "Soporte 🔧", "Diseñador 👁️", "Freelancer 🏄‍♂️", "Beatmaker 🎧", "Rockstar👨‍🎤"],
        typingSpeed: 100,
        erasingSpeed: 100,
        newTextDelay: 2000,
        displayTextArrayIndex: 0,
        charIndex: 0,
      };
    },
    created() {
      setTimeout(this.typeText, this.newTextDelay + 200);
    },
    methods: {
      typeText() {
        if (this.charIndex < this.displayTextArray[this.displayTextArrayIndex].length) {
          if (!this.typeStatus) this.typeStatus = true;
          this.typeValue += this.displayTextArray[this.displayTextArrayIndex].charAt(
            this.charIndex
          );
          this.charIndex += 1;
          setTimeout(this.typeText, this.typingSpeed);
        } else {
          this.typeStatus = false;
          setTimeout(this.eraseText, this.newTextDelay);
        }
      },
      eraseText() {
        if (this.charIndex > 0) {
          if (!this.typeStatus) this.typeStatus = true;
          this.typeValue = this.displayTextArray[this.displayTextArrayIndex].substring(
            0,
            this.charIndex - 1
          );
          this.charIndex -= 1;
          setTimeout(this.eraseText, this.erasingSpeed);
        } else {
          this.typeStatus = false;
          this.displayTextArrayIndex += 1;
          if (this.displayTextArrayIndex >= this.displayTextArray.length)
            this.displayTextArrayIndex = 0;
          setTimeout(this.typeText, this.typingSpeed + 1000);
        }
      },
    },
  };
  </script>
  
  <style scoped>
  .container {
    width: 100%;
    
    display: flex;
    
    
  }
  h1 {
    margin-left:3.8rem;
    margin-top: 4.2rem;
    color: white;
    font-size: 2rem;
    font-family: 'Josefin Sans', sans-serif;
    font-family: 'Kanit', sans-serif;
    font-family: 'Montserrat', sans-serif;
    
    }
h1 .blinking-cursor {
        color: #f39c12;
    }
  
  </style>
  