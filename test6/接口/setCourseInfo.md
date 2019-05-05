<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getCourseInfo  [返回](../README.md)
用例： [选择课程](../用例/选择课程.md)

- 功能：
    选择课程
    
- 权限：
    学生/老师：查看自己的课程信息，必须先登录，不能查看其他用户的课程信息。    
    
- API请求地址： 
    接口基本地址/v1/api/setCourseInfo/<user_id>

- 请求方式 ：
    GET
      
- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |user_id|用户的ID号。对应表USERS.USER_ID的值|
  |course_name|课程的NAME号。对应表COURSE.COURSE_NAME的值|
- 返回实例：

    如果是老师登录，则返回信息需要多一个课程编号

        {         
            "status": true,
            "info": null,
            "user_id":"201610111",    
            "user_name":"张三",
            "course_name":"IT新技术"
            "course_term":"2016级"           
        }
        
        
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |user_id|学号或者工号|
  |user_name|用户的真实姓名|  
  |course_name|课程名称|
  |course_term|学期|
 

