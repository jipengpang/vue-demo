<template>
  <div>
    <el-row>
<!--      绑定model="form"很重要，否则验证无法对应到form-item-->
      <el-form :model="form" label-width="120px" ref="form" style="width: 50%; margin: 0 auto;" :rules="formRules">
        <el-col :lg="24" :md="12" :sm="12">
          <el-form-item label="USERNAME" prop="username">
            <el-input v-model="form.username" placeholder="PLEASE INPUT A USERNAME" />
          </el-form-item>
        </el-col>
        <el-col :lg="24" :md="12" :sm="12">
          <el-form-item label="PASSWORD" prop="password">
            <el-input v-model="form.password" type="password" placeholder="PLEASE INPUT A PASSWORD"/>
          </el-form-item>
        </el-col>
        <el-col :lg="24" :md="12" :sm="12">
          <el-form-item label="RE-PASSWORD" prop="repassword">
            <el-input v-model="form.repassword" placeholder="PLEASE REPEAT THE PASSWORD"/>
          </el-form-item>
        </el-col>
      </el-form>

    </el-row>
    <el-row>
      <el-button type="primary" size="medium" style="width: 120px;">SUBMIT</el-button>
    </el-row>
<!--    <el-row>-->
<!--      <el-form :model="ruleForm" :rules="rules" ref="ruleForm" label-width="100px" class="demo-ruleForm">-->
<!--        <el-form-item label="活动名称" prop="name">-->
<!--          <el-input v-model="ruleForm.name"></el-input>-->
<!--        </el-form-item>-->
<!--        <el-form-item label="活动区域" prop="region">-->
<!--          <el-select v-model="ruleForm.region" placeholder="请选择活动区域">-->
<!--            <el-option label="区域一" value="shanghai"></el-option>-->
<!--            <el-option label="区域二" value="beijing"></el-option>-->
<!--          </el-select>-->
<!--        </el-form-item>-->
<!--        <el-form-item label="活动时间" required>-->
<!--          <el-col :span="11">-->
<!--            <el-form-item prop="date1">-->
<!--              <el-date-picker type="date" placeholder="选择日期" v-model="ruleForm.date1" style="width: 100%;"></el-date-picker>-->
<!--            </el-form-item>-->
<!--          </el-col>-->
<!--          <el-col class="line" :span="2">-</el-col>-->
<!--          <el-col :span="11">-->
<!--            <el-form-item prop="date2">-->
<!--              <el-time-picker placeholder="选择时间" v-model="ruleForm.date2" style="width: 100%;"></el-time-picker>-->
<!--            </el-form-item>-->
<!--          </el-col>-->
<!--        </el-form-item>-->
<!--        <el-form-item label="即时配送" prop="delivery">-->
<!--          <el-switch v-model="ruleForm.delivery"></el-switch>-->
<!--        </el-form-item>-->
<!--        <el-form-item label="活动性质" prop="type">-->
<!--          <el-checkbox-group v-model="ruleForm.type">-->
<!--            <el-checkbox label="美食/餐厅线上活动" name="type"></el-checkbox>-->
<!--            <el-checkbox label="地推活动" name="type"></el-checkbox>-->
<!--            <el-checkbox label="线下主题活动" name="type"></el-checkbox>-->
<!--            <el-checkbox label="单纯品牌曝光" name="type"></el-checkbox>-->
<!--          </el-checkbox-group>-->
<!--        </el-form-item>-->
<!--        <el-form-item label="特殊资源" prop="resource">-->
<!--          <el-radio-group v-model="ruleForm.resource">-->
<!--            <el-radio label="线上品牌商赞助"></el-radio>-->
<!--            <el-radio label="线下场地免费"></el-radio>-->
<!--          </el-radio-group>-->
<!--        </el-form-item>-->
<!--        <el-form-item label="活动形式" prop="desc">-->
<!--          <el-input type="textarea" v-model="ruleForm.desc"></el-input>-->
<!--        </el-form-item>-->
<!--        <el-form-item>-->
<!--          <el-button type="primary" @click="submitForm('ruleForm')">立即创建</el-button>-->
<!--          <el-button @click="resetForm('ruleForm')">重置</el-button>-->
<!--        </el-form-item>-->
<!--      </el-form>-->
<!--    </el-row>-->
  </div>
</template>
<script>
export default {
  name: 'FirstPage',
  data () {
    return {
      form: {
        username: '',
        password: '',
        repassword: ''
      },
      formRules: {
        username: [
          {
            required: true,
            message: '请输入用户名',
            trigger: 'blur'
          }, {
            min: 3,
            max: 5,
            message: '长度在 3 到 5 个字符'
          }
        ],
        password: [
          {
            required: true,
            message: '请输入密码',
            trigger: 'blur'
          }
        ]
      },

      // ruleForm: {
      //   name: '',
      //   region: '',
      //   date1: '',
      //   date2: '',
      //   delivery: false,
      //   type: [],
      //   resource: '',
      //   desc: ''
      // },
      // rules: {
      //   name: [
      //     { required: true, message: '请输入活动名称', trigger: 'blur' },
      //     { min: 3, max: 5, message: '长度在 3 到 5 个字符', trigger: 'blur' }
      //   ],
      //   region: [
      //     { required: true, message: '请选择活动区域', trigger: 'change' }
      //   ],
      //   date1: [
      //     { type: 'date', required: true, message: '请选择日期', trigger: 'change' }
      //   ],
      //   date2: [
      //     { type: 'date', required: true, message: '请选择时间', trigger: 'change' }
      //   ],
      //   type: [
      //     { type: 'array', required: true, message: '请至少选择一个活动性质', trigger: 'change' }
      //   ],
      //   resource: [
      //     { required: true, message: '请选择活动资源', trigger: 'change' }
      //   ],
      //   desc: [
      //     { required: true, message: '请填写活动形式', trigger: 'blur' }
      //   ]
      // }

    }
  }
}
</script>
<style>

</style>
