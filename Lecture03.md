

hadoop fs -get /user/maria_dev/wordcount/* /wordcount 

ls /wordcount


hadoop jar wordcount.jar com.WordCount /user/maria_dev/wordcount/wordcount.txt /user/maria_dev/wordcount/output.txt

