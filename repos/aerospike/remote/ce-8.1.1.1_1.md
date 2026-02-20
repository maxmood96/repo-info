## `aerospike:ce-8.1.1.1_1`

```console
$ docker pull aerospike@sha256:670024de159cd184cc80871c61f742b53fa8d035ada2f1b899c3bac1856c0ebe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.1.1.1_1` - linux; amd64

```console
$ docker pull aerospike@sha256:4f6496d67b71afdcda316fdbf008a66b8f84795c50a85b8845cf8aa785f01b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84106507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7424614d112aa80e5e9c7eea5ba18ce3c9d2ef380974dfe1279e9c5cf81983d8`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 21:06:33 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.1.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 20 Feb 2026 21:06:33 GMT
ARG AEROSPIKE_EDITION=community
# Fri, 20 Feb 2026 21:06:33 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Fri, 20 Feb 2026 21:06:33 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.1/aerospike-server-community_8.1.1.1_tools-12.1.1_ubuntu24.04_x86_64.tgz
# Fri, 20 Feb 2026 21:06:33 GMT
ARG AEROSPIKE_SHA_X86_64=bbbbb10b08d67391058da8c88df06da027b25f7bd4bf44959a14a78c392d10a7
# Fri, 20 Feb 2026 21:06:33 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.1/aerospike-server-community_8.1.1.1_tools-12.1.1_ubuntu24.04_aarch64.tgz
# Fri, 20 Feb 2026 21:06:33 GMT
ARG AEROSPIKE_SHA_AARCH64=5129d72c4dceb753a95f49a2cfc29788dd55acfb140ff4cee7431824301b13c0
# Fri, 20 Feb 2026 21:06:33 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 20 Feb 2026 21:06:33 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.1/aerospike-server-community_8.1.1.1_tools-12.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=bbbbb10b08d67391058da8c88df06da027b25f7bd4bf44959a14a78c392d10a7 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.1/aerospike-server-community_8.1.1.1_tools-12.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=5129d72c4dceb753a95f49a2cfc29788dd55acfb140ff4cee7431824301b13c0
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 20 Feb 2026 21:06:33 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 20 Feb 2026 21:06:33 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 20 Feb 2026 21:06:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 21:06:33 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 20 Feb 2026 21:06:33 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d05b052498e1d63676745e4c7bab4865d4fea54acd19e47c6a13189f5e818a3`  
		Last Modified: Fri, 20 Feb 2026 21:06:44 GMT  
		Size: 54.4 MB (54376597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5082e3e9889bb193ed618ccdff12e807c65f4e476dff266c18426db813e8d557`  
		Last Modified: Fri, 20 Feb 2026 21:06:43 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d1ebbe9f6a4bd93eeceb3faff5d2aaddf4c752b729e9c6dad1351764252dc7`  
		Last Modified: Fri, 20 Feb 2026 21:06:43 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.1.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:ebe1714da0f504bd2111d72bbc2427d56976fef4035663dde6a9307044fd57ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ae23a742c9231cb622354f74cfd4c15862b04dae6e861ced26dd76623d0ba6`

```dockerfile
```

-	Layers:
	-	`sha256:115c7e2e38ac7c93e52a38d7c91b73c82c7787608b84e7dc95917e5d252513ab`  
		Last Modified: Fri, 20 Feb 2026 21:06:43 GMT  
		Size: 2.2 MB (2180940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2742704f84001655ba4d49a98dc257c5568adc34635eccf387b7dce47611d41a`  
		Last Modified: Fri, 20 Feb 2026 21:06:43 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.1.1.1_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:f338bf3e5356cc9c20c004f4511fa9b8b24ee25d4694ab2b9b11928d2b693506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82054003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ff8dcb3ac9cc840270690cbd7facb1559bdf568c29539b4a3f234367426728`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 21:06:29 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.1.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 20 Feb 2026 21:06:29 GMT
ARG AEROSPIKE_EDITION=community
# Fri, 20 Feb 2026 21:06:29 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Fri, 20 Feb 2026 21:06:29 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.1/aerospike-server-community_8.1.1.1_tools-12.1.1_ubuntu24.04_x86_64.tgz
# Fri, 20 Feb 2026 21:06:29 GMT
ARG AEROSPIKE_SHA_X86_64=bbbbb10b08d67391058da8c88df06da027b25f7bd4bf44959a14a78c392d10a7
# Fri, 20 Feb 2026 21:06:29 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.1/aerospike-server-community_8.1.1.1_tools-12.1.1_ubuntu24.04_aarch64.tgz
# Fri, 20 Feb 2026 21:06:29 GMT
ARG AEROSPIKE_SHA_AARCH64=5129d72c4dceb753a95f49a2cfc29788dd55acfb140ff4cee7431824301b13c0
# Fri, 20 Feb 2026 21:06:29 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 20 Feb 2026 21:06:29 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.1/aerospike-server-community_8.1.1.1_tools-12.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=bbbbb10b08d67391058da8c88df06da027b25f7bd4bf44959a14a78c392d10a7 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.1/aerospike-server-community_8.1.1.1_tools-12.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=5129d72c4dceb753a95f49a2cfc29788dd55acfb140ff4cee7431824301b13c0
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 20 Feb 2026 21:06:29 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 20 Feb 2026 21:06:29 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 20 Feb 2026 21:06:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 21:06:29 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 20 Feb 2026 21:06:29 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48ead858f603827744234b63a641fa056402f96abc6575f894faf87b2a91c36`  
		Last Modified: Fri, 20 Feb 2026 21:06:42 GMT  
		Size: 53.2 MB (53186583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badcbc8b51f3e4a4a0b0ce71c7abf7979b7b9af8640c0da473c844f472fe9585`  
		Last Modified: Fri, 20 Feb 2026 21:06:40 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a99ec733893aba661911bd2e2906da10d2de877252ee1b5c5defe90f8c9c75f`  
		Last Modified: Fri, 20 Feb 2026 21:06:40 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.1.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:b3a10a20d5d56e1a581848fc88d8604e96905338851d794b7924de83c3c93afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9347ccfcf9d2996812adea24b8c51f489c4c64e743274598466e04d61ad346`

```dockerfile
```

-	Layers:
	-	`sha256:93a710c61d9a5cf43d7ad1aee0e7ebcc323fa7de2d3c170b6aa6e9a444727b13`  
		Last Modified: Fri, 20 Feb 2026 21:06:40 GMT  
		Size: 2.2 MB (2183220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef62245327cd9629be08823bf30b841e7496e82c12d4def6239cdfe2027229d0`  
		Last Modified: Fri, 20 Feb 2026 21:06:40 GMT  
		Size: 29.0 KB (29048 bytes)  
		MIME: application/vnd.in-toto+json
