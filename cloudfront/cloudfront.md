# Secure access to private files located in S3

* Signed URLs
* Signed Cookies
* Origin Access Identity


# Lambda@Edge

* No need to create in all region, create in 1 region and replicate to all regions

# Query Parameter forwarding
* '&' as delimiter
* Parameter names are case sensitive
* Has to be web distribution

# Distributions
* Web
* RTMP

# Misc
Singed Cookies - One single cookie for multiple S3 objects, can use custom policy to control access. Canned policies allow you to specify an expiration date only. Custom policies allow more complex restrictions. 