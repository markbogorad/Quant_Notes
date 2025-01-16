up:: [[BOOST]]
tags:: #Programming 
# Statistical Functions
- C++ has statistical distribution functions
- Can modify the normal to work with others
## EX: QuantNet Level 8 Exercise 5:
```
#include <boost/math/distributions/exponential.hpp>
#include <boost/math/distributions/poisson.hpp>
#include <iostream>
#include <cmath> // Required for additional calculations

int main() {
	using namespace std;
	using namespace boost::math;

// Exponential Distribution with lambda = 0.5 (mean = 2.0)
	exponential_distribution<double> myExponential(0.5); // Rate parameter lambda
	cout << "***Exponential Distribution" << endl;
	cout << "Mean: " << mean(myExponential) << endl;
	cout << "Standard Deviation: " << standard_deviation(myExponential) << endl;

// Distributional properties
	double x = 10.25;
	cout << "PDF: " << pdf(myExponential, x) << endl;
	cout << "CDF: " << cdf(myExponential, x) << endl;

// Choose precision
	cout.precision(10); // Number of values behind the comma

// Exponential distribution additional properties
	cout << "Variance: " << variance(myExponential) << endl;
	cout << "Median: " << median(myExponential) << endl;
	cout << "Mode: " << 0.0 << " (The mode of an exponential distribution is always 0)" << endl;
	cout << "Kurtosis excess: " << kurtosis_excess(myExponential) << endl;
	cout << "Kurtosis: " << kurtosis(myExponential) << endl;
	cout << "Skewness: " << skewness(myExponential) << endl;
	cout << "Characteristic function: " << chf(myExponential, x) << endl;
	cout << "Hazard: " << hazard(myExponential, x) << endl;



// Poisson Distribution with mean = 3.0
poisson_distribution<double> myPoisson(3.0); // Mean
	cout << "\n***Poisson Distribution" << endl;
	cout << "Mean: " << mean(myPoisson) << endl;
	cout << "Standard Deviation: " << standard_deviation(myPoisson) << endl;
	cout << "PDF: " << pdf(myPoisson, x) << endl;
	cout << "CDF: " << cdf(myPoisson, x) << endl;
	cout << "Variance: " << variance(myPoisson) << endl;
	cout << "Median: " << median(myPoisson) << endl;
	cout << "Mode: " << mode(myPoisson) << endl;
	cout << "Kurtosis excess: " << kurtosis_excess(myPoisson) << endl;
	cout << "Kurtosis: " << kurtosis(myPoisson) << endl;
	cout << "Skewness: " << skewness(myPoisson) << endl;
	cout << "Characteristic function: " << chf(myPoisson, x) << endl;
	cout << "Hazard: " << hazard(myPoisson, x) << endl;
	cout << "\n " << endl;

// PDF and CDF lists for the Poisson
	vector<double> pdfList;
	vector<double> cdfList;

	double start = 0.0;
	double end = 10.0;
	long N = 30; // Number of subdivisions

	x = 0.0;
	double h = (end - start) / double(N);

	for (long j = 1; j <= N; ++j)
{
	pdfList.push_back(pdf(myPoisson, x));
	cdfList.push_back(cdf(myPoisson, x));

	x += h;
}

cout << "Poisson PDF Lists:" << endl;
for (long j = 0; j < pdfList.size(); ++j)
{
	cout << pdfList[j] << ", ";
}

cout << "\n\n" << endl;
cout << "Poisson CDF Lists:" << endl;
for (long j = 0; j < cdfList.size(); ++j)

{
cout << cdfList[j] << ", ";
}

return 0;

}
```