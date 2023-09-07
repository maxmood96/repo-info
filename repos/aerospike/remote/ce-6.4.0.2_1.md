## `aerospike:ce-6.4.0.2_1`

```console
$ docker pull aerospike@sha256:3b0f033b2dd01c54e1b231a986d6b5a24e694b97670ed325166962b68fa5c7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `aerospike:ce-6.4.0.2_1` - linux; amd64

```console
$ docker pull aerospike@sha256:650cc2b821dc1290a027fef0156a93dd893d6f6826a5c28f3d2f93011c36cefa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79243146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade14a526aae9b4197a844d8c07ce9fb8ce4fff6fb0357e45b998a13812cf768`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Thu, 07 Sep 2023 00:20:51 GMT
ADD file:3a8cd4de7f163d93718670f4db1de49045f5e04af3a8aa27d81c0f14647db707 in / 
# Thu, 07 Sep 2023 00:20:51 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:46:26 GMT
ARG AEROSPIKE_EDITION=community
# Thu, 07 Sep 2023 02:46:26 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/6.4.0.2/aerospike-server-community_6.4.0.2_tools-9.0.0_debian12_x86_64.tgz
# Thu, 07 Sep 2023 02:46:26 GMT
ARG AEROSPIKE_SHA_X86_64=a5191f679100e5517e233851fd89da4f3420414938bb5c5d7dda4eebcca5363b
# Thu, 07 Sep 2023 02:46:26 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/6.4.0.2/aerospike-server-community_6.4.0.2_tools-9.0.0_debian12_aarch64.tgz
# Thu, 07 Sep 2023 02:46:26 GMT
ARG AEROSPIKE_SHA_AARCH64=eaa1d7832140b97c5ead800b308f2c631d0f0b1bb05a0f2108b4b5efca8b3e32
# Thu, 07 Sep 2023 02:46:26 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 07 Sep 2023 02:46:45 GMT
# ARGS: AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/6.4.0.2/aerospike-server-community_6.4.0.2_tools-9.0.0_debian12_aarch64.tgz AEROSPIKE_EDITION=community AEROSPIKE_SHA_AARCH64=eaa1d7832140b97c5ead800b308f2c631d0f0b1bb05a0f2108b4b5efca8b3e32 AEROSPIKE_SHA_X86_64=a5191f679100e5517e233851fd89da4f3420414938bb5c5d7dda4eebcca5363b AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/6.4.0.2/aerospike-server-community_6.4.0.2_tools-9.0.0_debian12_x86_64.tgz
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)*/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/')";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     pushd aerospike/pkg || exit 1;     ar -x ../aerospike-tools*.deb;     popd || exit 1;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done";
# Thu, 07 Sep 2023 02:46:46 GMT
COPY file:c76954551192450f2d9e2a428b0b3a3daeba46fccf29d07ceabb675e275a068e in /etc/aerospike/aerospike.template.conf 
# Thu, 07 Sep 2023 02:46:46 GMT
EXPOSE 3000 3001 3002
# Thu, 07 Sep 2023 02:46:46 GMT
COPY file:57ed4c0390f91371a6d5ddbdf0ecf475b40dc8871b369f3100b157df0d753fc5 in /entrypoint.sh 
# Thu, 07 Sep 2023 02:46:46 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 07 Sep 2023 02:46:46 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:360eba32fa65016e0d558c6af176db31a202e9a6071666f9b629cb8ba6ccedf0`  
		Last Modified: Thu, 07 Sep 2023 00:25:22 GMT  
		Size: 29.1 MB (29124494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304cc4ad9193429a462bd60b2a24773c7527c4f63a7f3d1b25b2fcacda25e6c1`  
		Last Modified: Thu, 07 Sep 2023 02:47:18 GMT  
		Size: 50.1 MB (50116462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f295aac887819ebf6f1ff9bfe77c595603bd4b6a1ef8c459ce81fb74b7b998`  
		Last Modified: Thu, 07 Sep 2023 02:47:12 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75f04bb0d3e9551f2a3d5b687be61a21dd8b7a4997e23a90350ffc73acd64ca`  
		Last Modified: Thu, 07 Sep 2023 02:47:12 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `aerospike:ce-6.4.0.2_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:10317477086375dc5c6fa8414455bcd3c73e6faa1970dd708f198fbb686092ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78507754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a63a57ba021c9882187e9a727932f619f1c33b563a2b01919934b3f81b6732e`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:57 GMT
ADD file:bc58956fa3d1aff2efb0264655d039fedfff28dc4ff19a65a235e82754ee1cfa in / 
# Tue, 15 Aug 2023 23:39:57 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:20:29 GMT
ARG AEROSPIKE_EDITION=community
# Thu, 31 Aug 2023 20:39:37 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/6.4.0.2/aerospike-server-community_6.4.0.2_tools-9.0.0_debian12_x86_64.tgz
# Thu, 31 Aug 2023 20:39:37 GMT
ARG AEROSPIKE_SHA_X86_64=a5191f679100e5517e233851fd89da4f3420414938bb5c5d7dda4eebcca5363b
# Thu, 31 Aug 2023 20:39:37 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/6.4.0.2/aerospike-server-community_6.4.0.2_tools-9.0.0_debian12_aarch64.tgz
# Thu, 31 Aug 2023 20:39:37 GMT
ARG AEROSPIKE_SHA_AARCH64=eaa1d7832140b97c5ead800b308f2c631d0f0b1bb05a0f2108b4b5efca8b3e32
# Thu, 31 Aug 2023 20:39:37 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 31 Aug 2023 20:39:52 GMT
# ARGS: AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/6.4.0.2/aerospike-server-community_6.4.0.2_tools-9.0.0_debian12_aarch64.tgz AEROSPIKE_EDITION=community AEROSPIKE_SHA_AARCH64=eaa1d7832140b97c5ead800b308f2c631d0f0b1bb05a0f2108b4b5efca8b3e32 AEROSPIKE_SHA_X86_64=a5191f679100e5517e233851fd89da4f3420414938bb5c5d7dda4eebcca5363b AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/6.4.0.2/aerospike-server-community_6.4.0.2_tools-9.0.0_debian12_x86_64.tgz
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)*/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/')";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     pushd aerospike/pkg || exit 1;     ar -x ../aerospike-tools*.deb;     popd || exit 1;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done";
# Thu, 31 Aug 2023 20:39:53 GMT
COPY file:c76954551192450f2d9e2a428b0b3a3daeba46fccf29d07ceabb675e275a068e in /etc/aerospike/aerospike.template.conf 
# Thu, 31 Aug 2023 20:39:53 GMT
EXPOSE 3000 3001 3002
# Thu, 31 Aug 2023 20:39:53 GMT
COPY file:57ed4c0390f91371a6d5ddbdf0ecf475b40dc8871b369f3100b157df0d753fc5 in /entrypoint.sh 
# Thu, 31 Aug 2023 20:39:53 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 31 Aug 2023 20:39:53 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:4ee097f9a36616fddb52e45aba72142c4bc6f2e594f0a746e406acfde4f02f51`  
		Last Modified: Tue, 15 Aug 2023 23:43:21 GMT  
		Size: 29.2 MB (29157256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d71fb20bcb00d78559f8f729487600c1b675a6f2bec45ce43400adeccc8fe3`  
		Last Modified: Thu, 31 Aug 2023 20:40:28 GMT  
		Size: 49.3 MB (49348312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe9cfaf7f50254f49fb24b6efe24b2e722c16cd5c5e42d9c388015a88cb0f81`  
		Last Modified: Thu, 31 Aug 2023 20:40:18 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fee9259dc333597110fad6461f645ca4f585af9652222cbff3022cb939878b`  
		Last Modified: Thu, 31 Aug 2023 20:40:18 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
