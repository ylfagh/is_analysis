@startuml
title 基于GitHub的实验管理平台--类图
class CLASS{
    CLASS_ID(课程编号)
    CLASS__NAME(课程名称)
}
class users {
    <b>user_id</b> （用户ID）
    name （用户真实姓名）
    github_username （用户GitHub账号）
    update_date （用户GitHub账号修改日期）
    password （用户密码）
    disable （用户是否禁用）
    CLASS_IDS(所选课程编号集合)
}
class teachers{
    <b>teacher_id</b> （老师工号）
    department （老师所属部门）
}
class students{
    <b>student_id</b> （学号）
    class （班级）
    result_sum（成绩汇总）
    web_sum （网站正确与否汇总）
}
class grades {
    <b>student_id</b> （学号）
    <b>test_id</b> （实验编号）
    result （该实验总分数）
    code (代码评分)
    improve（代码改进得分）
    report(实验报告得分)
    update_date （评改日期）
}

class tests {
    <b>test_id</b> （实验编号）
    title (实验名称)
}
CLASS <|- tests
users <|- students
users <|-- teachers

users "1"--"n" CLASS
students "1" -- "n"  grades
tests "1" -- "n"  grades


@enduml