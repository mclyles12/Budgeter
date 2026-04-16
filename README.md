# Budgeter

A comprehensive personal budget tracking web app with AI-powered chat assistant, featuring advanced financial management tools.

## Features

### AI Chat Assistant
- Natural language interface for logging expenses, income, and savings
- Intelligent financial advice based on your complete financial situation
- Dynamic responses based on your chosen budget strategy

### Financial Tracking
- **Transaction Ledger**: View and manage all financial transactions by month
- **Bills Overview**: Track fixed monthly bills, outstanding debts, and income sources
- **Savings Goal Tracking**: Customizable progress bar toward your savings goal
- **Recurring Items Management**: Add, edit, and remove recurring expenses/income

### Financial Goals & Strategy
- **Custom Savings Goals**: Set your own savings target and timeline
- **Budget Strategy Selection**: Choose between "stick to budget" or "focus on savings goal"
- **Dynamic AI Responses**: AI adapts its advice based on your selected strategy

### Image Upload
- Upload receipt photos or expense images
- Visual expense tracking (image display in chat)

### Speech-to-Text
- Voice input for hands-free expense logging
- Browser-based speech recognition (Chrome/Edge recommended)

###  Local Storage
- All data stored locally in your browser
- No account required, works offline

## Setup & Deployment

### Local Development
1. Serve the repository from a local web server instead of opening the file directly.
   - Example: `cd Budgeter && python3 -m http.server 8000`
   - Then open `http://localhost:8000/budget-ai.html`
2. If you want the AI chat endpoint to work locally, run Vercel Dev in the repo root:
   - `vercel dev`
   - This will serve both `budget-ai.html` and `api/chat.js` on `http://localhost:3000`
3. **First-time setup**: The AI will guide you through an interactive setup process
4. Start chatting with your personalized AI budget assistant!

### Vercel Deployment (Recommended)
1. **Fork/Clone this repository** to your GitHub account
2. **Connect to Vercel**:
   - Go to [vercel.com](https://vercel.com) and sign up/login
   - Click "New Project" and import your GitHub repository
3. **Set Environment Variable**:
   - In your Vercel project settings, go to "Environment Variables"
   - Add: `ANTHROPIC_API_KEY` with your Anthropic API key value
   - Make sure it's set for "Production", "Preview", and "Development"
4. **Deploy**:
   - Vercel will automatically detect the configuration and deploy
   - Your app will be available at `your-project.vercel.app`

### Manual API Key Setup (Not Recommended for Production)
If running locally without Vercel, you'll need to add your Anthropic API key directly to the serverless function. However, this exposes your key in the codebase - use Vercel environment variables instead.

## Security

- **API Key Protection**: Anthropic API key is stored securely in Vercel environment variables, never exposed in client-side code
- **Serverless Functions**: All AI API calls are proxied through Vercel's serverless functions
- **No Client-Side Secrets**: Sensitive credentials are never sent to the browser
- **HTTPS Only**: Vercel automatically provides SSL certificates for secure connections

## Usage

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

## Technical Details

- **AI Model**: Claude 3.5 Sonnet via Anthropic API
- **Storage**: Browser localStorage (no server required)
- **Speech Recognition**: Web Speech API (modern browsers only)
- **Image Handling**: Client-side base64 encoding
- **Responsive Design**: Works on desktop and mobile

## Privacy & Security

- All data stored locally in your browser
- No data sent to external servers (except Anthropic API for chat)
- API key stored in browser (consider security implications for production use)

## Budget Strategies

### Stick to Monthly Budget
- Focuses on maintaining spending within income limits
- Provides warnings about overspending
- Tracks budget compliance

### Focus on Savings Goal
- Prioritizes reaching your savings target
- Calculates required monthly savings
- Warns about expenses that impact your goal

## Recurring Items

Manage all your regular financial commitments:
- **Expenses**: Rent, utilities, subscriptions, loan payments
- **Income**: Salary, side gigs, passive income
- **Frequency**: Monthly, weekly, bi-weekly, yearly
- **Categories**: Organize by type (Entertainment, Utilities, etc.)

The AI assistant knows about all your recurring items and factors them into advice.
