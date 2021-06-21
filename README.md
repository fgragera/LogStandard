# RequestLogStandard

## Propusal:
Standardise the way in which requests for the different services a company may have are published. 

## Utility:
The utility we can give to having standardised requests are several, but we will focus on two.

* Ease when you move from project to project within your company and you have to work with incidents and need to use service requests, it is easier if you are used to working in a specific way.

* Creating general tools that need these requests, for example, we could have a tool that compares traffic between two different versions of our software, to catch the requests is easier if all projects use the same way to publish their requests. Otherwise it would be the tool that would have to adapt to how the other projects publish their requests.

## How we will do it:
We are going to implement a starter for spring-boot that will allow us to register a filter in the service to get the request that has arrived to the service to publish it in kafka, file, elastic.... What will be special about it is that it will have metadata that will tell us if it has been a POST, what headers the request had, name of the operation, etc.
The library will expose an API so that other tools can interpret this information that the service is extracting.
