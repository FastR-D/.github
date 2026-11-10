# FastR-D shared workflows

Versioned reusable CI primitives. Consumers pin a reviewed commit SHA and retain their own product test/build scripts.

## Node/npm check

Call `.github/workflows/node-npm-check.yml` with an optional repository-relative `working-directory` (default `.`). The caller owns `.github/scripts/ci-node.sh`; it runs after a clean `npm ci` on Node 24. This workflow checks out the caller's event SHA, including pull-request merge refs. It does not publish or deploy.
