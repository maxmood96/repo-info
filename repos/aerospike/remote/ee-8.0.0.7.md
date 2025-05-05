## `aerospike:ee-8.0.0.7`

```console
$ docker pull aerospike@sha256:52c0296f0ac3191821a992dec217a3e4d555f730d55e998a9ff1fadee68f28cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.0.0.7` - linux; amd64

```console
$ docker pull aerospike@sha256:a36b194259a1fe3061320306c9bfa497e8fa9d88293391dff9f6527e91b8678f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.3 MB (85346957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248c76d5e226e95f33c6cbdefbd4a826feb3b7e46990daad7ed82c8fcad314de`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Fri, 25 Apr 2025 21:09:11 GMT
ARG RELEASE
# Fri, 25 Apr 2025 21:09:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 25 Apr 2025 21:09:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 25 Apr 2025 21:09:11 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 25 Apr 2025 21:09:11 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Fri, 25 Apr 2025 21:09:11 GMT
CMD ["/bin/bash"]
# Fri, 25 Apr 2025 21:09:11 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.7 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_EDITION=enterprise
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.7/aerospike-server-enterprise_8.0.0.7_tools-11.2.2_ubuntu24.04_x86_64.tgz
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_SHA_X86_64=3c694546fe7ae6e41f6d62a26e6d134e35fb9de1b955683e60b9970b778c3e63
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.7/aerospike-server-enterprise_8.0.0.7_tools-11.2.2_ubuntu24.04_aarch64.tgz
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_SHA_AARCH64=6403cc7bc2941ff3958353e602b69dd16c9381e39c9e5d3262087818c019fc20
# Fri, 25 Apr 2025 21:09:11 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 25 Apr 2025 21:09:11 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.7/aerospike-server-enterprise_8.0.0.7_tools-11.2.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=3c694546fe7ae6e41f6d62a26e6d134e35fb9de1b955683e60b9970b778c3e63 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.7/aerospike-server-enterprise_8.0.0.7_tools-11.2.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=6403cc7bc2941ff3958353e602b69dd16c9381e39c9e5d3262087818c019fc20
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 25 Apr 2025 21:09:11 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 25 Apr 2025 21:09:11 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 25 Apr 2025 21:09:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 25 Apr 2025 21:09:11 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 25 Apr 2025 21:09:11 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cb712a19ff913e23b3f93b98338ed86afef75447859e782df12bc161954c42`  
		Last Modified: Mon, 05 May 2025 16:34:46 GMT  
		Size: 55.6 MB (55627126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52710de3c4afa684b303ad9fa5586f2ebd3edc5b8cefbdd2cb79d8d9e71edc23`  
		Last Modified: Mon, 05 May 2025 16:34:45 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24e96c0902b5e3857a6c1343297f88a95d9e2ce70e931161e4d89b13c94b665`  
		Last Modified: Mon, 05 May 2025 16:34:45 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.0.0.7` - unknown; unknown

```console
$ docker pull aerospike@sha256:6099d2c67e06feeb7a65c6fbda6e70fad573e991e1387d88da08782325d2ff7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1987077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8907b77031129552b5442fc6e043c120ef9f6c2b1e547db7fd3bfdc3cd9588a0`

```dockerfile
```

-	Layers:
	-	`sha256:de600e85533d7526e42ae86ce71fd48915ac57595632f9318e90fe6e7b08e0ff`  
		Last Modified: Mon, 05 May 2025 16:34:45 GMT  
		Size: 2.0 MB (1957914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43ea951d3a1947ef9b3a86b1ac6d8772e5fa46f174952202dba02c6d13082e3d`  
		Last Modified: Mon, 05 May 2025 16:34:45 GMT  
		Size: 29.2 KB (29163 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.0.0.7` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:39dc6b90f14ab025d13e74ff14294ab0689de7e8178e8eab657f67ad4584a3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83924665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4b992a94ca1161f4e3996666a707469e2a5920222024ddf701de01d803ec3a`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Fri, 25 Apr 2025 21:09:11 GMT
ARG RELEASE
# Fri, 25 Apr 2025 21:09:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 25 Apr 2025 21:09:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 25 Apr 2025 21:09:11 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 25 Apr 2025 21:09:11 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Fri, 25 Apr 2025 21:09:11 GMT
CMD ["/bin/bash"]
# Fri, 25 Apr 2025 21:09:11 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.7 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_EDITION=enterprise
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.7/aerospike-server-enterprise_8.0.0.7_tools-11.2.2_ubuntu24.04_x86_64.tgz
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_SHA_X86_64=3c694546fe7ae6e41f6d62a26e6d134e35fb9de1b955683e60b9970b778c3e63
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.7/aerospike-server-enterprise_8.0.0.7_tools-11.2.2_ubuntu24.04_aarch64.tgz
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_SHA_AARCH64=6403cc7bc2941ff3958353e602b69dd16c9381e39c9e5d3262087818c019fc20
# Fri, 25 Apr 2025 21:09:11 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 25 Apr 2025 21:09:11 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.7/aerospike-server-enterprise_8.0.0.7_tools-11.2.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=3c694546fe7ae6e41f6d62a26e6d134e35fb9de1b955683e60b9970b778c3e63 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.7/aerospike-server-enterprise_8.0.0.7_tools-11.2.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=6403cc7bc2941ff3958353e602b69dd16c9381e39c9e5d3262087818c019fc20
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 25 Apr 2025 21:09:11 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 25 Apr 2025 21:09:11 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 25 Apr 2025 21:09:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 25 Apr 2025 21:09:11 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 25 Apr 2025 21:09:11 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78792ba2ad90ce84c59f020f445c81502c12dd93b67e33307a798f10ce00875d`  
		Last Modified: Mon, 05 May 2025 16:34:33 GMT  
		Size: 55.1 MB (55075483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73960c3af2460fc62b78647c4e3eac917a9c275dacdef8774f433d1021d4c73`  
		Last Modified: Mon, 05 May 2025 16:34:30 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4cbb94e1dd975f8ad3f6a1df8467ed76aaeb951b9cb4dbfaa4d9d315e1ce97`  
		Last Modified: Mon, 05 May 2025 16:34:30 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.0.0.7` - unknown; unknown

```console
$ docker pull aerospike@sha256:57c9debb460d98a9427d775b775bc655d417645e6c714637ab48480a93ad8643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1989437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152b76b948bad955f71dd11e01273ceba8ac733a8bf5c1330961a91977764d7d`

```dockerfile
```

-	Layers:
	-	`sha256:af32a6fb7506d59c14faea78f16cf504629a3b88b8b62732d2a4de5145888816`  
		Last Modified: Mon, 05 May 2025 16:34:30 GMT  
		Size: 2.0 MB (1960194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ce7a8e4a30135def53c64c1cb486842bbd007a99b9f0deb6337d8d80e6a4e53`  
		Last Modified: Mon, 05 May 2025 16:34:30 GMT  
		Size: 29.2 KB (29243 bytes)  
		MIME: application/vnd.in-toto+json
