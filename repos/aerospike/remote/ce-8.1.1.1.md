## `aerospike:ce-8.1.1.1`

```console
$ docker pull aerospike@sha256:293979669c4ae3283db2d729e97acb998d3260b69c97c062e8ce22cdb3862a9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.1.1.1` - linux; amd64

```console
$ docker pull aerospike@sha256:d21115aecee47996a38c9296475b62abdc3e0036ff5b87f5ed796725b8a39aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84113529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528457d021e92051f5852004bddacd68961f038f645bc1e079be64280b63b46d`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:43:34 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.1.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 07 Apr 2026 01:43:34 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 07 Apr 2026 01:43:34 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 07 Apr 2026 01:43:34 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.1/aerospike-server-community_8.1.1.1_tools-12.1.1_ubuntu24.04_x86_64.tgz
# Tue, 07 Apr 2026 01:43:34 GMT
ARG AEROSPIKE_SHA_X86_64=bbbbb10b08d67391058da8c88df06da027b25f7bd4bf44959a14a78c392d10a7
# Tue, 07 Apr 2026 01:43:34 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.1/aerospike-server-community_8.1.1.1_tools-12.1.1_ubuntu24.04_aarch64.tgz
# Tue, 07 Apr 2026 01:43:34 GMT
ARG AEROSPIKE_SHA_AARCH64=5129d72c4dceb753a95f49a2cfc29788dd55acfb140ff4cee7431824301b13c0
# Tue, 07 Apr 2026 01:43:34 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 07 Apr 2026 01:43:34 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.1/aerospike-server-community_8.1.1.1_tools-12.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=bbbbb10b08d67391058da8c88df06da027b25f7bd4bf44959a14a78c392d10a7 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.1/aerospike-server-community_8.1.1.1_tools-12.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=5129d72c4dceb753a95f49a2cfc29788dd55acfb140ff4cee7431824301b13c0
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 07 Apr 2026 01:43:34 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 07 Apr 2026 01:43:34 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 07 Apr 2026 01:43:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:43:34 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 07 Apr 2026 01:43:34 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec26bc99182d863ed90de79f9e30916e97d3fcc263dab822e75bb8dca38d3655`  
		Last Modified: Tue, 07 Apr 2026 01:43:47 GMT  
		Size: 54.4 MB (54377772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5885c74d529fd11ee5d92b5b16561d550d4a0b898ee6e7cbde9c2d58481babde`  
		Last Modified: Tue, 07 Apr 2026 01:43:45 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9f44eb6677d00699402c46857a4219d9c37aa8c36bbcfb93f5605b8d4a2744`  
		Last Modified: Tue, 07 Apr 2026 01:43:46 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.1.1` - unknown; unknown

```console
$ docker pull aerospike@sha256:67119264de7dad83df66967672f85399c878a53adbde9d98074796d791101b9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35119a160c00fb4385933533e07242f97a3de772c271511e2b6dafd8aea4c6ff`

```dockerfile
```

-	Layers:
	-	`sha256:0c39b7f2d74864ec3139b6bda7e3e5a754791a8a71ef99ba142bc177c327ce52`  
		Last Modified: Tue, 07 Apr 2026 01:43:45 GMT  
		Size: 2.2 MB (2180960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15fc424d2f2cdca989829abed51832d0832d1bad181c1d774041130269ceb3d0`  
		Last Modified: Tue, 07 Apr 2026 01:43:45 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.1.1.1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:9ba3c749be143d33cd01c9b1c694548a48c4868ddefccababaf47351fe549de0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82064339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28baea9a5cf88ee9694a8cae82c281672531f057662b87b042d2617e490b7486`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:46:38 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.1.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 07 Apr 2026 01:46:38 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 07 Apr 2026 01:46:38 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 07 Apr 2026 01:46:38 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.1/aerospike-server-community_8.1.1.1_tools-12.1.1_ubuntu24.04_x86_64.tgz
# Tue, 07 Apr 2026 01:46:38 GMT
ARG AEROSPIKE_SHA_X86_64=bbbbb10b08d67391058da8c88df06da027b25f7bd4bf44959a14a78c392d10a7
# Tue, 07 Apr 2026 01:46:38 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.1/aerospike-server-community_8.1.1.1_tools-12.1.1_ubuntu24.04_aarch64.tgz
# Tue, 07 Apr 2026 01:46:38 GMT
ARG AEROSPIKE_SHA_AARCH64=5129d72c4dceb753a95f49a2cfc29788dd55acfb140ff4cee7431824301b13c0
# Tue, 07 Apr 2026 01:46:38 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 07 Apr 2026 01:46:38 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.1/aerospike-server-community_8.1.1.1_tools-12.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=bbbbb10b08d67391058da8c88df06da027b25f7bd4bf44959a14a78c392d10a7 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.1/aerospike-server-community_8.1.1.1_tools-12.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=5129d72c4dceb753a95f49a2cfc29788dd55acfb140ff4cee7431824301b13c0
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 07 Apr 2026 01:46:38 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 07 Apr 2026 01:46:38 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 07 Apr 2026 01:46:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:46:38 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 07 Apr 2026 01:46:38 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa794c3b5a47cfd067ae1d15e6e4262df0e9ae10df00903a992713b3e76a010e`  
		Last Modified: Tue, 07 Apr 2026 01:46:51 GMT  
		Size: 53.2 MB (53187966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f61564d07977988c24dbe2f18bae85edf749a7e4d4077660fb223b777d16391`  
		Last Modified: Tue, 07 Apr 2026 01:46:50 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abeebb831297a313082c16e2fb7f5e310880471161ae1685c07113a529b82198`  
		Last Modified: Tue, 07 Apr 2026 01:46:50 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.1.1` - unknown; unknown

```console
$ docker pull aerospike@sha256:4865a56874d0a78182127b4b6ab608080eeda6ece13d829d52be90b53a41f54a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d70b321a1e64efc6fc19d54db174147f1956ce7cab1d1509ff1c456e146cb24`

```dockerfile
```

-	Layers:
	-	`sha256:0f1a4806fd57bec25f76f617ca7b6857245953c6d126ff618006cb2cadf89e9e`  
		Last Modified: Tue, 07 Apr 2026 01:46:50 GMT  
		Size: 2.2 MB (2183240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cf9d020b6eb2b65dc4dbd3bc5d7dfe73a20fd2829861a59658780d0e215a3e2`  
		Last Modified: Tue, 07 Apr 2026 01:46:50 GMT  
		Size: 29.0 KB (29049 bytes)  
		MIME: application/vnd.in-toto+json
