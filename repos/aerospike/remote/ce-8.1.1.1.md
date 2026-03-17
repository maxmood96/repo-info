## `aerospike:ce-8.1.1.1`

```console
$ docker pull aerospike@sha256:8a0604e965e0cdeda1867cc9c0ce5927326a3ba8ce4be1a165d0e2a0a03f49fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.1.1.1` - linux; amd64

```console
$ docker pull aerospike@sha256:e2b30dbf03e3af985f60e442f985c0735b256622590a08c646bb4b3efe4ed7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84111938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1628973fb87a08d43f8973db5486fdc54b0c4dd9403727eba0593ad9a2a0b829`
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
# Tue, 17 Mar 2026 01:15:21 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.1.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 17 Mar 2026 01:15:21 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 17 Mar 2026 01:15:21 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 17 Mar 2026 01:15:21 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.1/aerospike-server-community_8.1.1.1_tools-12.1.1_ubuntu24.04_x86_64.tgz
# Tue, 17 Mar 2026 01:15:21 GMT
ARG AEROSPIKE_SHA_X86_64=bbbbb10b08d67391058da8c88df06da027b25f7bd4bf44959a14a78c392d10a7
# Tue, 17 Mar 2026 01:15:21 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.1/aerospike-server-community_8.1.1.1_tools-12.1.1_ubuntu24.04_aarch64.tgz
# Tue, 17 Mar 2026 01:15:21 GMT
ARG AEROSPIKE_SHA_AARCH64=5129d72c4dceb753a95f49a2cfc29788dd55acfb140ff4cee7431824301b13c0
# Tue, 17 Mar 2026 01:15:21 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 17 Mar 2026 01:15:21 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.1/aerospike-server-community_8.1.1.1_tools-12.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=bbbbb10b08d67391058da8c88df06da027b25f7bd4bf44959a14a78c392d10a7 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.1/aerospike-server-community_8.1.1.1_tools-12.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=5129d72c4dceb753a95f49a2cfc29788dd55acfb140ff4cee7431824301b13c0
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 17 Mar 2026 01:15:21 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 17 Mar 2026 01:15:21 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 17 Mar 2026 01:15:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:21 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 17 Mar 2026 01:15:21 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5477d3f57272d5508621d0173f21240b11f406397d4458a81c85ca13f0a4dd8`  
		Last Modified: Tue, 17 Mar 2026 01:15:34 GMT  
		Size: 54.4 MB (54377646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7337677f585cd2e9e65fae61b121a78c1d88ed10710f0c1ad79a3554cc5d087f`  
		Last Modified: Tue, 17 Mar 2026 01:15:32 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5135ba23835af1eca8ab8c8ce07389da56c4d42e27674437a0c7862633ab0540`  
		Last Modified: Tue, 17 Mar 2026 01:15:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.1.1` - unknown; unknown

```console
$ docker pull aerospike@sha256:11d59cd8b783d6abf56af6167b03a5ccace2c8800c99ea712eec0d5b074c2411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217b3de8e041194068616a3453999900eab236bca610dd5128136df3dd151545`

```dockerfile
```

-	Layers:
	-	`sha256:400cf524079e7ffc05a8b4d65a85ab21296a937ec71c41fd0d798411e9d288a8`  
		Last Modified: Tue, 17 Mar 2026 01:15:33 GMT  
		Size: 2.2 MB (2180956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7149910d56d958fe098523b5d33d6e55d3f1e0a932943b23aa0c8a5942df5912`  
		Last Modified: Tue, 17 Mar 2026 01:15:33 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.1.1.1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:c5d0bb463563a5b8c8f7950f01f064e331991118db7738e4f610401a9a595dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82059766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f75fa1874cddfc02a799d100e8d0c485c31572752270e1b3466050bed20f58`
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
# Tue, 17 Mar 2026 01:15:21 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.1.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 17 Mar 2026 01:15:21 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 17 Mar 2026 01:15:21 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 17 Mar 2026 01:15:21 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.1/aerospike-server-community_8.1.1.1_tools-12.1.1_ubuntu24.04_x86_64.tgz
# Tue, 17 Mar 2026 01:15:21 GMT
ARG AEROSPIKE_SHA_X86_64=bbbbb10b08d67391058da8c88df06da027b25f7bd4bf44959a14a78c392d10a7
# Tue, 17 Mar 2026 01:15:21 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.1/aerospike-server-community_8.1.1.1_tools-12.1.1_ubuntu24.04_aarch64.tgz
# Tue, 17 Mar 2026 01:15:21 GMT
ARG AEROSPIKE_SHA_AARCH64=5129d72c4dceb753a95f49a2cfc29788dd55acfb140ff4cee7431824301b13c0
# Tue, 17 Mar 2026 01:15:21 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 17 Mar 2026 01:15:21 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.1/aerospike-server-community_8.1.1.1_tools-12.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=bbbbb10b08d67391058da8c88df06da027b25f7bd4bf44959a14a78c392d10a7 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.1/aerospike-server-community_8.1.1.1_tools-12.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=5129d72c4dceb753a95f49a2cfc29788dd55acfb140ff4cee7431824301b13c0
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 17 Mar 2026 01:15:21 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 17 Mar 2026 01:15:21 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 17 Mar 2026 01:15:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:21 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 17 Mar 2026 01:15:21 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3927651c49b37e757fc252bd188b8f78dd5769902712a11ae958f368e899e7`  
		Last Modified: Tue, 17 Mar 2026 01:15:34 GMT  
		Size: 53.2 MB (53187757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0a91899b461dd7f1eecb9eac6eb011c5bcf421d0d96b95fd1de852b07938ab`  
		Last Modified: Tue, 17 Mar 2026 01:15:32 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669dec40e9fa9a80149a9fa6194e6bfe34c5a04a69a4139fa9f287576805438c`  
		Last Modified: Tue, 17 Mar 2026 01:15:32 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.1.1` - unknown; unknown

```console
$ docker pull aerospike@sha256:0bee6ef1f12df1d7584eb13666968b45bff1ec9f29a1e436a9b1545fcb166bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bc6dbc40cfea49ee4fd280e769b5d34f9268a35e9a3e766dff3d63f02cec7d`

```dockerfile
```

-	Layers:
	-	`sha256:2806e7cea1e07506af0e6c8f6ec8d3fd65cf6818e2b163932b2b4a6567cbf0ff`  
		Last Modified: Tue, 17 Mar 2026 01:15:32 GMT  
		Size: 2.2 MB (2183236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b92bab2f9391811912ed657fde72c6a2bd26b661b56288a807b8443284c9f047`  
		Last Modified: Tue, 17 Mar 2026 01:15:32 GMT  
		Size: 29.0 KB (29049 bytes)  
		MIME: application/vnd.in-toto+json
