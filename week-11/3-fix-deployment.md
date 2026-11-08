# Today, I fixed the Invalid JSON error occurred in the deployed react app in github pages.

## I debugged the app and I found:
1. The API requesting by the App is undefined.
2. Due to excluding of ENV variable for API URL in project repo, the app is choosing Base URL.

## Made changes in Github workflow YML file to use the ENV variable.

## After changes again the request failed due to CORS error. So, I added the Origin of React app in the server CORS middleware.

## Now, it is working.

## Here is the PROOF OF BUILD:
<a href="https://harsha91544.github.io/product-management-app/">Click to open the working product management app</a>