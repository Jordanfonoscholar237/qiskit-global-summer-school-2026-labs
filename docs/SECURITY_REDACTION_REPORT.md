# Security redaction report

The public-ready notebooks were processed automatically and reviewed for the following categories:

- IBM Quantum/API credential assignments
- IBM Cloud CRNs and instance identifiers
- Runtime job identifiers
- email addresses and telephone numbers
- local filesystem paths
- UUID-like identifiers in displayed text
- account/job-inspection outputs
- Python error tracebacks and execution counts

Sensitive values were replaced with placeholders such as `<YOUR_IBM_QUANTUM_TOKEN>`, `<YOUR_IBM_CLOUD_CRN>`, `<YOUR_JOB_ID>`, `<REDACTED_EMAIL>` and `<REDACTED_PHONE>`. Outputs from credential, account and job-management cells were removed. Plot and circuit images that did not contain detected sensitive text were retained.

## Automated processing totals

- **Emails:** 1
- **Phones:** 0
- **Crns:** 2
- **Job Ids:** 111
- **Uuids:** 7
- **Paths:** 124
- **Credential Literals:** 9
- **Error Outputs:** 17
- **Sensitive Outputs:** 39
- **Execution Counts:** 405

## Per-notebook processing

- **Lab0_Qiskit_Patterns.ipynb:** 69 cells; 1 source cells redacted; 2 outputs removed.
- **Lab1_Circuits_for_Real_Hardware.ipynb:** 90 cells; 1 source cells redacted; 3 outputs removed.
- **Lab2_Noise_Backends_Benchmarking.ipynb:** 128 cells; 2 source cells redacted; 1 outputs removed.
- **Lab3_Error_Mitigation.ipynb:** 245 cells; 6 source cells redacted; 15 outputs removed.
- **Lab4a_Quantum_Advantage.ipynb:** 22 cells; 0 source cells redacted; 0 outputs removed.
- **Lab4b_QAOA_Partition_Problem.ipynb:** 188 cells; 4 source cells redacted; 25 outputs removed.
- **Lab4c_Sample_Based_Quantum_Diagonalization.ipynb:** 119 cells; 3 source cells redacted; 10 outputs removed.

A final manual visual check is still recommended before making any repository public, especially after you add new outputs or rerun hardware cells.
