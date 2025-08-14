## `aerospike:ee-8.1.0.0_1`

```console
$ docker pull aerospike@sha256:5c3daa052d4b3aa2b04fdccb54fdbe19cc46e76e44695102ab6eb09baaebf179
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.1.0.0_1` - linux; amd64

```console
$ docker pull aerospike@sha256:df16cdfe1379f6f63f8916bfebdcd255a8701f27d21953b69c73a4156e489fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83811439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e349f4abdd83458dd7a712dd87d21812303e6578c5e0ec2a3493e19aa2af02`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 17:58:51 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.0.0 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 05 Aug 2025 17:58:51 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 05 Aug 2025 17:58:51 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 05 Aug 2025 17:58:51 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.0/aerospike-server-enterprise_8.1.0.0_tools-12.0.0_ubuntu24.04_x86_64.tgz
# Tue, 05 Aug 2025 17:58:51 GMT
ARG AEROSPIKE_SHA_X86_64=337b006397cc3c985618d80168c1ae9e546ae3be00b5f6f84413e6376a27e4af
# Tue, 05 Aug 2025 17:58:51 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.0/aerospike-server-enterprise_8.1.0.0_tools-12.0.0_ubuntu24.04_aarch64.tgz
# Tue, 05 Aug 2025 17:58:51 GMT
ARG AEROSPIKE_SHA_AARCH64=a1bea0974dd76e4a6a672e47bd5e9cb0990d6dee8e90b61e8ecbf0ee13c59771
# Tue, 05 Aug 2025 17:58:51 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 05 Aug 2025 17:58:51 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.0/aerospike-server-enterprise_8.1.0.0_tools-12.0.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=337b006397cc3c985618d80168c1ae9e546ae3be00b5f6f84413e6376a27e4af AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.0/aerospike-server-enterprise_8.1.0.0_tools-12.0.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=a1bea0974dd76e4a6a672e47bd5e9cb0990d6dee8e90b61e8ecbf0ee13c59771
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 05 Aug 2025 17:58:51 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 05 Aug 2025 17:58:51 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 05 Aug 2025 17:58:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 05 Aug 2025 17:58:51 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 05 Aug 2025 17:58:51 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262ae8a7dd5660827d5f458dedc1af8867dd82f48b451d1acfb156578ccac7dd`  
		Last Modified: Tue, 12 Aug 2025 17:23:54 GMT  
		Size: 54.1 MB (54085928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989f711753b9d345687dd7a881e6ffb60ec6f42dc717b6e1db36d490c0428e38`  
		Last Modified: Tue, 12 Aug 2025 17:23:49 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6471798344051437c90654161bc7414fde3cf281d9b179f8e5f162182119db9`  
		Last Modified: Tue, 12 Aug 2025 17:23:50 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.0.0_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:f9966ec3e4aaffdee97c45cb5abdbe556cc40a2dd94dbb167f5ce327bde5971d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5659a405d8e062f9219556fc44f0e111bce165228674fadb04e7e0e4a014081`

```dockerfile
```

-	Layers:
	-	`sha256:21ffeb3e903273ce6d7e63123c3c0482cfd264dfb6d774bd290358844edeccf7`  
		Last Modified: Tue, 12 Aug 2025 20:25:29 GMT  
		Size: 2.2 MB (2182949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9d3df4e17f0e341069e2be8800ef22d408f06e696b861b4c300802a1d20cadb`  
		Last Modified: Tue, 12 Aug 2025 20:25:30 GMT  
		Size: 29.0 KB (29028 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.1.0.0_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:d64195417f0738c75a19c5f1125b4611b616654e760f78d0288ac4b7ad9b5127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.2 MB (82171381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5929f97830d28eaaee765eb559dbbc159cf28b85bd7c132e47ee53d3c00e869e`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Tue, 05 Aug 2025 17:58:51 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.0.0 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 05 Aug 2025 17:58:51 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 05 Aug 2025 17:58:51 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 05 Aug 2025 17:58:51 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.0/aerospike-server-enterprise_8.1.0.0_tools-12.0.0_ubuntu24.04_x86_64.tgz
# Tue, 05 Aug 2025 17:58:51 GMT
ARG AEROSPIKE_SHA_X86_64=337b006397cc3c985618d80168c1ae9e546ae3be00b5f6f84413e6376a27e4af
# Tue, 05 Aug 2025 17:58:51 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.0/aerospike-server-enterprise_8.1.0.0_tools-12.0.0_ubuntu24.04_aarch64.tgz
# Tue, 05 Aug 2025 17:58:51 GMT
ARG AEROSPIKE_SHA_AARCH64=a1bea0974dd76e4a6a672e47bd5e9cb0990d6dee8e90b61e8ecbf0ee13c59771
# Tue, 05 Aug 2025 17:58:51 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 05 Aug 2025 17:58:51 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.0/aerospike-server-enterprise_8.1.0.0_tools-12.0.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=337b006397cc3c985618d80168c1ae9e546ae3be00b5f6f84413e6376a27e4af AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.0/aerospike-server-enterprise_8.1.0.0_tools-12.0.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=a1bea0974dd76e4a6a672e47bd5e9cb0990d6dee8e90b61e8ecbf0ee13c59771
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 05 Aug 2025 17:58:51 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 05 Aug 2025 17:58:51 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 05 Aug 2025 17:58:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 05 Aug 2025 17:58:51 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 05 Aug 2025 17:58:51 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962e12b5fc143a5974e141234e5fba3f06c0d579640580b052cfb3d23c437998`  
		Last Modified: Tue, 12 Aug 2025 17:23:00 GMT  
		Size: 53.3 MB (53308709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1587bd7238b3d4eddd1abfa5b57d0c6399ab7f8385aa4a853a235f34ded84a`  
		Last Modified: Tue, 12 Aug 2025 17:22:53 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade3552a60cdd3fdc2e0e36c3253af073be72ef481a441a3874a35ba508c7e83`  
		Last Modified: Tue, 12 Aug 2025 17:22:53 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.0.0_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:50ace92c27e85af1ce1b86582d2c6d30856abe019f3b93da6f53dc9099047890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e5156c6804767bb11d5a98cf347a3fb96952e70d956456171f8d6bb338dc099`

```dockerfile
```

-	Layers:
	-	`sha256:dd9602858f577b0618daf976a29fde53863089e8a9dad45482eb5fcb07035c33`  
		Last Modified: Tue, 12 Aug 2025 20:25:36 GMT  
		Size: 2.2 MB (2185229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d5e16dfd427702dbf0ecedaa5cb7a052fffa7fd8b51413a7005c6e66f6b5276`  
		Last Modified: Tue, 12 Aug 2025 20:25:37 GMT  
		Size: 29.1 KB (29108 bytes)  
		MIME: application/vnd.in-toto+json
