## `aerospike:ce-7.1.0.1_1`

```console
$ docker pull aerospike@sha256:4dd7e0f2b18337ca856532e1da16e86c306a8c5b1184ce11c54616222e0b099c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-7.1.0.1_1` - linux; amd64

```console
$ docker pull aerospike@sha256:1516b2ff400227527da1a22ebcb131dcc58d6eb21efc4751201f0ca461565507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78685761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78c4ec2b42655a1ef668a456b7b2329a1d88ada8d55a15c22848c2b7af5d704`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 02:22:43 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 04 Jun 2024 02:22:43 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 04 Jun 2024 02:22:43 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.1/aerospike-server-community_7.1.0.1_tools-11.0.1_ubuntu22.04_x86_64.tgz
# Tue, 04 Jun 2024 02:22:43 GMT
ARG AEROSPIKE_SHA_X86_64=f1e5be4382d0db88e42ee6405b85ca2b2c7b37035957f8ca49c5f556d60f3719
# Tue, 04 Jun 2024 02:22:43 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.1/aerospike-server-community_7.1.0.1_tools-11.0.1_ubuntu22.04_aarch64.tgz
# Tue, 04 Jun 2024 02:22:43 GMT
ARG AEROSPIKE_SHA_AARCH64=81d03b2fd9373805ddb89b02612602d93f4b6d543252da213d32d82f075d4020
# Tue, 04 Jun 2024 02:22:43 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 04 Jun 2024 02:22:43 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.1/aerospike-server-community_7.1.0.1_tools-11.0.1_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=f1e5be4382d0db88e42ee6405b85ca2b2c7b37035957f8ca49c5f556d60f3719 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.1/aerospike-server-community_7.1.0.1_tools-11.0.1_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=81d03b2fd9373805ddb89b02612602d93f4b6d543252da213d32d82f075d4020
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 04 Jun 2024 02:22:43 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 04 Jun 2024 02:22:43 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 04 Jun 2024 02:22:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Jun 2024 02:22:43 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 04 Jun 2024 02:22:43 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3842a9b4e6d5c2ddd5cb68b3abc80ff9e40cbae6bcf5258a4f8922943574ec2b`  
		Last Modified: Wed, 05 Jun 2024 02:20:06 GMT  
		Size: 49.1 MB (49149716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995245d38e93beda1f0c157b2b0be842f75f110db0142bfd5f164dabcf8da6d8`  
		Last Modified: Wed, 05 Jun 2024 02:20:05 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7bbdde4e88c302cfd25b6a368917c1ceab5d66edaec89e1c854d2d59f505e2`  
		Last Modified: Wed, 05 Jun 2024 02:20:05 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-7.1.0.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:157e1715687a06d9545993b9f426aac989b0b69bce04433d4a83d3c1cd1e78ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1883997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aaf865f5e8475e8bbd97b501441977786b6bcf988dd80b7909f83ef3cbaef3e`

```dockerfile
```

-	Layers:
	-	`sha256:8de2cf45e94cbda4e4511b51c6f58b4a30931951a4899685d48e880b4fef6e78`  
		Last Modified: Wed, 05 Jun 2024 02:20:06 GMT  
		Size: 1.9 MB (1855154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:203022a091d69a1817a6713906bdb6aa733d531cdd4d2fcccc7bf665b846b02a`  
		Last Modified: Wed, 05 Jun 2024 02:20:05 GMT  
		Size: 28.8 KB (28843 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-7.1.0.1_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:77c97901862922eeb379c56ee00d3aa36fd1aad463f92f2e0924851f4090af9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75894787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d514e2daa0105fa4817ef5e587a0f56ae8975b479c3730993b1b672cf3e23846`
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
# Tue, 04 Jun 2024 02:22:43 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 04 Jun 2024 02:22:43 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 04 Jun 2024 02:22:43 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.1/aerospike-server-community_7.1.0.1_tools-11.0.1_ubuntu22.04_x86_64.tgz
# Tue, 04 Jun 2024 02:22:43 GMT
ARG AEROSPIKE_SHA_X86_64=f1e5be4382d0db88e42ee6405b85ca2b2c7b37035957f8ca49c5f556d60f3719
# Tue, 04 Jun 2024 02:22:43 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.1/aerospike-server-community_7.1.0.1_tools-11.0.1_ubuntu22.04_aarch64.tgz
# Tue, 04 Jun 2024 02:22:43 GMT
ARG AEROSPIKE_SHA_AARCH64=81d03b2fd9373805ddb89b02612602d93f4b6d543252da213d32d82f075d4020
# Tue, 04 Jun 2024 02:22:43 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 04 Jun 2024 02:22:43 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.1/aerospike-server-community_7.1.0.1_tools-11.0.1_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=f1e5be4382d0db88e42ee6405b85ca2b2c7b37035957f8ca49c5f556d60f3719 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.1/aerospike-server-community_7.1.0.1_tools-11.0.1_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=81d03b2fd9373805ddb89b02612602d93f4b6d543252da213d32d82f075d4020
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 04 Jun 2024 02:22:43 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 04 Jun 2024 02:22:43 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 04 Jun 2024 02:22:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Jun 2024 02:22:43 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 04 Jun 2024 02:22:43 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce27cf92acfc998e720d7e43f8846229feb4f1ac30f2180882a62b71528d8de`  
		Last Modified: Wed, 05 Jun 2024 13:22:35 GMT  
		Size: 48.5 MB (48530715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f736ea52a85fd1a002c862c345653172b37663899807388ce776cddacaf41d63`  
		Last Modified: Wed, 05 Jun 2024 13:22:33 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa07dcf9344eef5bd60735d151168a36b6e23337c009260657c38af9786892a`  
		Last Modified: Wed, 05 Jun 2024 13:22:33 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-7.1.0.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:b982c044aa2778e3111cfdf62ddeaa83ba4c40d96eb3dccde63312ac91ab22e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1885490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39647c5ff5f843b771581b1f46240f8ca072733e3e9973e0cb4025bb7e602e4c`

```dockerfile
```

-	Layers:
	-	`sha256:fe90103e30ee3d001f85abd4f55b094b9bd8fcb3171c5be7947353240a66f12b`  
		Last Modified: Wed, 05 Jun 2024 13:22:34 GMT  
		Size: 1.9 MB (1856370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36ce34b3ed0280770f625f59ea73d68c8e884090485502c65f8dd65e0adcac60`  
		Last Modified: Wed, 05 Jun 2024 13:22:33 GMT  
		Size: 29.1 KB (29120 bytes)  
		MIME: application/vnd.in-toto+json
