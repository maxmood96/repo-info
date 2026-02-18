## `aerospike:ee-8.1.1.0_1`

```console
$ docker pull aerospike@sha256:11c2d560c83a8eaef072f0d35a67390440b1e034a04f88ef5b4248d6d84ad621
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.1.1.0_1` - linux; amd64

```console
$ docker pull aerospike@sha256:6be880225f4622941762e9ffa6fd558647b7cd22984fd43777623d74554d9fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86260103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c1cbc3950e0e5a398ff9825fbf4da40ee944fe47978880f5eee1c781f293b1`
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
# Tue, 17 Feb 2026 20:11:47 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.1.0 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 17 Feb 2026 20:11:47 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 17 Feb 2026 20:11:47 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 17 Feb 2026 20:11:47 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.0/aerospike-server-enterprise_8.1.1.0_tools-12.1.1_ubuntu24.04_x86_64.tgz
# Tue, 17 Feb 2026 20:11:47 GMT
ARG AEROSPIKE_SHA_X86_64=11c05208d3a982514c0b4ffd4e256f214f08aaf330e0712f659ade5c2782e982
# Tue, 17 Feb 2026 20:11:47 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.0/aerospike-server-enterprise_8.1.1.0_tools-12.1.1_ubuntu24.04_aarch64.tgz
# Tue, 17 Feb 2026 20:11:47 GMT
ARG AEROSPIKE_SHA_AARCH64=cfb43ed21b27bc77ccf5d35e42f47f7b40fba6c4002e755d4c20962f18608a77
# Tue, 17 Feb 2026 20:11:47 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 17 Feb 2026 20:11:47 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.0/aerospike-server-enterprise_8.1.1.0_tools-12.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=11c05208d3a982514c0b4ffd4e256f214f08aaf330e0712f659ade5c2782e982 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.0/aerospike-server-enterprise_8.1.1.0_tools-12.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=cfb43ed21b27bc77ccf5d35e42f47f7b40fba6c4002e755d4c20962f18608a77
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 17 Feb 2026 20:11:47 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 17 Feb 2026 20:11:47 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 17 Feb 2026 20:11:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:11:47 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 17 Feb 2026 20:11:47 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d292440644a80d2c313bd505f65e8a0dd5661ee9585bd903df82168279d517b4`  
		Last Modified: Tue, 17 Feb 2026 20:12:00 GMT  
		Size: 56.5 MB (56530198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9728aad01d7cf508bb3d4f33ef86857a90a02771a576c939521d19779d4ce6e0`  
		Last Modified: Tue, 17 Feb 2026 20:11:59 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddfe6e15f70f77ebf0e443b96c44aa220ebf88169d8a247d9a7acff4755d879`  
		Last Modified: Tue, 17 Feb 2026 20:11:59 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.1.0_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:96f6de47eaf7d0381582dff16455b317204a4d7c9d0648464c424146bf6ae98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ffcfb00b377c090b5682faf8b0cc6077adb472d51a7b2c4d15885bd5559aa1`

```dockerfile
```

-	Layers:
	-	`sha256:1d682317ed5bd7c9950fa9c64f915e8232cd2e870f4691bf6819b8954e4805be`  
		Last Modified: Tue, 17 Feb 2026 20:11:59 GMT  
		Size: 2.2 MB (2181581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:276cc9fe80b5c672496d0802a0053dbb88fea8830600401718bdfbbff9eb9294`  
		Last Modified: Tue, 17 Feb 2026 20:11:59 GMT  
		Size: 29.0 KB (28985 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.1.1.0_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:fb0e50a106e5666054002cc60b996669fc6a25529f695163cd5c026a9a1133e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84186832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74695462a484a7ee531eb9a0843346ec26eeaee361c0c0f543af3ea260518b21`
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
# Tue, 17 Feb 2026 20:11:02 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.1.0 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 17 Feb 2026 20:11:02 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 17 Feb 2026 20:11:02 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 17 Feb 2026 20:11:02 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.0/aerospike-server-enterprise_8.1.1.0_tools-12.1.1_ubuntu24.04_x86_64.tgz
# Tue, 17 Feb 2026 20:11:02 GMT
ARG AEROSPIKE_SHA_X86_64=11c05208d3a982514c0b4ffd4e256f214f08aaf330e0712f659ade5c2782e982
# Tue, 17 Feb 2026 20:11:02 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.0/aerospike-server-enterprise_8.1.1.0_tools-12.1.1_ubuntu24.04_aarch64.tgz
# Tue, 17 Feb 2026 20:11:02 GMT
ARG AEROSPIKE_SHA_AARCH64=cfb43ed21b27bc77ccf5d35e42f47f7b40fba6c4002e755d4c20962f18608a77
# Tue, 17 Feb 2026 20:11:02 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 17 Feb 2026 20:11:02 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.0/aerospike-server-enterprise_8.1.1.0_tools-12.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=11c05208d3a982514c0b4ffd4e256f214f08aaf330e0712f659ade5c2782e982 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.0/aerospike-server-enterprise_8.1.1.0_tools-12.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=cfb43ed21b27bc77ccf5d35e42f47f7b40fba6c4002e755d4c20962f18608a77
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 17 Feb 2026 20:11:02 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 17 Feb 2026 20:11:02 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 17 Feb 2026 20:11:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:11:02 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 17 Feb 2026 20:11:02 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e723135ed4c3ab9747a94a19303f6e87df63166f9c1660eeb57fe0c26ef35ed0`  
		Last Modified: Tue, 17 Feb 2026 20:11:16 GMT  
		Size: 55.3 MB (55319417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49f54f29cf8d57d74c716b17cbc12479b0f801fb5654be4c9e3f26b8c56ccc7`  
		Last Modified: Tue, 17 Feb 2026 20:11:14 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359730497b3320f26b22d3e1e4d33fc0cf9970ce87e81cde0cf360d7377506e5`  
		Last Modified: Tue, 17 Feb 2026 20:11:14 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.1.0_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:c11f988c0acc5b9996237c55d50f5ce50af5f1907b3749ddad12fa500c6433dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c7c3a32ad7ab7a1abc8f7ab3b5650a8ef57d207234b71a9569539c932265a4`

```dockerfile
```

-	Layers:
	-	`sha256:e440e3c4bc3d7d2fa36ad39613b374750d53b044ce7583504cdea2b4aefb9b5a`  
		Last Modified: Tue, 17 Feb 2026 20:11:15 GMT  
		Size: 2.2 MB (2183861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9073bda1db1dccfe71ca83d36876ed3b122adea7b61b070d5440e39521c09ac9`  
		Last Modified: Tue, 17 Feb 2026 20:11:14 GMT  
		Size: 29.1 KB (29065 bytes)  
		MIME: application/vnd.in-toto+json
