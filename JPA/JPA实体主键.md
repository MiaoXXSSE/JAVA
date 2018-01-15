# ObjectDB #

  [JPA主键：http://www.objectdb.com/java/jpa/entity/id](#http://www.objectdb.com/java/jpa/entity/id)

实体对象在保存对象前需要注解@Id

## 主键类型 ##

- 原始类型：布尔型，字节型，短型，char型，int型，long型，float型，double型。
- 包java.lang中的等价包装类：Byte，Short，Character，Integer，Long，Float，Double。
- java.math.BigInteger，java.math.BigDecimal。
- java.lang.String中。
- java.util.Date，java.sql.Date，java.sql.Time，java.sql.Timestamp。
- 任何枚举类型。
- 引用一个实体对象

## 复合主键 ##

由多个主键字段组成，每个字段需要是上面的类型

有多个主键字段时

<pre>
  @Entity  @IdClass(ProjectId.class)
  public class Project {
    @Id int departmentId;
    @Id long projectId;
  }
  
  Class ProjectId {
    int departmentId;
    long projectId;
}
</pre>
