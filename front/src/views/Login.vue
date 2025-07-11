<template>
    <AppLayout>
        <div class="bg-white dark:bg-gray-800 p-8 rounded-lg shadow-lg dark:shadow-gray-900 max-w-md mx-auto mt-20">
            <!-- 标题和深色模式按钮 -->
            <div class="flex justify-between items-center mb-6">
                <h1 class="text-4xl font-bold text-blue-900 dark:text-blue-300">首页</h1>
                <div class="flex space-x-2">
                    <button @click="themeStore.toggleTheme"
                        class="w-10 h-10 flex items-center justify-center rounded-full bg-gray-200 dark:bg-gray-700 text-gray-800 dark:text-gray-100 hover:bg-gray-300 dark:hover:bg-gray-600">
                        <div
                            :class="themeStore.isDarkTheme ? 'i-mdi-white-balance-sunny' : 'i-mdi-moon-waxing-crescent'">
                        </div>
                    </button>
                </div>
            </div>
        </div>
    </AppLayout>
</template>

<script setup lang="ts">
import { useThemeStore } from '@/stores/themeStore'
import AppLayout from '@/components/AppLayout.vue'

const themeStore = useThemeStore()
themeStore.applyTheme()
</script>
