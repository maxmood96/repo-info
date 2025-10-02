<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-8.1.0.1`](#aerospikece-8101)
-	[`aerospike:ce-8.1.0.1_1`](#aerospikece-8101_1)
-	[`aerospike:ee-8.1.0.1`](#aerospikeee-8101)
-	[`aerospike:ee-8.1.0.1_1`](#aerospikeee-8101_1)

## `aerospike:ce-8.1.0.1`

```console
$ docker pull aerospike@sha256:69c56eda3f2e9e21809595a47f78465c4c77049d14122c572706ee7208996066
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.1.0.1` - linux; amd64

```console
$ docker pull aerospike@sha256:7b765092966e7a1480292edd702a72688c8745ff35b7b234a60c1bc6c789c0ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83899892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603acbb28433c40081d940a5876b512b0dd6f43feccebec1253c930c9cb0714e`
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
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
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
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe603bcc664a30b1a41b316c0bb6b2c591efa40306856acfa93b08f2042a450d`  
		Last Modified: Thu, 02 Oct 2025 04:52:03 GMT  
		Size: 54.2 MB (54174586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f2b50a8b61366a44e2cfeaa77191dadae7b6fa94d9f73990a6232d2093f8dd`  
		Last Modified: Thu, 02 Oct 2025 04:51:56 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42876791bd143246146ad149ddcfcf3919276c1f1dbc30afc7d8a6fd19e1629`  
		Last Modified: Thu, 02 Oct 2025 04:51:57 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.0.1` - unknown; unknown

```console
$ docker pull aerospike@sha256:9ef409308b90d0082d5a8575b68d698ba9036b220ecaedd2e4a71652d7ccd1a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4fc76eeea64af5d11d9b148c230a30324c2d93250a1df1108e5ab38c41008c`

```dockerfile
```

-	Layers:
	-	`sha256:53c0722593ad594927a74d6b1a627b2be27bc5342a4bdb266115a1b6573b580f`  
		Last Modified: Thu, 02 Oct 2025 05:25:18 GMT  
		Size: 2.2 MB (2182312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cab25d3703211ad886bd4b35c557894c202d1178c40cfae06f4a6f776b5a83b`  
		Last Modified: Thu, 02 Oct 2025 05:25:19 GMT  
		Size: 29.0 KB (29012 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.1.0.1` - linux; arm64 variant v8

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
		Last Modified: Thu, 02 Oct 2025 20:39:23 GMT  
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

### `aerospike:ce-8.1.0.1` - unknown; unknown

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

## `aerospike:ce-8.1.0.1_1`

```console
$ docker pull aerospike@sha256:69c56eda3f2e9e21809595a47f78465c4c77049d14122c572706ee7208996066
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.1.0.1_1` - linux; amd64

```console
$ docker pull aerospike@sha256:7b765092966e7a1480292edd702a72688c8745ff35b7b234a60c1bc6c789c0ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83899892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603acbb28433c40081d940a5876b512b0dd6f43feccebec1253c930c9cb0714e`
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
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
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
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe603bcc664a30b1a41b316c0bb6b2c591efa40306856acfa93b08f2042a450d`  
		Last Modified: Thu, 02 Oct 2025 04:52:03 GMT  
		Size: 54.2 MB (54174586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f2b50a8b61366a44e2cfeaa77191dadae7b6fa94d9f73990a6232d2093f8dd`  
		Last Modified: Thu, 02 Oct 2025 04:51:56 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42876791bd143246146ad149ddcfcf3919276c1f1dbc30afc7d8a6fd19e1629`  
		Last Modified: Thu, 02 Oct 2025 04:51:57 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.0.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:9ef409308b90d0082d5a8575b68d698ba9036b220ecaedd2e4a71652d7ccd1a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4fc76eeea64af5d11d9b148c230a30324c2d93250a1df1108e5ab38c41008c`

```dockerfile
```

-	Layers:
	-	`sha256:53c0722593ad594927a74d6b1a627b2be27bc5342a4bdb266115a1b6573b580f`  
		Last Modified: Thu, 02 Oct 2025 05:25:18 GMT  
		Size: 2.2 MB (2182312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cab25d3703211ad886bd4b35c557894c202d1178c40cfae06f4a6f776b5a83b`  
		Last Modified: Thu, 02 Oct 2025 05:25:19 GMT  
		Size: 29.0 KB (29012 bytes)  
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
		Last Modified: Thu, 02 Oct 2025 20:39:23 GMT  
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

## `aerospike:ee-8.1.0.1`

```console
$ docker pull aerospike@sha256:2febd1b3672ad67aa1482441ed9504c7a943450a26755b6ca000f5032415cea0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.1.0.1` - linux; amd64

```console
$ docker pull aerospike@sha256:24ce5ddf33df4b59ed6bb2b9eee673990bacf9ef355b769761048c2f568ff0b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (85999471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e7282deeed6c1c25a9e2e45375d141c5f21607317a986dfa55820accbc3281`
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
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
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
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64f5c84a8a3275c0bc1b64754450f87efda8faeda048730c1023bd141c55d11`  
		Last Modified: Thu, 02 Oct 2025 04:52:02 GMT  
		Size: 56.3 MB (56274162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00e65b6ead720d6c308fb065668e1fa4b97125e97fcf5add38926710fda1053`  
		Last Modified: Thu, 02 Oct 2025 04:51:56 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4b58af3cf885bb29b0bf005a2e98d8abdc44d5118ed493aa76dace18beda78`  
		Last Modified: Thu, 02 Oct 2025 04:51:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.0.1` - unknown; unknown

```console
$ docker pull aerospike@sha256:cecc0bcdc50fffdf67ee377aef02695915cbc4fc2ccac9d9e161141f3b3907a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd0a288707899657191582f2daf147e5fd463551ff76469bf25bcea92fe0398`

```dockerfile
```

-	Layers:
	-	`sha256:ebee874590e5bc218c147a4d345b5dea4a6f5dbdc5a8bb2b0cd001ecf3cea974`  
		Last Modified: Thu, 02 Oct 2025 05:25:25 GMT  
		Size: 2.2 MB (2182953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47421e90faae2705c10aa3e1a9f4f4b72c555f965a9d7704862094d8e53d2b97`  
		Last Modified: Thu, 02 Oct 2025 05:25:25 GMT  
		Size: 29.0 KB (29026 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.1.0.1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:d178cf42d056f9b9b5c4df3c9b91551d8871ea9a41b2152ade59c81d41584f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84163541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5527e88f4e8d3fdf2c0fa55fbde607a3d50b335a11694585c64ab90288629ec9`
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
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376f3dd9a965d32d6c63322d3a40c4b516fbd213722278263896aca6b9f4306d`  
		Last Modified: Thu, 02 Oct 2025 01:11:03 GMT  
		Size: 55.3 MB (55299666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fb79da22ba2cd680e45e996d5d13b8cd7620b4be33ed19f75bfbc1f5490fb8`  
		Last Modified: Thu, 02 Oct 2025 01:10:59 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8f89f79de038345f6fa7f29c1465720561cbf37748cf6db5f7c1ca0d5492d5`  
		Last Modified: Thu, 02 Oct 2025 01:10:59 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.0.1` - unknown; unknown

```console
$ docker pull aerospike@sha256:2ef52c2f2ab571de20ec1f16d353c1152396489a70939c13dede4deb4e0b3733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d2ec96a3aae3b419df70c301fbce59a89c39a69d22fdd19797440b98d016df`

```dockerfile
```

-	Layers:
	-	`sha256:2c6eae641861fe964548e51453648d238be2a54343dada641ceb2d411df1c6df`  
		Last Modified: Thu, 02 Oct 2025 02:25:30 GMT  
		Size: 2.2 MB (2185233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c86c4a6f780b57a392811a19ef085730829bc280ff80146306369d873c197e4c`  
		Last Modified: Thu, 02 Oct 2025 02:25:31 GMT  
		Size: 29.1 KB (29108 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ee-8.1.0.1_1`

```console
$ docker pull aerospike@sha256:2febd1b3672ad67aa1482441ed9504c7a943450a26755b6ca000f5032415cea0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.1.0.1_1` - linux; amd64

```console
$ docker pull aerospike@sha256:24ce5ddf33df4b59ed6bb2b9eee673990bacf9ef355b769761048c2f568ff0b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (85999471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e7282deeed6c1c25a9e2e45375d141c5f21607317a986dfa55820accbc3281`
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
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
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
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64f5c84a8a3275c0bc1b64754450f87efda8faeda048730c1023bd141c55d11`  
		Last Modified: Thu, 02 Oct 2025 04:52:02 GMT  
		Size: 56.3 MB (56274162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00e65b6ead720d6c308fb065668e1fa4b97125e97fcf5add38926710fda1053`  
		Last Modified: Thu, 02 Oct 2025 04:51:56 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4b58af3cf885bb29b0bf005a2e98d8abdc44d5118ed493aa76dace18beda78`  
		Last Modified: Thu, 02 Oct 2025 04:51:56 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.0.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:cecc0bcdc50fffdf67ee377aef02695915cbc4fc2ccac9d9e161141f3b3907a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd0a288707899657191582f2daf147e5fd463551ff76469bf25bcea92fe0398`

```dockerfile
```

-	Layers:
	-	`sha256:ebee874590e5bc218c147a4d345b5dea4a6f5dbdc5a8bb2b0cd001ecf3cea974`  
		Last Modified: Thu, 02 Oct 2025 05:25:25 GMT  
		Size: 2.2 MB (2182953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47421e90faae2705c10aa3e1a9f4f4b72c555f965a9d7704862094d8e53d2b97`  
		Last Modified: Thu, 02 Oct 2025 05:25:25 GMT  
		Size: 29.0 KB (29026 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.1.0.1_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:d178cf42d056f9b9b5c4df3c9b91551d8871ea9a41b2152ade59c81d41584f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84163541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5527e88f4e8d3fdf2c0fa55fbde607a3d50b335a11694585c64ab90288629ec9`
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
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376f3dd9a965d32d6c63322d3a40c4b516fbd213722278263896aca6b9f4306d`  
		Last Modified: Thu, 02 Oct 2025 01:11:03 GMT  
		Size: 55.3 MB (55299666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fb79da22ba2cd680e45e996d5d13b8cd7620b4be33ed19f75bfbc1f5490fb8`  
		Last Modified: Thu, 02 Oct 2025 01:10:59 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8f89f79de038345f6fa7f29c1465720561cbf37748cf6db5f7c1ca0d5492d5`  
		Last Modified: Thu, 02 Oct 2025 01:10:59 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.0.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:2ef52c2f2ab571de20ec1f16d353c1152396489a70939c13dede4deb4e0b3733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d2ec96a3aae3b419df70c301fbce59a89c39a69d22fdd19797440b98d016df`

```dockerfile
```

-	Layers:
	-	`sha256:2c6eae641861fe964548e51453648d238be2a54343dada641ceb2d411df1c6df`  
		Last Modified: Thu, 02 Oct 2025 02:25:30 GMT  
		Size: 2.2 MB (2185233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c86c4a6f780b57a392811a19ef085730829bc280ff80146306369d873c197e4c`  
		Last Modified: Thu, 02 Oct 2025 02:25:31 GMT  
		Size: 29.1 KB (29108 bytes)  
		MIME: application/vnd.in-toto+json
