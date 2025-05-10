# JMeter GET Request Simulator

A performance testing project using Apache JMeter to simulate HTTP GET requests and analyze API performance.

## ? Overview

This repository contains a JMeter test plan designed to simulate and evaluate the performance of RESTful API GET requests. The test plan is configured to:

- Send concurrent GET requests to retrieve user data from a RESTful API
- Apply appropriate assertions to validate responses
- Collect performance metrics using various listeners

## ? Test Configuration

### Thread Group Setup

- **Users (Threads)**: 10 concurrent users
- **Ramp-up Period**: 5 seconds
- **Loop Count**: 5 iterations per user
- **Total Requests**: 50 requests (10 users ? 5 iterations)

### HTTP Request Details

- **Endpoint**: https://reqres.in/api/users?page=2
- **Method**: GET
- **Protocol**: HTTP/HTTPS
- **Connection**: Keep-alive enabled for better performance

### Assertions

Response assertions have been configured to verify:
- Response contains "email" field
- Successful HTTP status codes

## ? Performance Monitoring

The test plan includes multiple result collectors:

1. **Graph Results**: Visual representation of response times and throughput
2. **Summary Report**: Aggregated test metrics including:
   - Average response time
   - Min/Max response times
   - Throughput (requests/second)
   - Error rate percentage
3. **View Results Tree**: Detailed inspection of individual requests and responses

## ? Test Results

Initial test results with 10 concurrent users and 5 iterations each showed:

- Successful simulation of concurrent API requests
- Acceptable average response times
- Low error rate under the tested load
- Proper validation of response data

## ? How to Run

1. Install [Apache JMeter](https://jmeter.apache.org/download_jmeter.cgi) (v5.6.3 or later recommended)
2. Clone this repository
3. Open the `Thread Group.jmx` file in JMeter
4. Click the Run button or press Ctrl+R to start the test

## ? Use Cases

This simulator can be used for:

- API performance testing
- Load capacity evaluation
- Response time analysis
- Reliability testing
- Error handling validation

## ? Related Projects

If you need more advanced setups, check out the [jmeter-docker](https://github.com/ajeetraina/jmeter-docker) repository for setting up JMeter in a distributed Docker environment.

## ? License

This project is licensed under the MIT License - see the LICENSE file for details.