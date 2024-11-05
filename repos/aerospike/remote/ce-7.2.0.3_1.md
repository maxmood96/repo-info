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
