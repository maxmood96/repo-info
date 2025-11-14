<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-8.1.0.1`](#aerospikece-8101)
-	[`aerospike:ce-8.1.0.1_1`](#aerospikece-8101_1)
-	[`aerospike:ee-8.1.0.1`](#aerospikeee-8101)
-	[`aerospike:ee-8.1.0.1_1`](#aerospikeee-8101_1)

## `aerospike:ce-8.1.0.1`

```console
$ docker pull aerospike@sha256:7c6a6dba33a7996d0f5b47f817c1c4f5ae49406425ef1530e641474bca449f9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.1.0.1` - linux; amd64

```console
$ docker pull aerospike@sha256:d1e3c07d58ededddb12fa63bae5e10215291a1474934ce71d202e6b4fd687e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81498417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9bd843413989da1ab058d03ec273551f6c8bcf778a2b210c7658207d269489`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Tue, 16 Sep 2025 00:43:00 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 00:43:00 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.0.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 16 Sep 2025 00:43:00 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.1/aerospike-server-community_8.1.0.1_tools-12.0.2_ubuntu24.04_x86_64.tgz
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_SHA_X86_64=54b0b0c6a16e780392129d3894f12a41c48ded7e82d003b12c832aee06e7e18e
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.1/aerospike-server-community_8.1.0.1_tools-12.0.2_ubuntu24.04_aarch64.tgz
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_SHA_AARCH64=69519f31202d4d79d9d118ceee5080009e693b5590b09d72d7f947342d9d0b27
# Tue, 16 Sep 2025 00:43:00 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 16 Sep 2025 00:43:00 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.1/aerospike-server-community_8.1.0.1_tools-12.0.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=54b0b0c6a16e780392129d3894f12a41c48ded7e82d003b12c832aee06e7e18e AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.1/aerospike-server-community_8.1.0.1_tools-12.0.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=69519f31202d4d79d9d118ceee5080009e693b5590b09d72d7f947342d9d0b27
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8083136e73ad99268ead5293c4ce34ccf5c6e47f01bc86317251baeaffae75d0`  
		Last Modified: Thu, 09 Oct 2025 21:08:20 GMT  
		Size: 51.8 MB (51772977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07eb93b5539b0d2da8b104128708e6483969e2cbb384f9b7853c2a2fb93d92c7`  
		Last Modified: Thu, 09 Oct 2025 21:08:14 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90cdfbb9fa7d7740d18d1900cdc9555e14513b1d0ed2b6327131b10236bcd13`  
		Last Modified: Thu, 09 Oct 2025 21:08:14 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.0.1` - unknown; unknown

```console
$ docker pull aerospike@sha256:dcaff2a41ff16f0406ee4177374d6ef286fee234f882d8376ec7b53d3005667a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba072864a0b241c4945c134d098f30013fbef36fcdd673436d4093069515db60`

```dockerfile
```

-	Layers:
	-	`sha256:a768085d1772b1f3a0eeb29cc0a4da06b62c59732c5984c887a47e179d17ae7c`  
		Last Modified: Thu, 09 Oct 2025 23:25:19 GMT  
		Size: 2.2 MB (2182312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ff3b1dda93bfebc6bb41f238ac7e6033756f40256b0ece84bfd812ad7b2690a`  
		Last Modified: Thu, 09 Oct 2025 23:25:20 GMT  
		Size: 29.0 KB (29012 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.1.0.1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:3c25e8ad406473edeae25f2f9b35dea99ac63274a01f9260abc4ea443923e725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79858272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0080a7cb82ce03b29ca4b68105251e94badada576368ccc39954264a743ab0e`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:08:28 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.0.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 13 Nov 2025 23:08:28 GMT
ARG AEROSPIKE_EDITION=community
# Thu, 13 Nov 2025 23:08:28 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Thu, 13 Nov 2025 23:08:28 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.1/aerospike-server-community_8.1.0.1_tools-12.0.2_ubuntu24.04_x86_64.tgz
# Thu, 13 Nov 2025 23:08:28 GMT
ARG AEROSPIKE_SHA_X86_64=54b0b0c6a16e780392129d3894f12a41c48ded7e82d003b12c832aee06e7e18e
# Thu, 13 Nov 2025 23:08:28 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.1/aerospike-server-community_8.1.0.1_tools-12.0.2_ubuntu24.04_aarch64.tgz
# Thu, 13 Nov 2025 23:08:28 GMT
ARG AEROSPIKE_SHA_AARCH64=69519f31202d4d79d9d118ceee5080009e693b5590b09d72d7f947342d9d0b27
# Thu, 13 Nov 2025 23:08:28 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 13 Nov 2025 23:08:28 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.1/aerospike-server-community_8.1.0.1_tools-12.0.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=54b0b0c6a16e780392129d3894f12a41c48ded7e82d003b12c832aee06e7e18e AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.1/aerospike-server-community_8.1.0.1_tools-12.0.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=69519f31202d4d79d9d118ceee5080009e693b5590b09d72d7f947342d9d0b27
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 13 Nov 2025 23:08:28 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 13 Nov 2025 23:08:28 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 13 Nov 2025 23:08:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:08:28 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 13 Nov 2025 23:08:28 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d81b7957697d1ad41a95be5d245bc1dfd9fe58026b21a399003d63da20753e3`  
		Last Modified: Thu, 13 Nov 2025 23:09:13 GMT  
		Size: 51.0 MB (50994021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea21b3704853c46716c3e1c881f9bbac8d55cb7c55390c8c554881781fdce41b`  
		Last Modified: Thu, 13 Nov 2025 23:09:07 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9e20289c819d375a761054386992958777bd95c5da3fd83db674090dbad986`  
		Last Modified: Thu, 13 Nov 2025 23:09:07 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.0.1` - unknown; unknown

```console
$ docker pull aerospike@sha256:7f4ddf9c6277f7ac618aed02fa01e1556fdf5a79b0274022c38301dd599b4609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2213641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba486d1a59a4c655f937964e471aecb1845a7171abcebee438190c048df6cfe`

```dockerfile
```

-	Layers:
	-	`sha256:2d459099673c18af1f2ce8f16659a339cfce08550fa520bd3b3ca8fada985b08`  
		Last Modified: Fri, 14 Nov 2025 00:25:32 GMT  
		Size: 2.2 MB (2184592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aec971a9e4935fb70184f1d5e8f4d337e63775a4684758bd3c149c243362d6af`  
		Last Modified: Fri, 14 Nov 2025 00:25:33 GMT  
		Size: 29.0 KB (29049 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ce-8.1.0.1_1`

```console
$ docker pull aerospike@sha256:20002b8202b96cada26c27db1e3b196628cc6bc9a18feeba13324a4862f35f39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.1.0.1_1` - linux; amd64

```console
$ docker pull aerospike@sha256:d1e3c07d58ededddb12fa63bae5e10215291a1474934ce71d202e6b4fd687e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81498417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9bd843413989da1ab058d03ec273551f6c8bcf778a2b210c7658207d269489`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Tue, 16 Sep 2025 00:43:00 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 00:43:00 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.0.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 16 Sep 2025 00:43:00 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.1/aerospike-server-community_8.1.0.1_tools-12.0.2_ubuntu24.04_x86_64.tgz
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_SHA_X86_64=54b0b0c6a16e780392129d3894f12a41c48ded7e82d003b12c832aee06e7e18e
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.1/aerospike-server-community_8.1.0.1_tools-12.0.2_ubuntu24.04_aarch64.tgz
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_SHA_AARCH64=69519f31202d4d79d9d118ceee5080009e693b5590b09d72d7f947342d9d0b27
# Tue, 16 Sep 2025 00:43:00 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 16 Sep 2025 00:43:00 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.1/aerospike-server-community_8.1.0.1_tools-12.0.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=54b0b0c6a16e780392129d3894f12a41c48ded7e82d003b12c832aee06e7e18e AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.1/aerospike-server-community_8.1.0.1_tools-12.0.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=69519f31202d4d79d9d118ceee5080009e693b5590b09d72d7f947342d9d0b27
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8083136e73ad99268ead5293c4ce34ccf5c6e47f01bc86317251baeaffae75d0`  
		Last Modified: Thu, 09 Oct 2025 21:08:20 GMT  
		Size: 51.8 MB (51772977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07eb93b5539b0d2da8b104128708e6483969e2cbb384f9b7853c2a2fb93d92c7`  
		Last Modified: Thu, 09 Oct 2025 21:08:14 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90cdfbb9fa7d7740d18d1900cdc9555e14513b1d0ed2b6327131b10236bcd13`  
		Last Modified: Thu, 09 Oct 2025 21:08:14 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.0.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:dcaff2a41ff16f0406ee4177374d6ef286fee234f882d8376ec7b53d3005667a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba072864a0b241c4945c134d098f30013fbef36fcdd673436d4093069515db60`

```dockerfile
```

-	Layers:
	-	`sha256:a768085d1772b1f3a0eeb29cc0a4da06b62c59732c5984c887a47e179d17ae7c`  
		Last Modified: Thu, 09 Oct 2025 23:25:19 GMT  
		Size: 2.2 MB (2182312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ff3b1dda93bfebc6bb41f238ac7e6033756f40256b0ece84bfd812ad7b2690a`  
		Last Modified: Thu, 09 Oct 2025 23:25:20 GMT  
		Size: 29.0 KB (29012 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.1.0.1_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:f6bef904749c8c169ed058472a0e6bc58851e668723af753380c38cefc139b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79858074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aeb964dd7d1ad22a2584c71a251f055abb34e49bfb06c17da98e3f2a3f063d1`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Tue, 16 Sep 2025 00:43:00 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 00:43:00 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.0.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 16 Sep 2025 00:43:00 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.1/aerospike-server-community_8.1.0.1_tools-12.0.2_ubuntu24.04_x86_64.tgz
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_SHA_X86_64=54b0b0c6a16e780392129d3894f12a41c48ded7e82d003b12c832aee06e7e18e
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.1/aerospike-server-community_8.1.0.1_tools-12.0.2_ubuntu24.04_aarch64.tgz
# Tue, 16 Sep 2025 00:43:00 GMT
ARG AEROSPIKE_SHA_AARCH64=69519f31202d4d79d9d118ceee5080009e693b5590b09d72d7f947342d9d0b27
# Tue, 16 Sep 2025 00:43:00 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 16 Sep 2025 00:43:00 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.1/aerospike-server-community_8.1.0.1_tools-12.0.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=54b0b0c6a16e780392129d3894f12a41c48ded7e82d003b12c832aee06e7e18e AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.1/aerospike-server-community_8.1.0.1_tools-12.0.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=69519f31202d4d79d9d118ceee5080009e693b5590b09d72d7f947342d9d0b27
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecdabcac9c742cb6b04f636b3502871aed620799cc5194032ee2be97c0aee78`  
		Last Modified: Thu, 09 Oct 2025 21:09:03 GMT  
		Size: 51.0 MB (50994067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44761225235b0a1aa93ec8dbe68b6fbf1c4dcaa170fa064589d1fa8fb0e0c164`  
		Last Modified: Thu, 09 Oct 2025 21:09:00 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f8facd30e4e3035a929a0e41ee386b46af8095766400acd6dfe3943060df07`  
		Last Modified: Thu, 09 Oct 2025 21:08:59 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.0.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:007402ad683181eae7e2d8f3cff644d1ef1901601a952566d5527c0ecd9be517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2213684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e280d07683ed37e27b6f17386bbc883d0f516d53c87db3091b50582501b83d`

```dockerfile
```

-	Layers:
	-	`sha256:98cf296204cacdece47b7bf0e5cf7187a3fe40676e5a20221cf3057a7a9a9c3e`  
		Last Modified: Thu, 09 Oct 2025 23:25:54 GMT  
		Size: 2.2 MB (2184592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4f3698999ed79d105af757281417a3c5387977aa98dec56869654963ba9b68f`  
		Last Modified: Thu, 09 Oct 2025 23:25:55 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ee-8.1.0.1`

```console
$ docker pull aerospike@sha256:d278e6b397dc8a4f710a8d98a2b2d55b1d9d66cb5dcf9d252089309e9e5d75df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.1.0.1` - linux; amd64

```console
$ docker pull aerospike@sha256:66325602508f7c03ab9ddff032a48f9b080809cbde160d9001f00a4d2caa4a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83597616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f5bcf16d6c47df516dd084defbdb2354f7a6d2ef0441817ebcd10a8528adbb`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f66ba78bdfea33a95b02340ca7b68194d9c220e5e66077531436e63de91022`  
		Last Modified: Thu, 09 Oct 2025 21:08:19 GMT  
		Size: 53.9 MB (53872177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6aedf19f5b765dfb6a44723b93422492ce0f7ca0d4ec1ac208a017bc378a89`  
		Last Modified: Thu, 09 Oct 2025 21:08:16 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb65260043fa84fa998117f3eb69c3cdd6378f432c13afc2102909cf7f1a1ced`  
		Last Modified: Thu, 09 Oct 2025 21:08:16 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.0.1` - unknown; unknown

```console
$ docker pull aerospike@sha256:b8f7af28c77a3b40e6f1aa5ff4deed0f25e483d2641f5bcd203f172eee2edf5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a811dc8516de88440015dac539b6dee5ef62e4c7736d62d38c7c0850d368f6`

```dockerfile
```

-	Layers:
	-	`sha256:8a915ce12098950a9b1b3829f6fd320cb31373e11eaf4a4a3636ebb118ebfa81`  
		Last Modified: Thu, 09 Oct 2025 23:25:27 GMT  
		Size: 2.2 MB (2182953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb25b99ab81fe40dc93288a7c4695176f97e412813e03317a2c2e92e8967c9ed`  
		Last Modified: Thu, 09 Oct 2025 23:25:30 GMT  
		Size: 29.0 KB (29028 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.1.0.1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:f62ef1f6b2a00eeb7a26cfaf51adbce10855efd7d4d81d4ee62a7381f406285a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81945481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b03a90b426e3b99d4f215106053241cc56752606b24899e7c4ede8744867fa`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119a206be5f585de6cc62ba340c9b4b024673be5c62f9cfd6a81a8f5050e9b4e`  
		Last Modified: Thu, 09 Oct 2025 21:09:05 GMT  
		Size: 53.1 MB (53081474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c90206524b2012c20ef1c0ec7f98e135d6b04292cb69f9da36f0f566db8280`  
		Last Modified: Thu, 09 Oct 2025 21:09:00 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfa514ab8e6fcb3054379970299bcc77b09f2a254acab1f5cad848fbd45c135`  
		Last Modified: Thu, 09 Oct 2025 21:08:59 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.0.1` - unknown; unknown

```console
$ docker pull aerospike@sha256:094b7cb9d189e4c546fc9ac470bba0a3003619831fc3177b639f0be83bab5e14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97e2feff5c8a971f8000ec737e077d3c49478568e0c212dcc3fd30bce4c831c`

```dockerfile
```

-	Layers:
	-	`sha256:1dd94186069345d765205a60b8209940cfaf3e329fb6762d3229f8577a84444d`  
		Last Modified: Thu, 09 Oct 2025 23:25:43 GMT  
		Size: 2.2 MB (2185233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c33d6909cb8624dcf098ece875c0e8577a8489d369150e19f5e13313bc90bcab`  
		Last Modified: Thu, 09 Oct 2025 23:25:47 GMT  
		Size: 29.1 KB (29108 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ee-8.1.0.1_1`

```console
$ docker pull aerospike@sha256:d278e6b397dc8a4f710a8d98a2b2d55b1d9d66cb5dcf9d252089309e9e5d75df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.1.0.1_1` - linux; amd64

```console
$ docker pull aerospike@sha256:66325602508f7c03ab9ddff032a48f9b080809cbde160d9001f00a4d2caa4a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83597616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f5bcf16d6c47df516dd084defbdb2354f7a6d2ef0441817ebcd10a8528adbb`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f66ba78bdfea33a95b02340ca7b68194d9c220e5e66077531436e63de91022`  
		Last Modified: Thu, 09 Oct 2025 21:08:19 GMT  
		Size: 53.9 MB (53872177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6aedf19f5b765dfb6a44723b93422492ce0f7ca0d4ec1ac208a017bc378a89`  
		Last Modified: Thu, 09 Oct 2025 21:08:16 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb65260043fa84fa998117f3eb69c3cdd6378f432c13afc2102909cf7f1a1ced`  
		Last Modified: Thu, 09 Oct 2025 21:08:16 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.0.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:b8f7af28c77a3b40e6f1aa5ff4deed0f25e483d2641f5bcd203f172eee2edf5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a811dc8516de88440015dac539b6dee5ef62e4c7736d62d38c7c0850d368f6`

```dockerfile
```

-	Layers:
	-	`sha256:8a915ce12098950a9b1b3829f6fd320cb31373e11eaf4a4a3636ebb118ebfa81`  
		Last Modified: Thu, 09 Oct 2025 23:25:27 GMT  
		Size: 2.2 MB (2182953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb25b99ab81fe40dc93288a7c4695176f97e412813e03317a2c2e92e8967c9ed`  
		Last Modified: Thu, 09 Oct 2025 23:25:30 GMT  
		Size: 29.0 KB (29028 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.1.0.1_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:f62ef1f6b2a00eeb7a26cfaf51adbce10855efd7d4d81d4ee62a7381f406285a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81945481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b03a90b426e3b99d4f215106053241cc56752606b24899e7c4ede8744867fa`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119a206be5f585de6cc62ba340c9b4b024673be5c62f9cfd6a81a8f5050e9b4e`  
		Last Modified: Thu, 09 Oct 2025 21:09:05 GMT  
		Size: 53.1 MB (53081474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c90206524b2012c20ef1c0ec7f98e135d6b04292cb69f9da36f0f566db8280`  
		Last Modified: Thu, 09 Oct 2025 21:09:00 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfa514ab8e6fcb3054379970299bcc77b09f2a254acab1f5cad848fbd45c135`  
		Last Modified: Thu, 09 Oct 2025 21:08:59 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.0.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:094b7cb9d189e4c546fc9ac470bba0a3003619831fc3177b639f0be83bab5e14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97e2feff5c8a971f8000ec737e077d3c49478568e0c212dcc3fd30bce4c831c`

```dockerfile
```

-	Layers:
	-	`sha256:1dd94186069345d765205a60b8209940cfaf3e329fb6762d3229f8577a84444d`  
		Last Modified: Thu, 09 Oct 2025 23:25:43 GMT  
		Size: 2.2 MB (2185233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c33d6909cb8624dcf098ece875c0e8577a8489d369150e19f5e13313bc90bcab`  
		Last Modified: Thu, 09 Oct 2025 23:25:47 GMT  
		Size: 29.1 KB (29108 bytes)  
		MIME: application/vnd.in-toto+json
