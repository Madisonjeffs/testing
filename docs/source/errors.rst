Error Handling
==============

Error Codes
-----------
The Steamworks Web API will return error codes whenever possible. Below is a comprehensive collection of possible codes and their meaning.

.. list-table:: Common HTTP Status Codes
   :widths: 10 30 60
   :header-rows: 1

   * - Code
     - Text
     - Description
   * - 200
     - OK
     - Success!
   * - 400
     - Bad Request
     - Please verify that all required parameters are being sent.
   * - 401
     - Unauthorized
     - Access is denied. Retrying will not help. Please verify your key= parameter.
   * - 403
     - Forbidden
     - Access is denied. Retrying will not help. Please verify your key= parameter.
   * - 404
     - Not Found
     - The API requested does not exist.
   * - 405
     - Method Not Allowed
     - This API has been called with the wrong HTTP method, such as GET or PUSH.
   * - 429
     - Too Many Requests
     - You are being rate limited.
   * - 500
     - Internal Server Error
     - An unrecoverable error has occurred, please try again. If this continues to persist then please post to the Steamworks developer discussion with additional details of your request.
   * - 503
     - Service Unavailable
     - Server is temporarily unavailable, or too busy to respond. Please wait and try again later.