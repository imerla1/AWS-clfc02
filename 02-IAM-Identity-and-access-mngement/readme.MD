# IAM - Identity and Access Management


## MFA Multi Factor Authentiaction


Multi-Factor Authentication (MFA) is a security feature in AWS that adds an extra layer of protection to user accounts. AWS supports various MFA device options for users to enable MFA on their accounts. 

1) **Virtual MFA Devices**
   - These are software-based MFA devices that run on a smartphone or tablet.
   - Common apps include Google Authenticator and Authy.
   - Users scan a QR code to set up the virtual MFA on their device.
2) **Hardware MFA Devices:**
    - Physical hardware tokens that generate MFA codes.
    - Users receive a physical device that they can use to generate MFA codes.
    - Examples include devices from Yubico and Gemalto.

3) **SMS Text Messages:**
    - Users receive MFA codes via SMS on their registered mobile phone.
    - This option is less secure than using a dedicated MFA device.

4) **U2F Security Keys:**

    - Universal Second Factor (U2F) security keys provide hardware-based authentication.
    - Users insert the key into their computer's USB port or use a Bluetooth connection.

## AWS access ways

1) **AWS Management Console:**

    - **Web-Based Interface:** The AWS Management Console is a web-based user interface that allows users to interact with AWS services using a web browser. It provides a visual way to manage and configure AWS resources.

2) **AWS Command Line Interface (CLI):**

    - **Command-Line Access:** The AWS CLI is a command-line tool that allows users to interact with AWS services using text-based commands. It   provides a powerful and scriptable interface for managing AWS resources.

3) AWS SDKs (Software Development Kits):

    - **Programmatic Access:** AWS provides SDKs for various programming languages, including Java, Python, Ruby, and more. Developers can use these SDKs to integrate AWS services into their applications.