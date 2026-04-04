# Budgeter

A comprehensive personal budget tracking web app with AI-powered chat assistant, featuring advanced financial management tools.

## ✨ Features

### 🤖 AI Chat Assistant
- Natural language interface for logging expenses, income, and savings
- Intelligent financial advice based on your complete financial situation
- Dynamic responses based on your chosen budget strategy

### 📊 Financial Tracking
- **Transaction Ledger**: View and manage all financial transactions by month
- **Bills Overview**: Track fixed monthly bills, outstanding debts, and income sources
- **Savings Goal Tracking**: Customizable progress bar toward your savings goal
- **Recurring Items Management**: Add, edit, and remove recurring expenses/income

### 🎯 Financial Goals & Strategy
- **Custom Savings Goals**: Set your own savings target and timeline
- **Budget Strategy Selection**: Choose between "stick to budget" or "focus on savings goal"
- **Dynamic AI Responses**: AI adapts its advice based on your selected strategy

### 📷 Image Upload
- Upload receipt photos or expense images
- Visual expense tracking (image display in chat)

### 🎤 Speech-to-Text
- Voice input for hands-free expense logging
- Browser-based speech recognition (Chrome/Edge recommended)

### 💾 Local Storage
- All data stored locally in your browser
- No account required, works offline

## 🚀 Setup

1. Open `budget-ai.html` in a modern web browser (Chrome/Edge recommended for speech features)
2. **First-time setup**: The AI will guide you through an interactive setup process asking about:
   - Your income sources and hours worked
   - Housing situation (rent/mortgage)
   - Transportation costs (car payments, insurance, gas)
   - Utilities and subscriptions
   - Outstanding debts and loans
   - Savings goals
   - Other financial context
3. Add your Anthropic API key to the JavaScript code (replace the placeholder)
4. Start chatting with your personalized AI budget assistant!

## 📱 Usage

### Initial Setup
When you first open the app, the AI will walk you through a comprehensive financial assessment, similar to a conversation with a financial advisor. Answer the questions honestly to get personalized advice.

### Daily Use
- **Chat naturally**: "Spent $50 at grocery store" or "Got paid $500 today"
- **Voice input**: Click the 🎤 button and speak your expenses
- **Image upload**: Click 📷 to upload receipt photos
- **Track progress**: Check the **Ledger** tab for monthly summaries
- **Manage recurring items**: Use the **Settings** tab to add/edit/remove recurring expenses
- **View financial overview**: Check the **Bills** tab for your personalized financial summary

### Voice Commands Examples
- "I spent forty dollars at Target"
- "Put one hundred dollars in savings"
- "How am I doing this month?"

## 🔧 Technical Details

- **AI Model**: Claude 3.5 Sonnet via Anthropic API
- **Storage**: Browser localStorage (no server required)
- **Speech Recognition**: Web Speech API (modern browsers only)
- **Image Handling**: Client-side base64 encoding
- **Responsive Design**: Works on desktop and mobile

## 🔒 Privacy & Security

- All data stored locally in your browser
- No data sent to external servers (except Anthropic API for chat)
- API key stored in browser (consider security implications for production use)

## 🎯 Budget Strategies

### Stick to Monthly Budget
- Focuses on maintaining spending within income limits
- Provides warnings about overspending
- Tracks budget compliance

### Focus on Savings Goal
- Prioritizes reaching your savings target
- Calculates required monthly savings
- Warns about expenses that impact your goal

## 📋 Recurring Items

Manage all your regular financial commitments:
- **Expenses**: Rent, utilities, subscriptions, loan payments
- **Income**: Salary, side gigs, passive income
- **Frequency**: Monthly, weekly, bi-weekly, yearly
- **Categories**: Organize by type (Entertainment, Utilities, etc.)

The AI assistant knows about all your recurring items and factors them into advice.
