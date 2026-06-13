# Openverse

Openverse is a search engine providing programmatic access to the world's largest openly-licensed media catalog, covering 800M+ images and audio tracks from cultural institutions, museums, and creative commons sources.

## API

**Base URL:** `https://api.openverse.org/v1`

**Documentation:** https://docs.openverse.org/

**OpenAPI Spec:** https://api.openverse.org/v1/schema/?format=json

### Key Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/v1/images/` | GET | Search openly-licensed images |
| `/v1/images/{identifier}/` | GET | Retrieve image by UUID |
| `/v1/images/{identifier}/related/` | GET | Find related images |
| `/v1/images/{identifier}/thumb/` | GET | Download image thumbnail |
| `/v1/images/stats/` | GET | List image sources with counts |
| `/v1/audio/` | GET | Search openly-licensed audio |
| `/v1/audio/{identifier}/` | GET | Retrieve audio track by UUID |
| `/v1/audio/{identifier}/related/` | GET | Find related audio |
| `/v1/audio/{identifier}/thumb/` | GET | Download audio artwork thumbnail |
| `/v1/audio/{identifier}/waveform/` | GET | Get waveform peak data |
| `/v1/audio/stats/` | GET | List audio sources with counts |
| `/v1/auth_tokens/register/` | POST | Register an OAuth2 application |
| `/v1/auth_tokens/token/` | POST | Exchange credentials for access token |

### Authentication

Openverse supports both anonymous and authenticated access:

- **Anonymous:** No key needed; limited to 1 req/sec, max 20 results per page
- **Authenticated (Standard):** Register at `/v1/auth_tokens/register/` to obtain OAuth2 credentials; higher rate limits and up to 500 results per page
- **Enhanced:** By approval from the Openverse team for high-volume integrations

### Media Sources

**Images (800M+):**
- Flickr: 535M+
- iNaturalist: 266M+
- Wikimedia Commons: 87M+
- Europeana: 13M+
- Metropolitan Museum of Art, NASA, Smithsonian, Rijksmuseum, and 40+ more

**Audio (~5M):**
- Wikimedia Commons: 3.88M+
- Jamendo: 627K+
- Freesound: 587K+

### Pricing

The API is free with no paid plans. See [finops/finops.yml](finops/finops.yml) for details.

## Resources

- [Plans](plans/plans.yml)
- [Rate Limits](rate-limits/rate-limits.yml)
- [FinOps](finops/finops.yml)
- [GitHub Repository](https://github.com/WordPress/openverse)
- [Terms of Service](https://wordpress.github.io/openverse-api/terms_of_service.html)
- [JavaScript Client](https://www.npmjs.com/package/@openverse/api-client)
