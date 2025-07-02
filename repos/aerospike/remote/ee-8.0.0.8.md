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
