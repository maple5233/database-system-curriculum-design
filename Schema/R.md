## 模型间的关系表

排序规则为`utf8_general_ci`

以下没有指明可以空的都非空

### 选课关系表（课程-学生关系表）

```json
{
  course_selection_id	:	SMALLINT 主键，自增	// 选课关系的流水号
  student_id			:	外键				  // 选课的学生
  course_id				:	外键				  // 选课的课程
}
```

### 作业本表 （作业-学生关系表）

```json
{
  do_homework_id	:	SMALLINT 主键，自增	// 作业本的流水号
  homework_id		:	外键				  // 哪个作业
  student_id		:	外键				  // 谁写的
  submit_contant	:	VARCHAR	 可空		  // 写的内容
  submit_time		:	DATETIME		   // 提交时间
  homework_grade	:	TINYINT  可空		  // 作业的成绩
}
```

