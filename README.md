This Terraform project should be to enable proper permissions to an s3 bucket for Zappa and Django-s3 to access it.

I need to remember to make a Terraform file that can do this:

1. create an s3 bucket
2. (Make the name of the s3 bucket a user input)
3. Add the following to CORS
[
    {
        "AllowedHeaders": [
            "Authorization"
        ],
        "AllowedMethods": [
            "GET"
        ],
        "AllowedOrigins": [
            "*"
        ],
        "ExposeHeaders": [],
        "MaxAgeSeconds": 3000
    }
]

4. Enable ACLs (In the console, it's under Object Ownership)
