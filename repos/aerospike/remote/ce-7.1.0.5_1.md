## `aerospike:ce-7.1.0.5_1`

```console
$ docker pull aerospike@sha256:37f83c329f90d16798d9a6f4a03f50ff672fdfc6af226193d1d9819ba2149820
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-7.1.0.5_1` - linux; amd64

```console
$ docker pull aerospike@sha256:665faec34efebc01b8fccaad7698c79f1a1d8e1b418f555970a30fc28ad1eb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77368093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05d6ac7df1470c14ff384d97962d7744ef2560b87a9a9cdf2ab452cf20b8794`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Wed, 14 Aug 2024 06:09:32 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.5 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Wed, 14 Aug 2024 06:09:32 GMT
ARG AEROSPIKE_EDITION=community
# Wed, 14 Aug 2024 06:09:32 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.5/aerospike-server-community_7.1.0.5_tools-11.0.2_ubuntu22.04_x86_64.tgz
# Wed, 14 Aug 2024 06:09:32 GMT
ARG AEROSPIKE_SHA_X86_64=fdd8f48724872f024a787ececb1f8e21f15de74c82082bba840cf69f5ec2730c
# Wed, 14 Aug 2024 06:09:32 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.5/aerospike-server-community_7.1.0.5_tools-11.0.2_ubuntu22.04_aarch64.tgz
# Wed, 14 Aug 2024 06:09:32 GMT
ARG AEROSPIKE_SHA_AARCH64=0761c2b8a9cc84988aef5e988fc1eede1b62a56e9eac90d96dbc91dd35884c1b
# Wed, 14 Aug 2024 06:09:32 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Wed, 14 Aug 2024 06:09:32 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.5/aerospike-server-community_7.1.0.5_tools-11.0.2_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=fdd8f48724872f024a787ececb1f8e21f15de74c82082bba840cf69f5ec2730c AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.5/aerospike-server-community_7.1.0.5_tools-11.0.2_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=0761c2b8a9cc84988aef5e988fc1eede1b62a56e9eac90d96dbc91dd35884c1b
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Wed, 14 Aug 2024 06:09:32 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Wed, 14 Aug 2024 06:09:32 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Wed, 14 Aug 2024 06:09:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 14 Aug 2024 06:09:32 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 14 Aug 2024 06:09:32 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb341f9c8fd98ee3205c7168cdef643598f2dcc94aef4e23ebe1bccf16ed37f5`  
		Last Modified: Sat, 17 Aug 2024 01:59:02 GMT  
		Size: 47.8 MB (47829779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e59d8f09d1d99d1a38e7d0cd621d9f1c174795fb6156e34a92751f99c533a0`  
		Last Modified: Sat, 17 Aug 2024 01:59:02 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ddfa437b06dba0853b7285493127f5ff6259d8e20e3ea033c18445060ff70ff`  
		Last Modified: Sat, 17 Aug 2024 01:59:02 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-7.1.0.5_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:52e904627580c39ee0a3bf829cd11e6374fbfe571464fadc4a7c86dc03ed3cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1905582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ed674e98237157a842f9eedc0ad531ab5ba567e54d1787c732303b09777664`

```dockerfile
```

-	Layers:
	-	`sha256:1f30a28daf2319babb4fd126314e1bf4c2e52985ee6046ce2e6e5379b83a520e`  
		Last Modified: Sat, 17 Aug 2024 01:59:02 GMT  
		Size: 1.9 MB (1876690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca861b00ffd01c6c997e455eb795cde38a4bf2ce7632a7cb7e2514f7128f08e7`  
		Last Modified: Sat, 17 Aug 2024 01:59:02 GMT  
		Size: 28.9 KB (28892 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-7.1.0.5_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:b7c53cccfce67c6d59746806a856fd183ec389857fa0e22a000602f6870a786f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74592369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289b48561ba080dcc52e66602719bdf7b492892a2eeb5de3433127a5169eb199`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Wed, 14 Aug 2024 06:09:32 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.5 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Wed, 14 Aug 2024 06:09:32 GMT
ARG AEROSPIKE_EDITION=community
# Wed, 14 Aug 2024 06:09:32 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.5/aerospike-server-community_7.1.0.5_tools-11.0.2_ubuntu22.04_x86_64.tgz
# Wed, 14 Aug 2024 06:09:32 GMT
ARG AEROSPIKE_SHA_X86_64=fdd8f48724872f024a787ececb1f8e21f15de74c82082bba840cf69f5ec2730c
# Wed, 14 Aug 2024 06:09:32 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.5/aerospike-server-community_7.1.0.5_tools-11.0.2_ubuntu22.04_aarch64.tgz
# Wed, 14 Aug 2024 06:09:32 GMT
ARG AEROSPIKE_SHA_AARCH64=0761c2b8a9cc84988aef5e988fc1eede1b62a56e9eac90d96dbc91dd35884c1b
# Wed, 14 Aug 2024 06:09:32 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Wed, 14 Aug 2024 06:09:32 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.5/aerospike-server-community_7.1.0.5_tools-11.0.2_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=fdd8f48724872f024a787ececb1f8e21f15de74c82082bba840cf69f5ec2730c AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.5/aerospike-server-community_7.1.0.5_tools-11.0.2_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=0761c2b8a9cc84988aef5e988fc1eede1b62a56e9eac90d96dbc91dd35884c1b
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Wed, 14 Aug 2024 06:09:32 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Wed, 14 Aug 2024 06:09:32 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Wed, 14 Aug 2024 06:09:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 14 Aug 2024 06:09:32 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 14 Aug 2024 06:09:32 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73549a46d7784e54f116c908819d3b525553d5a37114c74fe365aeb0da3d0776`  
		Last Modified: Sat, 17 Aug 2024 02:14:30 GMT  
		Size: 47.2 MB (47231397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdeae78bb9d5a8bcb05b3cde45b5aadb640f3b4f0df5c26450aea55de9f86600`  
		Last Modified: Sat, 17 Aug 2024 02:14:28 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92f5acc9046e50c554aa125aa3c84ad7a3f206d42a7b1ae7845756beafa80ea`  
		Last Modified: Sat, 17 Aug 2024 02:14:28 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-7.1.0.5_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:f7838e0d6a4b439e55353501f2ec0d4c26a24836d54fcba8f404882e1a771dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1907218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a5ebfc089df76ad3e27829f2f20fa28a541638565aaa01c127f9332b397e00`

```dockerfile
```

-	Layers:
	-	`sha256:f7b0e6461f7804367bda4f9e4e947e0bcedafd7ae26d48f28dbe1c6e06020266`  
		Last Modified: Sat, 17 Aug 2024 02:14:29 GMT  
		Size: 1.9 MB (1878049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a476b4426ae5590e296742cb5a8fa6c8cdc3095befe37229996c2b2862cf7d61`  
		Last Modified: Sat, 17 Aug 2024 02:14:28 GMT  
		Size: 29.2 KB (29169 bytes)  
		MIME: application/vnd.in-toto+json
