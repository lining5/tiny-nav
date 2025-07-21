<template>
    <footer class="container mx-auto">
        <div class="flex items-center justify-center text-gray-500">
            <!-- 左侧内容：版权信息和链接 -->
            <div class="flex items-center gap-2">
                <span>Copyright © {{ currentYear }}</span>
            </div>

            <!-- 分隔符点 -->
            <span class="mx-2 text-gray-500">·</span>

            <!-- 右侧内容：GitHub图标链接 -->
            <div class="flex items-center gap-2">
            </div>
        </div>
    </footer>
</template>

<script setup lang="ts">
const currentYear = new Date().getFullYear()
</script>
