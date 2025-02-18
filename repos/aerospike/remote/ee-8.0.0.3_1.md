## `aerospike:ee-8.0.0.3_1`

```console
$ docker pull aerospike@sha256:6ea8935c5cea64cfb9818cec86fe37f3180ba39f5e83578b5cec2c902631f026
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.0.0.3_1` - linux; amd64

```console
$ docker pull aerospike@sha256:e0fbdfe1331a15d106439950e4d42750603b78b360fb9facc2f92190b89edb22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82027197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092dc5a638fed724dd255fee4cc3cbec8e06cad7ac21ca5d17e7037c4b008926`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Sat, 15 Feb 2025 03:00:21 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.3 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Sat, 15 Feb 2025 03:00:21 GMT
ARG AEROSPIKE_EDITION=enterprise
# Sat, 15 Feb 2025 03:00:21 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.3/aerospike-server-enterprise_8.0.0.3_tools-11.2.0_ubuntu24.04_x86_64.tgz
# Sat, 15 Feb 2025 03:00:21 GMT
ARG AEROSPIKE_SHA_X86_64=788ced5386fe117270dbae762a622f3258febd1a3a2f031f981f0c9fc855ed83
# Sat, 15 Feb 2025 03:00:21 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.3/aerospike-server-enterprise_8.0.0.3_tools-11.2.0_ubuntu24.04_aarch64.tgz
# Sat, 15 Feb 2025 03:00:21 GMT
ARG AEROSPIKE_SHA_AARCH64=a1c33abd94a79bed4da806b4d10f04f0feecb1b9e9e90cad43894331e45b20b3
# Sat, 15 Feb 2025 03:00:21 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Sat, 15 Feb 2025 03:00:21 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.3/aerospike-server-enterprise_8.0.0.3_tools-11.2.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=788ced5386fe117270dbae762a622f3258febd1a3a2f031f981f0c9fc855ed83 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.3/aerospike-server-enterprise_8.0.0.3_tools-11.2.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=a1c33abd94a79bed4da806b4d10f04f0feecb1b9e9e90cad43894331e45b20b3
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Sat, 15 Feb 2025 03:00:21 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Sat, 15 Feb 2025 03:00:21 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Sat, 15 Feb 2025 03:00:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 15 Feb 2025 03:00:21 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Sat, 15 Feb 2025 03:00:21 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 03 Feb 2025 23:00:26 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f026c7556dc87a06306df76e6246dc8f39a7fcc66c4fb8381c22c356e2b99da`  
		Last Modified: Tue, 18 Feb 2025 19:31:29 GMT  
		Size: 52.3 MB (52270606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b881ac0219007c2b598b90690a3ac7e0db361d36e05b03d0b43ff3282481c517`  
		Last Modified: Tue, 18 Feb 2025 19:31:12 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03d9a3bfbfcd474106fa62a1490421589bb541930e1eaec18ad3d7daa3aea86`  
		Last Modified: Tue, 18 Feb 2025 19:31:13 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.0.0.3_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:b85e55a51ae5e7c1b32b505505cd34fd2f08568ca94fb0e776deb8e88c8af227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1989320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d97f4bb7b3548816fa4645759ca8de3e46a15741b1682d1c190bbb43c265f48`

```dockerfile
```

-	Layers:
	-	`sha256:97e3c69eaf40ec51c6870f810db67fe8ae5a65f83ecac8f525db6073fc724065`  
		Last Modified: Tue, 18 Feb 2025 21:25:27 GMT  
		Size: 2.0 MB (1960157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:490e0384fe52d5112be658d90f1f0a4de5df890de0f26a8190a8950c39b89a4c`  
		Last Modified: Tue, 18 Feb 2025 21:25:27 GMT  
		Size: 29.2 KB (29163 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.0.0.3_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:2fd16ab6bfa3aae910d69a57d3883cf2c09c6116ff6246e7580f234855e2339a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80608602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259dfcf5929a339822951a5a63cfc47943c958fe09fcffd7c62038d6daadc93d`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Sat, 15 Feb 2025 03:00:21 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.3 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Sat, 15 Feb 2025 03:00:21 GMT
ARG AEROSPIKE_EDITION=enterprise
# Sat, 15 Feb 2025 03:00:21 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.3/aerospike-server-enterprise_8.0.0.3_tools-11.2.0_ubuntu24.04_x86_64.tgz
# Sat, 15 Feb 2025 03:00:21 GMT
ARG AEROSPIKE_SHA_X86_64=788ced5386fe117270dbae762a622f3258febd1a3a2f031f981f0c9fc855ed83
# Sat, 15 Feb 2025 03:00:21 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.3/aerospike-server-enterprise_8.0.0.3_tools-11.2.0_ubuntu24.04_aarch64.tgz
# Sat, 15 Feb 2025 03:00:21 GMT
ARG AEROSPIKE_SHA_AARCH64=a1c33abd94a79bed4da806b4d10f04f0feecb1b9e9e90cad43894331e45b20b3
# Sat, 15 Feb 2025 03:00:21 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Sat, 15 Feb 2025 03:00:21 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.3/aerospike-server-enterprise_8.0.0.3_tools-11.2.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=788ced5386fe117270dbae762a622f3258febd1a3a2f031f981f0c9fc855ed83 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.3/aerospike-server-enterprise_8.0.0.3_tools-11.2.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=a1c33abd94a79bed4da806b4d10f04f0feecb1b9e9e90cad43894331e45b20b3
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Sat, 15 Feb 2025 03:00:21 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Sat, 15 Feb 2025 03:00:21 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Sat, 15 Feb 2025 03:00:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 15 Feb 2025 03:00:21 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Sat, 15 Feb 2025 03:00:21 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Tue, 04 Feb 2025 06:04:53 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8e76d1b927ba3e573bbc8e94b55787857ef85dd02bef2b3e600106f62c133a`  
		Last Modified: Tue, 18 Feb 2025 19:31:05 GMT  
		Size: 51.7 MB (51712702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b26a4c369519d5372247f0677ef99f893e8114fa204fbb9e200c40e0b74ba5`  
		Last Modified: Tue, 18 Feb 2025 19:31:03 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957838168572ab463785d0bf6bdaa331eb556115947615131b2d8549b7a4c366`  
		Last Modified: Tue, 18 Feb 2025 19:31:04 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.0.0.3_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:2b9cf9d3f6aa452a49c36fbe16e45a5d70f6749bfce2813a96c5ac6b91f7c7f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1991680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7cf896e446746d6c9a4cfe0107f0e2cb60984a4f79f0b59f7ab165029cc49af`

```dockerfile
```

-	Layers:
	-	`sha256:b082ef9b2e9cfce04006d68653645b523389e1b7015c27f2932b30cbd078b315`  
		Last Modified: Tue, 18 Feb 2025 21:25:29 GMT  
		Size: 2.0 MB (1962437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be760d0448f3cafbb8db344ce5e736933fbba5c8fd3ac43084956401c60fb6cb`  
		Last Modified: Tue, 18 Feb 2025 21:25:29 GMT  
		Size: 29.2 KB (29243 bytes)  
		MIME: application/vnd.in-toto+json
