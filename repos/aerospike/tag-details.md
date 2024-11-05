<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-7.2.0.3`](#aerospikece-7203)
-	[`aerospike:ce-7.2.0.3_1`](#aerospikece-7203_1)
-	[`aerospike:ee-7.2.0.3`](#aerospikeee-7203)
-	[`aerospike:ee-7.2.0.3_1`](#aerospikeee-7203_1)

## `aerospike:ce-7.2.0.3`

```console
$ docker pull aerospike@sha256:71b95f1253f5d4ca4031ad780d4ec71e6b0eff6d38d6c85e0c133c091fbddbad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-7.2.0.3` - linux; amd64

```console
$ docker pull aerospike@sha256:1d2686780af5bfbfc5bde7258c9c629c43bc50b884fb0d39a125ccb94d4211d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77540158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2340b496dd66348665ccd2f4ec68d917f6be87f3b4929fb3922b0f00d9da7cd`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2024 23:25:06 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.2.0.3 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_EDITION=community
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.3/aerospike-server-community_7.2.0.3_tools-11.1.0_ubuntu24.04_x86_64.tgz
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_SHA_X86_64=d3a1c213879fd459ca340fc6fd57a16e07f0c7196cc88ee4bb6adba5099b6c6e
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.3/aerospike-server-community_7.2.0.3_tools-11.1.0_ubuntu24.04_aarch64.tgz
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_SHA_AARCH64=537b8c8e02e4c8878ca057942d6af663555ee25ff859d08e35b07c0c445339e0
# Fri, 01 Nov 2024 23:25:06 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 01 Nov 2024 23:25:06 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.3/aerospike-server-community_7.2.0.3_tools-11.1.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=d3a1c213879fd459ca340fc6fd57a16e07f0c7196cc88ee4bb6adba5099b6c6e AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.3/aerospike-server-community_7.2.0.3_tools-11.1.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=537b8c8e02e4c8878ca057942d6af663555ee25ff859d08e35b07c0c445339e0
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 01 Nov 2024 23:25:06 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 01 Nov 2024 23:25:06 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 01 Nov 2024 23:25:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 01 Nov 2024 23:25:06 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 01 Nov 2024 23:25:06 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81dd36f8d2d1e4b02b2d5cfb70bb595141974be612d9cd48e0c84d9ace14f0a`  
		Last Modified: Mon, 04 Nov 2024 20:58:39 GMT  
		Size: 47.8 MB (47787495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a79eba50eed3b88dadc5bb1e6a1b04deaa3001e2a597cee705af44f3fe93431`  
		Last Modified: Mon, 04 Nov 2024 20:58:37 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8870acd6f5f33a1562f803f29772073af5263682e8ab12653dc772616c5981`  
		Last Modified: Mon, 04 Nov 2024 20:58:37 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-7.2.0.3` - unknown; unknown

```console
$ docker pull aerospike@sha256:d97d65d85c6161908ec9d2a06847d391f68e5055cae22eaa7dad1f08830f04d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1891994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588dd2447689af01025478b0af8bcb1e55228bf83388e26f72b4fd445be9d4d9`

```dockerfile
```

-	Layers:
	-	`sha256:bd9a9157a760fa31dcbf257f9aad9d4e3ee8e0a9318fc405516a3aac47ec4892`  
		Last Modified: Mon, 04 Nov 2024 20:58:37 GMT  
		Size: 1.9 MB (1862847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aa1a60f50843a26abf6d0dd88985b50c6cefd105cc21b0a02311a5a64165f21`  
		Last Modified: Mon, 04 Nov 2024 20:58:37 GMT  
		Size: 29.1 KB (29147 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-7.2.0.3` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:dc584d5138f4282a38d9184a188343798da8a3fdc6f9be93a6a1b1c08a8863c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76094452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc7d206e01956bd770531959d4fa2d2cc9a06402219a6bcd1859b592ab80302`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2024 23:25:06 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.2.0.3 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_EDITION=community
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.3/aerospike-server-community_7.2.0.3_tools-11.1.0_ubuntu24.04_x86_64.tgz
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_SHA_X86_64=d3a1c213879fd459ca340fc6fd57a16e07f0c7196cc88ee4bb6adba5099b6c6e
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.3/aerospike-server-community_7.2.0.3_tools-11.1.0_ubuntu24.04_aarch64.tgz
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_SHA_AARCH64=537b8c8e02e4c8878ca057942d6af663555ee25ff859d08e35b07c0c445339e0
# Fri, 01 Nov 2024 23:25:06 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 01 Nov 2024 23:25:06 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.3/aerospike-server-community_7.2.0.3_tools-11.1.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=d3a1c213879fd459ca340fc6fd57a16e07f0c7196cc88ee4bb6adba5099b6c6e AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.3/aerospike-server-community_7.2.0.3_tools-11.1.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=537b8c8e02e4c8878ca057942d6af663555ee25ff859d08e35b07c0c445339e0
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 01 Nov 2024 23:25:06 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 01 Nov 2024 23:25:06 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 01 Nov 2024 23:25:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 01 Nov 2024 23:25:06 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 01 Nov 2024 23:25:06 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360eb3ae19a81e0919a9bdf844df8debb1f0fdd96f646be322c90797da458674`  
		Last Modified: Mon, 04 Nov 2024 21:01:56 GMT  
		Size: 47.2 MB (47206307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ffc0c2c49e75a905832c17f2f4d355ee3deffc3ec33d6fe260edfb11674ccb`  
		Last Modified: Mon, 04 Nov 2024 21:01:54 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09e8da80bbebff0adaab80e6f4c273e9b1979a3cfa1bd894a1b481ed0e5863f`  
		Last Modified: Mon, 04 Nov 2024 21:01:54 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-7.2.0.3` - unknown; unknown

```console
$ docker pull aerospike@sha256:cdd0f88f44e2882dd6a00798172d7141701e902c55ec8623d60b11c9be5f036a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1894327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cf2188a6d02717c3d66fce1163b190f131e9e02e30cd45abc7a81d3780f611a`

```dockerfile
```

-	Layers:
	-	`sha256:2127896a1aa579cf3b1f6c67f44b005df4b7dd9a30880747c0113cfd946d1b36`  
		Last Modified: Mon, 04 Nov 2024 21:01:55 GMT  
		Size: 1.9 MB (1865100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bd8cef15a8226a6b954974046403922c48f7288296849f610abdfaf21686cd8`  
		Last Modified: Mon, 04 Nov 2024 21:01:54 GMT  
		Size: 29.2 KB (29227 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ce-7.2.0.3_1`

```console
$ docker pull aerospike@sha256:71b95f1253f5d4ca4031ad780d4ec71e6b0eff6d38d6c85e0c133c091fbddbad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-7.2.0.3_1` - linux; amd64

```console
$ docker pull aerospike@sha256:1d2686780af5bfbfc5bde7258c9c629c43bc50b884fb0d39a125ccb94d4211d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77540158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2340b496dd66348665ccd2f4ec68d917f6be87f3b4929fb3922b0f00d9da7cd`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2024 23:25:06 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.2.0.3 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_EDITION=community
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.3/aerospike-server-community_7.2.0.3_tools-11.1.0_ubuntu24.04_x86_64.tgz
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_SHA_X86_64=d3a1c213879fd459ca340fc6fd57a16e07f0c7196cc88ee4bb6adba5099b6c6e
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.3/aerospike-server-community_7.2.0.3_tools-11.1.0_ubuntu24.04_aarch64.tgz
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_SHA_AARCH64=537b8c8e02e4c8878ca057942d6af663555ee25ff859d08e35b07c0c445339e0
# Fri, 01 Nov 2024 23:25:06 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 01 Nov 2024 23:25:06 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.3/aerospike-server-community_7.2.0.3_tools-11.1.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=d3a1c213879fd459ca340fc6fd57a16e07f0c7196cc88ee4bb6adba5099b6c6e AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.3/aerospike-server-community_7.2.0.3_tools-11.1.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=537b8c8e02e4c8878ca057942d6af663555ee25ff859d08e35b07c0c445339e0
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 01 Nov 2024 23:25:06 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 01 Nov 2024 23:25:06 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 01 Nov 2024 23:25:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 01 Nov 2024 23:25:06 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 01 Nov 2024 23:25:06 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81dd36f8d2d1e4b02b2d5cfb70bb595141974be612d9cd48e0c84d9ace14f0a`  
		Last Modified: Mon, 04 Nov 2024 20:58:39 GMT  
		Size: 47.8 MB (47787495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a79eba50eed3b88dadc5bb1e6a1b04deaa3001e2a597cee705af44f3fe93431`  
		Last Modified: Mon, 04 Nov 2024 20:58:37 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8870acd6f5f33a1562f803f29772073af5263682e8ab12653dc772616c5981`  
		Last Modified: Mon, 04 Nov 2024 20:58:37 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-7.2.0.3_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:d97d65d85c6161908ec9d2a06847d391f68e5055cae22eaa7dad1f08830f04d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1891994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588dd2447689af01025478b0af8bcb1e55228bf83388e26f72b4fd445be9d4d9`

```dockerfile
```

-	Layers:
	-	`sha256:bd9a9157a760fa31dcbf257f9aad9d4e3ee8e0a9318fc405516a3aac47ec4892`  
		Last Modified: Mon, 04 Nov 2024 20:58:37 GMT  
		Size: 1.9 MB (1862847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aa1a60f50843a26abf6d0dd88985b50c6cefd105cc21b0a02311a5a64165f21`  
		Last Modified: Mon, 04 Nov 2024 20:58:37 GMT  
		Size: 29.1 KB (29147 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-7.2.0.3_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:dc584d5138f4282a38d9184a188343798da8a3fdc6f9be93a6a1b1c08a8863c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76094452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc7d206e01956bd770531959d4fa2d2cc9a06402219a6bcd1859b592ab80302`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2024 23:25:06 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.2.0.3 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_EDITION=community
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.3/aerospike-server-community_7.2.0.3_tools-11.1.0_ubuntu24.04_x86_64.tgz
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_SHA_X86_64=d3a1c213879fd459ca340fc6fd57a16e07f0c7196cc88ee4bb6adba5099b6c6e
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.3/aerospike-server-community_7.2.0.3_tools-11.1.0_ubuntu24.04_aarch64.tgz
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_SHA_AARCH64=537b8c8e02e4c8878ca057942d6af663555ee25ff859d08e35b07c0c445339e0
# Fri, 01 Nov 2024 23:25:06 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 01 Nov 2024 23:25:06 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.3/aerospike-server-community_7.2.0.3_tools-11.1.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=d3a1c213879fd459ca340fc6fd57a16e07f0c7196cc88ee4bb6adba5099b6c6e AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.3/aerospike-server-community_7.2.0.3_tools-11.1.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=537b8c8e02e4c8878ca057942d6af663555ee25ff859d08e35b07c0c445339e0
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 01 Nov 2024 23:25:06 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 01 Nov 2024 23:25:06 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 01 Nov 2024 23:25:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 01 Nov 2024 23:25:06 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 01 Nov 2024 23:25:06 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360eb3ae19a81e0919a9bdf844df8debb1f0fdd96f646be322c90797da458674`  
		Last Modified: Mon, 04 Nov 2024 21:01:56 GMT  
		Size: 47.2 MB (47206307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ffc0c2c49e75a905832c17f2f4d355ee3deffc3ec33d6fe260edfb11674ccb`  
		Last Modified: Mon, 04 Nov 2024 21:01:54 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09e8da80bbebff0adaab80e6f4c273e9b1979a3cfa1bd894a1b481ed0e5863f`  
		Last Modified: Mon, 04 Nov 2024 21:01:54 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-7.2.0.3_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:cdd0f88f44e2882dd6a00798172d7141701e902c55ec8623d60b11c9be5f036a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1894327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cf2188a6d02717c3d66fce1163b190f131e9e02e30cd45abc7a81d3780f611a`

```dockerfile
```

-	Layers:
	-	`sha256:2127896a1aa579cf3b1f6c67f44b005df4b7dd9a30880747c0113cfd946d1b36`  
		Last Modified: Mon, 04 Nov 2024 21:01:55 GMT  
		Size: 1.9 MB (1865100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bd8cef15a8226a6b954974046403922c48f7288296849f610abdfaf21686cd8`  
		Last Modified: Mon, 04 Nov 2024 21:01:54 GMT  
		Size: 29.2 KB (29227 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ee-7.2.0.3`

```console
$ docker pull aerospike@sha256:a4271e5705e6c9d0399fc228c959e9b353efc65d190edfba7c8cce4add3d6dbb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-7.2.0.3` - linux; amd64

```console
$ docker pull aerospike@sha256:33c9c8edd17b1687edfc8880b470713b17680386c42b303b1d97ea1a46f47da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81688562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f3709ecf7cac69b443289eccd3ac90dddf02d6138f8c0eb11cf68895931b49`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2024 23:25:06 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.2.0.3 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_EDITION=enterprise
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.3/aerospike-server-enterprise_7.2.0.3_tools-11.1.0_ubuntu24.04_x86_64.tgz
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_SHA_X86_64=b165d757b6877dca3750f29e6acc836bdd8888e4d9fca62940fd19cb2bdd08a7
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.3/aerospike-server-enterprise_7.2.0.3_tools-11.1.0_ubuntu24.04_aarch64.tgz
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_SHA_AARCH64=8b9efedcda5e92be7f27e987eb46aeb4cd439106d86a744ba971adfb828c8a9f
# Fri, 01 Nov 2024 23:25:06 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 01 Nov 2024 23:25:06 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.3/aerospike-server-enterprise_7.2.0.3_tools-11.1.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=b165d757b6877dca3750f29e6acc836bdd8888e4d9fca62940fd19cb2bdd08a7 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.3/aerospike-server-enterprise_7.2.0.3_tools-11.1.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=8b9efedcda5e92be7f27e987eb46aeb4cd439106d86a744ba971adfb828c8a9f
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 01 Nov 2024 23:25:06 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 01 Nov 2024 23:25:06 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 01 Nov 2024 23:25:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 01 Nov 2024 23:25:06 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 01 Nov 2024 23:25:06 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e24647a13ac03487feae9ba78e91b7365c61f432fa9c3ea267e516172375e7a`  
		Last Modified: Mon, 04 Nov 2024 20:58:31 GMT  
		Size: 51.9 MB (51935900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0cf64a4d3d4858eea473a1f03612cd2631fe33681b82cf44bf7f44fc809a60`  
		Last Modified: Mon, 04 Nov 2024 20:58:30 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b52dc87058f5f732b24b9835295f605d7cf7b98497b4cf3d2dc9163ac297f62`  
		Last Modified: Mon, 04 Nov 2024 20:58:30 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.2.0.3` - unknown; unknown

```console
$ docker pull aerospike@sha256:854306f24af97c815691db4dd902fd0fa0bff5a8fd049d1cd72f2e1719d772a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1986378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8344ed799cb5134ede70a26d57080c748a3f3df3dd9f509221e3471957ccde48`

```dockerfile
```

-	Layers:
	-	`sha256:61fdb598969cff49c4ec053cd58f73cf0d062f9a1e9b77f0872a6ff50b943ff9`  
		Last Modified: Mon, 04 Nov 2024 20:58:30 GMT  
		Size: 2.0 MB (1957215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ab417726efeeb96e3e09d683eab02263222627bc7d06e81d8048f3cf1cdbc8`  
		Last Modified: Mon, 04 Nov 2024 20:58:30 GMT  
		Size: 29.2 KB (29163 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-7.2.0.3` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:88916853a0f75b4f943249e2421e03d9d6a05c576b8a15e4d2948ef01bc205a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80261742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f46179627a40d85119d128bc01a44b8ffa329b34ae4dc9ec4f0546904e8c6f`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2024 23:25:06 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.2.0.3 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_EDITION=enterprise
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.3/aerospike-server-enterprise_7.2.0.3_tools-11.1.0_ubuntu24.04_x86_64.tgz
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_SHA_X86_64=b165d757b6877dca3750f29e6acc836bdd8888e4d9fca62940fd19cb2bdd08a7
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.3/aerospike-server-enterprise_7.2.0.3_tools-11.1.0_ubuntu24.04_aarch64.tgz
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_SHA_AARCH64=8b9efedcda5e92be7f27e987eb46aeb4cd439106d86a744ba971adfb828c8a9f
# Fri, 01 Nov 2024 23:25:06 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 01 Nov 2024 23:25:06 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.3/aerospike-server-enterprise_7.2.0.3_tools-11.1.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=b165d757b6877dca3750f29e6acc836bdd8888e4d9fca62940fd19cb2bdd08a7 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.3/aerospike-server-enterprise_7.2.0.3_tools-11.1.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=8b9efedcda5e92be7f27e987eb46aeb4cd439106d86a744ba971adfb828c8a9f
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 01 Nov 2024 23:25:06 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 01 Nov 2024 23:25:06 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 01 Nov 2024 23:25:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 01 Nov 2024 23:25:06 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 01 Nov 2024 23:25:06 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856e7fd371e5cd3a8696457ad72eede2086752fefe080774ad7d1a1f0a23cb14`  
		Last Modified: Mon, 04 Nov 2024 21:01:13 GMT  
		Size: 51.4 MB (51373599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320ced0d753b80ccff0d42ff3e512c0d93fb4e9c2c06369d518ba250902001f1`  
		Last Modified: Mon, 04 Nov 2024 21:01:10 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6222101745650b932d3ec904fe19be80829b36a623ad8b8e5b8b4bc7c08618`  
		Last Modified: Mon, 04 Nov 2024 21:01:10 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.2.0.3` - unknown; unknown

```console
$ docker pull aerospike@sha256:8b2f75f05da4c2c0d29fd3a2041deb1fd3ec23ac4bbab4d5899324ab15816041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1988729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005a41f1ce9819fdd6bd32bb6a44dd7383e22d6abe5e8e60003b26b138e07773`

```dockerfile
```

-	Layers:
	-	`sha256:3af336806a6ab3ed30cea1119d48b47866940a90c83c9520abe3ffe83effc42a`  
		Last Modified: Mon, 04 Nov 2024 21:01:10 GMT  
		Size: 2.0 MB (1959486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:767d33637db95ab2ce7b0ff49ef7229236e370324fa9994dc9637044b4e72b79`  
		Last Modified: Mon, 04 Nov 2024 21:01:10 GMT  
		Size: 29.2 KB (29243 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ee-7.2.0.3_1`

```console
$ docker pull aerospike@sha256:a4271e5705e6c9d0399fc228c959e9b353efc65d190edfba7c8cce4add3d6dbb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-7.2.0.3_1` - linux; amd64

```console
$ docker pull aerospike@sha256:33c9c8edd17b1687edfc8880b470713b17680386c42b303b1d97ea1a46f47da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81688562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f3709ecf7cac69b443289eccd3ac90dddf02d6138f8c0eb11cf68895931b49`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2024 23:25:06 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.2.0.3 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_EDITION=enterprise
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.3/aerospike-server-enterprise_7.2.0.3_tools-11.1.0_ubuntu24.04_x86_64.tgz
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_SHA_X86_64=b165d757b6877dca3750f29e6acc836bdd8888e4d9fca62940fd19cb2bdd08a7
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.3/aerospike-server-enterprise_7.2.0.3_tools-11.1.0_ubuntu24.04_aarch64.tgz
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_SHA_AARCH64=8b9efedcda5e92be7f27e987eb46aeb4cd439106d86a744ba971adfb828c8a9f
# Fri, 01 Nov 2024 23:25:06 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 01 Nov 2024 23:25:06 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.3/aerospike-server-enterprise_7.2.0.3_tools-11.1.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=b165d757b6877dca3750f29e6acc836bdd8888e4d9fca62940fd19cb2bdd08a7 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.3/aerospike-server-enterprise_7.2.0.3_tools-11.1.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=8b9efedcda5e92be7f27e987eb46aeb4cd439106d86a744ba971adfb828c8a9f
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 01 Nov 2024 23:25:06 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 01 Nov 2024 23:25:06 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 01 Nov 2024 23:25:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 01 Nov 2024 23:25:06 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 01 Nov 2024 23:25:06 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e24647a13ac03487feae9ba78e91b7365c61f432fa9c3ea267e516172375e7a`  
		Last Modified: Mon, 04 Nov 2024 20:58:31 GMT  
		Size: 51.9 MB (51935900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0cf64a4d3d4858eea473a1f03612cd2631fe33681b82cf44bf7f44fc809a60`  
		Last Modified: Mon, 04 Nov 2024 20:58:30 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b52dc87058f5f732b24b9835295f605d7cf7b98497b4cf3d2dc9163ac297f62`  
		Last Modified: Mon, 04 Nov 2024 20:58:30 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.2.0.3_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:854306f24af97c815691db4dd902fd0fa0bff5a8fd049d1cd72f2e1719d772a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1986378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8344ed799cb5134ede70a26d57080c748a3f3df3dd9f509221e3471957ccde48`

```dockerfile
```

-	Layers:
	-	`sha256:61fdb598969cff49c4ec053cd58f73cf0d062f9a1e9b77f0872a6ff50b943ff9`  
		Last Modified: Mon, 04 Nov 2024 20:58:30 GMT  
		Size: 2.0 MB (1957215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ab417726efeeb96e3e09d683eab02263222627bc7d06e81d8048f3cf1cdbc8`  
		Last Modified: Mon, 04 Nov 2024 20:58:30 GMT  
		Size: 29.2 KB (29163 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-7.2.0.3_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:88916853a0f75b4f943249e2421e03d9d6a05c576b8a15e4d2948ef01bc205a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80261742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f46179627a40d85119d128bc01a44b8ffa329b34ae4dc9ec4f0546904e8c6f`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2024 23:25:06 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.2.0.3 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_EDITION=enterprise
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.3/aerospike-server-enterprise_7.2.0.3_tools-11.1.0_ubuntu24.04_x86_64.tgz
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_SHA_X86_64=b165d757b6877dca3750f29e6acc836bdd8888e4d9fca62940fd19cb2bdd08a7
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.3/aerospike-server-enterprise_7.2.0.3_tools-11.1.0_ubuntu24.04_aarch64.tgz
# Fri, 01 Nov 2024 23:25:06 GMT
ARG AEROSPIKE_SHA_AARCH64=8b9efedcda5e92be7f27e987eb46aeb4cd439106d86a744ba971adfb828c8a9f
# Fri, 01 Nov 2024 23:25:06 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 01 Nov 2024 23:25:06 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.3/aerospike-server-enterprise_7.2.0.3_tools-11.1.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=b165d757b6877dca3750f29e6acc836bdd8888e4d9fca62940fd19cb2bdd08a7 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.3/aerospike-server-enterprise_7.2.0.3_tools-11.1.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=8b9efedcda5e92be7f27e987eb46aeb4cd439106d86a744ba971adfb828c8a9f
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 01 Nov 2024 23:25:06 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 01 Nov 2024 23:25:06 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 01 Nov 2024 23:25:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 01 Nov 2024 23:25:06 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 01 Nov 2024 23:25:06 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856e7fd371e5cd3a8696457ad72eede2086752fefe080774ad7d1a1f0a23cb14`  
		Last Modified: Mon, 04 Nov 2024 21:01:13 GMT  
		Size: 51.4 MB (51373599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320ced0d753b80ccff0d42ff3e512c0d93fb4e9c2c06369d518ba250902001f1`  
		Last Modified: Mon, 04 Nov 2024 21:01:10 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6222101745650b932d3ec904fe19be80829b36a623ad8b8e5b8b4bc7c08618`  
		Last Modified: Mon, 04 Nov 2024 21:01:10 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.2.0.3_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:8b2f75f05da4c2c0d29fd3a2041deb1fd3ec23ac4bbab4d5899324ab15816041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1988729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005a41f1ce9819fdd6bd32bb6a44dd7383e22d6abe5e8e60003b26b138e07773`

```dockerfile
```

-	Layers:
	-	`sha256:3af336806a6ab3ed30cea1119d48b47866940a90c83c9520abe3ffe83effc42a`  
		Last Modified: Mon, 04 Nov 2024 21:01:10 GMT  
		Size: 2.0 MB (1959486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:767d33637db95ab2ce7b0ff49ef7229236e370324fa9994dc9637044b4e72b79`  
		Last Modified: Mon, 04 Nov 2024 21:01:10 GMT  
		Size: 29.2 KB (29243 bytes)  
		MIME: application/vnd.in-toto+json
