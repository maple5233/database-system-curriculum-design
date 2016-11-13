## 实体模型表

排序规则为`utf8_general_ci`

以下没有指明可以空的都非空

### 学生信息表Student

```json
表名：students
{
  student_id	:	SMALLINT 主键 自增		// 学生的学号
  student_name	:	CHAR(10) 索引	   		 // 学生的注册名字，一般是自己的姓名
  student_pass	:	VARCHAR	 			  // 学生的注册密码
}
```

### 课程信息表Course

```json
表名：courses
{
  course_id		:	SMALLINT 主键 自增		// 课程号
  course_name	:	CHAR(10) 索引			 // 课程的名字
  teacher_id	:	外键			 		 // 属于哪个老师
}
```

### 老师信息表Teacher

```json
表名：teachers
{
  teacher_id	:	SMALLINT 主键 自增       // 教师工号
  teacher_name	:	CHAR(10) 索引	   		  // 老师的注册名字，一般是自己的姓名
  teacher_pass	:	VARCHAR	 			   // 老师的注册密码
}
```

### 作业信息表Homework

```json
表名：homework
{
  homework_id			:	SMALLINT 主键 自增        // 作业流水号
  homework_title		:	VARCHAR				     // 作业的标题
  homework_contant		:	VARCHAR	 可空			    // 作业内容
  homework_create_date	:	DATE	 默认为添加时间	 // 作业的添加时间
  homework_ddl			:   DATETIME 可空				// 作业的deadline
  course_id				:   外键						// 作业属于哪门课程
}
```



