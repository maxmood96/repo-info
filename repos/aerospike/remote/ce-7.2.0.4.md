## `aerospike:ce-7.2.0.4`

```console
$ docker pull aerospike@sha256:f371c5264efbad9072eb7013a641c7e0624cd24263143d34170902d4f61db4f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-7.2.0.4` - linux; amd64

```console
$ docker pull aerospike@sha256:c7a7927e288abd7419cbd53e38cbc2cb31c2ae6301980b1b8ea35cb00782f5c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77539925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b41440d9efd383bac03caed62c06b6fd01f73b38265d3a611ff81117f18f2c9c`
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
# Thu, 21 Nov 2024 04:27:43 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.2.0.4 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 21 Nov 2024 04:27:43 GMT
ARG AEROSPIKE_EDITION=community
# Thu, 21 Nov 2024 04:27:43 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.4/aerospike-server-community_7.2.0.4_tools-11.1.1_ubuntu24.04_x86_64.tgz
# Thu, 21 Nov 2024 04:27:43 GMT
ARG AEROSPIKE_SHA_X86_64=381f61a93eea93d436ed3d4a810da15d90d7f5db7bfda51e807bb90a59263fb8
# Thu, 21 Nov 2024 04:27:43 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.4/aerospike-server-community_7.2.0.4_tools-11.1.1_ubuntu24.04_aarch64.tgz
# Thu, 21 Nov 2024 04:27:43 GMT
ARG AEROSPIKE_SHA_AARCH64=acdc3070ccdb7f24fc8b1fc1762eb803770a73db93d84d4eb3cdffdbccebf89a
# Thu, 21 Nov 2024 04:27:43 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 21 Nov 2024 04:27:43 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.4/aerospike-server-community_7.2.0.4_tools-11.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=381f61a93eea93d436ed3d4a810da15d90d7f5db7bfda51e807bb90a59263fb8 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.4/aerospike-server-community_7.2.0.4_tools-11.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=acdc3070ccdb7f24fc8b1fc1762eb803770a73db93d84d4eb3cdffdbccebf89a
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 21 Nov 2024 04:27:43 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 21 Nov 2024 04:27:43 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 21 Nov 2024 04:27:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 21 Nov 2024 04:27:43 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 21 Nov 2024 04:27:43 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449d17590cad94c7955a2e39cf4ca63d1a089cc996e65101a163d5a106adb5ec`  
		Last Modified: Tue, 03 Dec 2024 02:16:03 GMT  
		Size: 47.8 MB (47785652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95af2c8207a15d7f79b97c44c92e07c7b4908b6827ed0bb7026a880337d9f2f9`  
		Last Modified: Tue, 03 Dec 2024 02:16:01 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9f204dada651e4275a9e2e90afa449394662124cab8f3c9f8bc23e8700d372`  
		Last Modified: Tue, 03 Dec 2024 02:16:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-7.2.0.4` - unknown; unknown

```console
$ docker pull aerospike@sha256:8be4f65adc88844449881bf6f4fe066c50cfe37a82bbab13b16e962cfb54c28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1892021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf89dcce435f8c1c2f6a49e98135754112c0042ccd1ddfd53ff3df8847cdaa99`

```dockerfile
```

-	Layers:
	-	`sha256:b720efc4a670f5aff71d62721c03b3fc43d5c599b58490d4956cc0f19db58392`  
		Last Modified: Tue, 03 Dec 2024 02:16:02 GMT  
		Size: 1.9 MB (1862875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a4be66e9d90cb9312009049850e086f568a6bb07e44ca04b1842d872f33905a`  
		Last Modified: Tue, 03 Dec 2024 02:16:01 GMT  
		Size: 29.1 KB (29146 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-7.2.0.4` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:ffeac88e4e979890dba4f4d91b74d6fd7dcf362d66ada31fe9d460b5c48985d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76106657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a8e98bee563dfd4da46cf1d3cb2df3e89d16d31feb8314cec6d30708aa5ab9`
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
# Thu, 21 Nov 2024 04:27:43 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.2.0.4 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 21 Nov 2024 04:27:43 GMT
ARG AEROSPIKE_EDITION=community
# Thu, 21 Nov 2024 04:27:43 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.4/aerospike-server-community_7.2.0.4_tools-11.1.1_ubuntu24.04_x86_64.tgz
# Thu, 21 Nov 2024 04:27:43 GMT
ARG AEROSPIKE_SHA_X86_64=381f61a93eea93d436ed3d4a810da15d90d7f5db7bfda51e807bb90a59263fb8
# Thu, 21 Nov 2024 04:27:43 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.4/aerospike-server-community_7.2.0.4_tools-11.1.1_ubuntu24.04_aarch64.tgz
# Thu, 21 Nov 2024 04:27:43 GMT
ARG AEROSPIKE_SHA_AARCH64=acdc3070ccdb7f24fc8b1fc1762eb803770a73db93d84d4eb3cdffdbccebf89a
# Thu, 21 Nov 2024 04:27:43 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 21 Nov 2024 04:27:43 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.4/aerospike-server-community_7.2.0.4_tools-11.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=381f61a93eea93d436ed3d4a810da15d90d7f5db7bfda51e807bb90a59263fb8 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.2.0.4/aerospike-server-community_7.2.0.4_tools-11.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=acdc3070ccdb7f24fc8b1fc1762eb803770a73db93d84d4eb3cdffdbccebf89a
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 21 Nov 2024 04:27:43 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 21 Nov 2024 04:27:43 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 21 Nov 2024 04:27:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 21 Nov 2024 04:27:43 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 21 Nov 2024 04:27:43 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443e137c0a9f7b1987f41c0aeafd98f438718efd1236cc9e9fb85a1274551e3d`  
		Last Modified: Tue, 03 Dec 2024 05:38:19 GMT  
		Size: 47.2 MB (47211684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775defc9162795b48df892c38658cc3b93b3944e66a73753fb24897e6cb3eb00`  
		Last Modified: Tue, 03 Dec 2024 05:38:17 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d8de6b8a5143453ac0253f6550f3e6e07685b446396e803e672e2abade86a1`  
		Last Modified: Tue, 03 Dec 2024 05:38:18 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-7.2.0.4` - unknown; unknown

```console
$ docker pull aerospike@sha256:8355c46124c7c48d152f3c8a28d10eedc1141de0e42fa8b2417ad4ccb6d271e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1894355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1896940732b6d9d48fa9306c9b10d9ed7d56e7d7aa78a4f8bee38d6194f6e251`

```dockerfile
```

-	Layers:
	-	`sha256:0572e71bb03a8af0150dc0e6b761c1d9ab6a4d3105697e0cd0ffc9bcc4c17df0`  
		Last Modified: Tue, 03 Dec 2024 05:38:18 GMT  
		Size: 1.9 MB (1865128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec26767a2999fa69fdc4216e47e1ae4cd7514afb47da2b218c711fa6dbbc188f`  
		Last Modified: Tue, 03 Dec 2024 05:38:17 GMT  
		Size: 29.2 KB (29227 bytes)  
		MIME: application/vnd.in-toto+json
