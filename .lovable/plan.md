# Static reviews, service-area pages, and Surrey service headings

## Scope
- Replace the live Google Reviews integration with static testimonial content transcribed from the supplied reference images.
- Keep the existing reviews page and homepage review sections, but have both read directly from the static review list with no API keys, server request, loading state, or Google review configuration.
- Add Vancouver to the shared service-area data with its own neighbourhoods and localized copy.
- Ensure every listed service area is a real link to its individual area page, including the service-area links shown on the homepage.
- Update every individual service page’s main heading to end with “in Surrey BC”.

## Content changes
- Add these four supplied reviews: Sukhvir Sodhi, Pedraum Moghari, Saba Mahmood, and Arminder Singh.
- Preserve the wording, star rating, and relative dates visible in the references, with light punctuation cleanup only where needed for readability.
- Update service-area summaries and structured area coverage to include Vancouver where area lists are shown.

## Technical details
- Remove the Google Reviews server/query module and all imports, loaders, and query hooks that depend on it.
- Continue using the existing dynamic `/service-areas/$slug` route; each area card/link supplies its own slug, so every city resolves to a dedicated page with unique metadata and content.
- Convert homepage area names from plain text to typed route links.
- Verify the homepage, reviews page, service-area index, Vancouver page, and a representative service page in desktop and mobile layouts.
