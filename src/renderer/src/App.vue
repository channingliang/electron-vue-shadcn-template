<script setup>
import Versions from './components/Versions.vue'
import { Button } from '@renderer/components/ui/button'

const ipcHandle = () => window.electron.ipcRenderer.send('ping')
</script>

<template>
  <img alt="logo" class="logo" src="./assets/electron.svg" />
  <div class="creator">Powered by electron-vite</div>
  <div class="text">
    Build an Electron app with
    <span class="vue">Vue</span>
  </div>
  <p class="tip">Please try pressing <code>F12</code> to open the devTool</p>
  <div class="actions">
    <div class="action">
      <a href="https://electron-vite.org/" target="_blank" rel="noreferrer">Documentation</a>
    </div>
    <div class="action">
      <a target="_blank" rel="noreferrer" class="text-red-600 font-thin text-4xl" @click="ipcHandle">Send IPC</a>
    </div>

  </div>
  <Button variant="outline" class="mt-4 font-bold">Shadcn-vue</Button>
  <Versions />
</template>
