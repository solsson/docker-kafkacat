# A build of https://github.com/edenhill/kafkacat/pull/110
FROM solsson/kafkacat@sha256:ebebf47061300b14a4b4c2e1e4303ab29f65e4b95d34af1b14bb8f7ec6da7cef

RUN set -ex; \
  export DEBIAN_FRONTEND=noninteractive; \
  runDeps='curl jq'; \
  buildDeps='ca-certificates'; \
  apt-get update && apt-get install -y $runDeps $buildDeps --no-install-recommends; \
  rm -rf /var/lib/apt/lists/*; \
  \
  apt-get purge -y --auto-remove $buildDeps; \
  rm /var/log/dpkg.log /var/log/apt/*.log