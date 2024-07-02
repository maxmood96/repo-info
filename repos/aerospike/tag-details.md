<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-7.1.0.2`](#aerospikece-7102)
-	[`aerospike:ce-7.1.0.2_1`](#aerospikece-7102_1)
-	[`aerospike:ee-7.1.0.2`](#aerospikeee-7102)
-	[`aerospike:ee-7.1.0.2_1`](#aerospikeee-7102_1)

## `aerospike:ce-7.1.0.2`

```console
$ docker pull aerospike@sha256:b351d9439b5abb84bb533c55ff9941d3c97a45e194fab96ae699c3c0f04d521a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-7.1.0.2` - linux; amd64

```console
$ docker pull aerospike@sha256:3bd6ed3779c3a1a0a7a10f432b8564e5cfee559a331e39a64f0ca0f5eb797a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78685120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c6d6bef561a29caeac7eb3204328202d96fedafe4e44103301724de257690f`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Fri, 21 Jun 2024 23:01:26 GMT
ARG RELEASE
# Fri, 21 Jun 2024 23:01:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 23:01:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 23:01:26 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 23:01:26 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 21 Jun 2024 23:01:26 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 23:01:26 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.2 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_EDITION=community
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.2/aerospike-server-community_7.1.0.2_tools-11.0.1_ubuntu22.04_x86_64.tgz
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_SHA_X86_64=e72fcc9ad9105379dd2f91490ddb0ebba4e2b65ea560e35572162ee3647c6355
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.2/aerospike-server-community_7.1.0.2_tools-11.0.1_ubuntu22.04_aarch64.tgz
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_SHA_AARCH64=c8705d8ad740207bff4d4d2f1934c4582d30fa86d8c59c1347e240fcd5017130
# Fri, 21 Jun 2024 23:01:26 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 21 Jun 2024 23:01:26 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.2/aerospike-server-community_7.1.0.2_tools-11.0.1_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=e72fcc9ad9105379dd2f91490ddb0ebba4e2b65ea560e35572162ee3647c6355 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.2/aerospike-server-community_7.1.0.2_tools-11.0.1_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=c8705d8ad740207bff4d4d2f1934c4582d30fa86d8c59c1347e240fcd5017130
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 21 Jun 2024 23:01:26 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 21 Jun 2024 23:01:26 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 21 Jun 2024 23:01:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Jun 2024 23:01:26 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 21 Jun 2024 23:01:26 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513d004e775c294ac254ee9579afbc0fccb1c8f877d424e7042987bff6108f1d`  
		Last Modified: Tue, 02 Jul 2024 03:02:42 GMT  
		Size: 49.1 MB (49148777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c6d733cb8913005969983e50bae8546f5690100d8fa2e0b6f762b05e15b5fa`  
		Last Modified: Tue, 02 Jul 2024 03:02:41 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa35260e9dc33e9110dfdef3d88f96a9d6d40389f8fbfde3f77ed81eff82455b`  
		Last Modified: Tue, 02 Jul 2024 03:02:41 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-7.1.0.2` - unknown; unknown

```console
$ docker pull aerospike@sha256:eb71341e086093981cc1113a7849caaa583ddd8dac777c1f8e78c2c0c644c13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1884045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a628110c32792593a6a5dbc79e9540d99eccc0a00e926b9eb79eb7f3be862d3`

```dockerfile
```

-	Layers:
	-	`sha256:84be11ce0a74b847542310f1f927eb6bdbe447086ea72f2c8dc9c61fbf265098`  
		Last Modified: Tue, 02 Jul 2024 03:02:42 GMT  
		Size: 1.9 MB (1855155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5e9f885d5063d3a3b99042827b7702ab33198d26f0ec3bdc23aa52cc8726d83`  
		Last Modified: Tue, 02 Jul 2024 03:02:41 GMT  
		Size: 28.9 KB (28890 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-7.1.0.2` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:4b1ebfef781c0c4f74925456ae57d15b824731cd8c55194403f1e02d10bdb3ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75896979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1776349908f1bcdbe1061bb70eb0c9fbe0af157a3e49323dd7d2ada268ce583`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 23:01:26 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.2 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_EDITION=community
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.2/aerospike-server-community_7.1.0.2_tools-11.0.1_ubuntu22.04_x86_64.tgz
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_SHA_X86_64=e72fcc9ad9105379dd2f91490ddb0ebba4e2b65ea560e35572162ee3647c6355
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.2/aerospike-server-community_7.1.0.2_tools-11.0.1_ubuntu22.04_aarch64.tgz
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_SHA_AARCH64=c8705d8ad740207bff4d4d2f1934c4582d30fa86d8c59c1347e240fcd5017130
# Fri, 21 Jun 2024 23:01:26 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 21 Jun 2024 23:01:26 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.2/aerospike-server-community_7.1.0.2_tools-11.0.1_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=e72fcc9ad9105379dd2f91490ddb0ebba4e2b65ea560e35572162ee3647c6355 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.2/aerospike-server-community_7.1.0.2_tools-11.0.1_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=c8705d8ad740207bff4d4d2f1934c4582d30fa86d8c59c1347e240fcd5017130
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 21 Jun 2024 23:01:26 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 21 Jun 2024 23:01:26 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 21 Jun 2024 23:01:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Jun 2024 23:01:26 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 21 Jun 2024 23:01:26 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4af9555f58866a129718b306d8a100f7565e608e51f237700198c829e8f72ee`  
		Last Modified: Sat, 22 Jun 2024 02:45:28 GMT  
		Size: 48.5 MB (48532909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9c789d7e91dfb764ae860127d7d69af28a6ea02931517d8ad736d981808c80`  
		Last Modified: Sat, 22 Jun 2024 02:45:26 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9e7e2cebf77d04a45b80c4c9e0459d92f2e55fa5531cdba8a7544f6e5e647`  
		Last Modified: Sat, 22 Jun 2024 02:45:26 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-7.1.0.2` - unknown; unknown

```console
$ docker pull aerospike@sha256:743f1c71f60beedf434b0d9c117073e3861615939825b8cca1a2d801031cb9c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1885540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0091cec267c47e98cd937db755a8f49e1f3160c3e212bd7f09625cab91ddce6d`

```dockerfile
```

-	Layers:
	-	`sha256:ec5a508e62670f28deeb6a1f97ee79986421d4aa5f70b0fc855c2ab63a49ee08`  
		Last Modified: Sat, 22 Jun 2024 02:45:27 GMT  
		Size: 1.9 MB (1856371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e585fdab3855a5e8cd3cd0ecb7874870f69c3dfc6bcdbed346c228c39c542d66`  
		Last Modified: Sat, 22 Jun 2024 02:45:26 GMT  
		Size: 29.2 KB (29169 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ce-7.1.0.2_1`

```console
$ docker pull aerospike@sha256:b351d9439b5abb84bb533c55ff9941d3c97a45e194fab96ae699c3c0f04d521a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-7.1.0.2_1` - linux; amd64

```console
$ docker pull aerospike@sha256:3bd6ed3779c3a1a0a7a10f432b8564e5cfee559a331e39a64f0ca0f5eb797a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78685120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c6d6bef561a29caeac7eb3204328202d96fedafe4e44103301724de257690f`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Fri, 21 Jun 2024 23:01:26 GMT
ARG RELEASE
# Fri, 21 Jun 2024 23:01:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 23:01:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 23:01:26 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 23:01:26 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 21 Jun 2024 23:01:26 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 23:01:26 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.2 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_EDITION=community
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.2/aerospike-server-community_7.1.0.2_tools-11.0.1_ubuntu22.04_x86_64.tgz
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_SHA_X86_64=e72fcc9ad9105379dd2f91490ddb0ebba4e2b65ea560e35572162ee3647c6355
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.2/aerospike-server-community_7.1.0.2_tools-11.0.1_ubuntu22.04_aarch64.tgz
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_SHA_AARCH64=c8705d8ad740207bff4d4d2f1934c4582d30fa86d8c59c1347e240fcd5017130
# Fri, 21 Jun 2024 23:01:26 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 21 Jun 2024 23:01:26 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.2/aerospike-server-community_7.1.0.2_tools-11.0.1_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=e72fcc9ad9105379dd2f91490ddb0ebba4e2b65ea560e35572162ee3647c6355 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.2/aerospike-server-community_7.1.0.2_tools-11.0.1_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=c8705d8ad740207bff4d4d2f1934c4582d30fa86d8c59c1347e240fcd5017130
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 21 Jun 2024 23:01:26 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 21 Jun 2024 23:01:26 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 21 Jun 2024 23:01:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Jun 2024 23:01:26 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 21 Jun 2024 23:01:26 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513d004e775c294ac254ee9579afbc0fccb1c8f877d424e7042987bff6108f1d`  
		Last Modified: Tue, 02 Jul 2024 03:02:42 GMT  
		Size: 49.1 MB (49148777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c6d733cb8913005969983e50bae8546f5690100d8fa2e0b6f762b05e15b5fa`  
		Last Modified: Tue, 02 Jul 2024 03:02:41 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa35260e9dc33e9110dfdef3d88f96a9d6d40389f8fbfde3f77ed81eff82455b`  
		Last Modified: Tue, 02 Jul 2024 03:02:41 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-7.1.0.2_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:eb71341e086093981cc1113a7849caaa583ddd8dac777c1f8e78c2c0c644c13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1884045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a628110c32792593a6a5dbc79e9540d99eccc0a00e926b9eb79eb7f3be862d3`

```dockerfile
```

-	Layers:
	-	`sha256:84be11ce0a74b847542310f1f927eb6bdbe447086ea72f2c8dc9c61fbf265098`  
		Last Modified: Tue, 02 Jul 2024 03:02:42 GMT  
		Size: 1.9 MB (1855155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5e9f885d5063d3a3b99042827b7702ab33198d26f0ec3bdc23aa52cc8726d83`  
		Last Modified: Tue, 02 Jul 2024 03:02:41 GMT  
		Size: 28.9 KB (28890 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-7.1.0.2_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:4b1ebfef781c0c4f74925456ae57d15b824731cd8c55194403f1e02d10bdb3ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75896979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1776349908f1bcdbe1061bb70eb0c9fbe0af157a3e49323dd7d2ada268ce583`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 23:01:26 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.2 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_EDITION=community
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.2/aerospike-server-community_7.1.0.2_tools-11.0.1_ubuntu22.04_x86_64.tgz
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_SHA_X86_64=e72fcc9ad9105379dd2f91490ddb0ebba4e2b65ea560e35572162ee3647c6355
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.2/aerospike-server-community_7.1.0.2_tools-11.0.1_ubuntu22.04_aarch64.tgz
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_SHA_AARCH64=c8705d8ad740207bff4d4d2f1934c4582d30fa86d8c59c1347e240fcd5017130
# Fri, 21 Jun 2024 23:01:26 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 21 Jun 2024 23:01:26 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.2/aerospike-server-community_7.1.0.2_tools-11.0.1_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=e72fcc9ad9105379dd2f91490ddb0ebba4e2b65ea560e35572162ee3647c6355 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.2/aerospike-server-community_7.1.0.2_tools-11.0.1_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=c8705d8ad740207bff4d4d2f1934c4582d30fa86d8c59c1347e240fcd5017130
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 21 Jun 2024 23:01:26 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 21 Jun 2024 23:01:26 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 21 Jun 2024 23:01:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Jun 2024 23:01:26 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 21 Jun 2024 23:01:26 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4af9555f58866a129718b306d8a100f7565e608e51f237700198c829e8f72ee`  
		Last Modified: Sat, 22 Jun 2024 02:45:28 GMT  
		Size: 48.5 MB (48532909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9c789d7e91dfb764ae860127d7d69af28a6ea02931517d8ad736d981808c80`  
		Last Modified: Sat, 22 Jun 2024 02:45:26 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9e7e2cebf77d04a45b80c4c9e0459d92f2e55fa5531cdba8a7544f6e5e647`  
		Last Modified: Sat, 22 Jun 2024 02:45:26 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-7.1.0.2_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:743f1c71f60beedf434b0d9c117073e3861615939825b8cca1a2d801031cb9c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1885540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0091cec267c47e98cd937db755a8f49e1f3160c3e212bd7f09625cab91ddce6d`

```dockerfile
```

-	Layers:
	-	`sha256:ec5a508e62670f28deeb6a1f97ee79986421d4aa5f70b0fc855c2ab63a49ee08`  
		Last Modified: Sat, 22 Jun 2024 02:45:27 GMT  
		Size: 1.9 MB (1856371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e585fdab3855a5e8cd3cd0ecb7874870f69c3dfc6bcdbed346c228c39c542d66`  
		Last Modified: Sat, 22 Jun 2024 02:45:26 GMT  
		Size: 29.2 KB (29169 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ee-7.1.0.2`

```console
$ docker pull aerospike@sha256:db1c7f3ed59f86b28eb9a1783abad87a1828186a3eae76a490685730f5666313
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-7.1.0.2` - linux; amd64

```console
$ docker pull aerospike@sha256:392a84cac64261711607ed71890fa958853c4e1c85c83c69e52bd014251a5c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81991217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17f9b990c5d91531624947091b204f50ddc8da1b6a69201eb76c754500ea489`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Fri, 21 Jun 2024 23:01:26 GMT
ARG RELEASE
# Fri, 21 Jun 2024 23:01:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 23:01:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 23:01:26 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 23:01:26 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 21 Jun 2024 23:01:26 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 23:01:26 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.2 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_EDITION=enterprise
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.2/aerospike-server-enterprise_7.1.0.2_tools-11.0.1_ubuntu22.04_x86_64.tgz
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_SHA_X86_64=fd5027e877a2ca934d0f5efe9f52a8cb4d9ec933d394e8b0a565ce6dabc31ad3
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.2/aerospike-server-enterprise_7.1.0.2_tools-11.0.1_ubuntu22.04_aarch64.tgz
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_SHA_AARCH64=991873240c3a3e322dc8c3fcf872d4cf13963cc69e4b196c505aa029194e13e8
# Fri, 21 Jun 2024 23:01:26 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 21 Jun 2024 23:01:26 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.2/aerospike-server-enterprise_7.1.0.2_tools-11.0.1_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=fd5027e877a2ca934d0f5efe9f52a8cb4d9ec933d394e8b0a565ce6dabc31ad3 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.2/aerospike-server-enterprise_7.1.0.2_tools-11.0.1_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=991873240c3a3e322dc8c3fcf872d4cf13963cc69e4b196c505aa029194e13e8
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 21 Jun 2024 23:01:26 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 21 Jun 2024 23:01:26 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 21 Jun 2024 23:01:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Jun 2024 23:01:26 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 21 Jun 2024 23:01:26 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9730a9023cf56cd4645efdccc0c44dd112ad6cb246326e1ab21d59afc757ec8`  
		Last Modified: Tue, 02 Jul 2024 03:02:34 GMT  
		Size: 52.5 MB (52454874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434771df318e365a61d157cd9ac00f3d33aa5d2c1fec766d8ba77ca59ebd3eda`  
		Last Modified: Tue, 02 Jul 2024 03:02:33 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e888f92768c0773f4010e295c0325facbc92cdd9f39fc3e3d4315eb9b4ef68`  
		Last Modified: Tue, 02 Jul 2024 03:02:33 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.1.0.2` - unknown; unknown

```console
$ docker pull aerospike@sha256:1c4df3d30e123a8d89eb1a9eb5775edc1c54996faf9d78bfaff690000908f8d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1946048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4751f216a73ba500792a68bb1efd2a2296912cf7e1681ea207ddabbfdc1ac195`

```dockerfile
```

-	Layers:
	-	`sha256:b57bd9501baf08302f1a905b7a1bdb2a5ecd3407823605686dfe24320f6471b5`  
		Last Modified: Tue, 02 Jul 2024 03:02:33 GMT  
		Size: 1.9 MB (1917141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2ed0035407576abb5c5431bfa0acc50827b0c5f599d1dfc60edb862b212b1f4`  
		Last Modified: Tue, 02 Jul 2024 03:02:34 GMT  
		Size: 28.9 KB (28907 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-7.1.0.2` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:5baa23dcadd9d00bcc7fa9c87a7ad94b5dae6812d3764ab2d76388c87d552c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79172812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24b6f03b4e6c86dfcb8ec8097edab018a0878395b9923622737b1f8fca93fa4`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 23:01:26 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.2 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_EDITION=enterprise
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.2/aerospike-server-enterprise_7.1.0.2_tools-11.0.1_ubuntu22.04_x86_64.tgz
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_SHA_X86_64=fd5027e877a2ca934d0f5efe9f52a8cb4d9ec933d394e8b0a565ce6dabc31ad3
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.2/aerospike-server-enterprise_7.1.0.2_tools-11.0.1_ubuntu22.04_aarch64.tgz
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_SHA_AARCH64=991873240c3a3e322dc8c3fcf872d4cf13963cc69e4b196c505aa029194e13e8
# Fri, 21 Jun 2024 23:01:26 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 21 Jun 2024 23:01:26 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.2/aerospike-server-enterprise_7.1.0.2_tools-11.0.1_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=fd5027e877a2ca934d0f5efe9f52a8cb4d9ec933d394e8b0a565ce6dabc31ad3 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.2/aerospike-server-enterprise_7.1.0.2_tools-11.0.1_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=991873240c3a3e322dc8c3fcf872d4cf13963cc69e4b196c505aa029194e13e8
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 21 Jun 2024 23:01:26 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 21 Jun 2024 23:01:26 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 21 Jun 2024 23:01:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Jun 2024 23:01:26 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 21 Jun 2024 23:01:26 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7d06495d3fb8378188b5cc956c3019f8d15bae82105ad71382024926d3caf5`  
		Last Modified: Sat, 22 Jun 2024 02:43:16 GMT  
		Size: 51.8 MB (51808744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3e6ba1a9f26faaedff3e76458c798a448781d3b9c15150a77ae19219775604`  
		Last Modified: Sat, 22 Jun 2024 02:43:14 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0822695b752e12bb231509fa5c4fd121acf02bb24e12ef7b4e533848ff5bdb`  
		Last Modified: Sat, 22 Jun 2024 02:43:15 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.1.0.2` - unknown; unknown

```console
$ docker pull aerospike@sha256:886b7a54757a66b783461acc0b9383f1e04f0ffbab1129c9b828e62b59fe2834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1947554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f18b9aeda0701cb9affe16bb4e8a5a0fd847069007e41abda9a530def09247e`

```dockerfile
```

-	Layers:
	-	`sha256:285160d1a87d3780b26350b8bf2ae28d79ba01d958899d892b624df536192af2`  
		Last Modified: Sat, 22 Jun 2024 02:43:15 GMT  
		Size: 1.9 MB (1918369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1742857357b468c96c94f8e67dd5adc925e99c4d79d8471b74ab66ff2f23d4f1`  
		Last Modified: Sat, 22 Jun 2024 02:43:14 GMT  
		Size: 29.2 KB (29185 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ee-7.1.0.2_1`

```console
$ docker pull aerospike@sha256:db1c7f3ed59f86b28eb9a1783abad87a1828186a3eae76a490685730f5666313
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-7.1.0.2_1` - linux; amd64

```console
$ docker pull aerospike@sha256:392a84cac64261711607ed71890fa958853c4e1c85c83c69e52bd014251a5c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81991217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17f9b990c5d91531624947091b204f50ddc8da1b6a69201eb76c754500ea489`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Fri, 21 Jun 2024 23:01:26 GMT
ARG RELEASE
# Fri, 21 Jun 2024 23:01:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 23:01:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 23:01:26 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 23:01:26 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 21 Jun 2024 23:01:26 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 23:01:26 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.2 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_EDITION=enterprise
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.2/aerospike-server-enterprise_7.1.0.2_tools-11.0.1_ubuntu22.04_x86_64.tgz
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_SHA_X86_64=fd5027e877a2ca934d0f5efe9f52a8cb4d9ec933d394e8b0a565ce6dabc31ad3
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.2/aerospike-server-enterprise_7.1.0.2_tools-11.0.1_ubuntu22.04_aarch64.tgz
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_SHA_AARCH64=991873240c3a3e322dc8c3fcf872d4cf13963cc69e4b196c505aa029194e13e8
# Fri, 21 Jun 2024 23:01:26 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 21 Jun 2024 23:01:26 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.2/aerospike-server-enterprise_7.1.0.2_tools-11.0.1_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=fd5027e877a2ca934d0f5efe9f52a8cb4d9ec933d394e8b0a565ce6dabc31ad3 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.2/aerospike-server-enterprise_7.1.0.2_tools-11.0.1_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=991873240c3a3e322dc8c3fcf872d4cf13963cc69e4b196c505aa029194e13e8
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 21 Jun 2024 23:01:26 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 21 Jun 2024 23:01:26 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 21 Jun 2024 23:01:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Jun 2024 23:01:26 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 21 Jun 2024 23:01:26 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9730a9023cf56cd4645efdccc0c44dd112ad6cb246326e1ab21d59afc757ec8`  
		Last Modified: Tue, 02 Jul 2024 03:02:34 GMT  
		Size: 52.5 MB (52454874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434771df318e365a61d157cd9ac00f3d33aa5d2c1fec766d8ba77ca59ebd3eda`  
		Last Modified: Tue, 02 Jul 2024 03:02:33 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e888f92768c0773f4010e295c0325facbc92cdd9f39fc3e3d4315eb9b4ef68`  
		Last Modified: Tue, 02 Jul 2024 03:02:33 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.1.0.2_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:1c4df3d30e123a8d89eb1a9eb5775edc1c54996faf9d78bfaff690000908f8d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1946048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4751f216a73ba500792a68bb1efd2a2296912cf7e1681ea207ddabbfdc1ac195`

```dockerfile
```

-	Layers:
	-	`sha256:b57bd9501baf08302f1a905b7a1bdb2a5ecd3407823605686dfe24320f6471b5`  
		Last Modified: Tue, 02 Jul 2024 03:02:33 GMT  
		Size: 1.9 MB (1917141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2ed0035407576abb5c5431bfa0acc50827b0c5f599d1dfc60edb862b212b1f4`  
		Last Modified: Tue, 02 Jul 2024 03:02:34 GMT  
		Size: 28.9 KB (28907 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-7.1.0.2_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:5baa23dcadd9d00bcc7fa9c87a7ad94b5dae6812d3764ab2d76388c87d552c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79172812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24b6f03b4e6c86dfcb8ec8097edab018a0878395b9923622737b1f8fca93fa4`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 23:01:26 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.2 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_EDITION=enterprise
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.2/aerospike-server-enterprise_7.1.0.2_tools-11.0.1_ubuntu22.04_x86_64.tgz
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_SHA_X86_64=fd5027e877a2ca934d0f5efe9f52a8cb4d9ec933d394e8b0a565ce6dabc31ad3
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.2/aerospike-server-enterprise_7.1.0.2_tools-11.0.1_ubuntu22.04_aarch64.tgz
# Fri, 21 Jun 2024 23:01:26 GMT
ARG AEROSPIKE_SHA_AARCH64=991873240c3a3e322dc8c3fcf872d4cf13963cc69e4b196c505aa029194e13e8
# Fri, 21 Jun 2024 23:01:26 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 21 Jun 2024 23:01:26 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.2/aerospike-server-enterprise_7.1.0.2_tools-11.0.1_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=fd5027e877a2ca934d0f5efe9f52a8cb4d9ec933d394e8b0a565ce6dabc31ad3 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.2/aerospike-server-enterprise_7.1.0.2_tools-11.0.1_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=991873240c3a3e322dc8c3fcf872d4cf13963cc69e4b196c505aa029194e13e8
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 21 Jun 2024 23:01:26 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 21 Jun 2024 23:01:26 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 21 Jun 2024 23:01:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Jun 2024 23:01:26 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 21 Jun 2024 23:01:26 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7d06495d3fb8378188b5cc956c3019f8d15bae82105ad71382024926d3caf5`  
		Last Modified: Sat, 22 Jun 2024 02:43:16 GMT  
		Size: 51.8 MB (51808744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3e6ba1a9f26faaedff3e76458c798a448781d3b9c15150a77ae19219775604`  
		Last Modified: Sat, 22 Jun 2024 02:43:14 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0822695b752e12bb231509fa5c4fd121acf02bb24e12ef7b4e533848ff5bdb`  
		Last Modified: Sat, 22 Jun 2024 02:43:15 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.1.0.2_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:886b7a54757a66b783461acc0b9383f1e04f0ffbab1129c9b828e62b59fe2834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1947554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f18b9aeda0701cb9affe16bb4e8a5a0fd847069007e41abda9a530def09247e`

```dockerfile
```

-	Layers:
	-	`sha256:285160d1a87d3780b26350b8bf2ae28d79ba01d958899d892b624df536192af2`  
		Last Modified: Sat, 22 Jun 2024 02:43:15 GMT  
		Size: 1.9 MB (1918369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1742857357b468c96c94f8e67dd5adc925e99c4d79d8471b74ab66ff2f23d4f1`  
		Last Modified: Sat, 22 Jun 2024 02:43:14 GMT  
		Size: 29.2 KB (29185 bytes)  
		MIME: application/vnd.in-toto+json
