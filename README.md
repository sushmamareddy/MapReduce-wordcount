# MapReduce-wordcount

Running MR Job

Step 1 –Create a file named word_count_data.txt
Step 2 – hdfs dfs -put word_count_data.txt /user/root/
Step 3 – Create the mapper.py and reducer.py files
Step 4 – Run below command to start the job
  hadoop jar /usr/hdp/current/hadoop-mapreduce-client/hadoop-streaming.jar \
  -input /user/root/wordcount.txt \
  -output /user/root/wordcountoutput \
  -mapper mapper.py \
  -reducer reducer.py \
  -file /root/mapreduce/mapper.py \
  -file /root/mapreduce/reducer.py
Step 5 – Monitor the job here
  http://localhost:8088/cluster
