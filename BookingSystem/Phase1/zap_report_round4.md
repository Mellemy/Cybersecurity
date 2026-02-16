# ZAP by Checkmarx Scanning Report

ZAP by [Checkmarx](https://checkmarx.com/).


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 0 |
| Low | 3 |
| Informational | 5 |




## Insights

| Level | Reason | Site | Description | Statistic |
| --- | --- | --- | --- | --- |
| Low | Warning |  | ZAP warnings logged - see the zap.log file for details | 2    |
| Info | Informational | http://10.0.2.15:8004 | Percentage of responses with status code 2xx | 68 % |
| Info | Informational | http://10.0.2.15:8004 | Percentage of responses with status code 3xx | 24 % |
| Info | Exceeded Low | http://10.0.2.15:8004 | Percentage of responses with status code 4xx | 7 % |
| Info | Informational | http://10.0.2.15:8004 | Percentage of endpoints with content type application/javascript | 21 % |
| Info | Informational | http://10.0.2.15:8004 | Percentage of endpoints with content type image/png | 5 % |
| Info | Informational | http://10.0.2.15:8004 | Percentage of endpoints with content type text/css | 5 % |
| Info | Informational | http://10.0.2.15:8004 | Percentage of endpoints with content type text/html | 31 % |
| Info | Informational | http://10.0.2.15:8004 | Percentage of endpoints with content type text/plain | 15 % |
| Info | Informational | http://10.0.2.15:8004 | Percentage of endpoints with method GET | 84 % |
| Info | Informational | http://10.0.2.15:8004 | Percentage of endpoints with method POST | 15 % |
| Info | Informational | http://10.0.2.15:8004 | Count of total endpoints | 19    |
| Info | Informational | http://10.0.2.15:8004 | Percentage of slow responses | 1 % |
| Info | Informational | https://firefox-settings-attachments.cdn.mozilla.net | Percentage of responses with status code 2xx | 100 % |
| Info | Informational | https://firefox-settings-attachments.cdn.mozilla.net | Percentage of endpoints with content type text/plain | 100 % |
| Info | Informational | https://firefox-settings-attachments.cdn.mozilla.net | Percentage of endpoints with method GET | 100 % |
| Info | Informational | https://firefox-settings-attachments.cdn.mozilla.net | Count of total endpoints | 2    |
| Info | Informational | https://firefox-settings-attachments.cdn.mozilla.net | Percentage of slow responses | 50 % |




## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- |
| Strict-Transport-Security Header Not Set | Low | 2 |
| Timestamp Disclosure - Unix | Low | 2 |
| X-Content-Type-Options Header Missing | Low | 2 |
| Authentication Request Identified | Informational | 1 |
| Re-examine Cache-control Directives | Informational | 2 |
| Retrieved from Cache | Informational | 2 |
| Session Management Response Identified | Informational | 4 |
| User Agent Fuzzer | Informational | Systemic |




## Alert Detail



### [ Strict-Transport-Security Header Not Set ](https://www.zaproxy.org/docs/alerts/10035/)



##### Low (High)

### Description

HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.

* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/0f5d4b73-9f15-46e3-ac70-a15a25acc19c
  * Node Name: `https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/0f5d4b73-9f15-46e3-ac70-a15a25acc19c`
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/42520b78-dc12-495f-89bd-ce830a2c26c2
  * Node Name: `https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/42520b78-dc12-495f-89bd-ce830a2c26c2`
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``


Instances: 2

### Solution

Ensure that your web server, application server, load balancer, etc. is configured to enforce Strict-Transport-Security.

### Reference


* [ https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html ](https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html)
* [ https://owasp.org/www-community/Security_Headers ](https://owasp.org/www-community/Security_Headers)
* [ https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security ](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
* [ https://caniuse.com/stricttransportsecurity ](https://caniuse.com/stricttransportsecurity)
* [ https://datatracker.ietf.org/doc/html/rfc6797 ](https://datatracker.ietf.org/doc/html/rfc6797)


#### CWE Id: [ 319 ](https://cwe.mitre.org/data/definitions/319.html)


#### WASC Id: 15

#### Source ID: 3

### [ Timestamp Disclosure - Unix ](https://www.zaproxy.org/docs/alerts/10096/)



##### Low (Low)

### Description

A timestamp was disclosed by the application/web server. - Unix

* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/0f5d4b73-9f15-46e3-ac70-a15a25acc19c
  * Node Name: `https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/0f5d4b73-9f15-46e3-ac70-a15a25acc19c`
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `1769821803`
  * Other Info: `1769821803, which evaluates to: 2026-01-30 20:10:03.`
* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/42520b78-dc12-495f-89bd-ce830a2c26c2
  * Node Name: `https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/42520b78-dc12-495f-89bd-ce830a2c26c2`
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `1748394604`
  * Other Info: `1748394604, which evaluates to: 2025-05-27 21:10:04.`


Instances: 2

### Solution

Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.

### Reference


* [ https://cwe.mitre.org/data/definitions/200.html ](https://cwe.mitre.org/data/definitions/200.html)


#### CWE Id: [ 497 ](https://cwe.mitre.org/data/definitions/497.html)


#### WASC Id: 13

#### Source ID: 3

### [ X-Content-Type-Options Header Missing ](https://www.zaproxy.org/docs/alerts/10021/)



##### Low (Medium)

### Description

The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.

* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/0f5d4b73-9f15-46e3-ac70-a15a25acc19c
  * Node Name: `https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/0f5d4b73-9f15-46e3-ac70-a15a25acc19c`
  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/42520b78-dc12-495f-89bd-ce830a2c26c2
  * Node Name: `https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/42520b78-dc12-495f-89bd-ce830a2c26c2`
  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`


Instances: 2

### Solution

Ensure that the application/web server sets the Content-Type header appropriately, and that it sets the X-Content-Type-Options header to 'nosniff' for all web pages.
If possible, ensure that the end user uses a standards-compliant and modern web browser that does not perform MIME-sniffing at all, or that can be directed by the web application/web server to not perform MIME-sniffing.

### Reference


* [ https://learn.microsoft.com/en-us/previous-versions/windows/internet-explorer/ie-developer/compatibility/gg622941(v=vs.85) ](https://learn.microsoft.com/en-us/previous-versions/windows/internet-explorer/ie-developer/compatibility/gg622941(v=vs.85))
* [ https://owasp.org/www-community/Security_Headers ](https://owasp.org/www-community/Security_Headers)


#### CWE Id: [ 693 ](https://cwe.mitre.org/data/definitions/693.html)


#### WASC Id: 15

#### Source ID: 3

### [ Authentication Request Identified ](https://www.zaproxy.org/docs/alerts/10111/)



##### Informational (High)

### Description

The given request has been identified as an authentication request. The 'Other Info' field contains a set of key=value lines which identify any relevant fields. If the request is in a context which has an Authentication Method set to "Auto-Detect" then this rule will change the authentication to match the request identified.

* URL: http://10.0.2.15:8004/login
  * Node Name: `http://10.0.2.15:8004/login ()(csrf_token,password,username)`
  * Method: `POST`
  * Parameter: `username`
  * Attack: ``
  * Evidence: `password`
  * Other Info: `userParam=username
userValue=foo-bar@example.com
passwordParam=password
referer=http://10.0.2.15:8004/login
csrfToken=csrf_token`


Instances: 1

### Solution

This is an informational alert rather than a vulnerability and so there is nothing to fix.

### Reference


* [ https://www.zaproxy.org/docs/desktop/addons/authentication-helper/auth-req-id/ ](https://www.zaproxy.org/docs/desktop/addons/authentication-helper/auth-req-id/)



#### Source ID: 3

### [ Re-examine Cache-control Directives ](https://www.zaproxy.org/docs/alerts/10015/)



##### Informational (Low)

### Description

The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content. For static assets like css, js, or image files this might be intended, however, the resources should be reviewed to ensure that no sensitive content will be cached.

* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/0f5d4b73-9f15-46e3-ac70-a15a25acc19c
  * Node Name: `https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/0f5d4b73-9f15-46e3-ac70-a15a25acc19c`
  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `public, max-age=3600`
  * Other Info: ``
* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/42520b78-dc12-495f-89bd-ce830a2c26c2
  * Node Name: `https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/42520b78-dc12-495f-89bd-ce830a2c26c2`
  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `public, max-age=3600`
  * Other Info: ``


Instances: 2

### Solution

For secure content, ensure the cache-control HTTP header is set with "no-cache, no-store, must-revalidate". If an asset should be cached consider setting the directives "public, max-age, immutable".

### Reference


* [ https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching ](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching)
* [ https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/Cache-Control ](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/Cache-Control)
* [ https://grayduck.mn/2021/09/13/cache-control-recommendations/ ](https://grayduck.mn/2021/09/13/cache-control-recommendations/)


#### CWE Id: [ 525 ](https://cwe.mitre.org/data/definitions/525.html)


#### WASC Id: 13

#### Source ID: 3

### [ Retrieved from Cache ](https://www.zaproxy.org/docs/alerts/10050/)



##### Informational (Medium)

### Description

The content was retrieved from a shared cache. If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.

* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/0f5d4b73-9f15-46e3-ac70-a15a25acc19c
  * Node Name: `https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/0f5d4b73-9f15-46e3-ac70-a15a25acc19c`
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HIT`
  * Other Info: ``
* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/42520b78-dc12-495f-89bd-ce830a2c26c2
  * Node Name: `https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/42520b78-dc12-495f-89bd-ce830a2c26c2`
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HIT`
  * Other Info: ``


Instances: 2

### Solution

Validate that the response does not contain sensitive, personal or user-specific information. If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:
Cache-Control: no-cache, no-store, must-revalidate, private
Pragma: no-cache
Expires: 0
This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request.

### Reference


* [ https://datatracker.ietf.org/doc/html/rfc7234 ](https://datatracker.ietf.org/doc/html/rfc7234)
* [ https://datatracker.ietf.org/doc/html/rfc7231 ](https://datatracker.ietf.org/doc/html/rfc7231)
* [ https://www.rfc-editor.org/rfc/rfc9110.html ](https://www.rfc-editor.org/rfc/rfc9110.html)


#### CWE Id: [ 525 ](https://cwe.mitre.org/data/definitions/525.html)


#### Source ID: 3

### [ Session Management Response Identified ](https://www.zaproxy.org/docs/alerts/10112/)



##### Informational (Medium)

### Description

The given response has been identified as containing a session management token. The 'Other Info' field contains a set of header tokens that can be used in the Header Based Session Management Method. If the request is in a context which has a Session Management Method set to "Auto-Detect" then this rule will change the session management to use the tokens identified.

* URL: http://10.0.2.15:8004/login
  * Node Name: `http://10.0.2.15:8004/login`
  * Method: `GET`
  * Parameter: `csrf_token`
  * Attack: ``
  * Evidence: `csrf_token`
  * Other Info: `cookie:csrf_token`
* URL: http://10.0.2.15:8004/register
  * Node Name: `http://10.0.2.15:8004/register`
  * Method: `GET`
  * Parameter: `csrf_token`
  * Attack: ``
  * Evidence: `csrf_token`
  * Other Info: `cookie:csrf_token`
* URL: http://10.0.2.15:8004/login
  * Node Name: `http://10.0.2.15:8004/login`
  * Method: `GET`
  * Parameter: `csrf_token`
  * Attack: ``
  * Evidence: `csrf_token`
  * Other Info: `cookie:csrf_token`
* URL: http://10.0.2.15:8004/register
  * Node Name: `http://10.0.2.15:8004/register`
  * Method: `GET`
  * Parameter: `csrf_token`
  * Attack: ``
  * Evidence: `csrf_token`
  * Other Info: `cookie:csrf_token`


Instances: 4

### Solution

This is an informational alert rather than a vulnerability and so there is nothing to fix.

### Reference


* [ https://www.zaproxy.org/docs/desktop/addons/authentication-helper/session-mgmt-id/ ](https://www.zaproxy.org/docs/desktop/addons/authentication-helper/session-mgmt-id/)



#### Source ID: 3

### [ User Agent Fuzzer ](https://www.zaproxy.org/docs/alerts/10104/)



##### Informational (Medium)

### Description

Check for differences in response based on fuzzed User Agent (eg. mobile sites, access as a Search Engine Crawler). Compares the response statuscode and the hashcode of the response body with the original response.

* URL: http://10.0.2.15:8004/login
  * Node Name: `http://10.0.2.15:8004/login`
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/4.0 (compatible; MSIE 8.0; Windows NT 6.1)`
  * Evidence: ``
  * Other Info: ``
* URL: http://10.0.2.15:8004/register
  * Node Name: `http://10.0.2.15:8004/register`
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/4.0 (compatible; MSIE 8.0; Windows NT 6.1)`
  * Evidence: ``
  * Other Info: ``
* URL: http://10.0.2.15:8004/reservation
  * Node Name: `http://10.0.2.15:8004/reservation`
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/4.0 (compatible; MSIE 8.0; Windows NT 6.1)`
  * Evidence: ``
  * Other Info: ``
* URL: http://10.0.2.15:8004/login
  * Node Name: `http://10.0.2.15:8004/login ()(csrf_token,password,username)`
  * Method: `POST`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/4.0 (compatible; MSIE 8.0; Windows NT 6.1)`
  * Evidence: ``
  * Other Info: ``
* URL: http://10.0.2.15:8004/resources
  * Node Name: `http://10.0.2.15:8004/resources ()(csrf_token,resource_description,resource_id,resource_name)`
  * Method: `POST`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/4.0 (compatible; MSIE 8.0; Windows NT 6.1)`
  * Evidence: ``
  * Other Info: ``

Instances: Systemic


### Solution



### Reference


* [ https://owasp.org/wstg ](https://owasp.org/wstg)



#### Source ID: 1


