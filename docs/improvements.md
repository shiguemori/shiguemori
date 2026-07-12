# Improvement Backlog

This backlog captures recommended improvements for the profile repository. It is intentionally small and practical so the profile stays easy to maintain.

## Implemented In This Pass

- Rewrote the profile README for clearer positioning and faster scanning.
- Fixed broken character rendering by replacing corrupted emoji sequences with plain ASCII content.
- Added documentation for maintaining the profile.
- Added a GitHub Actions workflow for Markdown and link quality checks.
- Added local configuration files for Markdown linting and link checking.
- Added a repository analysis page to clarify this is a GitHub profile repository.

## Recommended Next Improvements

| Priority | Improvement | Why it matters |
| --- | --- | --- |
| High | Add a small "Selected Projects" section | Gives visitors proof of work beyond a technology list. |
| High | Pin or link 3 to 5 repositories that match the profile narrative | Reinforces the distributed systems and backend architecture positioning. |
| Medium | Add short case-study bullets for performance, reliability, or cloud cost wins | Converts seniority claims into concrete evidence. |
| Medium | Review all external badges quarterly | Badge services and dynamic cards can break or become slow. |
| Medium | Add a Portuguese version link if the target audience includes Brazil-first hiring | Keeps the profile accessible without making the main README too long. |
| Low | Add a lightweight contribution guide | Useful only if this repository receives external suggestions. |

## Suggested README Sections To Add Later

When there are strong public examples available, consider adding:

- `Selected Projects`: concise links with one-line context.
- `Architecture Notes`: public posts, talks, diagrams, or write-ups.
- `Open Source`: meaningful contributions or libraries maintained.
- `Speaking and Mentoring`: talks, articles, mentoring initiatives, or community work.

## Quality Criteria

A future change should be considered good when it:

- Makes the profile easier to understand in less time.
- Adds evidence instead of only adding more claims.
- Keeps the page visually balanced on desktop and mobile.
- Avoids fragile external dependencies unless they add clear value.
- Passes the Markdown and link checks in GitHub Actions.
