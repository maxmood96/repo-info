## `aerospike:ee-8.1.0.0`

```console
$ docker pull aerospike@sha256:e5607df4837727f23c1aa3a0fcc72e61d66d8779c35c80efabc384778e8c7fa2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.1.0.0` - linux; amd64

```console
$ docker pull aerospike@sha256:2a720d4fe7a28f9debf69d19535462fd956ec27ae11e20c603c4364ee94d9df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83811125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff3879708da2121ab160a33afd9824bd8e6f0d11487f168ba4e73c748015bc2`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 05 Aug 2025 17:58:51 GMT
ARG RELEASE
# Tue, 05 Aug 2025 17:58:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 05 Aug 2025 17:58:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 05 Aug 2025 17:58:51 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 05 Aug 2025 17:58:51 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 05 Aug 2025 17:58:51 GMT
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
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3f9522dad8359d61309bbf335d01ae9a979c6791f2e8bba5d6773a0587f393`  
		Last Modified: Mon, 01 Sep 2025 23:08:47 GMT  
		Size: 54.1 MB (54085766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d10abb24487bc7ae5bb198196b5d0ba8a0a2fb091e236251102fb46f0a5c43`  
		Last Modified: Mon, 01 Sep 2025 23:08:38 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d99c2673a7844953272ce3bf71ae30ed111307f3cc65b0d7c8606fe61d2d134`  
		Last Modified: Mon, 01 Sep 2025 23:08:09 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.0.0` - unknown; unknown

```console
$ docker pull aerospike@sha256:d2b802f01d4d7799edc31742e3fd58aeb54d969bb9ed9b7edc8293227ef00a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f27442422b174d23cb2607df051f340cd146645bb2bf7becd1e49e6080603058`

```dockerfile
```

-	Layers:
	-	`sha256:fc05e4db4f29c1d85682ac84924197953a229ac375b9eab34f65a90eab298fb4`  
		Last Modified: Tue, 02 Sep 2025 02:25:25 GMT  
		Size: 2.2 MB (2182949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b4c4914fe5c5f3ba1398f4df88cb7a1ee750748365b1aac41b5e7a936e8be1e`  
		Last Modified: Tue, 02 Sep 2025 02:25:26 GMT  
		Size: 29.0 KB (29028 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.1.0.0` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:769f49fa7e4eb4048680f39fad71fb8d11fdaafae6b2475b8d5ae1246c02813d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.2 MB (82171024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c05c56c5ff5ac4f4948f71966473af5242457d98276f759bc70aa74004ad985`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 05 Aug 2025 17:58:51 GMT
ARG RELEASE
# Tue, 05 Aug 2025 17:58:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 05 Aug 2025 17:58:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 05 Aug 2025 17:58:51 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 05 Aug 2025 17:58:51 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 05 Aug 2025 17:58:51 GMT
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
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd8c71ef736e39402ef72bc5a2182fc90a88f51d315f25c703d57001e4a8bc9`  
		Last Modified: Tue, 02 Sep 2025 00:11:25 GMT  
		Size: 53.3 MB (53308484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6943eac6211276cbc3b66b32658150e9a5e7098f4c030f059ad83c3c5a389246`  
		Last Modified: Tue, 02 Sep 2025 00:11:21 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3163e720bc210bc4205aa838d78586b855deffba2f788d55f21bcc1cd2f2c68`  
		Last Modified: Tue, 02 Sep 2025 00:11:22 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.0.0` - unknown; unknown

```console
$ docker pull aerospike@sha256:4b1da0dc03634a6d199319bb8dcfc2378e41024c85fccb431f77d7a6c0c9baf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebdfb148c63937f0103608569bfd5e231df0affe6630b17fb6288c1e62bef35`

```dockerfile
```

-	Layers:
	-	`sha256:b4401a691af89d94aeb850fa80a8a8783c3b69a45c70e17ec79abcdef4a26284`  
		Last Modified: Tue, 02 Sep 2025 02:25:30 GMT  
		Size: 2.2 MB (2185229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e698bf30e16870ce0e27beef41b327c87177af6874d3be1093c5f170b3de46`  
		Last Modified: Tue, 02 Sep 2025 02:25:31 GMT  
		Size: 29.1 KB (29108 bytes)  
		MIME: application/vnd.in-toto+json
