## `aerospike:ce-8.0.0.5`

```console
$ docker pull aerospike@sha256:a07890aef5848073c1ce6e80c6396a3de0db91e839ed947c2ac8bc56397a3bcd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.0.0.5` - linux; amd64

```console
$ docker pull aerospike@sha256:b6e3a4dede64b42f30b37c0edbf5ecc377e3fdd9718f7849b70ef3798f3dd7e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77712179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f04b8165493588a5131d2c4421e55645405d83f3ce583a2272530ab3bb4bb4`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 25 Feb 2025 21:03:12 GMT
ARG RELEASE
# Tue, 25 Feb 2025 21:03:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Feb 2025 21:03:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Feb 2025 21:03:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 25 Feb 2025 21:03:12 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 25 Feb 2025 21:03:12 GMT
CMD ["/bin/bash"]
# Tue, 25 Feb 2025 21:03:12 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.5 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 25 Feb 2025 21:03:12 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 25 Feb 2025 21:03:12 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.5/aerospike-server-community_8.0.0.5_tools-11.2.0_ubuntu24.04_x86_64.tgz
# Tue, 25 Feb 2025 21:03:12 GMT
ARG AEROSPIKE_SHA_X86_64=1b1a6a54ffdcc8ac730ff90b65cb0730d0dee3d0dead2c739dea1dde06a8f03d
# Tue, 25 Feb 2025 21:03:12 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.5/aerospike-server-community_8.0.0.5_tools-11.2.0_ubuntu24.04_aarch64.tgz
# Tue, 25 Feb 2025 21:03:12 GMT
ARG AEROSPIKE_SHA_AARCH64=bfee481a114da219b359b1dd8d8fbc0efb833057427084d65a0fdf366dc9a03f
# Tue, 25 Feb 2025 21:03:12 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 25 Feb 2025 21:03:12 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.5/aerospike-server-community_8.0.0.5_tools-11.2.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=1b1a6a54ffdcc8ac730ff90b65cb0730d0dee3d0dead2c739dea1dde06a8f03d AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.5/aerospike-server-community_8.0.0.5_tools-11.2.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=bfee481a114da219b359b1dd8d8fbc0efb833057427084d65a0fdf366dc9a03f
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 25 Feb 2025 21:03:12 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 25 Feb 2025 21:03:12 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 25 Feb 2025 21:03:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 25 Feb 2025 21:03:12 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 25 Feb 2025 21:03:12 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286e4414dda2e28f7d025304fca180142fc4d2fd50c8964ed23bbec8e2db19ff`  
		Last Modified: Wed, 09 Apr 2025 01:11:44 GMT  
		Size: 48.0 MB (47992229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b7cef9874c05e0f2554eead572ae601cd4b5be925d5debe0e8bf933bd9abc2`  
		Last Modified: Wed, 09 Apr 2025 01:11:43 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80c852c0528de44fd725b28fec1aabbc6c67183f6a3e7f37e6f2eda94a1faf9`  
		Last Modified: Wed, 09 Apr 2025 01:11:43 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.0.0.5` - unknown; unknown

```console
$ docker pull aerospike@sha256:572edcd0a4701597a94857acfe291a4ea48bcada2066f41b5a6e0dae8182fa67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1893195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f40e84fcd856d8d9feb3a41fec756e57f76e0fcdda5471576a3bfc05f1e20c`

```dockerfile
```

-	Layers:
	-	`sha256:2a811c482260d9b7cd1f709e2e91292b25b096e3366a23a1fdd70d107971a5f3`  
		Last Modified: Wed, 09 Apr 2025 01:11:43 GMT  
		Size: 1.9 MB (1864048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b156baa0e6e8c56e190b1fb0188949b76d7ae8b9e510fa549378f6b135cc45f1`  
		Last Modified: Wed, 09 Apr 2025 01:11:43 GMT  
		Size: 29.1 KB (29147 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.0.0.5` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:203ebe4960cd6b48117416d5350f4a8203faf7366b86beff0796c515fa54a0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78515837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33cb776caac21e4d06d26f26506e0e79e9422c029126befbfd84d211896b7d04`
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
# Tue, 25 Feb 2025 21:03:12 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.5 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 25 Feb 2025 21:03:12 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 25 Feb 2025 21:03:12 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.5/aerospike-server-community_8.0.0.5_tools-11.2.0_ubuntu24.04_x86_64.tgz
# Tue, 25 Feb 2025 21:03:12 GMT
ARG AEROSPIKE_SHA_X86_64=1b1a6a54ffdcc8ac730ff90b65cb0730d0dee3d0dead2c739dea1dde06a8f03d
# Tue, 25 Feb 2025 21:03:12 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.5/aerospike-server-community_8.0.0.5_tools-11.2.0_ubuntu24.04_aarch64.tgz
# Tue, 25 Feb 2025 21:03:12 GMT
ARG AEROSPIKE_SHA_AARCH64=bfee481a114da219b359b1dd8d8fbc0efb833057427084d65a0fdf366dc9a03f
# Tue, 25 Feb 2025 21:03:12 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 25 Feb 2025 21:03:12 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.5/aerospike-server-community_8.0.0.5_tools-11.2.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=1b1a6a54ffdcc8ac730ff90b65cb0730d0dee3d0dead2c739dea1dde06a8f03d AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.5/aerospike-server-community_8.0.0.5_tools-11.2.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=bfee481a114da219b359b1dd8d8fbc0efb833057427084d65a0fdf366dc9a03f
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 25 Feb 2025 21:03:12 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 25 Feb 2025 21:03:12 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 25 Feb 2025 21:03:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 25 Feb 2025 21:03:12 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 25 Feb 2025 21:03:12 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb4c8d38d99c76121c213a1baa8a8c1ebe0b9d89560fcd65ae8fc1fc896cdce`  
		Last Modified: Tue, 25 Feb 2025 23:38:10 GMT  
		Size: 49.6 MB (49619939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ed8249a9b4f153349323faf9be100ce7f3a441d57e1b90b918ab6bcfef45c8`  
		Last Modified: Tue, 25 Feb 2025 23:38:08 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93475464b1629145142cd3a5d50c7c6085c2c832ef91b256e7eb77c67856bc13`  
		Last Modified: Tue, 25 Feb 2025 23:38:08 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.0.0.5` - unknown; unknown

```console
$ docker pull aerospike@sha256:d132611d7dd8f731657a88f5d3af1afeae2e827f3c7b3fe83a70ef19460a7ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1897763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97642334fc881755c52c13c3706888cba4dda3e5f9ec13dd689621ec9e8e1480`

```dockerfile
```

-	Layers:
	-	`sha256:f2a3145a00b8bc600564c1c7775140eb2e586a4215ae612bb6a49eee8480e1d1`  
		Last Modified: Tue, 25 Feb 2025 23:38:08 GMT  
		Size: 1.9 MB (1868537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ff418e10e738f47f169e7283c901e2f8337b91c5ba6e5103ca6fe1effaf86f`  
		Last Modified: Tue, 25 Feb 2025 23:38:08 GMT  
		Size: 29.2 KB (29226 bytes)  
		MIME: application/vnd.in-toto+json
