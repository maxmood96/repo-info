## `aerospike:ee-7.1.0.6`

```console
$ docker pull aerospike@sha256:c572adf48dc5256dbf59966997ce59bc717373b7023257bdcf62312ca8280cef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-7.1.0.6` - linux; amd64

```console
$ docker pull aerospike@sha256:70407b1843e03810cb6b0042955d3e7de0c79ee72b098221ac7ae9508af5635d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.2 MB (82175908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71aeef2a7c0c8e388acfb380d19a98afbe124eb7a041115bc02cb276c783b00d`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Sat, 14 Sep 2024 10:22:53 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.6 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Sat, 14 Sep 2024 10:22:53 GMT
ARG AEROSPIKE_EDITION=enterprise
# Sat, 14 Sep 2024 10:22:53 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.6/aerospike-server-enterprise_7.1.0.6_tools-11.0.2_ubuntu22.04_x86_64.tgz
# Sat, 14 Sep 2024 10:22:53 GMT
ARG AEROSPIKE_SHA_X86_64=a9c6cee762efe92151117166da89c82637bb82aad80bffeb2972827e7581e23a
# Sat, 14 Sep 2024 10:22:53 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.6/aerospike-server-enterprise_7.1.0.6_tools-11.0.2_ubuntu22.04_aarch64.tgz
# Sat, 14 Sep 2024 10:22:53 GMT
ARG AEROSPIKE_SHA_AARCH64=148b362f1bd829aabf9e76525c2d9f7fc7ba07e9f43d293b9907f09acb8e7e4d
# Sat, 14 Sep 2024 10:22:53 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Sat, 14 Sep 2024 10:22:53 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.6/aerospike-server-enterprise_7.1.0.6_tools-11.0.2_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=a9c6cee762efe92151117166da89c82637bb82aad80bffeb2972827e7581e23a AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.6/aerospike-server-enterprise_7.1.0.6_tools-11.0.2_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=148b362f1bd829aabf9e76525c2d9f7fc7ba07e9f43d293b9907f09acb8e7e4d
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Sat, 14 Sep 2024 10:22:53 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Sat, 14 Sep 2024 10:22:53 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Sat, 14 Sep 2024 10:22:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Sep 2024 10:22:53 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Sat, 14 Sep 2024 10:22:53 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fea90d54466cfb015d71f0649485c7dca61035a3725edee84d05074520d490`  
		Last Modified: Mon, 16 Sep 2024 17:56:49 GMT  
		Size: 52.6 MB (52637595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ae3afa3d84b6418321321356daad31bfda14158e888476bd66de28b3ae1a0f`  
		Last Modified: Mon, 16 Sep 2024 17:56:48 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8ac946ccc4a02525fe6c328cb68bbddf888e34e33f4eab1f3aa275106a80c3`  
		Last Modified: Mon, 16 Sep 2024 17:56:48 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.1.0.6` - unknown; unknown

```console
$ docker pull aerospike@sha256:398ea970931ac90b9340dd1367caeafb628bf4843d2e45448f2452bd532212a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1971589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04fcb596585067053f10fcfe47c44d3db4fd4e1a6e13bb56148feefe469517d`

```dockerfile
```

-	Layers:
	-	`sha256:209e16c0c7fb5d75d2e89128f8a37cbc62f56bd94adc896f1169bc8f03f269fc`  
		Last Modified: Mon, 16 Sep 2024 17:56:48 GMT  
		Size: 1.9 MB (1942681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:339eaaf26b1a8e8d35c08ed5e933d9e0040bde06b2a638cff525e18befeb251e`  
		Last Modified: Mon, 16 Sep 2024 17:56:48 GMT  
		Size: 28.9 KB (28908 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-7.1.0.6` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:6515b750529a92b82c87cf2fdbeb76d1df00ae3b12db19046161e9e12d2b36ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79284995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0139968830320a6174e288f5044bb2b1c43c87177735cb8c9817af892e556a4b`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Sat, 14 Sep 2024 10:22:53 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.6 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Sat, 14 Sep 2024 10:22:53 GMT
ARG AEROSPIKE_EDITION=enterprise
# Sat, 14 Sep 2024 10:22:53 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.6/aerospike-server-enterprise_7.1.0.6_tools-11.0.2_ubuntu22.04_x86_64.tgz
# Sat, 14 Sep 2024 10:22:53 GMT
ARG AEROSPIKE_SHA_X86_64=a9c6cee762efe92151117166da89c82637bb82aad80bffeb2972827e7581e23a
# Sat, 14 Sep 2024 10:22:53 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.6/aerospike-server-enterprise_7.1.0.6_tools-11.0.2_ubuntu22.04_aarch64.tgz
# Sat, 14 Sep 2024 10:22:53 GMT
ARG AEROSPIKE_SHA_AARCH64=148b362f1bd829aabf9e76525c2d9f7fc7ba07e9f43d293b9907f09acb8e7e4d
# Sat, 14 Sep 2024 10:22:53 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Sat, 14 Sep 2024 10:22:53 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.6/aerospike-server-enterprise_7.1.0.6_tools-11.0.2_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=a9c6cee762efe92151117166da89c82637bb82aad80bffeb2972827e7581e23a AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.6/aerospike-server-enterprise_7.1.0.6_tools-11.0.2_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=148b362f1bd829aabf9e76525c2d9f7fc7ba07e9f43d293b9907f09acb8e7e4d
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Sat, 14 Sep 2024 10:22:53 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Sat, 14 Sep 2024 10:22:53 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Sat, 14 Sep 2024 10:22:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Sep 2024 10:22:53 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Sat, 14 Sep 2024 10:22:53 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476cf277da71ceea6daac94f8b7ed57577bf32ac4222ccb3d3fbacaf0176dcec`  
		Last Modified: Mon, 16 Sep 2024 17:56:48 GMT  
		Size: 51.9 MB (51924025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee5c493e89ebbadb868e2f3690158bf5d57c5cca922161dbac3409f6c7e385e`  
		Last Modified: Mon, 16 Sep 2024 17:56:46 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f408430b40de93258d371de8576df23e739bce8020ed64ca100bd12c124ab8e0`  
		Last Modified: Mon, 16 Sep 2024 17:56:46 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.1.0.6` - unknown; unknown

```console
$ docker pull aerospike@sha256:8c7de770676e5be5a7eb4c73fe9aa4088807630e248e34b35d59811b1873bc0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1973236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67aae757b219bea74cbaf7b0b3b95d67869a6a318690e0bbe22dd47bb21f3598`

```dockerfile
```

-	Layers:
	-	`sha256:00765aa9a43b0cd2356b5fccbd84c971df8b9100cce6c4b49f2935aa655084cc`  
		Last Modified: Mon, 16 Sep 2024 17:56:46 GMT  
		Size: 1.9 MB (1944052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:640520ab113ca97034508e023d73e7a1721de87b8bdf86da18c3f07f6938310f`  
		Last Modified: Mon, 16 Sep 2024 17:56:46 GMT  
		Size: 29.2 KB (29184 bytes)  
		MIME: application/vnd.in-toto+json
