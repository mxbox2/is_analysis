# 实验一：业务流程建模
### 流程图1：考试即成绩管理流程
PlantUML源码如下：
```
@startuml
|教务处|
start
:安排考试;
:安排考试表;
|#AntiqueWhite|教师|
:出卷;
split
    :A、B试卷;
split again
    :打印审批表;
        |班主任|
    :审批签字;
    :打印审批表;
end split
|教务处|
:打印试卷;
:试卷;
|#AntiqueWhite|学生|
:参加考试;
:答卷;
|教师|
:阅卷出成绩;
split
    :成绩单;
    |教务处|
    if(有不及格？)then(有)
        :安排补考;
        :补考安排表;
    endif
split again
|教师|
:答卷;
:装订存档;
endsplit
fork
:期末流程结束;
endfork
stop
@enduml
```
业务流程图如下：

![图片加载失败](./img1.png)

流程说明：

### 流程图2： 客户维修服务流程
PlantUML源码如下：
```
@startuml
|客户|
start
:申请服务;
|#AntiqueWhite|业务经理|
    if(是新客户吗？)then(是)
        :登记客户信息;
    else(不是)
    endif
        :上门勘察;
        :制定方案;
|客户|
 if(满意吗？)then(否)
    stop
 else(是)
    :签订服务合同;
     |业务经理|
        fork
            :安排工人;
         forkagain
            :安排材料;
        endfork
        :填写派工单;
     |工人|
     :领取材料;
     :上门服务;
     |客户|
     :验收并填写反馈意见;
     |业务经理|
     :交回派工单;
     |#AntiqueWhite|财务人员|
     :结束收款;
endif
stop
@enduml
```
业务流程图如下:

![图片加载失败](./img2.png)

流程说明：