## `aerospike:ee-8.0.0.8`

```console
$ docker pull aerospike@sha256:59ce06d7a36d585f1509a344dab061f1ca7c404d1613c6b9008747af470f77a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.0.0.8` - linux; amd64

```console
$ docker pull aerospike@sha256:ed0a0883ba960867faeffb3fda103a472d7ffabe52e6c1bf48b428369d335ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86234554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed4e1592f3c4172d07c82d19ef8460d60dc368afa2fa1281cf7e7ec78ef4015`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 27 May 2025 23:31:17 GMT
ARG RELEASE
# Tue, 27 May 2025 23:31:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 May 2025 23:31:17 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Tue, 27 May 2025 23:31:17 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.8 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 27 May 2025 23:31:17 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.8/aerospike-server-enterprise_8.0.0.8_tools-11.2.2_ubuntu24.04_x86_64.tgz
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_SHA_X86_64=4ce9c840dc4724b124ddb983d58856ddd2aea96584ca5498387be2e31aa1f892
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.8/aerospike-server-enterprise_8.0.0.8_tools-11.2.2_ubuntu24.04_aarch64.tgz
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_SHA_AARCH64=01abeedb92895a55ef12ae5275c7370e6d1b6bdb6d1ee53e3e6318c381e8778e
# Tue, 27 May 2025 23:31:17 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 27 May 2025 23:31:17 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.8/aerospike-server-enterprise_8.0.0.8_tools-11.2.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=4ce9c840dc4724b124ddb983d58856ddd2aea96584ca5498387be2e31aa1f892 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.8/aerospike-server-enterprise_8.0.0.8_tools-11.2.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=01abeedb92895a55ef12ae5275c7370e6d1b6bdb6d1ee53e3e6318c381e8778e
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 27 May 2025 23:31:17 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 27 May 2025 23:31:17 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 27 May 2025 23:31:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 27 May 2025 23:31:17 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 27 May 2025 23:31:17 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Thu, 29 May 2025 06:11:31 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4402903650abc38a4d826d56373e53493923e4c9f47ff24af399079aae38235`  
		Last Modified: Tue, 03 Jun 2025 04:15:50 GMT  
		Size: 56.5 MB (56516913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6b4fcd184cd10269322dd080f013e67e75ee1cf12c86b797f26485881056f8`  
		Last Modified: Tue, 03 Jun 2025 04:15:48 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2aa6acd992abd76d0c505c8fb96e111dc5c51bb10dac0edb2066ae24d8e092e`  
		Last Modified: Tue, 03 Jun 2025 04:15:49 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.0.0.8` - unknown; unknown

```console
$ docker pull aerospike@sha256:55c4532c717d3df68b2e9cdafc0032879aed3a6ec74116913919b16be2b4ff52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2116167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71eb0274500e0d5b3de54de9f9c345da94d50636a0de98a925ee459018200eb8`

```dockerfile
```

-	Layers:
	-	`sha256:4429fd4fa4600ef632af74f44f013e5486f9cd6c24cd00619597f453f7ff6bca`  
		Last Modified: Tue, 03 Jun 2025 04:15:49 GMT  
		Size: 2.1 MB (2087139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d59c63fb8700e24e094aa56e46c5afac4977b67a97f101b71725ba1642ffe02d`  
		Last Modified: Tue, 03 Jun 2025 04:15:48 GMT  
		Size: 29.0 KB (29028 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.0.0.8` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:ee92576f2ae51864835fb7bb5ffe415727b2c3bea11c738698bf7ff385e4e675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84802579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de907a3cec4d35fe06b3789680ff8c90c16e262980e3da6f548d23ec4a0ec9b`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 27 May 2025 23:31:17 GMT
ARG RELEASE
# Tue, 27 May 2025 23:31:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 May 2025 23:31:17 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Tue, 27 May 2025 23:31:17 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.8 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 27 May 2025 23:31:17 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.8/aerospike-server-enterprise_8.0.0.8_tools-11.2.2_ubuntu24.04_x86_64.tgz
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_SHA_X86_64=4ce9c840dc4724b124ddb983d58856ddd2aea96584ca5498387be2e31aa1f892
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.8/aerospike-server-enterprise_8.0.0.8_tools-11.2.2_ubuntu24.04_aarch64.tgz
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_SHA_AARCH64=01abeedb92895a55ef12ae5275c7370e6d1b6bdb6d1ee53e3e6318c381e8778e
# Tue, 27 May 2025 23:31:17 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 27 May 2025 23:31:17 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.8/aerospike-server-enterprise_8.0.0.8_tools-11.2.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=4ce9c840dc4724b124ddb983d58856ddd2aea96584ca5498387be2e31aa1f892 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.8/aerospike-server-enterprise_8.0.0.8_tools-11.2.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=01abeedb92895a55ef12ae5275c7370e6d1b6bdb6d1ee53e3e6318c381e8778e
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 27 May 2025 23:31:17 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 27 May 2025 23:31:17 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 27 May 2025 23:31:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 27 May 2025 23:31:17 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 27 May 2025 23:31:17 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Thu, 29 May 2025 06:11:37 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01138690d21f18c98ce2aad73f3ad332e5698b446d532a05b3d9cb077f7331a1`  
		Last Modified: Tue, 03 Jun 2025 04:15:40 GMT  
		Size: 55.9 MB (55948378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d41c1c249a9eed79b71e2ab527ad9b7cd405ad6075d06494d0a9b7b8544379d`  
		Last Modified: Tue, 03 Jun 2025 04:15:38 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58059762fc6a9fbf247f3c02f8f471a96c25389fbe550983cd635b74707680c7`  
		Last Modified: Tue, 03 Jun 2025 04:15:38 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.0.0.8` - unknown; unknown

```console
$ docker pull aerospike@sha256:589d9b63f71cd9b2b735fa23ad3d7bb8a18164c498a110b2e944c236ca69b8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2118527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d1bdfed3bbccaff74c11f9d158685824c3fedc40c3b93692ffadc00ee46a64`

```dockerfile
```

-	Layers:
	-	`sha256:0b76788321cd21cc264cb0167f28ff6aa7f29926a593fce112a430c876027511`  
		Last Modified: Tue, 03 Jun 2025 04:15:38 GMT  
		Size: 2.1 MB (2089419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:366cc54baf98c104cb58a30e1de3a025d37443d8bb40b46ca3158cd726e5ab1f`  
		Last Modified: Tue, 03 Jun 2025 04:15:38 GMT  
		Size: 29.1 KB (29108 bytes)  
		MIME: application/vnd.in-toto+json
