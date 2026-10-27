# Foreum

**Open-source forum software for building and running online communities.**

Foreum is a modern, self-hostable discussion platform for communities, product support, and knowledge sharing. It combines rich discussions, user management, moderation tools, and community administration in one application.

[Website](https://foreum.vercel.app) · [Issues](https://github.com/Foreum/foreum/issues) · [Contributing](https://github.com/Foreum/foreum/blob/main/CONTRIBUTING.md)

> Foreum is actively evolving. Some features and setup instructions may change as development progresses.

## Why Foreum?

Running a community involves more than publishing discussion threads. Foreum brings the tools needed to manage conversations, members, and community settings together in one platform.

- **Rich discussions**: Categories, tags, reactions, voting, bookmarks, and a rich-text editor.
- **Community management**: User profiles, roles, permissions, reputation, and groups.
- **Moderation**: Content reports, moderation tools, audit logs, and configurable trust levels.
- **Administration**: Analytics, announcements, custom pages, and appearance settings.
- **Authentication**: Email/password authentication and supported OAuth providers.
- **Customizable experience**: Responsive layouts and configurable light and dark themes.
- **Self-hosting**: Run your own community and control your deployment.

## Features

### Discussions and content

- Thread creation, editing, and management
- Categories, nested subcategories, and tags
- Rich-text editing with Plate.js
- Reactions, upvotes, and downvotes
- Bookmarks and thread subscriptions
- Thread drafts, pinning, and locking
- Full-text search

### Members and community

- User profiles and activity tracking
- Role-based access for users, moderators, and administrators
- Reputation and badges
- Configurable trust levels
- Groups, group forums, and events
- Event RSVPs
- Direct messaging
- In-app notifications

### Moderation and administration

- Content reporting and moderation audit logs
- Moderation tools and configurable content filtering
- Administrative dashboard and analytics
- Global settings and maintenance mode
- Community announcements and custom pages
- Theme customization, including colors, fonts, and presets

## Technology stack

Foreum is built with a modern, type-safe full-stack JavaScript and TypeScript ecosystem.

| Technology | Purpose |
| --- | --- |
| React | User interface |
| TanStack Start | Full-stack application framework |
| TanStack Router | Routing |
| tRPC | Type-safe APIs |
| Drizzle ORM | Database access |
| PostgreSQL | Database |
| Better Auth | Authentication |
| Plate.js | Rich-text editing |
| Tailwind CSS | Styling |
| shadcn/ui | UI components |
| pnpm | Package management |

## Getting started

Foreum is under active development. Before running it locally, make sure you have the required tools installed.

### Prerequisites

- Node.js
- pnpm
- PostgreSQL

Use a Node.js version compatible with the project's dependencies.

### 1. Clone the repository

```bash
git clone https://github.com/Foreum/foreum.git
cd foreum
```

### 2. Install dependencies

```bash
pnpm install
```

### 3. Configure environment variables

Copy the example environment file:

```bash
cp .env.example .env
```

On Windows, copy `.env.example` to `.env` using your preferred terminal or file manager.

At minimum, configure your PostgreSQL connection and authentication secret:

```env
DATABASE_URL="postgresql://user:password@localhost:5432/foreum"
BETTER_AUTH_SECRET="your-random-secret"
BASE_URL="http://localhost:3000"
```

See `.env.example` for the additional email and OAuth configuration options.

### 4. Prepare the database

Review the Drizzle configuration and database scripts before applying the schema:

```bash
pnpm db:push
```

Use this command against a development database. Avoid forcing schema changes against a database containing important data.

### 5. Start the development server

```bash
pnpm dev
```

Open the local URL printed by the development server.

## Available commands

| Command | Description |
| --- | --- |
| `pnpm dev` | Start the development server |
| `pnpm build` | Build the application and check TypeScript |
| `pnpm start` | Start the production server |
| `pnpm preview` | Preview the production build |
| `pnpm db:push` | Push the Drizzle schema to the database |
| `pnpm db:generate` | Generate database migrations |
| `pnpm db:migrate` | Apply database migrations |
| `pnpm db:studio` | Open Drizzle Studio |
| `pnpm test` | Run the test suite |
| `pnpm test:e2e` | Run end-to-end tests |

## Deployment

Foreum uses TanStack Start and Nitro. The repository includes deployment configuration that should be checked against your target environment before production use.

For production deployments, configure your database, authentication secret, public application URL, email delivery, OAuth credentials if needed, and file-upload provider.

Deployment instructions for specific platforms should be documented separately once each deployment path has been verified.

## Contributing

Contributions are welcome, including bug reports, feature proposals, documentation improvements, and code contributions.

1. Check the existing issues before starting substantial work.
2. Fork the repository and create a branch for your changes.
3. Keep changes focused and follow the conventions already used in the codebase.
4. Test your changes where possible.
5. Open a pull request explaining what changed and why.

Please read the [contribution guidelines](https://github.com/Foreum/foreum/blob/main/CONTRIBUTING.md) and follow the project's [Code of Conduct](https://github.com/Foreum/foreum/blob/main/CODE_OF_CONDUCT.md).

- [Report a bug](https://github.com/Foreum/foreum/issues)
- [Request a feature](https://github.com/Foreum/foreum/issues)

## Security

If you discover a security vulnerability, please follow the project's [security policy](https://github.com/Foreum/foreum/blob/main/SECURITY.md) rather than publicly disclosing sensitive details.

## Roadmap

Foreum is continuing to evolve. Planned improvements include email digests, real-time updates, and an extensibility system for plugins and themes.

Check the [issue tracker](https://github.com/Foreum/foreum/issues) for current discussions and development priorities.

## License

See the repository's license file for licensing terms.

## Support Foreum

If Foreum is useful to you:

- Star the repository.
- Report bugs and suggest improvements.
- Contribute code or documentation.
- Share the project with other developers and community builders.

**Build better communities with Foreum.**
