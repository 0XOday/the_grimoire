integer currPrice
integer lastMonthPrice
float estMortgage
float pChange

currPrice = Get next input
lastMonthPrice = Get next input

pChange = currPrice - lastMonthPrice
estMortgage = (currPrice * 0.045) / 12
Put "This house is $" to output
Put currPrice to output
Put "." to output
Put " The change is $" to output
Put pChange to output
Put " since last month.\n" to output
Put "The estimated monthly mortage is $" to output
Put estMortgage to output with 2 decimal places
Put "." to output