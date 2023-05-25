## `aerospike:ce-6.3.0.4`

```console
$ docker pull aerospike@sha256:08b3f5cd6122a9b727f830d697b9a87c36f1e24f708c49811b822c97537702c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `aerospike:ce-6.3.0.4` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:966f90b0326556623a8fe6ea857baac4bf91cc85b21110d33cee8e519c47d84d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76342168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2507d6680b85a440daa8379ec0ac551273a5238fae8d8b6bde2f5a081993ea54`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:23:08 GMT
ARG AEROSPIKE_EDITION=community
# Thu, 25 May 2023 22:40:47 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/6.3.0.4/aerospike-server-community_6.3.0.4_tools-8.3.0_debian11_x86_64.tgz
# Thu, 25 May 2023 22:40:47 GMT
ARG AEROSPIKE_SHA_X86_64=22725b99f150bdaeaa9af944f9cbba6810d470156f3665ef427d10d0098f08f0
# Thu, 25 May 2023 22:40:47 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/6.3.0.4/aerospike-server-community_6.3.0.4_tools-8.3.0_debian11_aarch64.tgz
# Thu, 25 May 2023 22:40:47 GMT
ARG AEROSPIKE_SHA_AARCH64=93dff36ecd4420e66d624bb597bcc5d23025bad7b24e67a03c69ae1dc5c45162
# Thu, 25 May 2023 22:40:47 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 25 May 2023 22:41:02 GMT
# ARGS: AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/6.3.0.4/aerospike-server-community_6.3.0.4_tools-8.3.0_debian11_aarch64.tgz AEROSPIKE_EDITION=community AEROSPIKE_SHA_AARCH64=93dff36ecd4420e66d624bb597bcc5d23025bad7b24e67a03c69ae1dc5c45162 AEROSPIKE_SHA_X86_64=22725b99f150bdaeaa9af944f9cbba6810d470156f3665ef427d10d0098f08f0 AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/6.3.0.4/aerospike-server-community_6.3.0.4_tools-8.3.0_debian11_x86_64.tgz
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)*/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/')";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     pushd aerospike/pkg || exit 1;     ar -x ../aerospike-tools*.deb;     popd || exit 1;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done";
# Thu, 25 May 2023 22:41:02 GMT
COPY file:c76954551192450f2d9e2a428b0b3a3daeba46fccf29d07ceabb675e275a068e in /etc/aerospike/aerospike.template.conf 
# Thu, 25 May 2023 22:41:02 GMT
EXPOSE 3000 3001 3002
# Thu, 25 May 2023 22:41:02 GMT
COPY file:57ed4c0390f91371a6d5ddbdf0ecf475b40dc8871b369f3100b157df0d753fc5 in /entrypoint.sh 
# Thu, 25 May 2023 22:41:02 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 25 May 2023 22:41:03 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709e102d962998cfa1dbde00fa13d7a6e6d6b56b337571db6ac6351e54b2244a`  
		Last Modified: Thu, 25 May 2023 22:41:35 GMT  
		Size: 46.3 MB (46287231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0491f1f24bb4f2e6521b61dd98276012e8b982bb51e6dcb2bbf051a4ba8602e`  
		Last Modified: Thu, 25 May 2023 22:41:29 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14036b22ea583d8ddc7565a084cb95c7d407e8419455f26ffb9c953a8e8cacf8`  
		Last Modified: Thu, 25 May 2023 22:41:29 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
