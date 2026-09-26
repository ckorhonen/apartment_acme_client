# Apartment ACME Client Instructions

This Ruby gem’s code lives in `lib/`, its RSpec suite is under `spec/`, and the Rakefile defines `bundle exec rake` as the default test task. Install with `bundle install`, then run `bundle exec rake` for a code-only change when the legacy Ruby/Rails dependencies work on the host.

The `encryption:create_crypto_client`, `encryption:renew_and_update_certificate`, and `encryption:update_nginx_config` tasks register ACME accounts, issue or renew certificates, rewrite Nginx configuration, and can restart Nginx. Use the documented test ACME setting only for an explicitly scoped integration task; routine test success never proves certificate issuance or service reload. Never commit private keys, certificate material, or real domain inventory.
