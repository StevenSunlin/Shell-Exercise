# 9.2 Page 226
- $REPLY变量 用read方式验证$REPLY, 写脚本　your name and your father name
- $SECONDS变量　写一个脚本　五次循环　每次休眠两秒　最后统计脚本运行时间
- $REPLY变量　用select 语句验证$REPLY变量
- $TMOUT变量　写脚本　限制输入时间为3秒　超时显示you name is Null.
- 计算string字符串长度的三种方法． expr length "$string" ;; echo ${#string} ;; echo "$string" | wc -L ;;
- ${string:position} ==> 从position开始抽取子串. ${string:position:length}==>从position开始抽取长度为length的子串
- {string: -position}和　{string:(position)}　==> 与6相反，从右向左．
- expr index $string $substring ==> 检索匹配的次数
- expr match $string $substring ==> 从开头匹配的长度，若无既是0
- expr $string ==>从1开始标号．　${string:position}==>从0开始标号．
- ${string#substring} ==> 删除匹配到的最短子串．　${string-substring} ==>删除匹配到的最长子串．
- ${string/substring/replacement} ==> 替换第一次与substring匹配的字符串．　${string//substring/replacement} ==> 替换所有与substring匹配的字符串．
- ${string/#substring/replacement} ==> 替换string开头处与substring相匹配的字符串．　${string/%substring/replacement} ==>　替换结尾处与substring相匹配的字符串．

# 9.3 Page232
- declare [选项]　变量名
- 参数列表　-r 只读; -i　整形数; -a 数组; -f 所有函数名及内容; -F 所有函数名; -x 声明为环境变量
- let 与 declare -i　
- eval tempval=\$$variable1 间接引用变量的第一种格式; tempval=${!variable1} 间接引用变量的第二种格式

# 9.5 Page 262
- expr
- bc　计算; scale ==>保留几位小数; 脚本中的格式: variable=`echo "options; expressions" | bc` ==> e.g. var3=`echo "scale=5; $var1 ^ 2" | bc`
- 练习: 利用bc 计算半径为20的圆面积, 保留小数点后五位
- 练习题

# 10.1 Page 268
- cat命令和more 命令；最大区别是分页；
-　sed; sed "s/var1/replace/g" 将var1全部替换为replace
- awk; echo $string | awk '{print length($0)}';; echo $string | awk '{print length($1)}';; echo $string | awk '{print substring($0,1,8)}';; echo $string | awk '{print substring)($string,25)}';;
- awk 调用命令要使用双引号
- I/O重定向; who | tee output 将who 输出添加到output文件中，同时屏幕打印who命令的输出内容;;　who | tee -a output 追加到output文件末尾
- 
