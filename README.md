# Next.js + Tambo + Prisma Database Template

A Next.js starter template featuring AI-powered database operations with Tambo's intelligent chat interface and Prisma's type-safe database client with SQLite.

## Prerequisites

- Node.js 18+
- Tambo API key

## Quick Setup

1. **Clone and install**
   ```bash
   git clone https://github.com/Joystonm/Next.js-Tambo-Appwrite-Database-Starter-Template.git
   cd Next.js-Tambo-Appwrite-Database-Starter-Template
   npm install
   ```

2. **Configure environment**
   ```bash
   cp .env.example .env.local
   ```
   Edit `.env.local` with your Tambo API key:
   - `NEXT_PUBLIC_TAMBO_API_KEY`: Your Tambo API key

3. **Setup database**
   ```bash
   npm run db:push
   ```

4. **Start the application**
   ```bash
   npm run dev
   ```

## What's Included

- **Next.js 14** - App Router with TypeScript
- **Tambo** - AI chat interface with tool integration
- **Prisma** - Type-safe database client
- **SQLite** - Local file-based database
- **Automated Setup** - CLI-based database setup
- **No Authentication** - Direct database access for development
- **Minimal UI** - Clean, responsive design
- **Two AI Tools** - Create and list notes via natural language

## Usage

Try these prompts:
- "Create a note called Ship Tambo template with content Ready to deploy"
- "Show all notes"
- "Add a note about meeting tomorrow with details Discuss project roadmap"

The AI will automatically create and retrieve notes from your SQLite database.

## Architecture

### Database Schema
- **Database**: SQLite (`prisma/dev.db`)
- **Table**: `Note`
- **Fields**: `id` (String), `note` (String), `content` (String), `createdAt` (DateTime)

### No Authentication
This template intentionally excludes:
- User login/signup
- Session management
- User-specific permissions

The running application requires no login and works directly with the database.

## Development Notes

- Database is stored locally in `prisma/dev.db`
- Schema changes should be made in `prisma/schema.prisma`
- Run `npm run db:push` after schema changes
- Prisma Client is automatically generated
