<template>
    <div>
      <!-- زر فتح الـDialog -->
      <button @click="openDialog">Open Dialog</button>
  
      <!-- Dialog -->
      <div v-if="showDialog" class="dialog-overlay">
        <div class="dialog-box">
          <h3>Dialog Title</h3>
          <p>This is the content of the dialog.</p>
          <button @click="closeDialog">Close</button>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        showDialog: false, // التحكم في إظهار وإخفاء الـDialog
      };
    },
    methods: {
      openDialog() {
        this.showDialog = true; // عرض الـDialog
      },
      closeDialog() {
        this.showDialog = false; // إخفاء الـDialog
      },
    },
  };
  </script>
  
  <style>
  /* تنسيقات الـDialog */
  .dialog-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .dialog-box {
    background: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    text-align: center;
  }
  </style>
  