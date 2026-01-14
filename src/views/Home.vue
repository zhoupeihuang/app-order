<template>
  <div class="order-app">
    <h2>Order Management (Sub-App)</h2>
    <el-tabs v-model="activeName">
      <el-tab-pane label="Pending" name="pending">
        <el-empty description="No pending orders" />
      </el-tab-pane>
      <el-tab-pane label="Shipped" name="shipped">
        <el-timeline>
          <el-timeline-item timestamp="2024/4/12" placement="top">
            <el-card>
              <h4>Order #12345 Shipped</h4>
              <p>FedEx Tracking: 88888888</p>
            </el-card>
          </el-timeline-item>
          <el-timeline-item timestamp="2024/4/3" placement="top">
            <el-card>
              <h4>Order #12344 Delivered</h4>
              <p>Signed by: Customer</p>
            </el-card>
          </el-timeline-item>
        </el-timeline>
      </el-tab-pane>
    </el-tabs>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const activeName = ref('shipped')
</script>

<style scoped>
.order-app {
  padding: 20px;
}
</style>
