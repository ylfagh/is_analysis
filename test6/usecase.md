```class
@startuml
title ����GitHub��ʵ�����ƽ̨--����ͼ
actor teachers
actor students
actor users
users <|-- teachers
users <|-- students

package �û������� {
users --up-> (��¼)
users --up-> (�ǳ�)
users --up-> (�鿴�û���Ϣ)
users --up-> (�޸��û���Ϣ)
users --up-> (�޸�����)
}
package ҵ�������� {
    users--->(ѡ��γ�)
teachers ---> (�����ɼ�)
teachers ---> (ѧ���б�)
students ---> (ѧ���б�)
students ---> (�鿴�ɼ�)
}
```
@enduml