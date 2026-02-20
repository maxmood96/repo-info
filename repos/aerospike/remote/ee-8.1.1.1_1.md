## `aerospike:ee-8.1.1.1_1`

```console
$ docker pull aerospike@sha256:70c27ca1357a4305f150b8b5cc6d93231a8d3d0693e1c2730f04a8bf995fbe80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.1.1.1_1` - linux; amd64

```console
$ docker pull aerospike@sha256:d773b8ff327833780e796e9d85c4edf2417acbd3a592366474e56ce4129c9f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86263502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c2c23bf63ff02fd3ad63e719104abe849c50c6d483afadbf5c5c7494a68cac`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 21:05:55 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.1.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 20 Feb 2026 21:05:55 GMT
ARG AEROSPIKE_EDITION=enterprise
# Fri, 20 Feb 2026 21:05:55 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Fri, 20 Feb 2026 21:05:55 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.1/aerospike-server-enterprise_8.1.1.1_tools-12.1.1_ubuntu24.04_x86_64.tgz
# Fri, 20 Feb 2026 21:05:55 GMT
ARG AEROSPIKE_SHA_X86_64=a2990f0970a7ca1bdec8068109dc0573ca975c5dd5d014a9a6f1b0a178849625
# Fri, 20 Feb 2026 21:05:55 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.1/aerospike-server-enterprise_8.1.1.1_tools-12.1.1_ubuntu24.04_aarch64.tgz
# Fri, 20 Feb 2026 21:05:55 GMT
ARG AEROSPIKE_SHA_AARCH64=1ccb5d3a9cb396ce6dcb58d24d71b2a5eb46f29ec3c24b62472318c02e668d4d
# Fri, 20 Feb 2026 21:05:55 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 20 Feb 2026 21:05:55 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.1/aerospike-server-enterprise_8.1.1.1_tools-12.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=a2990f0970a7ca1bdec8068109dc0573ca975c5dd5d014a9a6f1b0a178849625 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.1/aerospike-server-enterprise_8.1.1.1_tools-12.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=1ccb5d3a9cb396ce6dcb58d24d71b2a5eb46f29ec3c24b62472318c02e668d4d
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 20 Feb 2026 21:05:55 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 20 Feb 2026 21:05:55 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 20 Feb 2026 21:05:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 21:05:55 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 20 Feb 2026 21:05:55 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46248245b71b98858847c24e7a576c69e4b2714aea81c3459dd61d4f78e7f8d6`  
		Last Modified: Fri, 20 Feb 2026 21:06:08 GMT  
		Size: 56.5 MB (56533591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed92485b1810d4a613247a526bcb14b1bdb219f1408bfb8f748c3c59df13d19c`  
		Last Modified: Fri, 20 Feb 2026 21:06:06 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819b01425ae91af826f5e34c297c41f87c0fc1362aacde9d682ec737b7d82816`  
		Last Modified: Fri, 20 Feb 2026 21:06:06 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.1.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:b58925f9f53c3915c687abfc07a07dad2006bfc8163a1eaabbe1d34ad7f03932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57cd11d6ebec3bdee6bd65540d08347c7948b7cfb57bb1538af2ddea17428a67`

```dockerfile
```

-	Layers:
	-	`sha256:3ace8394aeb8726c7e88d80fb207ad3e6f0b8632a58b5c593db5ef7dffa86233`  
		Last Modified: Fri, 20 Feb 2026 21:06:07 GMT  
		Size: 2.2 MB (2181581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6b7bf2d5dc910b01e155482cc902ec5c07e8666ef15570a2d46d4fb9e63fa45`  
		Last Modified: Fri, 20 Feb 2026 21:06:06 GMT  
		Size: 29.0 KB (28984 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.1.1.1_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:d79edfd0c1b7c8d759430e0f77bb11149375743492c58657d089206fae36b39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84190182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c42f7586d97d7400b93ef7d1fdb5f32fe7d3ad3e58ad48a47681c365ac51967`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 21:05:46 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.1.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 20 Feb 2026 21:05:46 GMT
ARG AEROSPIKE_EDITION=enterprise
# Fri, 20 Feb 2026 21:05:46 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Fri, 20 Feb 2026 21:05:46 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.1/aerospike-server-enterprise_8.1.1.1_tools-12.1.1_ubuntu24.04_x86_64.tgz
# Fri, 20 Feb 2026 21:05:46 GMT
ARG AEROSPIKE_SHA_X86_64=a2990f0970a7ca1bdec8068109dc0573ca975c5dd5d014a9a6f1b0a178849625
# Fri, 20 Feb 2026 21:05:46 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.1/aerospike-server-enterprise_8.1.1.1_tools-12.1.1_ubuntu24.04_aarch64.tgz
# Fri, 20 Feb 2026 21:05:46 GMT
ARG AEROSPIKE_SHA_AARCH64=1ccb5d3a9cb396ce6dcb58d24d71b2a5eb46f29ec3c24b62472318c02e668d4d
# Fri, 20 Feb 2026 21:05:46 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 20 Feb 2026 21:05:46 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.1/aerospike-server-enterprise_8.1.1.1_tools-12.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=a2990f0970a7ca1bdec8068109dc0573ca975c5dd5d014a9a6f1b0a178849625 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.1/aerospike-server-enterprise_8.1.1.1_tools-12.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=1ccb5d3a9cb396ce6dcb58d24d71b2a5eb46f29ec3c24b62472318c02e668d4d
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 20 Feb 2026 21:05:46 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 20 Feb 2026 21:05:46 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 20 Feb 2026 21:05:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 21:05:46 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 20 Feb 2026 21:05:46 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc214d544e3ff5a63578307678f923e47dd449addfc732b9243f949119a028e`  
		Last Modified: Fri, 20 Feb 2026 21:06:00 GMT  
		Size: 55.3 MB (55322762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c3e8338e9c73eb9ba2842a3ec4831cbe77817427c6f739d0bd660710b44141`  
		Last Modified: Fri, 20 Feb 2026 21:05:58 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ec5e4a598f77b967b0b916dd724b1d7ca6b9a1fe49525c70d52d66af76cd45`  
		Last Modified: Fri, 20 Feb 2026 21:05:58 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.1.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:07d1078bdf10b32940be77e1966df2c173f6d67ec52f13d37d4d1ec75ef45bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b80f586b64e4ca3d07cdbd64b973d2adb792c44bd7184e6277eae99304c12a`

```dockerfile
```

-	Layers:
	-	`sha256:f5779c7be0b3b478c32d549185b19036f13fc77ba0c748b429c28dd4bb33e8a4`  
		Last Modified: Fri, 20 Feb 2026 21:05:59 GMT  
		Size: 2.2 MB (2183861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffa7ff30de9bddbf7828768ad325120344f2b2f93fe475c2e24089ac531913dd`  
		Last Modified: Fri, 20 Feb 2026 21:05:58 GMT  
		Size: 29.1 KB (29063 bytes)  
		MIME: application/vnd.in-toto+json
