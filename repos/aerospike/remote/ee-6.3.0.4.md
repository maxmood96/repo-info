## `aerospike:ee-6.3.0.4`

```console
$ docker pull aerospike@sha256:7c605b5ddfb69d0d95aa64674b818a141194f0baf211b82fe002d9cd256ad854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `aerospike:ee-6.3.0.4` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:170091f8cc31e6d393ff4eacb7843b3a7144e50d48da4e2fdfc69c1de6291fdc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79379521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7822e91e44f19be8a2d88c94a0baa6fae80eb44118d4fc8bb607ac1d74a31ff4`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:22:45 GMT
ARG AEROSPIKE_EDITION=enterprise
# Thu, 25 May 2023 22:40:24 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/6.3.0.4/aerospike-server-enterprise_6.3.0.4_tools-8.3.0_debian11_x86_64.tgz
# Thu, 25 May 2023 22:40:24 GMT
ARG AEROSPIKE_SHA_X86_64=85e25980c7e4d69d06cac1d1d17472c3beb2b79d4807232b84bb3dafa9de9ec0
# Thu, 25 May 2023 22:40:24 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/6.3.0.4/aerospike-server-enterprise_6.3.0.4_tools-8.3.0_debian11_aarch64.tgz
# Thu, 25 May 2023 22:40:24 GMT
ARG AEROSPIKE_SHA_AARCH64=74ae4f799b154e6eac9f8df9be3ae8b2d2d3abb5fefc783ee6b2df8dc97080ab
# Thu, 25 May 2023 22:40:24 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 25 May 2023 22:40:43 GMT
# ARGS: AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/6.3.0.4/aerospike-server-enterprise_6.3.0.4_tools-8.3.0_debian11_aarch64.tgz AEROSPIKE_EDITION=enterprise AEROSPIKE_SHA_AARCH64=74ae4f799b154e6eac9f8df9be3ae8b2d2d3abb5fefc783ee6b2df8dc97080ab AEROSPIKE_SHA_X86_64=85e25980c7e4d69d06cac1d1d17472c3beb2b79d4807232b84bb3dafa9de9ec0 AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/6.3.0.4/aerospike-server-enterprise_6.3.0.4_tools-8.3.0_debian11_x86_64.tgz
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)*/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/')";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     pushd aerospike/pkg || exit 1;     ar -x ../aerospike-tools*.deb;     popd || exit 1;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done";
# Thu, 25 May 2023 22:40:44 GMT
COPY file:c76954551192450f2d9e2a428b0b3a3daeba46fccf29d07ceabb675e275a068e in /etc/aerospike/aerospike.template.conf 
# Thu, 25 May 2023 22:40:44 GMT
EXPOSE 3000 3001 3002
# Thu, 25 May 2023 22:40:44 GMT
COPY file:57ed4c0390f91371a6d5ddbdf0ecf475b40dc8871b369f3100b157df0d753fc5 in /entrypoint.sh 
# Thu, 25 May 2023 22:40:44 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 25 May 2023 22:40:44 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6dde83835e0ce107c45a1cf6a33198bbeb95cd467612818680f3981bce632a6`  
		Last Modified: Thu, 25 May 2023 22:41:18 GMT  
		Size: 49.3 MB (49324584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d51ea54a2b115e4a05a212874c17f1cde085c722dceadde1fa33e3be97443fb`  
		Last Modified: Thu, 25 May 2023 22:41:12 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a74d7f989fd60a14f18e4c6fcdb5aa30e480350c7665034561090dbb130784`  
		Last Modified: Thu, 25 May 2023 22:41:12 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
