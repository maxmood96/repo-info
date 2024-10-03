<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-7.1.0.7`](#aerospikece-7107)
-	[`aerospike:ce-7.1.0.7_1`](#aerospikece-7107_1)
-	[`aerospike:ee-7.1.0.7`](#aerospikeee-7107)
-	[`aerospike:ee-7.1.0.7_1`](#aerospikeee-7107_1)

## `aerospike:ce-7.1.0.7`

```console
$ docker pull aerospike@sha256:e4a691660e9b9e921788093bf251c8a8731d0dfb2cc6574fdc53c935ef431106
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-7.1.0.7` - linux; amd64

```console
$ docker pull aerospike@sha256:f3dbab6237c8bd82f37ed34686a23db773035ee190db7698c29a732db39255d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77367918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839b0cf1d24ebf6a0a5adf5e68f6adafde849328db072d9c0551a3afe25d3323`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Thu, 03 Oct 2024 05:39:44 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.7 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_EDITION=community
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.7/aerospike-server-community_7.1.0.7_tools-11.0.2_ubuntu22.04_x86_64.tgz
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_SHA_X86_64=1c3eb9d2297aaa6d1175aa568cfd5ef671386e492496aa07d294452a188071c8
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.7/aerospike-server-community_7.1.0.7_tools-11.0.2_ubuntu22.04_aarch64.tgz
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_SHA_AARCH64=a4b9d959505469e40c4c14b1302138af05140d340024c41f67cf562536d356fa
# Thu, 03 Oct 2024 05:39:44 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 03 Oct 2024 05:39:44 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.7/aerospike-server-community_7.1.0.7_tools-11.0.2_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=1c3eb9d2297aaa6d1175aa568cfd5ef671386e492496aa07d294452a188071c8 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.7/aerospike-server-community_7.1.0.7_tools-11.0.2_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=a4b9d959505469e40c4c14b1302138af05140d340024c41f67cf562536d356fa
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 03 Oct 2024 05:39:44 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 03 Oct 2024 05:39:44 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 03 Oct 2024 05:39:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Oct 2024 05:39:44 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 03 Oct 2024 05:39:44 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49400dd09bc4ff7334606f502955ea330c80588870c2cae7b38d4652a9fa45c6`  
		Last Modified: Thu, 03 Oct 2024 16:58:02 GMT  
		Size: 47.8 MB (47829937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0790ea283cf4ab494cca8f60ba06d7cf0780d7693e7726cf1b1d82955813104b`  
		Last Modified: Thu, 03 Oct 2024 16:58:01 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca83c859fa652a08ac6d52a98cf91462dec4aec9a2e7f03b4eb7788a7bf521de`  
		Last Modified: Thu, 03 Oct 2024 16:58:01 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-7.1.0.7` - unknown; unknown

```console
$ docker pull aerospike@sha256:89e6086580bb926e5c10adfa987cb07bd713c4572233378f6622be90c59f6487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1905601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f30f58dfd0789858409ecdb135b30efdc4a44bf1c1ab69a3b8b610f9a5b8014`

```dockerfile
```

-	Layers:
	-	`sha256:cb127fa803292603ecec4753671bcc7e53dbd0a5d8e70ee0758f7acdda1a76df`  
		Last Modified: Thu, 03 Oct 2024 16:58:01 GMT  
		Size: 1.9 MB (1876703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff4de3a63959d91b1266a509f09751d050f2590279f1d4ef748191400f7427d`  
		Last Modified: Thu, 03 Oct 2024 16:58:01 GMT  
		Size: 28.9 KB (28898 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-7.1.0.7` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:2f6f4aa34505ae86e8f56b78e9ae72c24995ad8509f4d5e004b29193e94f0500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74593626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd391abfe8dd4c834b0ef23b989770c5fef95312ff490ee2a70dcf6dbfbd4e04`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Thu, 03 Oct 2024 05:39:44 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.7 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_EDITION=community
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.7/aerospike-server-community_7.1.0.7_tools-11.0.2_ubuntu22.04_x86_64.tgz
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_SHA_X86_64=1c3eb9d2297aaa6d1175aa568cfd5ef671386e492496aa07d294452a188071c8
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.7/aerospike-server-community_7.1.0.7_tools-11.0.2_ubuntu22.04_aarch64.tgz
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_SHA_AARCH64=a4b9d959505469e40c4c14b1302138af05140d340024c41f67cf562536d356fa
# Thu, 03 Oct 2024 05:39:44 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 03 Oct 2024 05:39:44 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.7/aerospike-server-community_7.1.0.7_tools-11.0.2_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=1c3eb9d2297aaa6d1175aa568cfd5ef671386e492496aa07d294452a188071c8 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.7/aerospike-server-community_7.1.0.7_tools-11.0.2_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=a4b9d959505469e40c4c14b1302138af05140d340024c41f67cf562536d356fa
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 03 Oct 2024 05:39:44 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 03 Oct 2024 05:39:44 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 03 Oct 2024 05:39:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Oct 2024 05:39:44 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 03 Oct 2024 05:39:44 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04e2ebbd1cd505644dd1ebeff63803a9e37afe77c33226f80da6a2d875fd74b`  
		Last Modified: Thu, 03 Oct 2024 16:59:17 GMT  
		Size: 47.2 MB (47233006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4169ebba7eb3c59003b63789a9de21d06642668eeb53bbe530cb6295b01797d`  
		Last Modified: Thu, 03 Oct 2024 16:59:15 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c51065dbfd3c7fc47015a6099f3de451637ede7e6376839201bfeb3a479e02`  
		Last Modified: Thu, 03 Oct 2024 16:59:15 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-7.1.0.7` - unknown; unknown

```console
$ docker pull aerospike@sha256:9a0e37bb0f46eec8764591480446fd0055dc278f777759f207f0ba359368b7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1907034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f2a895d0bedbbce6f94ae1692a4e0aef013815009b575004aadddafd9ec132`

```dockerfile
```

-	Layers:
	-	`sha256:4a312a66f5bf484bf08555782bd3779158d8d03052621d59277117fdfe7c35e2`  
		Last Modified: Thu, 03 Oct 2024 16:59:16 GMT  
		Size: 1.9 MB (1878062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcb8c0de61abd250ffb9e44d16e7ec0c2a053c8631df013e7c44e9246408077b`  
		Last Modified: Thu, 03 Oct 2024 16:59:15 GMT  
		Size: 29.0 KB (28972 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ce-7.1.0.7_1`

```console
$ docker pull aerospike@sha256:e4a691660e9b9e921788093bf251c8a8731d0dfb2cc6574fdc53c935ef431106
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-7.1.0.7_1` - linux; amd64

```console
$ docker pull aerospike@sha256:f3dbab6237c8bd82f37ed34686a23db773035ee190db7698c29a732db39255d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77367918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839b0cf1d24ebf6a0a5adf5e68f6adafde849328db072d9c0551a3afe25d3323`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Thu, 03 Oct 2024 05:39:44 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.7 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_EDITION=community
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.7/aerospike-server-community_7.1.0.7_tools-11.0.2_ubuntu22.04_x86_64.tgz
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_SHA_X86_64=1c3eb9d2297aaa6d1175aa568cfd5ef671386e492496aa07d294452a188071c8
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.7/aerospike-server-community_7.1.0.7_tools-11.0.2_ubuntu22.04_aarch64.tgz
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_SHA_AARCH64=a4b9d959505469e40c4c14b1302138af05140d340024c41f67cf562536d356fa
# Thu, 03 Oct 2024 05:39:44 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 03 Oct 2024 05:39:44 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.7/aerospike-server-community_7.1.0.7_tools-11.0.2_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=1c3eb9d2297aaa6d1175aa568cfd5ef671386e492496aa07d294452a188071c8 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.7/aerospike-server-community_7.1.0.7_tools-11.0.2_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=a4b9d959505469e40c4c14b1302138af05140d340024c41f67cf562536d356fa
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 03 Oct 2024 05:39:44 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 03 Oct 2024 05:39:44 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 03 Oct 2024 05:39:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Oct 2024 05:39:44 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 03 Oct 2024 05:39:44 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49400dd09bc4ff7334606f502955ea330c80588870c2cae7b38d4652a9fa45c6`  
		Last Modified: Thu, 03 Oct 2024 16:58:02 GMT  
		Size: 47.8 MB (47829937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0790ea283cf4ab494cca8f60ba06d7cf0780d7693e7726cf1b1d82955813104b`  
		Last Modified: Thu, 03 Oct 2024 16:58:01 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca83c859fa652a08ac6d52a98cf91462dec4aec9a2e7f03b4eb7788a7bf521de`  
		Last Modified: Thu, 03 Oct 2024 16:58:01 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-7.1.0.7_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:89e6086580bb926e5c10adfa987cb07bd713c4572233378f6622be90c59f6487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1905601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f30f58dfd0789858409ecdb135b30efdc4a44bf1c1ab69a3b8b610f9a5b8014`

```dockerfile
```

-	Layers:
	-	`sha256:cb127fa803292603ecec4753671bcc7e53dbd0a5d8e70ee0758f7acdda1a76df`  
		Last Modified: Thu, 03 Oct 2024 16:58:01 GMT  
		Size: 1.9 MB (1876703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff4de3a63959d91b1266a509f09751d050f2590279f1d4ef748191400f7427d`  
		Last Modified: Thu, 03 Oct 2024 16:58:01 GMT  
		Size: 28.9 KB (28898 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-7.1.0.7_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:2f6f4aa34505ae86e8f56b78e9ae72c24995ad8509f4d5e004b29193e94f0500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74593626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd391abfe8dd4c834b0ef23b989770c5fef95312ff490ee2a70dcf6dbfbd4e04`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Thu, 03 Oct 2024 05:39:44 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.7 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_EDITION=community
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.7/aerospike-server-community_7.1.0.7_tools-11.0.2_ubuntu22.04_x86_64.tgz
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_SHA_X86_64=1c3eb9d2297aaa6d1175aa568cfd5ef671386e492496aa07d294452a188071c8
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.7/aerospike-server-community_7.1.0.7_tools-11.0.2_ubuntu22.04_aarch64.tgz
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_SHA_AARCH64=a4b9d959505469e40c4c14b1302138af05140d340024c41f67cf562536d356fa
# Thu, 03 Oct 2024 05:39:44 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 03 Oct 2024 05:39:44 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.7/aerospike-server-community_7.1.0.7_tools-11.0.2_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=1c3eb9d2297aaa6d1175aa568cfd5ef671386e492496aa07d294452a188071c8 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.7/aerospike-server-community_7.1.0.7_tools-11.0.2_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=a4b9d959505469e40c4c14b1302138af05140d340024c41f67cf562536d356fa
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 03 Oct 2024 05:39:44 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 03 Oct 2024 05:39:44 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 03 Oct 2024 05:39:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Oct 2024 05:39:44 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 03 Oct 2024 05:39:44 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04e2ebbd1cd505644dd1ebeff63803a9e37afe77c33226f80da6a2d875fd74b`  
		Last Modified: Thu, 03 Oct 2024 16:59:17 GMT  
		Size: 47.2 MB (47233006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4169ebba7eb3c59003b63789a9de21d06642668eeb53bbe530cb6295b01797d`  
		Last Modified: Thu, 03 Oct 2024 16:59:15 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c51065dbfd3c7fc47015a6099f3de451637ede7e6376839201bfeb3a479e02`  
		Last Modified: Thu, 03 Oct 2024 16:59:15 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-7.1.0.7_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:9a0e37bb0f46eec8764591480446fd0055dc278f777759f207f0ba359368b7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1907034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f2a895d0bedbbce6f94ae1692a4e0aef013815009b575004aadddafd9ec132`

```dockerfile
```

-	Layers:
	-	`sha256:4a312a66f5bf484bf08555782bd3779158d8d03052621d59277117fdfe7c35e2`  
		Last Modified: Thu, 03 Oct 2024 16:59:16 GMT  
		Size: 1.9 MB (1878062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcb8c0de61abd250ffb9e44d16e7ec0c2a053c8631df013e7c44e9246408077b`  
		Last Modified: Thu, 03 Oct 2024 16:59:15 GMT  
		Size: 29.0 KB (28972 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ee-7.1.0.7`

```console
$ docker pull aerospike@sha256:083ff1f5c61fa68a7ab0db6787d929d57be93509c5569a4f4291c95f8bd2af70
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-7.1.0.7` - linux; amd64

```console
$ docker pull aerospike@sha256:3aa30f11f04a9577624a58546a5f15f35d04d174873bb44b786d9e97635c8e8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80670246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b110ab017963af00027faba044c7a82a3547758841a6271ebdb41ef895ce1997`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Thu, 03 Oct 2024 05:39:44 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.7 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_EDITION=enterprise
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.7/aerospike-server-enterprise_7.1.0.7_tools-11.0.2_ubuntu22.04_x86_64.tgz
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_SHA_X86_64=8056019e033377ad1302739781bf941396f478d02f685f2c457957e4f02b7fb3
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.7/aerospike-server-enterprise_7.1.0.7_tools-11.0.2_ubuntu22.04_aarch64.tgz
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_SHA_AARCH64=45d22a934aae73498227c413943abb381ee2347f31338a26480f336322d8bac9
# Thu, 03 Oct 2024 05:39:44 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 03 Oct 2024 05:39:44 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.7/aerospike-server-enterprise_7.1.0.7_tools-11.0.2_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=8056019e033377ad1302739781bf941396f478d02f685f2c457957e4f02b7fb3 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.7/aerospike-server-enterprise_7.1.0.7_tools-11.0.2_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=45d22a934aae73498227c413943abb381ee2347f31338a26480f336322d8bac9
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 03 Oct 2024 05:39:44 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 03 Oct 2024 05:39:44 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 03 Oct 2024 05:39:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Oct 2024 05:39:44 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 03 Oct 2024 05:39:44 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa76d91564706361a392a3443c37f92f2743b1c5f5fe7bc20a4e1b502504ebc`  
		Last Modified: Thu, 03 Oct 2024 16:58:16 GMT  
		Size: 51.1 MB (51132269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794c738f6c4296fa3e6a683726d572864827d9b81d217de04a47fa86bfbc010e`  
		Last Modified: Thu, 03 Oct 2024 16:58:14 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8f87d8da07f9cab58b834951a2045d64feacd1bbc53f71fe835d2d56e62aae`  
		Last Modified: Thu, 03 Oct 2024 16:58:14 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.1.0.7` - unknown; unknown

```console
$ docker pull aerospike@sha256:a14e2a8adb8d38aa2304438b186326b15d8dd9b876d73e90978342537eeacb35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1970034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34665d60768b3e7343e1d190b003272381e8e3e294ff71072f2c5fa6429f74a9`

```dockerfile
```

-	Layers:
	-	`sha256:65a1e9cde167c61300446ce08c713f6bed1a2e8d7351559827cd47c6eab116d2`  
		Last Modified: Thu, 03 Oct 2024 16:58:15 GMT  
		Size: 1.9 MB (1941120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55655011cae7c1911bad873d3d067be37fb1253d3f018ed1909209f2421ef215`  
		Last Modified: Thu, 03 Oct 2024 16:58:15 GMT  
		Size: 28.9 KB (28914 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-7.1.0.7` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:37ae675731507fb0bc99be401981f4ecfe5cc8e3ddad44aea19c0ae3dedcb692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77863758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0de7839ed0433ed3f25b313f1ee6a9f259bdec16c3fe4881321cb976d81929`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Thu, 03 Oct 2024 05:39:44 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.7 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_EDITION=enterprise
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.7/aerospike-server-enterprise_7.1.0.7_tools-11.0.2_ubuntu22.04_x86_64.tgz
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_SHA_X86_64=8056019e033377ad1302739781bf941396f478d02f685f2c457957e4f02b7fb3
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.7/aerospike-server-enterprise_7.1.0.7_tools-11.0.2_ubuntu22.04_aarch64.tgz
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_SHA_AARCH64=45d22a934aae73498227c413943abb381ee2347f31338a26480f336322d8bac9
# Thu, 03 Oct 2024 05:39:44 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 03 Oct 2024 05:39:44 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.7/aerospike-server-enterprise_7.1.0.7_tools-11.0.2_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=8056019e033377ad1302739781bf941396f478d02f685f2c457957e4f02b7fb3 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.7/aerospike-server-enterprise_7.1.0.7_tools-11.0.2_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=45d22a934aae73498227c413943abb381ee2347f31338a26480f336322d8bac9
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 03 Oct 2024 05:39:44 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 03 Oct 2024 05:39:44 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 03 Oct 2024 05:39:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Oct 2024 05:39:44 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 03 Oct 2024 05:39:44 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83392ab287cc78e279476cf022450cfdc9d2b7d1b1dd6ef280e4616f61cad362`  
		Last Modified: Thu, 03 Oct 2024 16:58:30 GMT  
		Size: 50.5 MB (50503140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcecb5c3881e1c871a17f65211cc6f9f103fe9cc2c473c27637491f99ff65d`  
		Last Modified: Thu, 03 Oct 2024 16:58:28 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899c486719c5c85d77b77efb63242e1828d8b53a3e59a33d89f304ff40576665`  
		Last Modified: Thu, 03 Oct 2024 16:58:28 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.1.0.7` - unknown; unknown

```console
$ docker pull aerospike@sha256:cd3f467289d566bc2a7d00114163fffcc33d7af7f2bd068b123237f117310261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1971479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d253ced343444c5e17f135853c140d7b5d41388a2e1f1a62613e7ef7281a75c`

```dockerfile
```

-	Layers:
	-	`sha256:31afa140e1655f58bfc5fceb386bbbd68bc78481fbe0f39f1e52491a6dfa7dbc`  
		Last Modified: Thu, 03 Oct 2024 16:58:28 GMT  
		Size: 1.9 MB (1942491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:824e3775f4d94472110cf3322a4cfc48227e40edd90019a7205d6e951a7356b5`  
		Last Modified: Thu, 03 Oct 2024 16:58:28 GMT  
		Size: 29.0 KB (28988 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ee-7.1.0.7_1`

```console
$ docker pull aerospike@sha256:083ff1f5c61fa68a7ab0db6787d929d57be93509c5569a4f4291c95f8bd2af70
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-7.1.0.7_1` - linux; amd64

```console
$ docker pull aerospike@sha256:3aa30f11f04a9577624a58546a5f15f35d04d174873bb44b786d9e97635c8e8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80670246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b110ab017963af00027faba044c7a82a3547758841a6271ebdb41ef895ce1997`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Thu, 03 Oct 2024 05:39:44 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.7 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_EDITION=enterprise
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.7/aerospike-server-enterprise_7.1.0.7_tools-11.0.2_ubuntu22.04_x86_64.tgz
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_SHA_X86_64=8056019e033377ad1302739781bf941396f478d02f685f2c457957e4f02b7fb3
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.7/aerospike-server-enterprise_7.1.0.7_tools-11.0.2_ubuntu22.04_aarch64.tgz
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_SHA_AARCH64=45d22a934aae73498227c413943abb381ee2347f31338a26480f336322d8bac9
# Thu, 03 Oct 2024 05:39:44 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 03 Oct 2024 05:39:44 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.7/aerospike-server-enterprise_7.1.0.7_tools-11.0.2_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=8056019e033377ad1302739781bf941396f478d02f685f2c457957e4f02b7fb3 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.7/aerospike-server-enterprise_7.1.0.7_tools-11.0.2_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=45d22a934aae73498227c413943abb381ee2347f31338a26480f336322d8bac9
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 03 Oct 2024 05:39:44 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 03 Oct 2024 05:39:44 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 03 Oct 2024 05:39:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Oct 2024 05:39:44 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 03 Oct 2024 05:39:44 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa76d91564706361a392a3443c37f92f2743b1c5f5fe7bc20a4e1b502504ebc`  
		Last Modified: Thu, 03 Oct 2024 16:58:16 GMT  
		Size: 51.1 MB (51132269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794c738f6c4296fa3e6a683726d572864827d9b81d217de04a47fa86bfbc010e`  
		Last Modified: Thu, 03 Oct 2024 16:58:14 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8f87d8da07f9cab58b834951a2045d64feacd1bbc53f71fe835d2d56e62aae`  
		Last Modified: Thu, 03 Oct 2024 16:58:14 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.1.0.7_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:a14e2a8adb8d38aa2304438b186326b15d8dd9b876d73e90978342537eeacb35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1970034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34665d60768b3e7343e1d190b003272381e8e3e294ff71072f2c5fa6429f74a9`

```dockerfile
```

-	Layers:
	-	`sha256:65a1e9cde167c61300446ce08c713f6bed1a2e8d7351559827cd47c6eab116d2`  
		Last Modified: Thu, 03 Oct 2024 16:58:15 GMT  
		Size: 1.9 MB (1941120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55655011cae7c1911bad873d3d067be37fb1253d3f018ed1909209f2421ef215`  
		Last Modified: Thu, 03 Oct 2024 16:58:15 GMT  
		Size: 28.9 KB (28914 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-7.1.0.7_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:37ae675731507fb0bc99be401981f4ecfe5cc8e3ddad44aea19c0ae3dedcb692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77863758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0de7839ed0433ed3f25b313f1ee6a9f259bdec16c3fe4881321cb976d81929`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Thu, 03 Oct 2024 05:39:44 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.7 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_EDITION=enterprise
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.7/aerospike-server-enterprise_7.1.0.7_tools-11.0.2_ubuntu22.04_x86_64.tgz
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_SHA_X86_64=8056019e033377ad1302739781bf941396f478d02f685f2c457957e4f02b7fb3
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.7/aerospike-server-enterprise_7.1.0.7_tools-11.0.2_ubuntu22.04_aarch64.tgz
# Thu, 03 Oct 2024 05:39:44 GMT
ARG AEROSPIKE_SHA_AARCH64=45d22a934aae73498227c413943abb381ee2347f31338a26480f336322d8bac9
# Thu, 03 Oct 2024 05:39:44 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 03 Oct 2024 05:39:44 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.7/aerospike-server-enterprise_7.1.0.7_tools-11.0.2_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=8056019e033377ad1302739781bf941396f478d02f685f2c457957e4f02b7fb3 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.7/aerospike-server-enterprise_7.1.0.7_tools-11.0.2_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=45d22a934aae73498227c413943abb381ee2347f31338a26480f336322d8bac9
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 03 Oct 2024 05:39:44 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 03 Oct 2024 05:39:44 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 03 Oct 2024 05:39:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Oct 2024 05:39:44 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 03 Oct 2024 05:39:44 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83392ab287cc78e279476cf022450cfdc9d2b7d1b1dd6ef280e4616f61cad362`  
		Last Modified: Thu, 03 Oct 2024 16:58:30 GMT  
		Size: 50.5 MB (50503140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcecb5c3881e1c871a17f65211cc6f9f103fe9cc2c473c27637491f99ff65d`  
		Last Modified: Thu, 03 Oct 2024 16:58:28 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899c486719c5c85d77b77efb63242e1828d8b53a3e59a33d89f304ff40576665`  
		Last Modified: Thu, 03 Oct 2024 16:58:28 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.1.0.7_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:cd3f467289d566bc2a7d00114163fffcc33d7af7f2bd068b123237f117310261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1971479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d253ced343444c5e17f135853c140d7b5d41388a2e1f1a62613e7ef7281a75c`

```dockerfile
```

-	Layers:
	-	`sha256:31afa140e1655f58bfc5fceb386bbbd68bc78481fbe0f39f1e52491a6dfa7dbc`  
		Last Modified: Thu, 03 Oct 2024 16:58:28 GMT  
		Size: 1.9 MB (1942491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:824e3775f4d94472110cf3322a4cfc48227e40edd90019a7205d6e951a7356b5`  
		Last Modified: Thu, 03 Oct 2024 16:58:28 GMT  
		Size: 29.0 KB (28988 bytes)  
		MIME: application/vnd.in-toto+json
