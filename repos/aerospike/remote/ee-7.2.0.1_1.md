## `aerospike:ee-7.2.0.1_1`

```console
$ docker pull aerospike@sha256:9cd4cc86a2295be05006072fafc78b2ead32404e930f82dfb4fa51d0974ab577
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-7.2.0.1_1` - linux; amd64

```console
$ docker pull aerospike@sha256:5378ac0cb842fc3bb76a05e586130712e48bc1aa8b31c62adc5053de28b9e4f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81996404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b8ab7304ad1ddc75562697fa06bba8c1d1ff3f33ba614273765a76c82b28c8`
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
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.2.0.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 08 Oct 2024 00:12:46 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 08 Oct 2024 00:12:46 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.1/aerospike-server-enterprise_7.2.0.1_tools-11.1.0_ubuntu24.04_x86_64.tgz
# Tue, 08 Oct 2024 00:12:46 GMT
ARG AEROSPIKE_SHA_X86_64=37b509968d8bb381c39ad308249c4f8be5d8672db3c8b55cad4894d4afb4302a
# Tue, 08 Oct 2024 00:12:46 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.1/aerospike-server-enterprise_7.2.0.1_tools-11.1.0_ubuntu24.04_aarch64.tgz
# Tue, 08 Oct 2024 00:12:46 GMT
ARG AEROSPIKE_SHA_AARCH64=90a93dd277c7607a349d23e88c1576304bae459dd73291455370da77bf9d73bb
# Tue, 08 Oct 2024 00:12:46 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 08 Oct 2024 00:12:46 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.1/aerospike-server-enterprise_7.2.0.1_tools-11.1.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=37b509968d8bb381c39ad308249c4f8be5d8672db3c8b55cad4894d4afb4302a AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.1/aerospike-server-enterprise_7.2.0.1_tools-11.1.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=90a93dd277c7607a349d23e88c1576304bae459dd73291455370da77bf9d73bb
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
	-	`sha256:59c4c7fd36b8fa395322b03b457ae8396bdf504836a549018c15804a6f8f0d28`  
		Last Modified: Sat, 12 Oct 2024 00:00:40 GMT  
		Size: 52.2 MB (52243655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c5301c2fcac5ff7481fb57477d8210cd82243a4a873ea96854d0f7df239835`  
		Last Modified: Sat, 12 Oct 2024 00:00:39 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affd08663d7e8889c31f4c0f5754f28f51d3d375991d8399edd5b80861bd6611`  
		Last Modified: Sat, 12 Oct 2024 00:00:35 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.2.0.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:cb37023f07f4d64a74838cdd0d3cbd3ca982ba8e1a417fe844aa6f533c489605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1971751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cbab55014ca2f9ff451f7ebcaf7a45bc16367d2b75c4309e7b36cca4c60edd`

```dockerfile
```

-	Layers:
	-	`sha256:3ff8e9787f83233bed3d6d1c792c0a24012b21e0c9993a702710b6d6f7d29a80`  
		Last Modified: Sat, 12 Oct 2024 00:00:39 GMT  
		Size: 1.9 MB (1942804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47519a7885282709d8b873f5eba74837b8449e7a51218093adc723e134acefed`  
		Last Modified: Sat, 12 Oct 2024 00:00:39 GMT  
		Size: 28.9 KB (28947 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-7.2.0.1_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:365e552c539b45ef6d5aaec3f8fec70dd73e160b56806b47d49b0beda46f0adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80592072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff2339091a89d1e48cc3270287213a4fc7214d10ac9186defb40950972853645`
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
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.2.0.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 08 Oct 2024 00:12:46 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 08 Oct 2024 00:12:46 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.1/aerospike-server-enterprise_7.2.0.1_tools-11.1.0_ubuntu24.04_x86_64.tgz
# Tue, 08 Oct 2024 00:12:46 GMT
ARG AEROSPIKE_SHA_X86_64=37b509968d8bb381c39ad308249c4f8be5d8672db3c8b55cad4894d4afb4302a
# Tue, 08 Oct 2024 00:12:46 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.1/aerospike-server-enterprise_7.2.0.1_tools-11.1.0_ubuntu24.04_aarch64.tgz
# Tue, 08 Oct 2024 00:12:46 GMT
ARG AEROSPIKE_SHA_AARCH64=90a93dd277c7607a349d23e88c1576304bae459dd73291455370da77bf9d73bb
# Tue, 08 Oct 2024 00:12:46 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 08 Oct 2024 00:12:46 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.1/aerospike-server-enterprise_7.2.0.1_tools-11.1.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=37b509968d8bb381c39ad308249c4f8be5d8672db3c8b55cad4894d4afb4302a AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.1/aerospike-server-enterprise_7.2.0.1_tools-11.1.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=90a93dd277c7607a349d23e88c1576304bae459dd73291455370da77bf9d73bb
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
	-	`sha256:6a41e5b46c3a7f664d7c1d150c878bc05f32d2b97b87ed88dbf63ba98a174018`  
		Last Modified: Sat, 12 Oct 2024 00:53:08 GMT  
		Size: 51.7 MB (51704168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cf3b97f51d0bd94b30192f5ccd4838c12b9d5082db389f0a71bce27eaef971`  
		Last Modified: Sat, 12 Oct 2024 00:53:06 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82bc406657a0f0a00d5a34b62aa31a969820c8619e5b6af4fd1016fbced4ed2e`  
		Last Modified: Sat, 12 Oct 2024 00:53:06 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.2.0.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:c4a0180cf70a28d0e489bfb0d5083c77bec088266042f86e58784fe09362c4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1973990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2baf805d48cfdf826cb497a87ec5b0b392a6b5da31fbf4ec9de3fc19ed01b75`

```dockerfile
```

-	Layers:
	-	`sha256:f995d97cf4838a1aa9d32ae0749258cfecdaae13cae94d379931126a6892bdb7`  
		Last Modified: Sat, 12 Oct 2024 00:53:06 GMT  
		Size: 1.9 MB (1944969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c80f3b63d328c1e0f1e5ce1fc3d0351755e0dd5c807725e305bab4a962b81b2`  
		Last Modified: Sat, 12 Oct 2024 00:53:06 GMT  
		Size: 29.0 KB (29021 bytes)  
		MIME: application/vnd.in-toto+json
