Clerk already installed and connected. wire it into Next.js app: provider, auth pages, redirects, route protection and user menu.

## Design

Use Clerk;s `dark` theme from `@clerk/ui/themes` as teh base.

Override Clerk appearance variables using the app's existing CSS variables. Do no hardcode colors.

### Sign-in and sign up pages:

- large screens: simple two panel layout
- left : compact logo, tagline, short text-only feature list.
- right: centered Clerk form
- small screens: form only
- no gradients
- no oversized hero sections
- no feature cards
- no scroll-heavy layouts.

keep layout minimal and professional.


## Implementation

Wrap root layout with `ClerkProvidor` using Clerks `dark` theme

Create sigh-in sign-up pages using Clerk components.

Use `proxy.ts` at the project root not `middleware.ts`

define public routes using teh existing sign-in and sign-up env vars. Protect everything else by default.

update `/`:

- authenticated users redirect to `/editor`
- unauthenticated users redirect to `sign/in`

Add Clerk's built-in `UserButton` to the editor navbar right section for profile settings and logout.

Keep Clerk's default menu and profile flows intact. Do not rebuild or heavily customize Clerk internals.

Use existing Clerk env vars. Do no rename or invent new ones.

## Dependencies

install: @clerk/ui

## Check when done 
- `proxy.ts` exists at root
- all routes are protected except public auth paths
- auth pages use CSS variables with no hardcoded colors
- `ClerkProvider` wraps the root layout
- `npm run build` passes