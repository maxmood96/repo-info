## `aerospike:ce-8.1.1.0`

```console
$ docker pull aerospike@sha256:9ed8e55e8477aa1566b1d9260d75ca69f5e9ff7d4662e602a20de6968f37f75d
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
$ docker pull aerospike@sha256:5a6f55dae13bc8440d6b1bd5bd9bd1b94181b0ec1b86d671feb608c8e76b11d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82053399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8866511a543a414c92a3dad4fa57fb9d348c531d5fda1abfe7c8fa20aa4ebd75`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:02 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.1.0 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 17 Feb 2026 20:12:02 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 17 Feb 2026 20:12:02 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 17 Feb 2026 20:12:02 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.0/aerospike-server-community_8.1.1.0_tools-12.1.1_ubuntu24.04_x86_64.tgz
# Tue, 17 Feb 2026 20:12:02 GMT
ARG AEROSPIKE_SHA_X86_64=efffa17793cf85aad6ba47fc053ef63ee57f6f993dbe7c87a9e2309c313da446
# Tue, 17 Feb 2026 20:12:02 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.0/aerospike-server-community_8.1.1.0_tools-12.1.1_ubuntu24.04_aarch64.tgz
# Tue, 17 Feb 2026 20:12:02 GMT
ARG AEROSPIKE_SHA_AARCH64=c66ad3082316c9064c88b0d3448d287565edd3e7b34990010023ee2a1c6463f4
# Tue, 17 Feb 2026 20:12:02 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 17 Feb 2026 20:12:02 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.0/aerospike-server-community_8.1.1.0_tools-12.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=efffa17793cf85aad6ba47fc053ef63ee57f6f993dbe7c87a9e2309c313da446 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.1.0/aerospike-server-community_8.1.1.0_tools-12.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=c66ad3082316c9064c88b0d3448d287565edd3e7b34990010023ee2a1c6463f4
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 17 Feb 2026 20:12:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 17 Feb 2026 20:12:02 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c25602c23863826d7d7639a8a3b334c2bc5a856818b2c9756217b1cb9d1cf51`  
		Last Modified: Tue, 17 Feb 2026 20:12:15 GMT  
		Size: 53.2 MB (53185986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978fb2972566d4546cfdb2a9cc64ca724574211a81ec9d176f687a1cb52f0c25`  
		Last Modified: Tue, 17 Feb 2026 20:12:13 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d07bdf1c0aeb7d0e7331f126b9391f92863b3beda7dcf49e3faa075f8e34100`  
		Last Modified: Tue, 17 Feb 2026 20:12:14 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.1.0` - unknown; unknown

```console
$ docker pull aerospike@sha256:c4424206a89105e877d01983b01b96f122aedc813ff709c21373863f8cad2ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154889d9ab1babf9ae1a87e9cb56d19383ab2a69866fb69456725e35c9d99999`

```dockerfile
```

-	Layers:
	-	`sha256:c3f1489466965b195d53ecf99abe826686a21fba52513743b536314aa61bc865`  
		Last Modified: Tue, 17 Feb 2026 20:12:14 GMT  
		Size: 2.2 MB (2183220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:363161fc591a9aab7c52f2ed77aea1bb8bc9e5dd354ffa6b18ebcf0a4dcbad85`  
		Last Modified: Tue, 17 Feb 2026 20:12:13 GMT  
		Size: 29.0 KB (29049 bytes)  
		MIME: application/vnd.in-toto+json
