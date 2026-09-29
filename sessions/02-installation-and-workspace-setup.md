## The Agentic Loop

Claude Code works through an **agentic loop** — a continuous cycle of understanding the request, taking action, verifying the result, and iterating when necessary.

![Claude Code Agentic Loop](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT42LWCOApJVsDP3AOmRKJg7TFxT11QhuS7zrQBySGHlZVucCtUqhVQ42U&s=10)

### How the Loop Works

1. **Prompt**
   - You provide a task or goal to Claude Code.

2. **Gather Context**
   - Claude determines what information it needs and interacts with the model.
   - The model can return text or a tool call that Claude Code can execute.

3. **Take Action**
   - Claude performs actions based on the gathered context.
   - Examples include reading files, editing files, and running commands.

4. **Verify Results**
   - Claude checks whether the result satisfies the original request.
   - It can inspect changes, run commands, or use other available tools.

5. **Iterate or Finish**
   - If the result is complete and verifiable, Claude finishes.
   - If it is not complete, Claude continues the loop and takes additional actions until the task is complete and verifiable.

### Developer Control

Throughout the loop, you can:

- Provide additional context
- Interrupt Claude
- Correct its direction
- Add requirements
- Steer it toward the desired result

This allows you to remain involved while Claude handles execution and verification.