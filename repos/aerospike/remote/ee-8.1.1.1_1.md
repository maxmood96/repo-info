## `aerospike:ee-8.1.1.1_1`

```console
$ docker pull aerospike@sha256:eb232826637404cbb240e6ecf65ebb62605ff76441014a6939923a33d64cc379
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.1.1.1_1` - linux; amd64

```console
$ docker pull aerospike@sha256:212580d7d81a9dfddeb35b9dce662dacf12f870ee461de11d12bbb4481cfc6b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86269998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32984a80d6fe576732f458c9d9d59d9fd08d00b06f16b9dd5e0d759a3b0d7f89`
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
# Tue, 07 Apr 2026 01:42:57 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.1.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 07 Apr 2026 01:42:57 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 07 Apr 2026 01:42:57 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 07 Apr 2026 01:42:57 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.1/aerospike-server-enterprise_8.1.1.1_tools-12.1.1_ubuntu24.04_x86_64.tgz
# Tue, 07 Apr 2026 01:42:57 GMT
ARG AEROSPIKE_SHA_X86_64=a2990f0970a7ca1bdec8068109dc0573ca975c5dd5d014a9a6f1b0a178849625
# Tue, 07 Apr 2026 01:42:57 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.1/aerospike-server-enterprise_8.1.1.1_tools-12.1.1_ubuntu24.04_aarch64.tgz
# Tue, 07 Apr 2026 01:42:57 GMT
ARG AEROSPIKE_SHA_AARCH64=1ccb5d3a9cb396ce6dcb58d24d71b2a5eb46f29ec3c24b62472318c02e668d4d
# Tue, 07 Apr 2026 01:42:57 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 07 Apr 2026 01:42:57 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.1/aerospike-server-enterprise_8.1.1.1_tools-12.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=a2990f0970a7ca1bdec8068109dc0573ca975c5dd5d014a9a6f1b0a178849625 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.1/aerospike-server-enterprise_8.1.1.1_tools-12.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=1ccb5d3a9cb396ce6dcb58d24d71b2a5eb46f29ec3c24b62472318c02e668d4d
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 07 Apr 2026 01:42:57 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 07 Apr 2026 01:42:57 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 07 Apr 2026 01:42:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:42:57 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 07 Apr 2026 01:42:57 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cbde5279f05dec1934176fb1e5391eadb44bd51acc58fcdfcd5b9aa799a1b4`  
		Last Modified: Tue, 07 Apr 2026 01:43:10 GMT  
		Size: 56.5 MB (56534245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e8007f0af677e177cd43c4b89a273a4e5c12710c52e3d397dc6fc9bf9c27ed`  
		Last Modified: Tue, 07 Apr 2026 01:43:09 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1251dfa46076454a83cc5d9d4ca1ff625356958647637dced0bea7f4b34bf1`  
		Last Modified: Tue, 07 Apr 2026 01:43:09 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.1.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:796f02fb319354e32e5608979ad77f7aca4942ff540b32486145f7e9fb475d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edde610240f768b20b64089f51adf2e0717c2ec929cfe5d8432ecb77087447aa`

```dockerfile
```

-	Layers:
	-	`sha256:b1ee3c870ff32c284dfb8f6f930f0a232df2cb98247f9fffc9f4caf610fb3d50`  
		Last Modified: Tue, 07 Apr 2026 01:43:09 GMT  
		Size: 2.2 MB (2181601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee645c78552703792d4781918022e2584f4266fe9cc2c32da5ced9b17007d92b`  
		Last Modified: Tue, 07 Apr 2026 01:43:09 GMT  
		Size: 29.0 KB (28985 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.1.1.1_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:649f0f5a30c60c15d4f248c0f8484414608580b85d202b8167740ced3df11a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84201237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f5a178aab95e2d0cd286a49769f606ea14642a838648e775b12caf73e8ae81`
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
# Tue, 07 Apr 2026 01:46:12 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.1.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 07 Apr 2026 01:46:12 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 07 Apr 2026 01:46:12 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 07 Apr 2026 01:46:12 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.1/aerospike-server-enterprise_8.1.1.1_tools-12.1.1_ubuntu24.04_x86_64.tgz
# Tue, 07 Apr 2026 01:46:12 GMT
ARG AEROSPIKE_SHA_X86_64=a2990f0970a7ca1bdec8068109dc0573ca975c5dd5d014a9a6f1b0a178849625
# Tue, 07 Apr 2026 01:46:12 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.1/aerospike-server-enterprise_8.1.1.1_tools-12.1.1_ubuntu24.04_aarch64.tgz
# Tue, 07 Apr 2026 01:46:12 GMT
ARG AEROSPIKE_SHA_AARCH64=1ccb5d3a9cb396ce6dcb58d24d71b2a5eb46f29ec3c24b62472318c02e668d4d
# Tue, 07 Apr 2026 01:46:12 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 07 Apr 2026 01:46:12 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.1/aerospike-server-enterprise_8.1.1.1_tools-12.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=a2990f0970a7ca1bdec8068109dc0573ca975c5dd5d014a9a6f1b0a178849625 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.1/aerospike-server-enterprise_8.1.1.1_tools-12.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=1ccb5d3a9cb396ce6dcb58d24d71b2a5eb46f29ec3c24b62472318c02e668d4d
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 07 Apr 2026 01:46:12 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 07 Apr 2026 01:46:12 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 07 Apr 2026 01:46:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:46:12 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 07 Apr 2026 01:46:12 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763ad149be31ea2256a7e50e14082f2a23eebcdf1d5cf4d2239f56c6b377e6ed`  
		Last Modified: Tue, 07 Apr 2026 01:46:25 GMT  
		Size: 55.3 MB (55324864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4186adf1bff4ab3c855f3bc9fa02fac0110d828839222adf5e18c4ea264ac468`  
		Last Modified: Tue, 07 Apr 2026 01:46:24 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b73665e69e5805ae5f8c98fd632a47181e5880e0efdb6e4499a2864e1887f6d`  
		Last Modified: Tue, 07 Apr 2026 01:46:23 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.1.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:d42e92cc72b5f439e495a8dd3e1f89b8125639ad4b12b2a459f4a949d1b2c0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de31d3730a5477d605596627020629a5e75d2e63014937b68c337cd3dc995c25`

```dockerfile
```

-	Layers:
	-	`sha256:99a73bb907de21a47e3fdaab49afa82fd929f23c688947cffa754b4aae081314`  
		Last Modified: Tue, 07 Apr 2026 01:46:23 GMT  
		Size: 2.2 MB (2183881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24fdc646d2167464e2e5423022397350bc02f3f88168a250c5aa3207b29443c5`  
		Last Modified: Tue, 07 Apr 2026 01:46:23 GMT  
		Size: 29.1 KB (29063 bytes)  
		MIME: application/vnd.in-toto+json
