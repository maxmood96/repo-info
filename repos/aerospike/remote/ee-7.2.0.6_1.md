## `aerospike:ee-7.2.0.6_1`

```console
$ docker pull aerospike@sha256:d5c2e0b2b46a9f15b3f3b15c7ebbb8cad1e9e2cf9fe1152391a5f1b49c531120
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-7.2.0.6_1` - linux; amd64

```console
$ docker pull aerospike@sha256:8820989a84be1520c5e238e1a0ab1f1d2d635b4a15cea1534ed2eb3ccb01fcd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81694732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b056f2b65497745a011072d57c409d4b7b23189e0332d5600be421eacd0b3879`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Fri, 03 Jan 2025 06:32:37 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.2.0.6 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 03 Jan 2025 06:32:37 GMT
ARG AEROSPIKE_EDITION=enterprise
# Fri, 03 Jan 2025 06:32:37 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.6/aerospike-server-enterprise_7.2.0.6_tools-11.1.1_ubuntu24.04_x86_64.tgz
# Fri, 03 Jan 2025 06:32:37 GMT
ARG AEROSPIKE_SHA_X86_64=de6ac63d85e12bcac6671b28ad5bb8e850f5cf02643ebea34efa3778a2036f4d
# Fri, 03 Jan 2025 06:32:37 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.6/aerospike-server-enterprise_7.2.0.6_tools-11.1.1_ubuntu24.04_aarch64.tgz
# Fri, 03 Jan 2025 06:32:37 GMT
ARG AEROSPIKE_SHA_AARCH64=8b3d3eb31f18eaf015ed675954c1561110f839378029d3c46a742d9b2c97922d
# Fri, 03 Jan 2025 06:32:37 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 03 Jan 2025 06:32:37 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.6/aerospike-server-enterprise_7.2.0.6_tools-11.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=de6ac63d85e12bcac6671b28ad5bb8e850f5cf02643ebea34efa3778a2036f4d AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.6/aerospike-server-enterprise_7.2.0.6_tools-11.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=8b3d3eb31f18eaf015ed675954c1561110f839378029d3c46a742d9b2c97922d
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 03 Jan 2025 06:32:37 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 03 Jan 2025 06:32:37 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 03 Jan 2025 06:32:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Jan 2025 06:32:37 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 03 Jan 2025 06:32:37 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe97bcb3b5c24706c7a0381228e1c41c1440d69c989f07289c612437bb69ab1`  
		Last Modified: Tue, 07 Jan 2025 01:30:23 GMT  
		Size: 51.9 MB (51940466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1911d34d1753e1f608f1bd7d1e493332578b2ab73a0a305dc2b934b881401006`  
		Last Modified: Tue, 07 Jan 2025 01:30:23 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47893e2b46fdfd09be3dd9d42ae3355884d36ae8015337fcae4b616fb56fd7d5`  
		Last Modified: Tue, 07 Jan 2025 01:30:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.2.0.6_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:3a14cf287bd8a3fcaf7f0deafd1763a457c4c258be07c6015ca43cf83ca05035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1985366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c89799a852a9b580c6e3b7bc1ec1310ec2c57d911e4079fdde6458f66c7ace`

```dockerfile
```

-	Layers:
	-	`sha256:4b187a0c6fe973985e56c91782b9351ccc840f8110cc6a4438b7bc69c6776186`  
		Last Modified: Tue, 07 Jan 2025 01:30:23 GMT  
		Size: 2.0 MB (1956203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:697940b78d3e3beb85b5358530e0b1a6748e9cf6d3a8e78983dd423f5e64c070`  
		Last Modified: Tue, 07 Jan 2025 01:30:23 GMT  
		Size: 29.2 KB (29163 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-7.2.0.6_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:55510e50725fee2c3f360c774afb1815d4df6551e8836e4aa5d47afb0e8a5ab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80292132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6cb5d54b617429c8d72f7163ca9b6df9272fcf52da59c99b9020a13e71250ac`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Fri, 03 Jan 2025 06:32:37 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.2.0.6 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 03 Jan 2025 06:32:37 GMT
ARG AEROSPIKE_EDITION=enterprise
# Fri, 03 Jan 2025 06:32:37 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.6/aerospike-server-enterprise_7.2.0.6_tools-11.1.1_ubuntu24.04_x86_64.tgz
# Fri, 03 Jan 2025 06:32:37 GMT
ARG AEROSPIKE_SHA_X86_64=de6ac63d85e12bcac6671b28ad5bb8e850f5cf02643ebea34efa3778a2036f4d
# Fri, 03 Jan 2025 06:32:37 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.6/aerospike-server-enterprise_7.2.0.6_tools-11.1.1_ubuntu24.04_aarch64.tgz
# Fri, 03 Jan 2025 06:32:37 GMT
ARG AEROSPIKE_SHA_AARCH64=8b3d3eb31f18eaf015ed675954c1561110f839378029d3c46a742d9b2c97922d
# Fri, 03 Jan 2025 06:32:37 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 03 Jan 2025 06:32:37 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.6/aerospike-server-enterprise_7.2.0.6_tools-11.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=de6ac63d85e12bcac6671b28ad5bb8e850f5cf02643ebea34efa3778a2036f4d AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.6/aerospike-server-enterprise_7.2.0.6_tools-11.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=8b3d3eb31f18eaf015ed675954c1561110f839378029d3c46a742d9b2c97922d
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 03 Jan 2025 06:32:37 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 03 Jan 2025 06:32:37 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 03 Jan 2025 06:32:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Jan 2025 06:32:37 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 03 Jan 2025 06:32:37 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a781e7faba116405f27cb7549963b740bb666c485d235b7fb65ed627ba690d`  
		Last Modified: Tue, 07 Jan 2025 02:51:57 GMT  
		Size: 51.4 MB (51397159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40c12714aa593930761394cb7bf335031c47a0ffcda22438172a49593a8b206`  
		Last Modified: Tue, 07 Jan 2025 02:51:54 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41691579814abc33c07d61fa256b1f7d29cfb27fa77f44dc488af416fc082132`  
		Last Modified: Tue, 07 Jan 2025 02:51:54 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.2.0.6_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:7c365c8afd79e23272c902190e5d80530d4191bfa291b50b43e189672d71ac5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1987726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6928be37529bd021b9fe54f9a7c848400b9204e8544ec48048cfd95c7e2b92d6`

```dockerfile
```

-	Layers:
	-	`sha256:219de40bd43debcf13132335f58887f3489f07169bc405261fb655ea1d1a5d26`  
		Last Modified: Tue, 07 Jan 2025 02:51:55 GMT  
		Size: 2.0 MB (1958483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:164d03d8b0b15d862f1ec39a13c4476bf22cfe17aa4e35024896c91be01f3a5e`  
		Last Modified: Tue, 07 Jan 2025 02:51:54 GMT  
		Size: 29.2 KB (29243 bytes)  
		MIME: application/vnd.in-toto+json
