/*
Description: 牛客后台会记录每个用户的试卷作答记录到exam_record表，现在有两个用户的作答记录详情如下：

用户1001在2021年9月1日晚上10点11分12秒开始作答试卷9001，并在50分钟后提交，得了90分；
用户1002在2021年9月4日上午7点1分2秒开始作答试卷9002，并在10分钟后退出了平台。
试卷作答记录表exam_record中，表已建好，其结构如下，请用一条语句将这两条记录插入表中。
*/

INSERT INTO exam_record(id, uid, exam_id, start_time, submit_time, score)
VALUES(NULL, 1001, 9001, "2021-09-01 22:11:12", "2021-09-01 22:11:12" + INTERVAL 50 minute, 90),
(NULL, 1002, 9002, "2021-09-04 07:01:02", NULL, NULL);

#Key Point 1: 如果要插入多行，指令是 values <row1>,<row2>...多行之间用逗号隔开
INSERT INTO table_name(column_name1, column_name2,...)
VALUES(value1, value2,...), (value3, value4,...);

#Key Point 2: INTERVAL 时间间隔关键字，常和date_add() 或 date_sub()搭配使用
#表示方法1
A.T_DATE = B.T_DATE+ interval '1' hour  1小时以后
A.T_DATE = B.T_DATE+ interval 1 hour    1小时以后
A.T_DATE = B.T_DATE+ interval +1 hour   1小时以后
#表示方法2
A.T_DATE = B.T_DATE+ interval -1 hour   1小时之前
A.T_DATE = B.T_DATE+ interval '-1' hour 1小时之前
A.T_DATE = B.T_DATE+ interval -'1' hour 1小时之前
#表示方法3
A.T_DATE = B.T_DATE- interval -'1' hour 1小时之后（负负得正）
