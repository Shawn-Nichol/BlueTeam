Google Dorking, also known as Google hacking, refers to the use of advanced search techniques using specific search strings or operators within Google's search engine to discover sensitive information or vulnerabilitites on the internet.

This technique involves using specific search queries operators and filters to find information that isn't typically indexed in regular searches. By employing advanced operators like "site, filetype, intittle, inurl, and more," users can narrow down search results to find exposed data vulnerable websites, login pages, confidential documents, and other sensitive information inadvertently shared online.

# Specifie file types
site: example.com filetype:pdf "confidential"

# Locate login pages
intittle:"WordPress Login" site:.com

# Finding Vulnerable URLs
intitle:"index of" site:example.com

# Exploting Public Documents
site:.edu filetype:xls intext:"budge planning"

# Identifying Network devices
intitle:"Login" inur"admin site:.com

# Exploring specific domains
site: gov filetype:pptx "artificial intelligence"
