## 基于ant Design封装的搜索组件 
![SearchFrom](https://img.xuewuzhijing.top/admin/SearchFrom.png)
 
 ##### 参数：
  > name:input的名称  
  type："text" "number" 两种类型，number只能输入数字
  input的数量：根据name元素的个数生成
 ```
 searchCriteria:{
    name:{
            name:"游戏名称",
            id:"游戏Id",
            xxx:"4",
            sss:"55",
            sss:"8888"
        },
    type:{
        name:"text",
        id:"number"
    }
 }
 ```
 
 ##### result:
 
 ```
  handleSearch = e => {
     e.preventDefault();
     this.props.form.validateFields((err, values) => {
         console.log('Received values of form: ', values);
         this.props.criteriaVal(values) //值回调给父元素
 });
 };
  ```       