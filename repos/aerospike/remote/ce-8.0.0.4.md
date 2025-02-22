## `aerospike:ce-8.0.0.4`

```console
$ docker pull aerospike@sha256:3ded1f4c882cf4a4b28425dfd65550f85bd378b05c052f33619d58020f37cadb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.0.0.4` - linux; amd64

```console
$ docker pull aerospike@sha256:0e30ceccdb330259731bdf8fe9c94246ea3568f27c4aba027c958b5f3a284adb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80152084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:091cab9ee96268dc81b2364524eef0f6f5ef7beffbcc6148f16036afa5bc189f`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2025 20:36:12 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.4 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 21 Feb 2025 20:36:12 GMT
ARG AEROSPIKE_EDITION=community
# Fri, 21 Feb 2025 20:36:12 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.4/aerospike-server-community_8.0.0.4_tools-11.2.0_ubuntu24.04_x86_64.tgz
# Fri, 21 Feb 2025 20:36:12 GMT
ARG AEROSPIKE_SHA_X86_64=98ecd7da193d3311cd2fe31790e9ab8de672f233fdf255be7557f0f73ef6bd9d
# Fri, 21 Feb 2025 20:36:12 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.4/aerospike-server-community_8.0.0.4_tools-11.2.0_ubuntu24.04_aarch64.tgz
# Fri, 21 Feb 2025 20:36:12 GMT
ARG AEROSPIKE_SHA_AARCH64=a919333f5317489e59756cc112f4b07df5a28c3a436022f58b6cc514c7d8fa8f
# Fri, 21 Feb 2025 20:36:12 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 21 Feb 2025 20:36:12 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.4/aerospike-server-community_8.0.0.4_tools-11.2.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=98ecd7da193d3311cd2fe31790e9ab8de672f233fdf255be7557f0f73ef6bd9d AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.4/aerospike-server-community_8.0.0.4_tools-11.2.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=a919333f5317489e59756cc112f4b07df5a28c3a436022f58b6cc514c7d8fa8f
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 21 Feb 2025 20:36:12 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 21 Feb 2025 20:36:12 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 21 Feb 2025 20:36:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Feb 2025 20:36:12 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 21 Feb 2025 20:36:12 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee69580000446c96b1af70f09211a01c0252c4fe076ad7ea21918169ead0971`  
		Last Modified: Fri, 21 Feb 2025 22:27:38 GMT  
		Size: 50.4 MB (50395492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31dd3b18e93e85729b78dbb427beba5cfd056831206f26fe0228098aa120ac0e`  
		Last Modified: Fri, 21 Feb 2025 22:27:37 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9046f8155fde5a93da6d33f3c55f9e7ce3378b5cb3bc6bd714520f815b0483`  
		Last Modified: Fri, 21 Feb 2025 22:27:37 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.0.0.4` - unknown; unknown

```console
$ docker pull aerospike@sha256:b43dc77577c9ec2df532a93926b97df574700e94523bd431aa83350d3abefcf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1895422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b64d05a3b6043235191efca354667e0e186d2b334f663cfaacdc6e26d2eddbb`

```dockerfile
```

-	Layers:
	-	`sha256:963acdcebcddcf74f25aad0f4a7af99b4bb21814f50e08edbb61f31edf2c7243`  
		Last Modified: Fri, 21 Feb 2025 22:27:37 GMT  
		Size: 1.9 MB (1866275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02f841e67b54532b32fe81973b2ccbec633b9ef4e9aeb16d48359ca7fe021d92`  
		Last Modified: Fri, 21 Feb 2025 22:27:37 GMT  
		Size: 29.1 KB (29147 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.0.0.4` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:579273ad59621ea749d7e553dd8235e049470a2df56aea531c5832ec502328fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78515923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0c561abea22316f3c83b87626efbcec26bc1404cb521f1fddceef499e7fbce`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2025 20:36:12 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.4 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 21 Feb 2025 20:36:12 GMT
ARG AEROSPIKE_EDITION=community
# Fri, 21 Feb 2025 20:36:12 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.4/aerospike-server-community_8.0.0.4_tools-11.2.0_ubuntu24.04_x86_64.tgz
# Fri, 21 Feb 2025 20:36:12 GMT
ARG AEROSPIKE_SHA_X86_64=98ecd7da193d3311cd2fe31790e9ab8de672f233fdf255be7557f0f73ef6bd9d
# Fri, 21 Feb 2025 20:36:12 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.4/aerospike-server-community_8.0.0.4_tools-11.2.0_ubuntu24.04_aarch64.tgz
# Fri, 21 Feb 2025 20:36:12 GMT
ARG AEROSPIKE_SHA_AARCH64=a919333f5317489e59756cc112f4b07df5a28c3a436022f58b6cc514c7d8fa8f
# Fri, 21 Feb 2025 20:36:12 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 21 Feb 2025 20:36:12 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.4/aerospike-server-community_8.0.0.4_tools-11.2.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=98ecd7da193d3311cd2fe31790e9ab8de672f233fdf255be7557f0f73ef6bd9d AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.4/aerospike-server-community_8.0.0.4_tools-11.2.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=a919333f5317489e59756cc112f4b07df5a28c3a436022f58b6cc514c7d8fa8f
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 21 Feb 2025 20:36:12 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 21 Feb 2025 20:36:12 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 21 Feb 2025 20:36:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Feb 2025 20:36:12 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 21 Feb 2025 20:36:12 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3322c9e11e1ba81822e256270287e5b901212b8494f4ea8d000a3b9a92dc58e`  
		Last Modified: Fri, 21 Feb 2025 22:28:40 GMT  
		Size: 49.6 MB (49620023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33bd9e8d526f67a35737df834b72d9e7fe3939da4fc0d0f9f0c046000014cbd`  
		Last Modified: Fri, 21 Feb 2025 22:28:38 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222adf97bbde2a3d45ccc745e18490d21fa8538b478d0b28762759f7203d4af4`  
		Last Modified: Fri, 21 Feb 2025 22:28:38 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.0.0.4` - unknown; unknown

```console
$ docker pull aerospike@sha256:24c09006ef040fd6b9abbf166eaa931549ad7c7af8eb094120ecfbe46b957770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1897764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb008e72ed7432b3505301d61245b83d78932cf30792445d3e877c570ad116b`

```dockerfile
```

-	Layers:
	-	`sha256:6dba86ea0996f52ddeedd0141d2aa555b37b1cd9207d4757c31d41266443a23e`  
		Last Modified: Fri, 21 Feb 2025 22:28:39 GMT  
		Size: 1.9 MB (1868537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1822323b293f8121855618040d166e02924a1286a6faad85468016bbc3ddfcaf`  
		Last Modified: Fri, 21 Feb 2025 22:28:41 GMT  
		Size: 29.2 KB (29227 bytes)  
		MIME: application/vnd.in-toto+json
