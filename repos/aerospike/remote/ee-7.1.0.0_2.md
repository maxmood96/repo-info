## `aerospike:ee-7.1.0.0_2`

```console
$ docker pull aerospike@sha256:d45e454d315ad6d5e11507d84c8342d805ccc34be8bf14bd995fb354bc7892bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-7.1.0.0_2` - linux; amd64

```console
$ docker pull aerospike@sha256:b1a5e18ed65696bbe36cd9d6b4550bcefc706be01ec6b9e0981b86efdf3d33db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81979253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d7b1def620dc9de8678d68d2402744483c3fe14e1be76836607c062d415397`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Fri, 31 May 2024 01:15:47 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.0 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 31 May 2024 01:15:47 GMT
ARG AEROSPIKE_EDITION=enterprise
# Fri, 31 May 2024 01:15:47 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.0/aerospike-server-enterprise_7.1.0.0_tools-11.0.0_ubuntu22.04_x86_64.tgz
# Fri, 31 May 2024 01:15:47 GMT
ARG AEROSPIKE_SHA_X86_64=6046f85cd37ebbbca8f3ad7a2079954a223de5a433ddb34104a8362846bdd002
# Fri, 31 May 2024 01:15:47 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.0/aerospike-server-enterprise_7.1.0.0_tools-11.0.0_ubuntu22.04_aarch64.tgz
# Fri, 31 May 2024 01:15:47 GMT
ARG AEROSPIKE_SHA_AARCH64=20f50036269a1b59b611dae35952f80f77fdd549355590011af9fa51c7c1a94f
# Fri, 31 May 2024 01:15:47 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 31 May 2024 01:15:47 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.0/aerospike-server-enterprise_7.1.0.0_tools-11.0.0_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=6046f85cd37ebbbca8f3ad7a2079954a223de5a433ddb34104a8362846bdd002 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.0/aerospike-server-enterprise_7.1.0.0_tools-11.0.0_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=20f50036269a1b59b611dae35952f80f77fdd549355590011af9fa51c7c1a94f
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 31 May 2024 01:15:47 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 31 May 2024 01:15:47 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 31 May 2024 01:15:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 31 May 2024 01:15:47 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 31 May 2024 01:15:47 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:a8b1c5f80c2d2a757adc963e3fe2dad0b4d229f83df3349fbb70e4d12dd48822`  
		Last Modified: Sat, 27 Apr 2024 14:45:30 GMT  
		Size: 29.5 MB (29533949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a409a56a884202a6f273e7b4fb83a71297b32d0ba585aad0f61c0d8650ded1b7`  
		Last Modified: Fri, 31 May 2024 16:55:19 GMT  
		Size: 52.4 MB (52443020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8789137123d1abd91f5b5435b5f05f5febb161af874e2df33e84d61607f0fe54`  
		Last Modified: Fri, 31 May 2024 16:55:17 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be8de7b293500cf803d77b39a1ba00a8232ee744d58fdd63521ec0d4317ff2b`  
		Last Modified: Fri, 31 May 2024 16:55:15 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.1.0.0_2` - unknown; unknown

```console
$ docker pull aerospike@sha256:f142dd53f7ea10c94f127778a4727fb9e8d3081c91142dd27044d4b10d105598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1945051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfb5b2e6e548c8af7dcbb29ae9c4a96f92c0ec2d9a5ae5b89c61d7dee1a16b8`

```dockerfile
```

-	Layers:
	-	`sha256:29f19f944a494c5b364be03b49afa5cdad7882195a67835a410e1b7832ee2c03`  
		Last Modified: Fri, 31 May 2024 16:55:18 GMT  
		Size: 1.9 MB (1916192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3aa26abc02a3f10584233803be26ee60d125b306303a0068eafcb394bf1a82`  
		Last Modified: Fri, 31 May 2024 16:55:17 GMT  
		Size: 28.9 KB (28859 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-7.1.0.0_2` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:6e5ee39fddb0160dd0a0165acaefd16aed564c0ed28b685b585541e89eda8637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79149502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ba54e5ef3d98c9376a61df2eefc72ca5b4fe90b26f031b8709772e831d810d`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Fri, 31 May 2024 01:15:47 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.0 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 31 May 2024 01:15:47 GMT
ARG AEROSPIKE_EDITION=enterprise
# Fri, 31 May 2024 01:15:47 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.0/aerospike-server-enterprise_7.1.0.0_tools-11.0.0_ubuntu22.04_x86_64.tgz
# Fri, 31 May 2024 01:15:47 GMT
ARG AEROSPIKE_SHA_X86_64=6046f85cd37ebbbca8f3ad7a2079954a223de5a433ddb34104a8362846bdd002
# Fri, 31 May 2024 01:15:47 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.0/aerospike-server-enterprise_7.1.0.0_tools-11.0.0_ubuntu22.04_aarch64.tgz
# Fri, 31 May 2024 01:15:47 GMT
ARG AEROSPIKE_SHA_AARCH64=20f50036269a1b59b611dae35952f80f77fdd549355590011af9fa51c7c1a94f
# Fri, 31 May 2024 01:15:47 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 31 May 2024 01:15:47 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.0/aerospike-server-enterprise_7.1.0.0_tools-11.0.0_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=6046f85cd37ebbbca8f3ad7a2079954a223de5a433ddb34104a8362846bdd002 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.0/aerospike-server-enterprise_7.1.0.0_tools-11.0.0_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=20f50036269a1b59b611dae35952f80f77fdd549355590011af9fa51c7c1a94f
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 31 May 2024 01:15:47 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 31 May 2024 01:15:47 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 31 May 2024 01:15:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 31 May 2024 01:15:47 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 31 May 2024 01:15:47 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:d5a2ad729c09fbfdb259ae764f92188efc67a615ffde9bb34a46298d1edf3cd6`  
		Last Modified: Sat, 27 Apr 2024 14:45:36 GMT  
		Size: 27.4 MB (27360530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806b90243c12d7390c841eaa9cd11b07bbaeba047e8b523a9089b6c305110526`  
		Last Modified: Sat, 01 Jun 2024 00:17:57 GMT  
		Size: 51.8 MB (51786683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03eb6a29f601d9a08074dcfbfe74f52fb059f0b9eb6a82de61717a4159b76bc6`  
		Last Modified: Sat, 01 Jun 2024 00:17:55 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b4cbc2c8fe1563c73bc517402c3ed29bf765e5a228de2796a37cb857ccee82`  
		Last Modified: Sat, 01 Jun 2024 00:17:55 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.1.0.0_2` - unknown; unknown

```console
$ docker pull aerospike@sha256:c1cb0a4c27b22f77e20cb0c3490a70e8eb182d00d211c32d6af556481ae4e7de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1947504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea156605a76631e327cb63148d0a0af519388f2051597702c8755473c8b3843c`

```dockerfile
```

-	Layers:
	-	`sha256:097727ef0fc95e79b845b83cb74457955b22ea031674df4c4fb7cc3c4ad0fea9`  
		Last Modified: Sat, 01 Jun 2024 00:17:56 GMT  
		Size: 1.9 MB (1918368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22d78e2942e2b8b95216b6bd171bd45da4fbf49a00617fb53b4b26fa7365cf5b`  
		Last Modified: Sat, 01 Jun 2024 00:17:55 GMT  
		Size: 29.1 KB (29136 bytes)  
		MIME: application/vnd.in-toto+json
