CXX=spark-submit
CXXFLAGS=--num-executors=8 --executor-cores 4
input = input.txt
#input = soc-LiveJournal1.txt
output = output

all:
	#$(CXX) $(CXXFLAGS) ex05.py $(input) $(output)
	#################This is for scala##############
	sbt package
	$(CXX) $(CXXFLAGS) --class "A2" --master local[4] target/scala-2.11/a2_2.11-1.0.jar $(input) $(output)
	#################Scala ends here##############
demo:
	# $(CXX) $(CXXFLAGS) ex05.py $(input) $(output)
	#################This is for scala##############
	$(CXX) $(CXXFLAGS) --class "A2" --master local[4] target/scala-2.11/a2_2.11-1.0.jar $(input) $(output)
	#$(CXX) $(CXXFLAGS) --driver-memory 5g --class "A2" --master local[4] target/scala-2.11/a2_2.11-1.0.jar $(input) $(output)
	#################Scala ends here##############
clean:
	rm -r output
clean-all:
	rm -r output
	#################This is for scala##############
	rm -r project
	rm -r target
	#################Scala ends here##############
