## `aerospike:ee-7.1.0.4`

```console
$ docker pull aerospike@sha256:55e5fc5109752961f811fb88adb74d6da04b39c6a81238f7b3df183273beff14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `aerospike:ee-7.1.0.4` - linux; amd64

```console
$ docker pull aerospike@sha256:4ffb19bd3d174c05244f1ffd784812c0486b1af006500f069a62d7b3f4cb00ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80668378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8322daf9a5f13d6a7679e5255c62f1664a229b1a86576d493e746f98bcd389`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 25 Jul 2024 02:10:16 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.4 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 25 Jul 2024 02:10:16 GMT
ARG AEROSPIKE_EDITION=enterprise
# Thu, 25 Jul 2024 02:10:16 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.4/aerospike-server-enterprise_7.1.0.4_tools-11.0.2_ubuntu22.04_x86_64.tgz
# Thu, 25 Jul 2024 02:10:16 GMT
ARG AEROSPIKE_SHA_X86_64=4c0b1111b36ee1ef92cf3d3f05d8a94153e625deb9402895242d416138ab4ce0
# Thu, 25 Jul 2024 02:10:16 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.4/aerospike-server-enterprise_7.1.0.4_tools-11.0.2_ubuntu22.04_aarch64.tgz
# Thu, 25 Jul 2024 02:10:16 GMT
ARG AEROSPIKE_SHA_AARCH64=02d1eb109ad21abcbd898cb0f31b221f888f98489b400d73ac39031c6ada8afd
# Thu, 25 Jul 2024 02:10:16 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 25 Jul 2024 02:10:16 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.4/aerospike-server-enterprise_7.1.0.4_tools-11.0.2_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=4c0b1111b36ee1ef92cf3d3f05d8a94153e625deb9402895242d416138ab4ce0 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.4/aerospike-server-enterprise_7.1.0.4_tools-11.0.2_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=02d1eb109ad21abcbd898cb0f31b221f888f98489b400d73ac39031c6ada8afd
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 25 Jul 2024 02:10:16 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 25 Jul 2024 02:10:16 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 25 Jul 2024 02:10:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Jul 2024 02:10:16 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 25 Jul 2024 02:10:16 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b519cb0cb88ebfde35c9af70be7b16d2f659b4105a1fa77b1863aeab21d3697f`  
		Last Modified: Thu, 25 Jul 2024 20:08:42 GMT  
		Size: 51.1 MB (51132033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92806e0aaf731cbf6bb8d3fa2c1e41fb2d25f419a08e8fbe189a7fe6903ba2d0`  
		Last Modified: Thu, 25 Jul 2024 20:08:39 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2e2edd47e10ade7484e3819b9de8589743baf8469e4ff76d8908c9427bb981`  
		Last Modified: Thu, 25 Jul 2024 20:08:39 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.1.0.4` - unknown; unknown

```console
$ docker pull aerospike@sha256:4a7bc82f8131f20f8402af66bcae472e14df6435aa2708d8fd3725e797145b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1970015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad81e84dcf5cc54ebf6d937938643685f8aa0f7f56988e9d4290d31dbb24d35b`

```dockerfile
```

-	Layers:
	-	`sha256:a944503948278ca558f03fd801d59053ed2b1ea4f1e865ea12ad5130ffbda3e1`  
		Last Modified: Thu, 25 Jul 2024 20:08:40 GMT  
		Size: 1.9 MB (1941107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190bddde1702fa8a3b63642867d5ed0eaf77684263b25f4053a4ea7927438435`  
		Last Modified: Thu, 25 Jul 2024 20:08:39 GMT  
		Size: 28.9 KB (28908 bytes)  
		MIME: application/vnd.in-toto+json
