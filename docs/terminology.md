# TriTrap Terminology

This document defines the core terms used throughout the TriTrap architecture.

Establishing consistent terminology ensures that protocol specifications, architecture documentation, and implementation discussions remain precise.

---

## Client

The entity that submits an inference request to the TriTrap system.

A client may be an application, service, or user interacting with the Gate node.

---

## Gate Node

The authorization and routing component of the system.

The Gate node:

• validates client requests  
• generates execution permits  
• determines execution lane routing  
• enforces execution policy  

The Gate node does **not perform inference workloads**.

---

## Permit

A Permit is the authorization artifact that allows a workload to execute within the system.

Permits define:

• the workload being authorized  
• the permitted execution environment  
• the time validity of the authorization  
• the verification policy to be applied

Execution lanes must validate permits before performing any workload.

TriTrap follows a **deny-by-default execution model**, meaning that workloads cannot execute without a valid permit.

---

## Execution Lane

An isolated execution environment responsible for performing inference workloads.

Execution lanes:

• receive workloads from the Gate node  
• validate permits  
• execute the authorized workload  
• generate execution receipts  

Multiple lanes may execute the same workload to enable verification.

---

## Receipt

A Receipt is the artifact produced by an execution lane after completing a workload.

Receipts contain:

• permit reference  
• workload identity  
• execution output hash  
• execution metadata  
• lane signature  

Receipts are submitted to the verification layer.

---

## Verification Layer

The verification layer evaluates receipts produced by execution lanes.

Responsibilities include:

• validating receipt authenticity  
• comparing execution outputs  
• determining the accepted result  

Verification policies may include deterministic comparison or consensus evaluation.

---

## Arbitration

Arbitration is the process used to resolve multiple execution results.

When multiple receipts exist, the arbitration logic determines which output is accepted as the final result.

---

## Workload

The computational task submitted by a client.

In the context of TriTrap, workloads are typically inference requests executed within machine learning models.

Each workload is represented by a **workload hash** used for validation and tracking.

---

## Workload Hash

A cryptographic hash representing the workload being executed.

The workload hash ensures that:

• the authorized workload matches the executed workload  
• execution results correspond to the correct request  

---

## Output Hash

A cryptographic hash representing the output produced by execution.

The output hash enables comparison between results produced by different execution lanes.

---

## Deterministic Verification

A verification approach where outputs are validated using deterministic comparison or defined verification policies.

This ensures that execution outcomes can be evaluated reliably across independent execution lanes.

---

## Multi-Lane Execution

A system design where the same workload may be executed across multiple independent execution lanes.

Multi-lane execution enables verification and detection of execution inconsistencies.

---

## Authorization Boundary

The architectural separation between authorization and execution.

In TriTrap:

• the Gate node performs authorization  
• execution lanes perform computation  

This separation ensures controlled workload execution.
