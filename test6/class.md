@startuml
title ����GitHub��ʵ�����ƽ̨--��ͼ
class CLASS{
    CLASS_ID(�γ̱��)
    CLASS__NAME(�γ�����)
}
class users {
    <b>user_id</b> ���û�ID��
    name ���û���ʵ������
    github_username ���û�GitHub�˺ţ�
    update_date ���û�GitHub�˺��޸����ڣ�
    password ���û����룩
    disable ���û��Ƿ���ã�
    CLASS_IDS(��ѡ�γ̱�ż���)
}
class teachers{
    <b>teacher_id</b> ����ʦ���ţ�
    department ����ʦ�������ţ�
}
class students{
    <b>student_id</b> ��ѧ�ţ�
    class ���༶��
    result_sum���ɼ����ܣ�
    web_sum ����վ��ȷ�����ܣ�
}
class grades {
    <b>student_id</b> ��ѧ�ţ�
    <b>test_id</b> ��ʵ���ţ�
    result ����ʵ���ܷ�����
    code (��������)
    improve������Ľ��÷֣�
    report(ʵ�鱨��÷�)
    update_date ���������ڣ�
}

class tests {
    <b>test_id</b> ��ʵ���ţ�
    title (ʵ������)
}
CLASS <|- tests
users <|- students
users <|-- teachers

users "1"--"n" CLASS
students "1" -- "n"  grades
tests "1" -- "n"  grades


@enduml