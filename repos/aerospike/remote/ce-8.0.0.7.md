## `aerospike:ce-8.0.0.7`

```console
$ docker pull aerospike@sha256:7988e39fd04af8ab42fc1b42679da650247dfcc19080eecd39b908dd03e2f352
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.0.0.7` - linux; amd64

```console
$ docker pull aerospike@sha256:8629b0dd449f1110ac831d32a93a6eaee5842dac1f0b29449e70b69bb80873d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81064811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8f1be8cfa9b1bd15fdf4df73f521ac12f29f94593ecc5a9d7178dbd8272199`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Fri, 25 Apr 2025 21:09:11 GMT
ARG RELEASE
# Fri, 25 Apr 2025 21:09:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 25 Apr 2025 21:09:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 25 Apr 2025 21:09:11 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 25 Apr 2025 21:09:11 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Fri, 25 Apr 2025 21:09:11 GMT
CMD ["/bin/bash"]
# Fri, 25 Apr 2025 21:09:11 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.7 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_EDITION=community
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.7/aerospike-server-community_8.0.0.7_tools-11.2.2_ubuntu24.04_x86_64.tgz
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_SHA_X86_64=89b6ac9b14156730fb663daa0a43095c12423aa2b1332b4a28c060e5f4124d77
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.7/aerospike-server-community_8.0.0.7_tools-11.2.2_ubuntu24.04_aarch64.tgz
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_SHA_AARCH64=8715553eeb690d42a83a514460bd15fa5a079b6adb0486532270cc48e138975f
# Fri, 25 Apr 2025 21:09:11 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 25 Apr 2025 21:09:11 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.7/aerospike-server-community_8.0.0.7_tools-11.2.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=89b6ac9b14156730fb663daa0a43095c12423aa2b1332b4a28c060e5f4124d77 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.7/aerospike-server-community_8.0.0.7_tools-11.2.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=8715553eeb690d42a83a514460bd15fa5a079b6adb0486532270cc48e138975f
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 25 Apr 2025 21:09:11 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 25 Apr 2025 21:09:11 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 25 Apr 2025 21:09:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 25 Apr 2025 21:09:11 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 25 Apr 2025 21:09:11 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e84ef7efb8c9926528d6cd0691b8c74c32f3722a5cf969c896afbe4d5338846`  
		Last Modified: Fri, 09 May 2025 03:22:04 GMT  
		Size: 51.3 MB (51344983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790569eaa1f084d78e966c843edbb5fa83b7afeed4d67c908071d052752805f7`  
		Last Modified: Fri, 09 May 2025 03:22:01 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95b09d57a44fbb7fa005f7a1d5ab3d6116a9a78de9fed62c5b0c25ca6b3f7dd`  
		Last Modified: Fri, 09 May 2025 03:22:01 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.0.0.7` - unknown; unknown

```console
$ docker pull aerospike@sha256:294c421c6b7633ea25e3f41fa591db2654f77279b0bc205d777a8e1f97e76f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1893179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bdb2eac6f2bd0b320ad279aa024bc4e1937960deb5b865227ed10a0f844da44`

```dockerfile
```

-	Layers:
	-	`sha256:28b219894eb86ae3134a019874d0b204964f28f4e6d1faec5c73a73aeb5789d6`  
		Last Modified: Mon, 05 May 2025 16:34:53 GMT  
		Size: 1.9 MB (1864032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304de4da11bb8f66c07dd7578d312b0af0ca47b59ee4daef816a06a41f06f8fb`  
		Last Modified: Mon, 05 May 2025 16:34:52 GMT  
		Size: 29.1 KB (29147 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.0.0.7` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:ba8f29216342420d0f3d6f575de04c4edc1e05375c6ffeb7b4617252ae5b77f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79616587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d966cf9d45097938ed54e919f7622ff3118882043a7ccfbaad084b4753061738`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Fri, 25 Apr 2025 21:09:11 GMT
ARG RELEASE
# Fri, 25 Apr 2025 21:09:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 25 Apr 2025 21:09:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 25 Apr 2025 21:09:11 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 25 Apr 2025 21:09:11 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Fri, 25 Apr 2025 21:09:11 GMT
CMD ["/bin/bash"]
# Fri, 25 Apr 2025 21:09:11 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.7 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_EDITION=community
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.7/aerospike-server-community_8.0.0.7_tools-11.2.2_ubuntu24.04_x86_64.tgz
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_SHA_X86_64=89b6ac9b14156730fb663daa0a43095c12423aa2b1332b4a28c060e5f4124d77
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.7/aerospike-server-community_8.0.0.7_tools-11.2.2_ubuntu24.04_aarch64.tgz
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_SHA_AARCH64=8715553eeb690d42a83a514460bd15fa5a079b6adb0486532270cc48e138975f
# Fri, 25 Apr 2025 21:09:11 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 25 Apr 2025 21:09:11 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.7/aerospike-server-community_8.0.0.7_tools-11.2.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=89b6ac9b14156730fb663daa0a43095c12423aa2b1332b4a28c060e5f4124d77 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.7/aerospike-server-community_8.0.0.7_tools-11.2.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=8715553eeb690d42a83a514460bd15fa5a079b6adb0486532270cc48e138975f
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 25 Apr 2025 21:09:11 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 25 Apr 2025 21:09:11 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 25 Apr 2025 21:09:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 25 Apr 2025 21:09:11 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 25 Apr 2025 21:09:11 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22587de06b85a92627d1f30b1db9f511fae74776b9c540aaaaea4a28f7445630`  
		Last Modified: Fri, 09 May 2025 05:51:20 GMT  
		Size: 50.8 MB (50767410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc22fee227c2341a751f26e689008146f5b1206d0fd151c60d4cc25decbc541`  
		Last Modified: Fri, 09 May 2025 05:51:14 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c68b619e3056e6108c19d1e48abdee52c66267ed96d6be0922a3e7f7e5ad25`  
		Last Modified: Fri, 09 May 2025 05:51:19 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.0.0.7` - unknown; unknown

```console
$ docker pull aerospike@sha256:8f9f13ab004468f0aec057e84d1151057d0ddd2db62f8504ed72a53188cd116e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1895521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7850adc0f6689137c8fec7772b4f2f02c6978e457920ffb87f1bfa76b7b44eb`

```dockerfile
```

-	Layers:
	-	`sha256:4e822857f531c90d33ce40655a168d4346c21de634edbcd94ec40094eac23609`  
		Last Modified: Mon, 05 May 2025 16:35:15 GMT  
		Size: 1.9 MB (1866294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c8db19c83eeca0d1e733f6bdfefc641cf28a25e3588112ff66bca891aeb2cde`  
		Last Modified: Mon, 05 May 2025 16:35:14 GMT  
		Size: 29.2 KB (29227 bytes)  
		MIME: application/vnd.in-toto+json
