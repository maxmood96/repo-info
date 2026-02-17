## `aerospike:ce-8.1.1.0`

```console
$ docker pull aerospike@sha256:41f1a92943cc655a82070e4a0910f4386ed798a9efaf76491fff563962d4a520
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.1.1.0` - linux; amd64

```console
$ docker pull aerospike@sha256:760a711fcdf9f79686ae8344b514e09fe2bb4670f4eb3f4f912c164cf9d591a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84105833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ccf22d34d5b0f9e5f4acfa3c0343e9392ae0c7fb8f70759daed3654e02f87b`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:05 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.1.0 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 17 Feb 2026 20:12:05 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 17 Feb 2026 20:12:05 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 17 Feb 2026 20:12:05 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.0/aerospike-server-community_8.1.1.0_tools-12.1.1_ubuntu24.04_x86_64.tgz
# Tue, 17 Feb 2026 20:12:05 GMT
ARG AEROSPIKE_SHA_X86_64=efffa17793cf85aad6ba47fc053ef63ee57f6f993dbe7c87a9e2309c313da446
# Tue, 17 Feb 2026 20:12:05 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.0/aerospike-server-community_8.1.1.0_tools-12.1.1_ubuntu24.04_aarch64.tgz
# Tue, 17 Feb 2026 20:12:05 GMT
ARG AEROSPIKE_SHA_AARCH64=c66ad3082316c9064c88b0d3448d287565edd3e7b34990010023ee2a1c6463f4
# Tue, 17 Feb 2026 20:12:05 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 17 Feb 2026 20:12:05 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.0/aerospike-server-community_8.1.1.0_tools-12.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=efffa17793cf85aad6ba47fc053ef63ee57f6f993dbe7c87a9e2309c313da446 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.0/aerospike-server-community_8.1.1.0_tools-12.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=c66ad3082316c9064c88b0d3448d287565edd3e7b34990010023ee2a1c6463f4
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 17 Feb 2026 20:12:05 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 17 Feb 2026 20:12:05 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 17 Feb 2026 20:12:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:05 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 17 Feb 2026 20:12:05 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e8d8a26902dc43baebcda4b2f3beb1150ce367395715048071f7c923e1937e`  
		Last Modified: Tue, 17 Feb 2026 20:12:19 GMT  
		Size: 54.4 MB (54375928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580af07d4a067b5da7e8b63cb84209cbd9c2b2d27c68c199c0aa31f4c05eb9cc`  
		Last Modified: Tue, 17 Feb 2026 20:12:18 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383556127e4d7e1e8039a268b80f161babe868722db5f91e8f5ef5846d718272`  
		Last Modified: Tue, 17 Feb 2026 20:12:18 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.1.0` - unknown; unknown

```console
$ docker pull aerospike@sha256:781b8dbaceb8c11c7613f791ba31e0c25350ffcf06b0305cc91711955d17e389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f16cd63507415b937d6e99e933228c03951fd03a48ffde4c3f6513aba94fa5`

```dockerfile
```

-	Layers:
	-	`sha256:43ae433fb6ebafc7f75dd70ae9cab3b4f7c260407a9ca3e5547447d4dc0736be`  
		Last Modified: Tue, 17 Feb 2026 20:12:18 GMT  
		Size: 2.2 MB (2180940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ddd9db188a146901711bb13c203c58f8eaacd82bc79d2b460065bc495fd0f20`  
		Last Modified: Tue, 17 Feb 2026 20:12:18 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.1.1.0` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:eede28cae6e83bfe56f188addd7df16e9e34078027b47bd861bb3a34b8021109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84264594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c628646219f9fb3eda7f5448fba9ef0f9ff369a76d67123f49faa5bf7274c41d`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 20:01:26 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.1.0 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Mon, 09 Feb 2026 20:01:26 GMT
ARG AEROSPIKE_EDITION=community
# Mon, 09 Feb 2026 20:01:26 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Mon, 09 Feb 2026 20:01:26 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.0/aerospike-server-community_8.1.1.0_tools-12.1.1_ubuntu24.04_x86_64.tgz
# Mon, 09 Feb 2026 20:01:26 GMT
ARG AEROSPIKE_SHA_X86_64=efffa17793cf85aad6ba47fc053ef63ee57f6f993dbe7c87a9e2309c313da446
# Mon, 09 Feb 2026 20:01:26 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.0/aerospike-server-community_8.1.1.0_tools-12.1.1_ubuntu24.04_aarch64.tgz
# Mon, 09 Feb 2026 20:01:26 GMT
ARG AEROSPIKE_SHA_AARCH64=c66ad3082316c9064c88b0d3448d287565edd3e7b34990010023ee2a1c6463f4
# Mon, 09 Feb 2026 20:01:26 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Mon, 09 Feb 2026 20:01:26 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.0/aerospike-server-community_8.1.1.0_tools-12.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=efffa17793cf85aad6ba47fc053ef63ee57f6f993dbe7c87a9e2309c313da446 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.0/aerospike-server-community_8.1.1.0_tools-12.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=c66ad3082316c9064c88b0d3448d287565edd3e7b34990010023ee2a1c6463f4
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Mon, 09 Feb 2026 20:01:26 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Mon, 09 Feb 2026 20:01:26 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Mon, 09 Feb 2026 20:01:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 20:01:26 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Mon, 09 Feb 2026 20:01:26 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335e4bb10e3bae84f939bf85879cd087acce2bd9719d5aeaf6686c80d6084ede`  
		Last Modified: Mon, 09 Feb 2026 20:01:39 GMT  
		Size: 55.4 MB (55398469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925c28645521e1844eee40e81215f7668f8106f3ea4eee52d5ba85bd3616b300`  
		Last Modified: Mon, 09 Feb 2026 20:01:37 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d306b6286a8587dcf7b7006f7da3144f8ad0aa2c1c8e41aeea0547752b1a7342`  
		Last Modified: Mon, 09 Feb 2026 20:01:37 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.1.0` - unknown; unknown

```console
$ docker pull aerospike@sha256:a425c323ed6c35b54c24d09b8d76664bc9e928130f188a294007e210c2810ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac86130573d107ef83f6fca185837f87457a28b264b6bea8c951cd220c816be9`

```dockerfile
```

-	Layers:
	-	`sha256:c10ffc912d3b633341039b7734774a602b15edea2b11336e997fcaeff8075b16`  
		Last Modified: Mon, 09 Feb 2026 20:01:37 GMT  
		Size: 2.2 MB (2183220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8ce4d41fdb2044ca7afe1e570d3b345d0e4e0d5b8ff9d42ba8430168fe2603a`  
		Last Modified: Mon, 09 Feb 2026 20:01:37 GMT  
		Size: 29.0 KB (29049 bytes)  
		MIME: application/vnd.in-toto+json
