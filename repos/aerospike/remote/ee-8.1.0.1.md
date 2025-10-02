## `aerospike:ee-8.1.0.1`

```console
$ docker pull aerospike@sha256:b7d67b48af0385802434de3e63d9588a4a02675bbb782c1847bdb9213f1d4d40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.1.0.1` - linux; amd64

```console
$ docker pull aerospike@sha256:7a4653c7a39becaa6c876e1e070082f6a4b0f4cb9e1828f94ff98ff47dc29661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83597948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b4c46a988fba9774a1d13ec3ed71524eef4eb733a02f67d9ef21cdd6c45ac3d`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 00:43:00 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.0.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 16 Sep 2025 00:43:00 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.1/aerospike-server-enterprise_8.1.0.1_tools-12.0.2_ubuntu24.04_x86_64.tgz
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_SHA_X86_64=dbedd8c4e5355ce61f2f3cd647a22068d87c2920718b36aee75f0734eb0dc96d
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.1/aerospike-server-enterprise_8.1.0.1_tools-12.0.2_ubuntu24.04_aarch64.tgz
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_SHA_AARCH64=de1b31a71f29bd5d23210b0e8baa6476bb61565b6a1b858149e34349667e4a4d
# Tue, 16 Sep 2025 00:43:00 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 16 Sep 2025 00:43:00 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.1/aerospike-server-enterprise_8.1.0.1_tools-12.0.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=dbedd8c4e5355ce61f2f3cd647a22068d87c2920718b36aee75f0734eb0dc96d AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.1/aerospike-server-enterprise_8.1.0.1_tools-12.0.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=de1b31a71f29bd5d23210b0e8baa6476bb61565b6a1b858149e34349667e4a4d
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 16 Sep 2025 00:43:00 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 16 Sep 2025 00:43:00 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 16 Sep 2025 00:43:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 16 Sep 2025 00:43:00 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 16 Sep 2025 00:43:00 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f2e74bfb6bef70ee6c5fab1f442fe59095616a8a699d97393a26403c5099bc`  
		Last Modified: Tue, 16 Sep 2025 16:51:35 GMT  
		Size: 53.9 MB (53872199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7422b313fc3828454111826bb92bdddd1d5fbe65661fe5b98877257f5ef07fd3`  
		Last Modified: Tue, 16 Sep 2025 16:51:31 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ca6808ef741ecacc9345724e47882e4d931f773f4833770535356766562cad`  
		Last Modified: Tue, 16 Sep 2025 16:51:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.0.1` - unknown; unknown

```console
$ docker pull aerospike@sha256:76771e89982d40d7cc49a44313062fa46a50d21c28c18007557206eb572da7ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f048539cb55d95caae1ed8d3e5ac137b783ae0c6223e4623e488653adeb55eac`

```dockerfile
```

-	Layers:
	-	`sha256:579a52db85a69f7126ef3b45a0e7f9d76e0cdd271426d5e7ef9f3ca077f3fc85`  
		Last Modified: Tue, 16 Sep 2025 17:25:34 GMT  
		Size: 2.2 MB (2182953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59a9fd73f90303595e3490300364bacce828b9dd1ebca27fad15f74b6ac96e4a`  
		Last Modified: Tue, 16 Sep 2025 17:25:34 GMT  
		Size: 29.0 KB (29028 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.1.0.1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:d178cf42d056f9b9b5c4df3c9b91551d8871ea9a41b2152ade59c81d41584f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84163541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5527e88f4e8d3fdf2c0fa55fbde607a3d50b335a11694585c64ab90288629ec9`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 16 Sep 2025 00:43:00 GMT
ARG RELEASE
# Tue, 16 Sep 2025 00:43:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Sep 2025 00:43:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Sep 2025 00:43:00 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 16 Sep 2025 00:43:00 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 16 Sep 2025 00:43:00 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 00:43:00 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.0.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 16 Sep 2025 00:43:00 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.1/aerospike-server-enterprise_8.1.0.1_tools-12.0.2_ubuntu24.04_x86_64.tgz
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_SHA_X86_64=dbedd8c4e5355ce61f2f3cd647a22068d87c2920718b36aee75f0734eb0dc96d
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.1/aerospike-server-enterprise_8.1.0.1_tools-12.0.2_ubuntu24.04_aarch64.tgz
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_SHA_AARCH64=de1b31a71f29bd5d23210b0e8baa6476bb61565b6a1b858149e34349667e4a4d
# Tue, 16 Sep 2025 00:43:00 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 16 Sep 2025 00:43:00 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.1/aerospike-server-enterprise_8.1.0.1_tools-12.0.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=dbedd8c4e5355ce61f2f3cd647a22068d87c2920718b36aee75f0734eb0dc96d AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.1/aerospike-server-enterprise_8.1.0.1_tools-12.0.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=de1b31a71f29bd5d23210b0e8baa6476bb61565b6a1b858149e34349667e4a4d
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 16 Sep 2025 00:43:00 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 16 Sep 2025 00:43:00 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 16 Sep 2025 00:43:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 16 Sep 2025 00:43:00 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 16 Sep 2025 00:43:00 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376f3dd9a965d32d6c63322d3a40c4b516fbd213722278263896aca6b9f4306d`  
		Last Modified: Thu, 02 Oct 2025 01:11:03 GMT  
		Size: 55.3 MB (55299666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fb79da22ba2cd680e45e996d5d13b8cd7620b4be33ed19f75bfbc1f5490fb8`  
		Last Modified: Thu, 02 Oct 2025 01:10:59 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8f89f79de038345f6fa7f29c1465720561cbf37748cf6db5f7c1ca0d5492d5`  
		Last Modified: Thu, 02 Oct 2025 01:10:59 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.0.1` - unknown; unknown

```console
$ docker pull aerospike@sha256:2ef52c2f2ab571de20ec1f16d353c1152396489a70939c13dede4deb4e0b3733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d2ec96a3aae3b419df70c301fbce59a89c39a69d22fdd19797440b98d016df`

```dockerfile
```

-	Layers:
	-	`sha256:2c6eae641861fe964548e51453648d238be2a54343dada641ceb2d411df1c6df`  
		Last Modified: Thu, 02 Oct 2025 02:25:30 GMT  
		Size: 2.2 MB (2185233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c86c4a6f780b57a392811a19ef085730829bc280ff80146306369d873c197e4c`  
		Last Modified: Thu, 02 Oct 2025 02:25:31 GMT  
		Size: 29.1 KB (29108 bytes)  
		MIME: application/vnd.in-toto+json
