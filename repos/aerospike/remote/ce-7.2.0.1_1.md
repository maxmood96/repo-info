## `aerospike:ce-7.2.0.1_1`

```console
$ docker pull aerospike@sha256:968d2500fdbcaccc308bf97f831b5c84ec1bf34f4eedcc58fdb07274e19d9dc0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-7.2.0.1_1` - linux; amd64

```console
$ docker pull aerospike@sha256:023efd827ffde0c06e647a2a45945e27f2544d953c565af62458be76ff756020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77850132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eca5b6270f644e716495033ab88d32653f2fb4ad111b5665e27e6c128b9a12e`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 08 Oct 2024 00:12:46 GMT
ARG RELEASE
# Tue, 08 Oct 2024 00:12:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Oct 2024 00:12:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Oct 2024 00:12:46 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Oct 2024 00:12:46 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Tue, 08 Oct 2024 00:12:46 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 00:12:46 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.2.0.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 08 Oct 2024 00:12:46 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 08 Oct 2024 00:12:46 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.1/aerospike-server-community_7.2.0.1_tools-11.1.0_ubuntu24.04_x86_64.tgz
# Tue, 08 Oct 2024 00:12:46 GMT
ARG AEROSPIKE_SHA_X86_64=48b7151ba4d3665e1265f4c3bfa0ac84d62f5085e1e1ac30c6da1e06232e6c21
# Tue, 08 Oct 2024 00:12:46 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.1/aerospike-server-community_7.2.0.1_tools-11.1.0_ubuntu24.04_aarch64.tgz
# Tue, 08 Oct 2024 00:12:46 GMT
ARG AEROSPIKE_SHA_AARCH64=c8af8a0530d1988dd92ccf3c6a70daf2c77dded66949ad491978848a52d9d8e4
# Tue, 08 Oct 2024 00:12:46 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 08 Oct 2024 00:12:46 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.1/aerospike-server-community_7.2.0.1_tools-11.1.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=48b7151ba4d3665e1265f4c3bfa0ac84d62f5085e1e1ac30c6da1e06232e6c21 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.1/aerospike-server-community_7.2.0.1_tools-11.1.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=c8af8a0530d1988dd92ccf3c6a70daf2c77dded66949ad491978848a52d9d8e4
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 08 Oct 2024 00:12:46 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 08 Oct 2024 00:12:46 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 08 Oct 2024 00:12:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Oct 2024 00:12:46 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 08 Oct 2024 00:12:46 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a967356bd177c9bd2da1e266a50a5ba9777e8bb8148e6d562a33af0bd6407f58`  
		Last Modified: Sat, 12 Oct 2024 00:00:35 GMT  
		Size: 48.1 MB (48097387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc32679b18989f1cd33b5c6c150e52f1721c42dfe5c237e3bbcfd6ba8d0e68b`  
		Last Modified: Sat, 12 Oct 2024 00:00:35 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affd08663d7e8889c31f4c0f5754f28f51d3d375991d8399edd5b80861bd6611`  
		Last Modified: Sat, 12 Oct 2024 00:00:35 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-7.2.0.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:5155f04a319a6608c747c306175f202add13045e442d47c2f557baa68a390146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1878850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b34602dc0ce63c5ef03a4b1bf78eae4f1f1db6349b6ecc166a2b6baec3ddb5c`

```dockerfile
```

-	Layers:
	-	`sha256:b580bf21d2272e058607695bb792c3a41f72d5f9f4c5d7122bf4787c680ca0bc`  
		Last Modified: Sat, 12 Oct 2024 00:00:35 GMT  
		Size: 1.8 MB (1849920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a05c84b12671cea1a260021c3fc97c1082b097810efc6ca8149bba5fd78179c`  
		Last Modified: Sat, 12 Oct 2024 00:00:35 GMT  
		Size: 28.9 KB (28930 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-7.2.0.1_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:daf3012c7e27a92abf6904989a1391b073096a9106edc7613feeb3982568adb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76429231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7aa93cff5f9798ba2979a8957067a519cd56323347078dcf83c09c98f45e0f9`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 08 Oct 2024 00:12:46 GMT
ARG RELEASE
# Tue, 08 Oct 2024 00:12:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Oct 2024 00:12:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Oct 2024 00:12:46 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Oct 2024 00:12:46 GMT
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
# Tue, 08 Oct 2024 00:12:46 GMT
CMD ["/bin/bash"]
# Tue, 08 Oct 2024 00:12:46 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.2.0.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 08 Oct 2024 00:12:46 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 08 Oct 2024 00:12:46 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.1/aerospike-server-community_7.2.0.1_tools-11.1.0_ubuntu24.04_x86_64.tgz
# Tue, 08 Oct 2024 00:12:46 GMT
ARG AEROSPIKE_SHA_X86_64=48b7151ba4d3665e1265f4c3bfa0ac84d62f5085e1e1ac30c6da1e06232e6c21
# Tue, 08 Oct 2024 00:12:46 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.1/aerospike-server-community_7.2.0.1_tools-11.1.0_ubuntu24.04_aarch64.tgz
# Tue, 08 Oct 2024 00:12:46 GMT
ARG AEROSPIKE_SHA_AARCH64=c8af8a0530d1988dd92ccf3c6a70daf2c77dded66949ad491978848a52d9d8e4
# Tue, 08 Oct 2024 00:12:46 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 08 Oct 2024 00:12:46 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.1/aerospike-server-community_7.2.0.1_tools-11.1.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=48b7151ba4d3665e1265f4c3bfa0ac84d62f5085e1e1ac30c6da1e06232e6c21 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.1/aerospike-server-community_7.2.0.1_tools-11.1.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=c8af8a0530d1988dd92ccf3c6a70daf2c77dded66949ad491978848a52d9d8e4
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 08 Oct 2024 00:12:46 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 08 Oct 2024 00:12:46 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 08 Oct 2024 00:12:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Oct 2024 00:12:46 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 08 Oct 2024 00:12:46 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:0741829382faee1dada646b49acf3f4349f0c757e16139b7bb1874c6339d996e`  
		Last Modified: Thu, 10 Oct 2024 08:59:51 GMT  
		Size: 28.9 MB (28885616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13438720fa000492d13cf9969a6da76dba695b82e3a530d9ca30c1a7e858313e`  
		Last Modified: Sat, 12 Oct 2024 00:53:49 GMT  
		Size: 47.5 MB (47541333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ee252442d744ff1da283f4da9da450dc56bd3cf0d4cd0690fe75dd7889ec1f`  
		Last Modified: Sat, 12 Oct 2024 00:53:47 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5412a615565acfc537f76ea74e42e1b3c6737e0ad8dd688195257b2c106191`  
		Last Modified: Sat, 12 Oct 2024 00:53:47 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-7.2.0.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:b0f2498f5062342c94816c2fad8b81dabc4f89bc55eeecb198793e31b598ef10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1881072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69f82706d72f77919d480fb33a10564df225ec479c992f44f42cc9dadb06584`

```dockerfile
```

-	Layers:
	-	`sha256:ea438fd9b6ef0c8323eda92fd70171edc9ab3d05c020f150ae34d03a46ac80a0`  
		Last Modified: Sat, 12 Oct 2024 00:53:48 GMT  
		Size: 1.9 MB (1852067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2348db6da5dab4f44a90884bfdb2f268b79aead1c6022309f9b3c717ce623c58`  
		Last Modified: Sat, 12 Oct 2024 00:53:47 GMT  
		Size: 29.0 KB (29005 bytes)  
		MIME: application/vnd.in-toto+json
