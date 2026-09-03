# 📘 n8n Learning Notes — Day 1

> **Topic:** Fundamentals — Interface, Workflows, Nodes & Triggers  
> **Goal:** Understand the basic structure of n8n and build and execute a simple workflow.

---

## 📑 Table of Contents

- [1. What is n8n?](#1--what-is-n8n)
- [2. What is a Workflow?](#2--what-is-a-workflow)
- [3. What is a Node?](#3--what-is-a-node)
- [4. What is a Trigger?](#4--what-is-a-trigger)
- [5. n8n Interface / Canvas](#5--n8n-interface--canvas)
- [6. Edit Fields Node](#6--edit-fields-node)
- [7. First Workflow — Practical](#7--first-workflow--practical)
- [8. How Execution Works](#8--how-execution-works)
- [9. Key Terminology](#9--key-terminology)
- [10. Day 1 Revision](#10--day-1-revision)
- [11. Day 1 Learning Outcome](#11--day-1-learning-outcome)
- [12. Official References](#12--official-references)

---

## 1. 🔹 What is n8n?

**n8n** is a workflow automation platform that connects applications, APIs, and services so tasks can be performed automatically.

### Example

```text
GitHub
   ↓
 n8n
   ↓
Process Data
   ↓
Teams Notification
```

### 💡 Key Idea

Instead of performing repetitive tasks manually, n8n can connect the required services and execute the process automatically.

---

## 2. 🔹 What is a Workflow?

A **workflow** is a collection of connected nodes that work together to automate a process.

### Example

```text
Trigger
   ↓
Get Data
   ↓
Process Data
   ↓
Send Notification
```

The complete flow above is called a **workflow**.

### 🧠 Remember

> **Workflow = Complete automation flow**

---

## 3. 🔹 What is a Node?

A **node** is an individual building block of an n8n workflow.

Nodes can:

- Start workflows
- Fetch data
- Send data
- Process data
- Transform data
- Apply conditions and logic
- Connect with external services

### Common Nodes

| Node | Purpose |
|---|---|
| **Manual Trigger** | Starts the workflow manually |
| **Edit Fields** | Creates or modifies data |
| **IF** | Checks a condition |
| **HTTP Request** | Calls an API |

### Example

```text
Manual Trigger
      ↓
Edit Fields
      ↓
IF
      ↓
HTTP Request
```

In this example, there are **4 nodes**.

### 🧠 Remember

> **Node = Individual task / building block**

---

## 4. 🔹 What is a Trigger?

A **trigger** starts a workflow. It determines **when the workflow should begin**.

### Common Trigger Types

- ▶️ **Manual Trigger**
- ⏰ **Schedule Trigger**
- 🌐 **Webhook Trigger**
- 🔔 **App/Event Trigger**

### Manual Trigger

The **Manual Trigger** allows you to start a workflow yourself.

It is especially useful during:

- Development
- Testing
- Debugging

### Example

```text
Click "Execute Workflow"
          ↓
    Manual Trigger
          ↓
     Next Node
```

### 🧠 Remember

> **Trigger = Workflow starter**

---

## 5. 🖥️ n8n Interface / Canvas

The **workflow canvas** is the main area where you build your workflow.

You can use the canvas to:

- Add nodes
- Connect nodes
- Configure nodes
- Arrange nodes
- Test workflows
- Inspect workflow execution

### Basic Workflow Structure

```text
WORKFLOW
   │
   ├── TRIGGER
   │
   ├── NODE
   │
   ├── NODE
   │
   └── NODE
```

### Example

```text
Manual Trigger
       ↓
Edit Fields
       ↓
IF
       ↓
HTTP Request
```

---

## 6. 🔹 Edit Fields Node

The **Edit Fields** node is used to create or modify workflow data.

### Example Fields

```text
name       = Noman
profession = DevOps Engineer
goal       = AIOps
```

### Expected Output

```json
{
  "name": "Noman",
  "profession": "DevOps Engineer",
  "goal": "AIOps"
}
```

### 💡 Why is this useful?

It allows you to prepare or modify data before sending it to another node.

For example:

```text
Input Data
    ↓
Edit Fields
    ↓
Modified Data
    ↓
Next Node
```

---

## 7. 🧪 First Workflow — Practical

### Goal

Create your first simple n8n workflow.

### Workflow

```text
Manual Trigger
      ↓
Edit Fields
```

### Step 1 — Add Manual Trigger

Create a new workflow and add:

**Manual Trigger**

This node will start the workflow when you manually execute it.

### Step 2 — Add Edit Fields

Connect:

```text
Manual Trigger → Edit Fields
```

### Step 3 — Add the Following Fields

```text
name       = Noman
profession = DevOps Engineer
goal       = AIOps
```

### Step 4 — Execute the Workflow

Click:

**Execute Workflow**

### Expected Result

```json
{
  "name": "Noman",
  "profession": "DevOps Engineer",
  "goal": "AIOps"
}
```

✅ If you can see this output, your first workflow is working correctly.

---

## 8. ⚙️ How Execution Works

### Manual Execution

The basic execution flow is:

```text
Click Execute Workflow
          ↓
    Manual Trigger
          ↓
      Edit Fields
          ↓
        Output
```

### Automatic Execution

Later, workflows can start automatically through triggers such as:

```text
Schedule
   ↓
Workflow
```

or:

```text
Webhook
   ↓
Workflow
```

or:

```text
Application Event
   ↓
Workflow
```

These trigger types will be covered in later lessons.

---

## 9. 📚 Key Terminology

| Term | Meaning |
|---|---|
| **n8n** | Workflow automation platform |
| **Workflow** | Complete automation flow |
| **Node** | Individual task / building block |
| **Trigger** | Mechanism that starts a workflow |
| **Canvas** | Main area for building workflows |
| **Execution** | A run of the workflow |
| **Input** | Data received by a node |
| **Output** | Data produced by a node |

---

## 10. 🧠 Day 1 Revision

Remember these six points:

```text
n8n       = Automation Platform
Workflow  = Complete Automation Flow
Node      = Individual Task
Trigger   = Workflow Starter
Canvas    = Workflow Building Area
Execution = Workflow Run
```

### ⭐ One-Minute Revision

> **n8n** is the automation platform.  
> A **workflow** is the complete automation process.  
> A **node** performs an individual task.  
> A **trigger** starts the workflow.  
> The **canvas** is where the workflow is built.  
> An **execution** is one run of the workflow.

---

## 11. 🎯 Day 1 Learning Outcome

By the end of Day 1, you should be able to:

- [x] Navigate the n8n interface and canvas
- [x] Create a new workflow
- [x] Add and connect nodes
- [x] Use a Manual Trigger
- [x] Use Edit Fields to create data
- [x] Execute a workflow
- [x] Inspect workflow output

---

## 12. 🔗 Official References

- [n8n — Build your first workflow](https://docs.n8n.io/get-started/build-your-first-workflow)
- [n8n — Create and run workflows](https://docs.n8n.io/build/understand-workflows/create-and-run-workflows)
- [n8n — Work with nodes](https://docs.n8n.io/build/understand-workflows/workflow-components/work-with-nodes)
- [n8n — Foundations / N8N101 Essentials](https://learn.n8n.io/)

---

## ✅ Day 1 Status

**Completed:** n8n Fundamentals

**Next:** Day 2 — Triggers & Schedule Trigger

---
