## `aerospike:ee-8.1.1.1`

```console
$ docker pull aerospike@sha256:1250e6603f1c36b960b8eb1760c996dd98b69e670d77b76a158f2bf4c7c69667
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.1.1.1` - linux; amd64

```console
$ docker pull aerospike@sha256:669dcf4ca086b8ff9ddaab40c13791be2856fb36ccc542e727431c1464f515e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86268363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d1305ac153e4abd8563bd247865b2e3aff3e3a0bb3c3692f504499089e823c8`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:14:49 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.1.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 17 Mar 2026 01:14:49 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 17 Mar 2026 01:14:49 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 17 Mar 2026 01:14:49 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.1/aerospike-server-enterprise_8.1.1.1_tools-12.1.1_ubuntu24.04_x86_64.tgz
# Tue, 17 Mar 2026 01:14:49 GMT
ARG AEROSPIKE_SHA_X86_64=a2990f0970a7ca1bdec8068109dc0573ca975c5dd5d014a9a6f1b0a178849625
# Tue, 17 Mar 2026 01:14:49 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.1/aerospike-server-enterprise_8.1.1.1_tools-12.1.1_ubuntu24.04_aarch64.tgz
# Tue, 17 Mar 2026 01:14:49 GMT
ARG AEROSPIKE_SHA_AARCH64=1ccb5d3a9cb396ce6dcb58d24d71b2a5eb46f29ec3c24b62472318c02e668d4d
# Tue, 17 Mar 2026 01:14:49 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 17 Mar 2026 01:14:49 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.1/aerospike-server-enterprise_8.1.1.1_tools-12.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=a2990f0970a7ca1bdec8068109dc0573ca975c5dd5d014a9a6f1b0a178849625 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.1/aerospike-server-enterprise_8.1.1.1_tools-12.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=1ccb5d3a9cb396ce6dcb58d24d71b2a5eb46f29ec3c24b62472318c02e668d4d
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 17 Mar 2026 01:14:49 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 17 Mar 2026 01:14:49 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 17 Mar 2026 01:14:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:14:49 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 17 Mar 2026 01:14:49 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9107aa4483161a57a5f35d7783f51cc7f4730414ecf057e0f673a9f283601715`  
		Last Modified: Tue, 17 Mar 2026 01:15:03 GMT  
		Size: 56.5 MB (56534072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c817357a10bbd49b5cd4b9356ced9a24b3828d9ae21b243ed831780ae0a357ea`  
		Last Modified: Tue, 17 Mar 2026 01:15:01 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5564fe02c8f6e8507d377f47517d08043fc89e41e0be82ebf01cef0746e426`  
		Last Modified: Tue, 17 Mar 2026 01:15:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.1.1` - unknown; unknown

```console
$ docker pull aerospike@sha256:913f5369c9372ac99d3408382f82fe149838ce45adad931b11faa9412de1e9e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1378ec41210e197e2b6eb29ddb7ab4cf9a186c66c3d64baff749974662c4bb34`

```dockerfile
```

-	Layers:
	-	`sha256:ee2e72bb9d0fc204383d9247564be2a6a32d4155e2311e3ca1f2c7d330efa22f`  
		Last Modified: Tue, 17 Mar 2026 01:15:01 GMT  
		Size: 2.2 MB (2181597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42ab16e8616d1906cb57f78fc2c6613b4f8f3c156193e3cf5a8fd2ab954b2e49`  
		Last Modified: Tue, 17 Mar 2026 01:15:01 GMT  
		Size: 29.0 KB (28985 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.1.1.1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:0329576e485f4fc548375766283eb0a49f0fbbb5bb35446c6369de8e1d25e60f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84196806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d8fae177ee73458c57e724edcee3e6dfc5677ab2b5e58de0376f32a227a5e1`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:14:49 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.1.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 17 Mar 2026 01:14:49 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 17 Mar 2026 01:14:49 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 17 Mar 2026 01:14:49 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.1/aerospike-server-enterprise_8.1.1.1_tools-12.1.1_ubuntu24.04_x86_64.tgz
# Tue, 17 Mar 2026 01:14:49 GMT
ARG AEROSPIKE_SHA_X86_64=a2990f0970a7ca1bdec8068109dc0573ca975c5dd5d014a9a6f1b0a178849625
# Tue, 17 Mar 2026 01:14:49 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.1/aerospike-server-enterprise_8.1.1.1_tools-12.1.1_ubuntu24.04_aarch64.tgz
# Tue, 17 Mar 2026 01:14:49 GMT
ARG AEROSPIKE_SHA_AARCH64=1ccb5d3a9cb396ce6dcb58d24d71b2a5eb46f29ec3c24b62472318c02e668d4d
# Tue, 17 Mar 2026 01:14:49 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 17 Mar 2026 01:14:49 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.1/aerospike-server-enterprise_8.1.1.1_tools-12.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=a2990f0970a7ca1bdec8068109dc0573ca975c5dd5d014a9a6f1b0a178849625 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.1/aerospike-server-enterprise_8.1.1.1_tools-12.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=1ccb5d3a9cb396ce6dcb58d24d71b2a5eb46f29ec3c24b62472318c02e668d4d
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 17 Mar 2026 01:14:49 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 17 Mar 2026 01:14:49 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 17 Mar 2026 01:14:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:14:49 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 17 Mar 2026 01:14:49 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff037cae9d54da2d1e9eb9d994f82e3e0bfe8ea490625b07595f8cee2c5e3c83`  
		Last Modified: Tue, 17 Mar 2026 01:15:03 GMT  
		Size: 55.3 MB (55324796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bb1d7c8a136c27ea1eef730de87e7641b1ef1f2aa2d4f31eec3e3091b3bdb7`  
		Last Modified: Tue, 17 Mar 2026 01:15:01 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4b21408f93b41e148aa1ed8e3070ea423948927fd8e2f96fc8ebbd063732cd`  
		Last Modified: Tue, 17 Mar 2026 01:15:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.1.1` - unknown; unknown

```console
$ docker pull aerospike@sha256:c76845d4a8447333b3b2a79a9d1c6d2e920a92c6a91ecc61d70ccec7814411e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f628cde39608c4ae063c48f5fe873606a957d845cd9e059b82ea673e0bfd170`

```dockerfile
```

-	Layers:
	-	`sha256:6495dab68342b90b36c048be2f10badfaade1e9bf6e91fd025396b412664ee71`  
		Last Modified: Tue, 17 Mar 2026 01:15:01 GMT  
		Size: 2.2 MB (2183877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0931d1678fca6ef8cb9613eee329ac96d538596be2f555258cf9e2e2a20f9f3`  
		Last Modified: Tue, 17 Mar 2026 01:15:01 GMT  
		Size: 29.1 KB (29065 bytes)  
		MIME: application/vnd.in-toto+json
