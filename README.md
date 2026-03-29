# SQL Server to PostgreSQL — Content Repository

This repository contains the content for the **SQL Server to PostgreSQL DBA Guide**, an interactive learning platform that helps experienced SQL Server DBAs transition to PostgreSQL through side-by-side comparisons.

If you know a concept, command, or workflow in SQL Server and want to help others learn the PostgreSQL equivalent — this is the right place to contribute.

---

## What is a "topic"?

Content is organized into **topics** (e.g. *Backup & Recovery*, *User Management*, *Index Maintenance*). Each topic contains one or more **concepts**, where each concept shows the SQL Server approach alongside the PostgreSQL equivalent, with a brief explanation of the key difference.

---

## How to contribute

### Option 1 — Use the Builder Tool (easiest)

The live site includes an interactive **JSON Builder** tool that guides you through creating content without writing any JSON by hand:

1. Go to the site and open the **JSON Builder** tool
2. Fill in the form — topic name, description, and as many concepts as you like
3. For each concept, paste in your SQL Server code and PostgreSQL equivalent, add short descriptions, and optionally note a key difference
4. The tool generates a ready-to-submit JSON file for you — just download or copy it

Once you have your JSON file, follow the submission steps below.

### Option 2 — Write the JSON manually

If you're comfortable with JSON, you can write your topic file directly. Each file lives in the `content/topics/` folder and follows this structure:

```json
{
  "id": "your-topic-id",
  "title": "Your Topic Title",
  "description": "A short description of what this topic covers.",
  "author": "your-github-username",
  "concepts": [
    {
      "title": "Concept Name",
      "sqlDescription": "How this works in SQL Server.",
      "sqlCode": "-- T-SQL example\nSELECT ...",
      "pgDescription": "How this works in PostgreSQL.",
      "pgCode": "-- PostgreSQL example\nSELECT ...",
      "keyDifference": "Optional: one sentence on the most important difference."
    }
  ]
}
```

You can use `content/schema.json` to validate your file if your editor supports JSON Schema.

---

## Submitting your contribution

1. **Fork** this repository
2. Add your topic JSON file to `content/topics/`
3. Open a **Pull Request** with a short description of what you've added or changed

That's it. Someone will review it, give feedback if needed, and merge it in.

---

## Attribution

If you'd like credit for your contribution, include your GitHub username in the `author` field of your topic file (as shown in the example above). It's optional — leave it out if you'd prefer to contribute anonymously.

---

## Partial contributions are welcome

You don't need to know both sides to contribute. If you're a SQL Server expert but haven't used PostgreSQL (or vice versa), you can submit a topic with only one side filled in — leave the other side's code and description blank or add a placeholder comment.

Partial submissions should be flagged by adding the **"Help Wanted"** label to your Pull Request. This signals to other contributors that the missing side needs to be filled in before the topic can go live.

---

## Content guidelines

- **Accuracy first** — test your code examples before submitting. Both the SQL Server and PostgreSQL examples should actually work.
- **Practical focus** — real-world DBA scenarios are more valuable than textbook examples.
- **Assume SQL Server knowledge** — you don't need to explain SQL Server, just explain what's different in PostgreSQL.
- **Keep descriptions concise** — a sentence or two per description is usually enough.

---

## Questions or ideas?

Open an issue if you have a topic suggestion, spot an error, or want to discuss something before writing a full contribution. All feedback is welcome.
