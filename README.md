# cache-proof

Live checks for Zode's node-local Actions cache (zodeops/zoded `docs/ci-contract.md`, "Actions cache"). Each run is a real GitHub Actions job on a Zode runner. Run it twice: the first run fills the cache and the second reads it back.

- `big`: `actions/cache` restore of a 1 GB cache, timed.
- `node`: `actions/setup-node` with `cache: npm`.
- `buildx`: `docker/build-push-action` with `type=gha`.
- `artifacts`: upload and download of an artifact, which goes through to GitHub.
- `scope`: the fork pull request check. It saves `poison` on a fork PR, and main must miss it.
fork change 1794495914
