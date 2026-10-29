# Email AI Agent

An n8n workflow that reads incoming Gmail messages, classifies them with AI, applies a label, and prepares a personalized reply draft for human review.

## Flow

`Gmail Trigger → AI analysis → Classification → Label → Gmail draft`

## Design choice

The workflow does not blindly send AI-generated emails. It creates a draft so a person can review the response before it is sent.

## Setup

Import `workflow.json` into n8n and connect your own Gmail and OpenAI credentials. Configure the labels, prompt, sender rules, and draft behavior before activation.

This is a demo workflow and contains no credentials or client data.
