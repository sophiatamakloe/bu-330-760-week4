# Week 4: Math Agent with Tool Use

This repository contains my completed Week 4 GenAI homework assignment for building a math agent that uses tools to solve different types of questions. The final version of the agent can perform arithmetic calculations and retrieve product prices from a product catalog.

## Repository Files

- `README.md`
- `agent.py`
- `calculator.py`
- `products.json`
- `math_questions.md`
- `pyproject.toml`
- `.env.example`
- `.gitignore`

## Project Goal

The goal of this assignment was to improve a starter AI agent by adding tool use. Instead of relying only on the language model, the agent should call tools when needed to complete tasks more accurately and efficiently.

## What I Implemented

I completed the missing `product_lookup` tool inside `agent.py`.

This tool:

- Opens `products.json`
- Reads available product names and prices
- Returns the requested product price
- Supports product-related questions from the assignment

The final agent uses two tools:

- `calculator_tool` for arithmetic calculations
- `product_lookup` for product catalog lookups

## Iteration and Evaluation

### Initial Evaluation

When I first ran the starter project:

- Math questions worked correctly using the calculator tool
- Product-price questions failed because the agent had no access to catalog data
- Additional setup issues included API key errors, quota limits, and provider configuration problems

### Changes Made

To improve performance, I:

- Configured the environment variables correctly
- Updated the model provider settings
- Implemented the missing `product_lookup` tool
- Retested the full question set

### Final Evaluation

After these changes:

- The agent solved math questions successfully
- The agent retrieved product prices correctly
- The agent combined product lookups with arithmetic reasoning
- All required question types were handled successfully

This showed clear improvement from the original version.

## Development Process

### Stage 1: Environment Setup

I resolved API key, billing, and model selection issues so the agent could run consistently.

### Stage 2: Tool Completion

I added the missing lookup tool and verified it could read from `products.json`.

### Stage 3: Final Testing

I reran the full assignment and confirmed the tools were being used correctly.

## What I Learned

This assignment helped me understand that practical AI systems often rely on external tools rather than only model memory. Tool integration improves reliability, accuracy, and usefulness.

I also learned the importance of debugging environment configuration issues as part of real-world development workflows.

## Git Workflow

This repository includes multiple commits showing project setup, implementation progress, testing, and final submission updates.

## How to Run

1. Clone the repository  
2. Create a `.env` file from `.env.example`  
3. Add a valid provider API key  
4. Verify that the `MODEL` setting in `agent.py` matches your provider  
5. Run the program:

```bash
uv run agent.py
