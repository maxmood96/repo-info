<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-8.0.0.8`](#aerospikece-8008)
-	[`aerospike:ce-8.0.0.8_1`](#aerospikece-8008_1)
-	[`aerospike:ee-8.0.0.8`](#aerospikeee-8008)
-	[`aerospike:ee-8.0.0.8_1`](#aerospikeee-8008_1)

## `aerospike:ce-8.0.0.8`

```console
$ docker pull aerospike@sha256:b74f63d5f195ecf76b3363a318633729901d96167b93be6c11067a4134dfa7fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.0.0.8` - linux; amd64

```console
$ docker pull aerospike@sha256:3d3645f7299cc84bca49b0b665b3dd19932221808de8299923584948b822ac10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84142085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276286c5447ed436963bf530ad4b4aa4306188f71c92c8efa0df5c4bf2d91925`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 27 May 2025 23:31:17 GMT
ARG RELEASE
# Tue, 27 May 2025 23:31:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 May 2025 23:31:17 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 27 May 2025 23:31:17 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.8 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 27 May 2025 23:31:17 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.8/aerospike-server-community_8.0.0.8_tools-11.2.2_ubuntu24.04_x86_64.tgz
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_SHA_X86_64=a8da3e4cfeb6d03a457bfc20a827de7498cd3482e651f0af9538f7422d1e5dfb
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.8/aerospike-server-community_8.0.0.8_tools-11.2.2_ubuntu24.04_aarch64.tgz
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_SHA_AARCH64=55ab5d5a778eaa19c06d262982fab8008bed6fe9c7aae2450cdadf3f41d2e0ac
# Tue, 27 May 2025 23:31:17 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 27 May 2025 23:31:17 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.8/aerospike-server-community_8.0.0.8_tools-11.2.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=a8da3e4cfeb6d03a457bfc20a827de7498cd3482e651f0af9538f7422d1e5dfb AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.8/aerospike-server-community_8.0.0.8_tools-11.2.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=55ab5d5a778eaa19c06d262982fab8008bed6fe9c7aae2450cdadf3f41d2e0ac
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 27 May 2025 23:31:17 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 27 May 2025 23:31:17 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 27 May 2025 23:31:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 27 May 2025 23:31:17 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 27 May 2025 23:31:17 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c622527fe1e2748b48c7d7014a9612368019ed6f6d1f4e721ed88e4033fe219`  
		Last Modified: Wed, 02 Jul 2025 03:10:02 GMT  
		Size: 54.4 MB (54421414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc2a1bad74c43253ef39390efac58305af82413cae4dfa0599081a9c1c9d06e`  
		Last Modified: Wed, 02 Jul 2025 03:09:58 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1400e3e23fbbdb74a63d0b37a778e5202db25ef399bc7440da45b71cbd51d4`  
		Last Modified: Wed, 02 Jul 2025 03:09:58 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.0.0.8` - unknown; unknown

```console
$ docker pull aerospike@sha256:2ddc86240b438a3449c1a8a3f3c3ec2616128f9546acb566c3d7bf980d984b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1573eaf7a05c4a9d166d531162824f3cf7e22b8f182c99cb4c897d6e60f9fb6e`

```dockerfile
```

-	Layers:
	-	`sha256:2b94db37781e5455e33752e72d8c5821b56129c89954a89e5b20e1c765370f16`  
		Last Modified: Wed, 02 Jul 2025 05:25:19 GMT  
		Size: 2.2 MB (2180043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75c7d34ec26dc3d9d469af581227edfc930e65bfc8f37537c3767aec5cc2221c`  
		Last Modified: Wed, 02 Jul 2025 05:25:20 GMT  
		Size: 29.0 KB (29012 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.0.0.8` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:d598139ed7ecaddb2066f631ba11b978c6e5259d89d15d6491a297b70953ae50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82718497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0711677b3ef757fc6b789689f84004b46f8b5d1857cdd94016b4e32f6918a72d`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 27 May 2025 23:31:17 GMT
ARG RELEASE
# Tue, 27 May 2025 23:31:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 May 2025 23:31:17 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 27 May 2025 23:31:17 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.8 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 27 May 2025 23:31:17 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.8/aerospike-server-community_8.0.0.8_tools-11.2.2_ubuntu24.04_x86_64.tgz
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_SHA_X86_64=a8da3e4cfeb6d03a457bfc20a827de7498cd3482e651f0af9538f7422d1e5dfb
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.8/aerospike-server-community_8.0.0.8_tools-11.2.2_ubuntu24.04_aarch64.tgz
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_SHA_AARCH64=55ab5d5a778eaa19c06d262982fab8008bed6fe9c7aae2450cdadf3f41d2e0ac
# Tue, 27 May 2025 23:31:17 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 27 May 2025 23:31:17 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.8/aerospike-server-community_8.0.0.8_tools-11.2.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=a8da3e4cfeb6d03a457bfc20a827de7498cd3482e651f0af9538f7422d1e5dfb AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.8/aerospike-server-community_8.0.0.8_tools-11.2.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=55ab5d5a778eaa19c06d262982fab8008bed6fe9c7aae2450cdadf3f41d2e0ac
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 27 May 2025 23:31:17 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 27 May 2025 23:31:17 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 27 May 2025 23:31:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 27 May 2025 23:31:17 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 27 May 2025 23:31:17 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f97f1ee92e42058506f0342610fad1c428023ba33adfbdfe46e6cbf10055108`  
		Last Modified: Wed, 02 Jul 2025 04:18:10 GMT  
		Size: 53.9 MB (53860177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bd93fb75f7d5fb5c439383982ecbe1233a6c94184e2e346c94409484ab1eba`  
		Last Modified: Wed, 02 Jul 2025 04:18:02 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3beb0ea5c5b19934c19f055438582052f4721ea87ab339a3061320c9b8c434`  
		Last Modified: Wed, 02 Jul 2025 04:18:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.0.0.8` - unknown; unknown

```console
$ docker pull aerospike@sha256:453eb540d842a9bfb978fc7467e847586acce76d3c095d30c9d697ea1f55d050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c5b759399488e5fbedbf3d63c15f2ef04505c479ec61a56470c28803c3717f`

```dockerfile
```

-	Layers:
	-	`sha256:29c823042c8dbe66957f28b455d6f3eb014874b6a54ee613325d141c8a659df7`  
		Last Modified: Wed, 02 Jul 2025 05:25:24 GMT  
		Size: 2.2 MB (2182323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed346acef84812815be0b084296e872cf7a0b9251709695504ae796a9b22397`  
		Last Modified: Wed, 02 Jul 2025 05:25:25 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ce-8.0.0.8_1`

```console
$ docker pull aerospike@sha256:08716079600c08978a234816a95902266476735ff824964cae307fb3a1314522
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.0.0.8_1` - linux; amd64

```console
$ docker pull aerospike@sha256:612f9d59fff9827538f68cfe8e31003be83d4f0d34ef7345dd8354bde1d78046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84139071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f4c3d7bad03ad4e1850fbb1a7a6139569cd180fb66e8b31ae28e69b701c449`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 27 May 2025 23:31:17 GMT
ARG RELEASE
# Tue, 27 May 2025 23:31:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 May 2025 23:31:17 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Tue, 27 May 2025 23:31:17 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.8 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 27 May 2025 23:31:17 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.8/aerospike-server-community_8.0.0.8_tools-11.2.2_ubuntu24.04_x86_64.tgz
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_SHA_X86_64=a8da3e4cfeb6d03a457bfc20a827de7498cd3482e651f0af9538f7422d1e5dfb
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.8/aerospike-server-community_8.0.0.8_tools-11.2.2_ubuntu24.04_aarch64.tgz
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_SHA_AARCH64=55ab5d5a778eaa19c06d262982fab8008bed6fe9c7aae2450cdadf3f41d2e0ac
# Tue, 27 May 2025 23:31:17 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 27 May 2025 23:31:17 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.8/aerospike-server-community_8.0.0.8_tools-11.2.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=a8da3e4cfeb6d03a457bfc20a827de7498cd3482e651f0af9538f7422d1e5dfb AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.8/aerospike-server-community_8.0.0.8_tools-11.2.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=55ab5d5a778eaa19c06d262982fab8008bed6fe9c7aae2450cdadf3f41d2e0ac
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 27 May 2025 23:31:17 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 27 May 2025 23:31:17 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 27 May 2025 23:31:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 27 May 2025 23:31:17 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 27 May 2025 23:31:17 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a755721ff2c98c4e4513c00afda59e30191a99fec517b916b609eb61692c30`  
		Last Modified: Thu, 05 Jun 2025 03:22:06 GMT  
		Size: 54.4 MB (54421433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b0644b4fde082d2e3d518dd337c18fff95fee4b567dfedad774b41eee2c906`  
		Last Modified: Thu, 05 Jun 2025 00:01:38 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088cc3042d53af9389a67bccf00f9bc7a51534cebb0472c2adebea635168de5d`  
		Last Modified: Wed, 04 Jun 2025 23:48:34 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.0.0.8_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:bafdeeb553c8f2c1c18d20cc198af14e1699d0ba6b7a4618443c9905434c40b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2115512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7cf87e0afb03618ce22909580406febb5ff496355a15492626357e49ee9a6d`

```dockerfile
```

-	Layers:
	-	`sha256:a7e661e3fe13c6117bbbb427ccb06d86bc1085648f2efaf2ce1e3da5055088ac`  
		Last Modified: Mon, 23 Jun 2025 17:59:21 GMT  
		Size: 2.1 MB (2086500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b871d57d58eb6309f2778166a4448e12388642f6b06bc343faf65d821402ca4`  
		Last Modified: Mon, 23 Jun 2025 17:59:20 GMT  
		Size: 29.0 KB (29012 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.0.0.8_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:d598139ed7ecaddb2066f631ba11b978c6e5259d89d15d6491a297b70953ae50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82718497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0711677b3ef757fc6b789689f84004b46f8b5d1857cdd94016b4e32f6918a72d`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 27 May 2025 23:31:17 GMT
ARG RELEASE
# Tue, 27 May 2025 23:31:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 May 2025 23:31:17 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 27 May 2025 23:31:17 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.8 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 27 May 2025 23:31:17 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.8/aerospike-server-community_8.0.0.8_tools-11.2.2_ubuntu24.04_x86_64.tgz
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_SHA_X86_64=a8da3e4cfeb6d03a457bfc20a827de7498cd3482e651f0af9538f7422d1e5dfb
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.8/aerospike-server-community_8.0.0.8_tools-11.2.2_ubuntu24.04_aarch64.tgz
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_SHA_AARCH64=55ab5d5a778eaa19c06d262982fab8008bed6fe9c7aae2450cdadf3f41d2e0ac
# Tue, 27 May 2025 23:31:17 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 27 May 2025 23:31:17 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.8/aerospike-server-community_8.0.0.8_tools-11.2.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=a8da3e4cfeb6d03a457bfc20a827de7498cd3482e651f0af9538f7422d1e5dfb AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.8/aerospike-server-community_8.0.0.8_tools-11.2.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=55ab5d5a778eaa19c06d262982fab8008bed6fe9c7aae2450cdadf3f41d2e0ac
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 27 May 2025 23:31:17 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 27 May 2025 23:31:17 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 27 May 2025 23:31:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 27 May 2025 23:31:17 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 27 May 2025 23:31:17 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f97f1ee92e42058506f0342610fad1c428023ba33adfbdfe46e6cbf10055108`  
		Last Modified: Wed, 02 Jul 2025 04:18:10 GMT  
		Size: 53.9 MB (53860177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bd93fb75f7d5fb5c439383982ecbe1233a6c94184e2e346c94409484ab1eba`  
		Last Modified: Wed, 02 Jul 2025 04:18:02 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3beb0ea5c5b19934c19f055438582052f4721ea87ab339a3061320c9b8c434`  
		Last Modified: Wed, 02 Jul 2025 04:18:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.0.0.8_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:453eb540d842a9bfb978fc7467e847586acce76d3c095d30c9d697ea1f55d050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c5b759399488e5fbedbf3d63c15f2ef04505c479ec61a56470c28803c3717f`

```dockerfile
```

-	Layers:
	-	`sha256:29c823042c8dbe66957f28b455d6f3eb014874b6a54ee613325d141c8a659df7`  
		Last Modified: Wed, 02 Jul 2025 05:25:24 GMT  
		Size: 2.2 MB (2182323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed346acef84812815be0b084296e872cf7a0b9251709695504ae796a9b22397`  
		Last Modified: Wed, 02 Jul 2025 05:25:25 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ee-8.0.0.8`

```console
$ docker pull aerospike@sha256:fe6aca0a858e998538bf07dccedc23388ac2a6a77e9362e94e61f17d40b8f24e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.0.0.8` - linux; amd64

```console
$ docker pull aerospike@sha256:c432542bf7603c27cf91a115fce7834d3bebeea70c606cf9c11145095c6a9118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86237542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ef3e1fcda828f3ce289135b2c3359f4cdb18393a1a0296e5ac0a0aaf464100`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 27 May 2025 23:31:17 GMT
ARG RELEASE
# Tue, 27 May 2025 23:31:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 May 2025 23:31:17 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 27 May 2025 23:31:17 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.8 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 27 May 2025 23:31:17 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.8/aerospike-server-enterprise_8.0.0.8_tools-11.2.2_ubuntu24.04_x86_64.tgz
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_SHA_X86_64=4ce9c840dc4724b124ddb983d58856ddd2aea96584ca5498387be2e31aa1f892
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.8/aerospike-server-enterprise_8.0.0.8_tools-11.2.2_ubuntu24.04_aarch64.tgz
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_SHA_AARCH64=01abeedb92895a55ef12ae5275c7370e6d1b6bdb6d1ee53e3e6318c381e8778e
# Tue, 27 May 2025 23:31:17 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 27 May 2025 23:31:17 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.8/aerospike-server-enterprise_8.0.0.8_tools-11.2.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=4ce9c840dc4724b124ddb983d58856ddd2aea96584ca5498387be2e31aa1f892 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.8/aerospike-server-enterprise_8.0.0.8_tools-11.2.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=01abeedb92895a55ef12ae5275c7370e6d1b6bdb6d1ee53e3e6318c381e8778e
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 27 May 2025 23:31:17 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 27 May 2025 23:31:17 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 27 May 2025 23:31:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 27 May 2025 23:31:17 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 27 May 2025 23:31:17 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d120a9b018a4fbc763e6d2d01d14fd0bd430c38acfaf69e54601db52c4aec0e2`  
		Last Modified: Wed, 02 Jul 2025 03:10:07 GMT  
		Size: 56.5 MB (56516873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6d020a70f49a2395d3df459035af6c6e6d24fe9dd8ec3a31d3bfdb121f4782`  
		Last Modified: Wed, 02 Jul 2025 03:10:03 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3f1df3ab14a78786bf6f341dbe272af422ee1b41f246452d4cc430366130d5`  
		Last Modified: Wed, 02 Jul 2025 03:10:03 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.0.0.8` - unknown; unknown

```console
$ docker pull aerospike@sha256:1cc1cc69b87f3e3334d2a83750cd369db80b7e808fd2b87e99065ab0f6c65dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b2a664aea7b1a5ad625823e02c167a00d3c6e4d00bead29c6b8f7d0dc764de`

```dockerfile
```

-	Layers:
	-	`sha256:25031e6378069327069d52842b5f4224b96bf189e716d347a4b91277f110af06`  
		Last Modified: Wed, 02 Jul 2025 05:25:28 GMT  
		Size: 2.2 MB (2180684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fbb9bf21bd02ba44cec7ef388d0dced44d53d7ff8221a7d817e43ad2b856bf1`  
		Last Modified: Wed, 02 Jul 2025 05:25:29 GMT  
		Size: 29.0 KB (29028 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.0.0.8` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:6dee4e4f8befe46c48207a3a28ac183c195be5266b42b22062b59a0c778e30d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84806471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443ea071742d26e1a5cddc88054eae5077b42302640a37461249093d2d71c487`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 27 May 2025 23:31:17 GMT
ARG RELEASE
# Tue, 27 May 2025 23:31:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 May 2025 23:31:17 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 27 May 2025 23:31:17 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.8 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 27 May 2025 23:31:17 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.8/aerospike-server-enterprise_8.0.0.8_tools-11.2.2_ubuntu24.04_x86_64.tgz
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_SHA_X86_64=4ce9c840dc4724b124ddb983d58856ddd2aea96584ca5498387be2e31aa1f892
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.8/aerospike-server-enterprise_8.0.0.8_tools-11.2.2_ubuntu24.04_aarch64.tgz
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_SHA_AARCH64=01abeedb92895a55ef12ae5275c7370e6d1b6bdb6d1ee53e3e6318c381e8778e
# Tue, 27 May 2025 23:31:17 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 27 May 2025 23:31:17 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.8/aerospike-server-enterprise_8.0.0.8_tools-11.2.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=4ce9c840dc4724b124ddb983d58856ddd2aea96584ca5498387be2e31aa1f892 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.8/aerospike-server-enterprise_8.0.0.8_tools-11.2.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=01abeedb92895a55ef12ae5275c7370e6d1b6bdb6d1ee53e3e6318c381e8778e
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 27 May 2025 23:31:17 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 27 May 2025 23:31:17 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 27 May 2025 23:31:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 27 May 2025 23:31:17 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 27 May 2025 23:31:17 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617adfb4b12f81e88026a728f841b4fe2548a160a13146ff74d16fceda37f424`  
		Last Modified: Wed, 02 Jul 2025 04:18:04 GMT  
		Size: 55.9 MB (55948150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d754d89d257b8a2f927455510dc90a498143a1594f7c3bdee64dcf8da17747d0`  
		Last Modified: Wed, 02 Jul 2025 04:18:01 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8a5366353edf09eb38767b7a3887f4c22c9a2417b257f0a1f63e0e0c0bdf1f`  
		Last Modified: Wed, 02 Jul 2025 04:18:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.0.0.8` - unknown; unknown

```console
$ docker pull aerospike@sha256:11dd230ac24c34c98f1329a965acc3a322c971ae02a70688b5e6bbe36f19a8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddcc15cdee5b213df0540f294470900511f57b838db15d12588d5c22ae72df3e`

```dockerfile
```

-	Layers:
	-	`sha256:5e5af65889e745046b451d1b6225fd203688adb278a728a14228116dc187aa97`  
		Last Modified: Wed, 02 Jul 2025 05:25:33 GMT  
		Size: 2.2 MB (2182964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5cc33ff5e2abd296af6ce6fc71ff35ec65a516b0f06a434e89ab2ca50f9ea16`  
		Last Modified: Wed, 02 Jul 2025 05:25:34 GMT  
		Size: 29.1 KB (29108 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ee-8.0.0.8_1`

```console
$ docker pull aerospike@sha256:fe6aca0a858e998538bf07dccedc23388ac2a6a77e9362e94e61f17d40b8f24e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.0.0.8_1` - linux; amd64

```console
$ docker pull aerospike@sha256:c432542bf7603c27cf91a115fce7834d3bebeea70c606cf9c11145095c6a9118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86237542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ef3e1fcda828f3ce289135b2c3359f4cdb18393a1a0296e5ac0a0aaf464100`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 27 May 2025 23:31:17 GMT
ARG RELEASE
# Tue, 27 May 2025 23:31:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 May 2025 23:31:17 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 27 May 2025 23:31:17 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.8 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 27 May 2025 23:31:17 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.8/aerospike-server-enterprise_8.0.0.8_tools-11.2.2_ubuntu24.04_x86_64.tgz
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_SHA_X86_64=4ce9c840dc4724b124ddb983d58856ddd2aea96584ca5498387be2e31aa1f892
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.8/aerospike-server-enterprise_8.0.0.8_tools-11.2.2_ubuntu24.04_aarch64.tgz
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_SHA_AARCH64=01abeedb92895a55ef12ae5275c7370e6d1b6bdb6d1ee53e3e6318c381e8778e
# Tue, 27 May 2025 23:31:17 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 27 May 2025 23:31:17 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.8/aerospike-server-enterprise_8.0.0.8_tools-11.2.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=4ce9c840dc4724b124ddb983d58856ddd2aea96584ca5498387be2e31aa1f892 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.8/aerospike-server-enterprise_8.0.0.8_tools-11.2.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=01abeedb92895a55ef12ae5275c7370e6d1b6bdb6d1ee53e3e6318c381e8778e
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 27 May 2025 23:31:17 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 27 May 2025 23:31:17 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 27 May 2025 23:31:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 27 May 2025 23:31:17 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 27 May 2025 23:31:17 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d120a9b018a4fbc763e6d2d01d14fd0bd430c38acfaf69e54601db52c4aec0e2`  
		Last Modified: Wed, 02 Jul 2025 03:10:07 GMT  
		Size: 56.5 MB (56516873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6d020a70f49a2395d3df459035af6c6e6d24fe9dd8ec3a31d3bfdb121f4782`  
		Last Modified: Wed, 02 Jul 2025 03:10:03 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3f1df3ab14a78786bf6f341dbe272af422ee1b41f246452d4cc430366130d5`  
		Last Modified: Wed, 02 Jul 2025 03:10:03 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.0.0.8_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:1cc1cc69b87f3e3334d2a83750cd369db80b7e808fd2b87e99065ab0f6c65dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b2a664aea7b1a5ad625823e02c167a00d3c6e4d00bead29c6b8f7d0dc764de`

```dockerfile
```

-	Layers:
	-	`sha256:25031e6378069327069d52842b5f4224b96bf189e716d347a4b91277f110af06`  
		Last Modified: Wed, 02 Jul 2025 05:25:28 GMT  
		Size: 2.2 MB (2180684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fbb9bf21bd02ba44cec7ef388d0dced44d53d7ff8221a7d817e43ad2b856bf1`  
		Last Modified: Wed, 02 Jul 2025 05:25:29 GMT  
		Size: 29.0 KB (29028 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.0.0.8_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:6dee4e4f8befe46c48207a3a28ac183c195be5266b42b22062b59a0c778e30d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84806471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443ea071742d26e1a5cddc88054eae5077b42302640a37461249093d2d71c487`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 27 May 2025 23:31:17 GMT
ARG RELEASE
# Tue, 27 May 2025 23:31:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 May 2025 23:31:17 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 27 May 2025 23:31:17 GMT
CMD ["/bin/bash"]
# Tue, 27 May 2025 23:31:17 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.8 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 27 May 2025 23:31:17 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.8/aerospike-server-enterprise_8.0.0.8_tools-11.2.2_ubuntu24.04_x86_64.tgz
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_SHA_X86_64=4ce9c840dc4724b124ddb983d58856ddd2aea96584ca5498387be2e31aa1f892
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.8/aerospike-server-enterprise_8.0.0.8_tools-11.2.2_ubuntu24.04_aarch64.tgz
# Tue, 27 May 2025 23:31:17 GMT
ARG AEROSPIKE_SHA_AARCH64=01abeedb92895a55ef12ae5275c7370e6d1b6bdb6d1ee53e3e6318c381e8778e
# Tue, 27 May 2025 23:31:17 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 27 May 2025 23:31:17 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.8/aerospike-server-enterprise_8.0.0.8_tools-11.2.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=4ce9c840dc4724b124ddb983d58856ddd2aea96584ca5498387be2e31aa1f892 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.8/aerospike-server-enterprise_8.0.0.8_tools-11.2.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=01abeedb92895a55ef12ae5275c7370e6d1b6bdb6d1ee53e3e6318c381e8778e
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 27 May 2025 23:31:17 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 27 May 2025 23:31:17 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 27 May 2025 23:31:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 27 May 2025 23:31:17 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 27 May 2025 23:31:17 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617adfb4b12f81e88026a728f841b4fe2548a160a13146ff74d16fceda37f424`  
		Last Modified: Wed, 02 Jul 2025 04:18:04 GMT  
		Size: 55.9 MB (55948150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d754d89d257b8a2f927455510dc90a498143a1594f7c3bdee64dcf8da17747d0`  
		Last Modified: Wed, 02 Jul 2025 04:18:01 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8a5366353edf09eb38767b7a3887f4c22c9a2417b257f0a1f63e0e0c0bdf1f`  
		Last Modified: Wed, 02 Jul 2025 04:18:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.0.0.8_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:11dd230ac24c34c98f1329a965acc3a322c971ae02a70688b5e6bbe36f19a8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddcc15cdee5b213df0540f294470900511f57b838db15d12588d5c22ae72df3e`

```dockerfile
```

-	Layers:
	-	`sha256:5e5af65889e745046b451d1b6225fd203688adb278a728a14228116dc187aa97`  
		Last Modified: Wed, 02 Jul 2025 05:25:33 GMT  
		Size: 2.2 MB (2182964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5cc33ff5e2abd296af6ce6fc71ff35ec65a516b0f06a434e89ab2ca50f9ea16`  
		Last Modified: Wed, 02 Jul 2025 05:25:34 GMT  
		Size: 29.1 KB (29108 bytes)  
		MIME: application/vnd.in-toto+json
