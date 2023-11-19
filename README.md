# Domain Checker

This simple Go application checks the DNS records of a given domain, including MX (Mail Exchange), SPF (Sender Policy Framework), and DMARC (Domain-based Message Authentication, Reporting, and Conformance) records.

## Usage

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/domain-checker.git
    ```

2. Navigate to the project directory:

    ```bash
    cd domain-checker
    ```

3. Run the application:

    ```bash
    go run main.go
    ```

4. Enter domain names one by one when prompted.

    ```plaintext
    Enter a domain name (or type 'exit' to end): example.com
    ```

    The program will output information about the domain's MX, SPF, and DMARC records.

5. To exit the program, type 'exit' when prompted.

## Output Format

The output format of the program is as follows:

```plaintext
domain, hasMX, hasSPF, spfRecord, hasDMARC, dmarcRecord
example.com, true, true, v=spf1 ... , true, v=DMARC1 ...
```

    - domain: The domain name being checked.
    - hasMX: Whether the domain has Mail Exchange records.
    - hasSPF: Whether the domain has Sender Policy Framework records.
    - spfRecord: The SPF record of the domain (if present).
    - hasDMARC: Whether the domain has DMARC records.
    - dmarcRecord: The DMARC record of the domain (if present).