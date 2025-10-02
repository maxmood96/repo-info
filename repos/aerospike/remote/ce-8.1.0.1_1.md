## `aerospike:ce-8.1.0.1_1`

```console
$ docker pull aerospike@sha256:647363b56b0645023eacc1706eddc27f6be79719f032bbb4eaa9af9dec0be058
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.1.0.1_1` - linux; amd64

```console
$ docker pull aerospike@sha256:ca77c20fa87860f0cf43ef106cde46905d1f7f61c53d7aa62da8051791e7051f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81498633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0fd5acaee088f583f57eeee07872f4d2493cd0a1ec6d550de48421d0fce79a`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
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
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff7d754ad97468c2c83385814b64790987f6708308c9b3febd02c15ba692f16`  
		Last Modified: Tue, 16 Sep 2025 16:52:14 GMT  
		Size: 51.8 MB (51772884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d314e61b2a9d82a7172cf5aacd2d6340d41ea24fa3e18c7ac37ae649f2f2684`  
		Last Modified: Tue, 16 Sep 2025 16:52:12 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c8486e8430ae8b790c0ba55ead53ae7d51d5ea186749e30e92dfb0b925366b`  
		Last Modified: Tue, 16 Sep 2025 16:52:15 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.0.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:67ed1b165e73f3a5b48f1e4ac3d989c77f61ac1be6bee2d9c6fb3e2c7975d631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b41ee3ef5b63db99721f3e2cfedeba4aebf39725b406bc8136ffc713c02f15e2`

```dockerfile
```

-	Layers:
	-	`sha256:fc72b536bf410cc20e13b08e87349915cd03fcf4c356ce372784b35b6d502f4d`  
		Last Modified: Tue, 16 Sep 2025 17:25:24 GMT  
		Size: 2.2 MB (2182312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc37e12e6451afd28bfce864b97d9db62ef7c821fbc1780acdbad819b92ca473`  
		Last Modified: Tue, 16 Sep 2025 17:25:24 GMT  
		Size: 29.0 KB (29009 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.1.0.1_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:efccd6091ef9a183936552891ca9e88dfc5220e89f2acf00db160312306d236d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82073264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c9b3863a8c3f605f7b40e7a9bedddc5eeca3217ca5be1ef6648de9762f28be3`
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
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
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
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492f5e55f24a80b825f8d37103cfe0d4ddb36c537b048df4a47b6c0355aa3af6`  
		Last Modified: Thu, 02 Oct 2025 01:11:29 GMT  
		Size: 53.2 MB (53209389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbd4b166d9168509d9420dfea33db9d9694ba3ba8dee88ad7eab43f8804040d`  
		Last Modified: Thu, 02 Oct 2025 01:55:36 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f800a0ecbd82857388c98095020ae2af89af021551e9346f156224000f91ad`  
		Last Modified: Thu, 02 Oct 2025 01:55:37 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.0.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:4da817098b6f72c7117d1125f9f51d608801bae5f604bfef9c68212d015168dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2213684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b7c857ac051855b4d71ba9cdba566de1018c1f58851880a5119db3e473d445`

```dockerfile
```

-	Layers:
	-	`sha256:07303c7017a766e6c8ac4bd827eae716face772f85c77d6c0d9fa6207c44c21b`  
		Last Modified: Thu, 02 Oct 2025 02:25:22 GMT  
		Size: 2.2 MB (2184592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c5c8f407e1e12aeda2b9853fbf7bf37bf5199ad259f183efb9028afe9793393`  
		Last Modified: Thu, 02 Oct 2025 02:25:22 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json
