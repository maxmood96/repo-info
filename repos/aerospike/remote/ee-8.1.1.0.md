## `aerospike:ee-8.1.1.0`

```console
$ docker pull aerospike@sha256:ddcc73e614c9988dcc2d7524fd6ba0541cd1c5c54f005aff560d37954eba87e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.1.1.0` - linux; amd64

```console
$ docker pull aerospike@sha256:74dea9d06b2670db7e2642ba151fd0c6ca543997d5e2fc36d064ec708f93f799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88660714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e1adee88bd31fb494e673f11aaa217de8b07d309fddb6759fda21ce1ffd963`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 20:01:37 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.1.0 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Mon, 09 Feb 2026 20:01:37 GMT
ARG AEROSPIKE_EDITION=enterprise
# Mon, 09 Feb 2026 20:01:37 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Mon, 09 Feb 2026 20:01:37 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.0/aerospike-server-enterprise_8.1.1.0_tools-12.1.1_ubuntu24.04_x86_64.tgz
# Mon, 09 Feb 2026 20:01:37 GMT
ARG AEROSPIKE_SHA_X86_64=11c05208d3a982514c0b4ffd4e256f214f08aaf330e0712f659ade5c2782e982
# Mon, 09 Feb 2026 20:01:37 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.0/aerospike-server-enterprise_8.1.1.0_tools-12.1.1_ubuntu24.04_aarch64.tgz
# Mon, 09 Feb 2026 20:01:37 GMT
ARG AEROSPIKE_SHA_AARCH64=cfb43ed21b27bc77ccf5d35e42f47f7b40fba6c4002e755d4c20962f18608a77
# Mon, 09 Feb 2026 20:01:37 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Mon, 09 Feb 2026 20:01:37 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.0/aerospike-server-enterprise_8.1.1.0_tools-12.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=11c05208d3a982514c0b4ffd4e256f214f08aaf330e0712f659ade5c2782e982 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.0/aerospike-server-enterprise_8.1.1.0_tools-12.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=cfb43ed21b27bc77ccf5d35e42f47f7b40fba6c4002e755d4c20962f18608a77
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Mon, 09 Feb 2026 20:01:37 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Mon, 09 Feb 2026 20:01:37 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Mon, 09 Feb 2026 20:01:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 20:01:37 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Mon, 09 Feb 2026 20:01:37 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe630ac5a265e976fbaf689defd6fa6313cef25e343876a3a8a9286411aade3`  
		Last Modified: Mon, 09 Feb 2026 20:01:49 GMT  
		Size: 58.9 MB (58932407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fc992b4f5276444c22f4fc00926aa4ce8044f542626c5e3c915b34767f5bef`  
		Last Modified: Mon, 09 Feb 2026 20:01:47 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786f749492e2d03e70abe9ec4eeb23618cbc0922c5491b1c75ca807981906941`  
		Last Modified: Mon, 09 Feb 2026 20:01:47 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.1.0` - unknown; unknown

```console
$ docker pull aerospike@sha256:4642033003e7d1f7e209dbeff3596e54feb628f1c6f6e09dce26756534cfdf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65dd027ffaf14a8b3150eaa20145d1ab8cb5c04ab93f8cefce0a16b900ac6c35`

```dockerfile
```

-	Layers:
	-	`sha256:97e494fff4056d20f56136d485fc6954c1f52b9a4ef31f59a8d2394952910347`  
		Last Modified: Mon, 09 Feb 2026 20:01:47 GMT  
		Size: 2.2 MB (2181581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f68c59b6d0f4eed1cf3fde7e24240418aadb1d04b4302ea912efb3d68a1065b`  
		Last Modified: Mon, 09 Feb 2026 20:01:47 GMT  
		Size: 29.0 KB (28985 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.1.1.0` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:7a5633115ad9c2f023d8a3155675a30e5b8d43cfa2c2c88946cbfc1094d2d7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86405686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c18c0928a5045b460b99a6afbc2ab0e08e8b356fcd4bcfa257d03535b314b9`
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
# Mon, 09 Feb 2026 20:01:31 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.1.0 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Mon, 09 Feb 2026 20:01:31 GMT
ARG AEROSPIKE_EDITION=enterprise
# Mon, 09 Feb 2026 20:01:31 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Mon, 09 Feb 2026 20:01:31 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.0/aerospike-server-enterprise_8.1.1.0_tools-12.1.1_ubuntu24.04_x86_64.tgz
# Mon, 09 Feb 2026 20:01:31 GMT
ARG AEROSPIKE_SHA_X86_64=11c05208d3a982514c0b4ffd4e256f214f08aaf330e0712f659ade5c2782e982
# Mon, 09 Feb 2026 20:01:31 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.0/aerospike-server-enterprise_8.1.1.0_tools-12.1.1_ubuntu24.04_aarch64.tgz
# Mon, 09 Feb 2026 20:01:31 GMT
ARG AEROSPIKE_SHA_AARCH64=cfb43ed21b27bc77ccf5d35e42f47f7b40fba6c4002e755d4c20962f18608a77
# Mon, 09 Feb 2026 20:01:31 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Mon, 09 Feb 2026 20:01:31 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.0/aerospike-server-enterprise_8.1.1.0_tools-12.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=11c05208d3a982514c0b4ffd4e256f214f08aaf330e0712f659ade5c2782e982 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.1.0/aerospike-server-enterprise_8.1.1.0_tools-12.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=cfb43ed21b27bc77ccf5d35e42f47f7b40fba6c4002e755d4c20962f18608a77
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Mon, 09 Feb 2026 20:01:31 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Mon, 09 Feb 2026 20:01:31 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Mon, 09 Feb 2026 20:01:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 20:01:31 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Mon, 09 Feb 2026 20:01:31 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0b6c5ae4643a99b5c96385ee0a2867be46592117b2f49cba6d6f6a401dddb7`  
		Last Modified: Mon, 09 Feb 2026 20:01:44 GMT  
		Size: 57.5 MB (57539563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6519d95b7d6da93419331594629ce49bc241bcecd9bebfae91691b1bbd535d9e`  
		Last Modified: Mon, 09 Feb 2026 20:01:42 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03964e8e02b78145267a56ae65c86fa70c663f77acbbcb502f31392ab4715eee`  
		Last Modified: Mon, 09 Feb 2026 20:01:43 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.1.0` - unknown; unknown

```console
$ docker pull aerospike@sha256:0cbbb9787ebba6ba9bd872ef503b62a07cdf69636ea29165dfbffb92aeec11a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538064462bd25bf9e0b577493222715da6e4cd3f6d1137c80c03e05abcf2b947`

```dockerfile
```

-	Layers:
	-	`sha256:122ff1119ba8e544b346bef71bd943c5b12a731b01b121276a607fa1d6229a09`  
		Last Modified: Mon, 09 Feb 2026 20:01:43 GMT  
		Size: 2.2 MB (2183861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd9b3dcc3660fbef3677772937ca918a6f471571cccfc49df928f503f1d637a`  
		Last Modified: Mon, 09 Feb 2026 20:01:43 GMT  
		Size: 29.1 KB (29064 bytes)  
		MIME: application/vnd.in-toto+json
