# A build of https://github.com/edenhill/kafkacat/pull/110
FROM solsson/kafkacat@sha256:b32eedf936f3cde44cd164ddc77dfcf7565a8af4e357ff6de1abe4389ca530c9

RUN set -ex; \
  export DEBIAN_FRONTEND=noninteractive; \
  runDeps='curl jq'; \
  buildDeps='ca-certificates'; \
  apt-get update && apt-get install -y $runDeps $buildDeps --no-install-recommends; \
  rm -rf /var/lib/apt/lists/*; \
  \
  apt-get purge -y --auto-remove $buildDeps; \
  rm /var/log/dpkg.log /var/log/apt/*.log