## `aerospike:ce-8.1.0.0_1`

```console
$ docker pull aerospike@sha256:cb062a91e890f362b1d049a9bffa93a81a7c2cce65f803ee54d2a1c5c1e3c3fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.1.0.0_1` - linux; amd64

```console
$ docker pull aerospike@sha256:9a0c6bc5954b8f4232a349c49ad5a56d416f8db07b08488e1e0b4f5cb7930887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81711181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a740201daba5288f50a9eb7f97839aaae6c7412e34f36492fb8093f6b8d2fca`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 17:58:51 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.0.0 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 05 Aug 2025 17:58:51 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 05 Aug 2025 17:58:51 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 05 Aug 2025 17:58:51 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.0/aerospike-server-community_8.1.0.0_tools-12.0.0_ubuntu24.04_x86_64.tgz
# Tue, 05 Aug 2025 17:58:51 GMT
ARG AEROSPIKE_SHA_X86_64=74a469cecd5ac0c69ae85ca99e0c78337cf2b279af8b7154620da774a9f208b5
# Tue, 05 Aug 2025 17:58:51 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.0/aerospike-server-community_8.1.0.0_tools-12.0.0_ubuntu24.04_aarch64.tgz
# Tue, 05 Aug 2025 17:58:51 GMT
ARG AEROSPIKE_SHA_AARCH64=39805f5fd6d832d63b4aa9161adaee40a2db55438ca6d11c1c5554474b38bad8
# Tue, 05 Aug 2025 17:58:51 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 05 Aug 2025 17:58:51 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.0/aerospike-server-community_8.1.0.0_tools-12.0.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=74a469cecd5ac0c69ae85ca99e0c78337cf2b279af8b7154620da774a9f208b5 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.0/aerospike-server-community_8.1.0.0_tools-12.0.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=39805f5fd6d832d63b4aa9161adaee40a2db55438ca6d11c1c5554474b38bad8
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 05 Aug 2025 17:58:51 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 05 Aug 2025 17:58:51 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 05 Aug 2025 17:58:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 05 Aug 2025 17:58:51 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 05 Aug 2025 17:58:51 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9972e4c1f565a3811b82f5f8272cc661b4c4d628c65f1b44ed2645f525e462d`  
		Last Modified: Tue, 12 Aug 2025 17:24:02 GMT  
		Size: 52.0 MB (51985667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59681dd0fdeac6e72fc77131a368b0f0064d561bc1c1a1151f62fa6627e844fe`  
		Last Modified: Tue, 12 Aug 2025 17:23:56 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de800b8b2e508a7ece4a10b1e26562cdcc76df824001bb59d97bf98d8e38520c`  
		Last Modified: Tue, 12 Aug 2025 17:24:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.0.0_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:dc20344e6f3400c60fe0a41786d6f38cee0c9b25deb5b7797ee0b89cd7d9681a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fcf6fa9e10e6411821a96c141495d4e5e14c227b8afcf080bbf64bbc2b340d1`

```dockerfile
```

-	Layers:
	-	`sha256:2f49568ceda956dff8037535ac5a646f3b0564dcf93e0ec1bcb2101f79837748`  
		Last Modified: Tue, 12 Aug 2025 20:25:22 GMT  
		Size: 2.2 MB (2182308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:febcff362d94bb433cad05158c8f1eb961c8e16a0a88d6514e9ac17b660d1d7c`  
		Last Modified: Tue, 12 Aug 2025 20:25:23 GMT  
		Size: 29.0 KB (29011 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.1.0.0_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:95a0f6705d06a15a10bf67b6b67fb9bde4db3f253a9116e04e2da55e2901d6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80080401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6274cba663ef50d45786b529708af4af52e622c8f924bb8ced964d16d2cb566f`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 17:58:51 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.0.0 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 05 Aug 2025 17:58:51 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 05 Aug 2025 17:58:51 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 05 Aug 2025 17:58:51 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.0/aerospike-server-community_8.1.0.0_tools-12.0.0_ubuntu24.04_x86_64.tgz
# Tue, 05 Aug 2025 17:58:51 GMT
ARG AEROSPIKE_SHA_X86_64=74a469cecd5ac0c69ae85ca99e0c78337cf2b279af8b7154620da774a9f208b5
# Tue, 05 Aug 2025 17:58:51 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.0/aerospike-server-community_8.1.0.0_tools-12.0.0_ubuntu24.04_aarch64.tgz
# Tue, 05 Aug 2025 17:58:51 GMT
ARG AEROSPIKE_SHA_AARCH64=39805f5fd6d832d63b4aa9161adaee40a2db55438ca6d11c1c5554474b38bad8
# Tue, 05 Aug 2025 17:58:51 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 05 Aug 2025 17:58:51 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.0/aerospike-server-community_8.1.0.0_tools-12.0.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=74a469cecd5ac0c69ae85ca99e0c78337cf2b279af8b7154620da774a9f208b5 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.0/aerospike-server-community_8.1.0.0_tools-12.0.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=39805f5fd6d832d63b4aa9161adaee40a2db55438ca6d11c1c5554474b38bad8
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 05 Aug 2025 17:58:51 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 05 Aug 2025 17:58:51 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 05 Aug 2025 17:58:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 05 Aug 2025 17:58:51 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 05 Aug 2025 17:58:51 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3dd836038f70f692d929d546b2c7aab7ffe10967a4df7c3848ef065884bf5f4`  
		Last Modified: Tue, 12 Aug 2025 21:48:56 GMT  
		Size: 51.2 MB (51217724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8834c289b7ae7126db82579980faad51dddd5bee3db7c2533ca9e8f5573fc4e`  
		Last Modified: Tue, 12 Aug 2025 17:56:14 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b367466e26ff993f988eb82b55e1e336cf863afcc2a4bf0da5422186e9a373ea`  
		Last Modified: Tue, 12 Aug 2025 17:56:15 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.0.0_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:ae55f561cc3502ebe42ee74e2e753ec456269a5b7d39d39cdda4fc018b5be1fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2213680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb192b7bfdfd12e55e9e3b81b3a06bc9682c9a53d4db19e80edcf5775fcbcc9`

```dockerfile
```

-	Layers:
	-	`sha256:5609748adf5348617a6c1656e9b4d6bb1f8df13486e38cd5ef2208ced27124c3`  
		Last Modified: Tue, 12 Aug 2025 20:25:27 GMT  
		Size: 2.2 MB (2184588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e197e1ec72e74c5848e2cb6dbcbe6cfc5c351ae875f5b094b0b1c98b00c29dd`  
		Last Modified: Tue, 12 Aug 2025 20:25:28 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json
