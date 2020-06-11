<template>
  <div class="app-container">
    <el-form :model="role" label-width="80px" label-position="left">
      <el-form-item label="车类型" required>
        <el-radio-group v-model="form.resource">
          <el-radio label="普通车" />
          <el-radio label="C位车" />
        </el-radio-group>
      </el-form-item>
      <el-row :gutter="12">
        <el-col :span="6">
          <el-form-item label="品牌" required>
            <el-select v-model="form.region" placeholder="请选择">
              <el-option label="区域一" value="shanghai" />
              <el-option label="区域二" value="beijing" />
            </el-select>
          </el-form-item>
        </el-col>
        <el-col :span="6">
          <el-form-item label="厂商" required>
            <el-select v-model="form.region" placeholder="请选择">
              <el-option label="区域一" value="shanghai" />
              <el-option label="区域二" value="beijing" />
            </el-select>
          </el-form-item>
        </el-col>
      </el-row>
      <el-row :gutter="12">
        <el-col :span="6">
          <el-form-item label="车系" required>
            <el-select v-model="form.region" placeholder="请选择">
              <el-option label="区域一" value="shanghai" />
              <el-option label="区域二" value="beijing" />
            </el-select>
          </el-form-item>
        </el-col>
        <el-col :span="6">
          <el-form-item label="车型" required>
            <el-select v-model="form.region" placeholder="请选择">
              <el-option label="区域一" value="shanghai" />
              <el-option label="区域二" value="beijing" />
            </el-select>
          </el-form-item>
        </el-col>
      </el-row>

    </el-form>
    <div style="text-align:left;">
      <el-button type="danger">取消</el-button>
      <el-button type="primary">确定</el-button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        name: '',
        region: '',
        date1: '',
        date2: '',
        delivery: false,
        type: [],
        resource: '',
        desc: ''
      }
    }
  },

  created() {
    // Mock: get all routes and roles list from server
  }
}
</script>

<style lang="scss" scoped>
.app-container {
  .roles-table {
    margin-top: 30px;
  }
  .permission-tree {
    margin-bottom: 30px;
  }
}
</style>
