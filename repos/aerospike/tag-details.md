<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-8.0.0.7`](#aerospikece-8007)
-	[`aerospike:ce-8.0.0.7_1`](#aerospikece-8007_1)
-	[`aerospike:ee-8.0.0.7`](#aerospikeee-8007)
-	[`aerospike:ee-8.0.0.7_1`](#aerospikeee-8007_1)

## `aerospike:ce-8.0.0.7`

```console
$ docker pull aerospike@sha256:3a30c89ef60c2740a54eb714fa1ebc63afd1cc8822f921d1a8d8c979db9df972
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.0.0.7` - linux; amd64

```console
$ docker pull aerospike@sha256:8a88f4a66f9b38f407bd607a20154c5d7edb4a189a4223c8c21c8bc20b3a490d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81064773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15e390db16377d96e166c8622ae2b6d5067e10bb1ef3479bfa65a56c11c5458`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ee451cfbff0b14c6c4ef82325300566b8bcec9bfb1d8ed7925e5b07163daec`  
		Last Modified: Fri, 25 Apr 2025 21:50:49 GMT  
		Size: 51.3 MB (51344821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0755ce0c06e7e0dbd663f19d913eb64d721efcb62199722dd688fc5bc8a9b8`  
		Last Modified: Fri, 25 Apr 2025 21:50:47 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a535d7af140afdb9c0e0b21351be6f896017e1327c409975c1dea2c49b606ff`  
		Last Modified: Fri, 25 Apr 2025 21:50:47 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.0.0.7` - unknown; unknown

```console
$ docker pull aerospike@sha256:a6928a5e76bafb8f6d43014a834a501bea9737cb5706905e480f53747b007580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1893175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f15e19d36006cc7ed152d5320930a74516926a96703d8303af5b4ab94016b2`

```dockerfile
```

-	Layers:
	-	`sha256:bb8a85feedcb3072a7ab51e3ae9222687b54c27e853c7ac4d7070f15929070fb`  
		Last Modified: Fri, 25 Apr 2025 21:50:48 GMT  
		Size: 1.9 MB (1864028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89339d2cfc3d7b6f9c6fda5b9749728f63263ce8838ea28a2b50dd5cb636ec93`  
		Last Modified: Fri, 25 Apr 2025 21:50:47 GMT  
		Size: 29.1 KB (29147 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.0.0.7` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:c66eddab6a2168ecb90ba3459f9ea572bece4e4689aa3a6b17b8d263494cda43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79616680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c504931518bbe64362db2c9aeb71de10df38136d8bf19f2defac73208a8d3c2`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
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
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7667ca2782234d13b33be65f40d78c1207eabdb7d452c37f1c27ca386b8a2581`  
		Last Modified: Fri, 25 Apr 2025 21:51:52 GMT  
		Size: 50.8 MB (50767421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be597a594e489a0b21b90db8bca106d46914f1f32c54826d1a399491d2eba21b`  
		Last Modified: Fri, 25 Apr 2025 21:51:50 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6116153bdd8fe2932fd6ed9d2f84e80733de4d0bb602d97a51b644d5553003d9`  
		Last Modified: Fri, 25 Apr 2025 21:51:50 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.0.0.7` - unknown; unknown

```console
$ docker pull aerospike@sha256:8f1e31b31ba0b63bdcef8729d91824f85312d7df5eb006e16b88827d72fef135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1895516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7a89057faca3b3eb6e6f9790b1272c2a013a78961a7d3af33b623b5e80e697`

```dockerfile
```

-	Layers:
	-	`sha256:220b7f9b394b2633cb0aab30705a00818eb0c538c12d00a254d6b074e8d1534c`  
		Last Modified: Fri, 25 Apr 2025 21:51:51 GMT  
		Size: 1.9 MB (1866290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acce13d6f7da22c94da9f8eaf056e11ae5c22741580e7d991d982b0d56ba86bb`  
		Last Modified: Fri, 25 Apr 2025 21:51:50 GMT  
		Size: 29.2 KB (29226 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ce-8.0.0.7_1`

```console
$ docker pull aerospike@sha256:3a30c89ef60c2740a54eb714fa1ebc63afd1cc8822f921d1a8d8c979db9df972
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.0.0.7_1` - linux; amd64

```console
$ docker pull aerospike@sha256:8a88f4a66f9b38f407bd607a20154c5d7edb4a189a4223c8c21c8bc20b3a490d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81064773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15e390db16377d96e166c8622ae2b6d5067e10bb1ef3479bfa65a56c11c5458`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ee451cfbff0b14c6c4ef82325300566b8bcec9bfb1d8ed7925e5b07163daec`  
		Last Modified: Fri, 25 Apr 2025 21:50:49 GMT  
		Size: 51.3 MB (51344821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0755ce0c06e7e0dbd663f19d913eb64d721efcb62199722dd688fc5bc8a9b8`  
		Last Modified: Fri, 25 Apr 2025 21:50:47 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a535d7af140afdb9c0e0b21351be6f896017e1327c409975c1dea2c49b606ff`  
		Last Modified: Fri, 25 Apr 2025 21:50:47 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.0.0.7_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:a6928a5e76bafb8f6d43014a834a501bea9737cb5706905e480f53747b007580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1893175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f15e19d36006cc7ed152d5320930a74516926a96703d8303af5b4ab94016b2`

```dockerfile
```

-	Layers:
	-	`sha256:bb8a85feedcb3072a7ab51e3ae9222687b54c27e853c7ac4d7070f15929070fb`  
		Last Modified: Fri, 25 Apr 2025 21:50:48 GMT  
		Size: 1.9 MB (1864028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89339d2cfc3d7b6f9c6fda5b9749728f63263ce8838ea28a2b50dd5cb636ec93`  
		Last Modified: Fri, 25 Apr 2025 21:50:47 GMT  
		Size: 29.1 KB (29147 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.0.0.7_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:c66eddab6a2168ecb90ba3459f9ea572bece4e4689aa3a6b17b8d263494cda43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79616680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c504931518bbe64362db2c9aeb71de10df38136d8bf19f2defac73208a8d3c2`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
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
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7667ca2782234d13b33be65f40d78c1207eabdb7d452c37f1c27ca386b8a2581`  
		Last Modified: Fri, 25 Apr 2025 21:51:52 GMT  
		Size: 50.8 MB (50767421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be597a594e489a0b21b90db8bca106d46914f1f32c54826d1a399491d2eba21b`  
		Last Modified: Fri, 25 Apr 2025 21:51:50 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6116153bdd8fe2932fd6ed9d2f84e80733de4d0bb602d97a51b644d5553003d9`  
		Last Modified: Fri, 25 Apr 2025 21:51:50 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.0.0.7_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:8f1e31b31ba0b63bdcef8729d91824f85312d7df5eb006e16b88827d72fef135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1895516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7a89057faca3b3eb6e6f9790b1272c2a013a78961a7d3af33b623b5e80e697`

```dockerfile
```

-	Layers:
	-	`sha256:220b7f9b394b2633cb0aab30705a00818eb0c538c12d00a254d6b074e8d1534c`  
		Last Modified: Fri, 25 Apr 2025 21:51:51 GMT  
		Size: 1.9 MB (1866290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acce13d6f7da22c94da9f8eaf056e11ae5c22741580e7d991d982b0d56ba86bb`  
		Last Modified: Fri, 25 Apr 2025 21:51:50 GMT  
		Size: 29.2 KB (29226 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ee-8.0.0.7`

```console
$ docker pull aerospike@sha256:b245babe21da1ddd5dfbe3feaa23db22c3dbab0d8d4d60fbb6fc96b00fae8e93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.0.0.7` - linux; amd64

```console
$ docker pull aerospike@sha256:79ac3386a866ae6b840de901b55eb4007d608f2947cadc0b6482d78c78ab0d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.3 MB (85347009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff90ff90374b133b04c0d9b6bf90f126ea6c8720545a9bb06e46cf4a5cfe1bd`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
CMD ["/bin/bash"]
# Fri, 25 Apr 2025 21:09:11 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.7 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_EDITION=enterprise
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.7/aerospike-server-enterprise_8.0.0.7_tools-11.2.2_ubuntu24.04_x86_64.tgz
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_SHA_X86_64=3c694546fe7ae6e41f6d62a26e6d134e35fb9de1b955683e60b9970b778c3e63
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.7/aerospike-server-enterprise_8.0.0.7_tools-11.2.2_ubuntu24.04_aarch64.tgz
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_SHA_AARCH64=6403cc7bc2941ff3958353e602b69dd16c9381e39c9e5d3262087818c019fc20
# Fri, 25 Apr 2025 21:09:11 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 25 Apr 2025 21:09:11 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.7/aerospike-server-enterprise_8.0.0.7_tools-11.2.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=3c694546fe7ae6e41f6d62a26e6d134e35fb9de1b955683e60b9970b778c3e63 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.7/aerospike-server-enterprise_8.0.0.7_tools-11.2.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=6403cc7bc2941ff3958353e602b69dd16c9381e39c9e5d3262087818c019fc20
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09b41ddf66e2534a8dc92fdb84f1cab35d7e80b0c90b8b941d676fefc368169`  
		Last Modified: Fri, 25 Apr 2025 21:50:41 GMT  
		Size: 55.6 MB (55627060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee3eb829bfa2d50355c2adbb55a85d6f22054a8f1f587da4dcaf571bbaf2a40`  
		Last Modified: Fri, 25 Apr 2025 21:50:40 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f83ca2ba0078602a55a494c68844f6122928b9d1150066015dd42ce1ffe61d8`  
		Last Modified: Fri, 25 Apr 2025 21:50:40 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.0.0.7` - unknown; unknown

```console
$ docker pull aerospike@sha256:57f4f71d4622599fb0062736d1997b75d86e9fd429d008114622a5afe46760fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1987072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0457739e21ae605847717d1c2f4d6b7bbb8f8734b8063063be7a629456ad8f`

```dockerfile
```

-	Layers:
	-	`sha256:659edb3bd61148d4127435c1bbc16c201f12ccc03b1563571118bfaee1cb657c`  
		Last Modified: Fri, 25 Apr 2025 21:50:40 GMT  
		Size: 2.0 MB (1957910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc5698903ee2db5ca9d5e9c26c1864d7a96f8dcc3a17e1edae79f461923f2f26`  
		Last Modified: Fri, 25 Apr 2025 21:50:40 GMT  
		Size: 29.2 KB (29162 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.0.0.7` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:0e234c1b85c1a96e59cb01e40a0fb5a321547f3a5c24a76bd32585af41a683e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83924760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef74d6673b257dcff57defa454173fa1cba89cb668f1f6608273548c938a81b`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Fri, 25 Apr 2025 21:09:11 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.7 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_EDITION=enterprise
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.7/aerospike-server-enterprise_8.0.0.7_tools-11.2.2_ubuntu24.04_x86_64.tgz
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_SHA_X86_64=3c694546fe7ae6e41f6d62a26e6d134e35fb9de1b955683e60b9970b778c3e63
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.7/aerospike-server-enterprise_8.0.0.7_tools-11.2.2_ubuntu24.04_aarch64.tgz
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_SHA_AARCH64=6403cc7bc2941ff3958353e602b69dd16c9381e39c9e5d3262087818c019fc20
# Fri, 25 Apr 2025 21:09:11 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 25 Apr 2025 21:09:11 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.7/aerospike-server-enterprise_8.0.0.7_tools-11.2.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=3c694546fe7ae6e41f6d62a26e6d134e35fb9de1b955683e60b9970b778c3e63 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.7/aerospike-server-enterprise_8.0.0.7_tools-11.2.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=6403cc7bc2941ff3958353e602b69dd16c9381e39c9e5d3262087818c019fc20
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
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb971b8587e55b03ee0f80115da9ea9c4cdb2954522a15bf7e7d414d572e188`  
		Last Modified: Fri, 25 Apr 2025 21:51:16 GMT  
		Size: 55.1 MB (55075503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a89f17fe6e8281119777ae211e84839b493b15fe195bc66e68c2b7c88bd5f1e`  
		Last Modified: Fri, 25 Apr 2025 21:51:13 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e77dabb1ff5b6f5990e1e956c1ecd5b2c4aed5f730928bf605a39872e18de2e`  
		Last Modified: Fri, 25 Apr 2025 21:51:13 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.0.0.7` - unknown; unknown

```console
$ docker pull aerospike@sha256:d26f25739be92207deb22f606f03cb099b67f3d2d48de1d54f46694973943930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1989433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38092d063089854468462c1edf9b8b32b9a8fa65c89e80c7e4b87d40451881f8`

```dockerfile
```

-	Layers:
	-	`sha256:eeeb20d4e72ffe34c2ef44932e54594cb166359d77e91aafb9e8915809dd10d4`  
		Last Modified: Fri, 25 Apr 2025 21:51:13 GMT  
		Size: 2.0 MB (1960190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c376d8bc8d885ec169e008aadf4d38bf4315f7c7f577481248db39b3417cd49`  
		Last Modified: Fri, 25 Apr 2025 21:51:13 GMT  
		Size: 29.2 KB (29243 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ee-8.0.0.7_1`

```console
$ docker pull aerospike@sha256:b245babe21da1ddd5dfbe3feaa23db22c3dbab0d8d4d60fbb6fc96b00fae8e93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.0.0.7_1` - linux; amd64

```console
$ docker pull aerospike@sha256:79ac3386a866ae6b840de901b55eb4007d608f2947cadc0b6482d78c78ab0d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.3 MB (85347009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff90ff90374b133b04c0d9b6bf90f126ea6c8720545a9bb06e46cf4a5cfe1bd`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
CMD ["/bin/bash"]
# Fri, 25 Apr 2025 21:09:11 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.7 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_EDITION=enterprise
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.7/aerospike-server-enterprise_8.0.0.7_tools-11.2.2_ubuntu24.04_x86_64.tgz
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_SHA_X86_64=3c694546fe7ae6e41f6d62a26e6d134e35fb9de1b955683e60b9970b778c3e63
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.7/aerospike-server-enterprise_8.0.0.7_tools-11.2.2_ubuntu24.04_aarch64.tgz
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_SHA_AARCH64=6403cc7bc2941ff3958353e602b69dd16c9381e39c9e5d3262087818c019fc20
# Fri, 25 Apr 2025 21:09:11 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 25 Apr 2025 21:09:11 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.7/aerospike-server-enterprise_8.0.0.7_tools-11.2.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=3c694546fe7ae6e41f6d62a26e6d134e35fb9de1b955683e60b9970b778c3e63 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.7/aerospike-server-enterprise_8.0.0.7_tools-11.2.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=6403cc7bc2941ff3958353e602b69dd16c9381e39c9e5d3262087818c019fc20
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09b41ddf66e2534a8dc92fdb84f1cab35d7e80b0c90b8b941d676fefc368169`  
		Last Modified: Fri, 25 Apr 2025 21:50:41 GMT  
		Size: 55.6 MB (55627060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee3eb829bfa2d50355c2adbb55a85d6f22054a8f1f587da4dcaf571bbaf2a40`  
		Last Modified: Fri, 25 Apr 2025 21:50:40 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f83ca2ba0078602a55a494c68844f6122928b9d1150066015dd42ce1ffe61d8`  
		Last Modified: Fri, 25 Apr 2025 21:50:40 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.0.0.7_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:57f4f71d4622599fb0062736d1997b75d86e9fd429d008114622a5afe46760fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1987072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0457739e21ae605847717d1c2f4d6b7bbb8f8734b8063063be7a629456ad8f`

```dockerfile
```

-	Layers:
	-	`sha256:659edb3bd61148d4127435c1bbc16c201f12ccc03b1563571118bfaee1cb657c`  
		Last Modified: Fri, 25 Apr 2025 21:50:40 GMT  
		Size: 2.0 MB (1957910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc5698903ee2db5ca9d5e9c26c1864d7a96f8dcc3a17e1edae79f461923f2f26`  
		Last Modified: Fri, 25 Apr 2025 21:50:40 GMT  
		Size: 29.2 KB (29162 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.0.0.7_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:0e234c1b85c1a96e59cb01e40a0fb5a321547f3a5c24a76bd32585af41a683e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83924760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef74d6673b257dcff57defa454173fa1cba89cb668f1f6608273548c938a81b`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Fri, 25 Apr 2025 21:09:11 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.7 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_EDITION=enterprise
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.7/aerospike-server-enterprise_8.0.0.7_tools-11.2.2_ubuntu24.04_x86_64.tgz
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_SHA_X86_64=3c694546fe7ae6e41f6d62a26e6d134e35fb9de1b955683e60b9970b778c3e63
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.7/aerospike-server-enterprise_8.0.0.7_tools-11.2.2_ubuntu24.04_aarch64.tgz
# Fri, 25 Apr 2025 21:09:11 GMT
ARG AEROSPIKE_SHA_AARCH64=6403cc7bc2941ff3958353e602b69dd16c9381e39c9e5d3262087818c019fc20
# Fri, 25 Apr 2025 21:09:11 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 25 Apr 2025 21:09:11 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.7/aerospike-server-enterprise_8.0.0.7_tools-11.2.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=3c694546fe7ae6e41f6d62a26e6d134e35fb9de1b955683e60b9970b778c3e63 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.7/aerospike-server-enterprise_8.0.0.7_tools-11.2.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=6403cc7bc2941ff3958353e602b69dd16c9381e39c9e5d3262087818c019fc20
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
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb971b8587e55b03ee0f80115da9ea9c4cdb2954522a15bf7e7d414d572e188`  
		Last Modified: Fri, 25 Apr 2025 21:51:16 GMT  
		Size: 55.1 MB (55075503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a89f17fe6e8281119777ae211e84839b493b15fe195bc66e68c2b7c88bd5f1e`  
		Last Modified: Fri, 25 Apr 2025 21:51:13 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e77dabb1ff5b6f5990e1e956c1ecd5b2c4aed5f730928bf605a39872e18de2e`  
		Last Modified: Fri, 25 Apr 2025 21:51:13 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.0.0.7_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:d26f25739be92207deb22f606f03cb099b67f3d2d48de1d54f46694973943930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1989433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38092d063089854468462c1edf9b8b32b9a8fa65c89e80c7e4b87d40451881f8`

```dockerfile
```

-	Layers:
	-	`sha256:eeeb20d4e72ffe34c2ef44932e54594cb166359d77e91aafb9e8915809dd10d4`  
		Last Modified: Fri, 25 Apr 2025 21:51:13 GMT  
		Size: 2.0 MB (1960190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c376d8bc8d885ec169e008aadf4d38bf4315f7c7f577481248db39b3417cd49`  
		Last Modified: Fri, 25 Apr 2025 21:51:13 GMT  
		Size: 29.2 KB (29243 bytes)  
		MIME: application/vnd.in-toto+json
