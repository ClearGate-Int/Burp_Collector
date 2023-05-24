A Multi-Processing Tool for extracting information to XLSX file from a Burp Suite file (After Generating Enough Traffic).

1. Extract API Endpoints based on the XML/JSON Content-Type in the response (SOAP, REST and GraphQL).
2. Collect --bitrix result to JSON file with body and parameters for Postman Application
3. Extract PATHs and Possible APIs from response body.
4. Extract URLs from response body.
5. Extract Secrets (AWS/Google/Firebase,etc').
6. Collect JSON files based on Burp response via REGEX

OPTION - 1: In Burp Suite: Right Click on the domain in the Target Scope - Select "save selected items" and then select "Base64-encode" (Some requests may be missing from the target tree scope - Burp Suite issue...).

OPTION - 2: In Burp Suite: Navigate to Proxy - HTTP History - Press CTRL + A - Right Click - Select "save selected items" - Leave "Base64-encode" checked (This way all of your requests will be included, again go blame PortSwigger).

Installation: 

      pip install -r requirements.txt
      python -m spacy download en_core_web_sm

Usage: Burp_API_Extractor

Options:
  -h, --help            
  
      show this help message and exit
  
  -f, --file  
  
      Burp File (Right Click on the domain in the Target Scope and select save selected items and select Base64 encode)

  -dr, --directory  
  
      Directroy containing all Burp Suite output files (Right Click on the domain in the Target Scope and select save selected items and select Base64 encode)
      
  -a, --all  
  
      Use all methods (Generate API Endpoints for Bitrix Task, Collect APIs, URLs, Postman and Secrets)
      
  -b, --bitrix  
  
      Generate API Endpoints to xlsx file based on JSON/XML Content-Type via Burp Response (Recommended for Bitrix24 Task)
      
   -p, --postman  
  
      Collect --bitrix result to JSON file with body and parameters for Postman Application    
  
   -w, --wordlist  
  
      Create a tailored wordlist for your target (Based on Request/Responses including Headers/Cookies and body
   
   -J, --js 
  
      Collect JS/MAP URLs based on Burp response via REGEX to Excel file
      
  -i, --api  
  
      Collect APIs and PATHs based on Burp response via REGEX
      
   -j, --json  
  
      Collect JSON Files based on Burp request PATH via REGEX     
      
  -s, --secrets  
  
      Collect Secrets (AWS/Google keys, etc') based on Burp response via REGEX (Can be a bit slow...)
      
  -u, --urls  
  
      Collect URLs based on Burp response via REGEX
      
  -t, --threads  
  
     Number of threads run in parallel (Use this if you want to speed up the process) 
      
  -v, --verbose  
  
      If set, output will be printed to the screen with colors       
