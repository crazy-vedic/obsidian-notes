# 1. Based on process size
	if a 200kb size process took 2ms, then future 190 kb should also take 2ms
# 2. Based on process type
	Operating system process(3-5 units)
	User Processes
		Interactive (5-6)
		Foreground(10-15 units)
		Background(15-20 units)
# 3. Based on simple averaging
	Burst time of prcoess now is the average of all past averages
# 4. Dynamic Averaging
	Tn+1 = a tn + (1-a)Tn
		where:
			Tn is predicted
			tn is actual
			a is smoothening factor (0->1)
	Second process can be calculated based on previous process