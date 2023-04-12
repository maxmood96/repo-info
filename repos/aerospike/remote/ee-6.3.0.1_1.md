## `aerospike:ee-6.3.0.1_1`

```console
$ docker pull aerospike@sha256:96e37fc07e578107d13f21362958f424c6de9458eddcef0bb2c8887c37167b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `aerospike:ee-6.3.0.1_1` - linux; amd64

```console
$ docker pull aerospike@sha256:253f8a28a9b2d645d3b498bd5f15cacaf39330129ea43b0ba6f2c0fe9c7c44b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81284499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c511875d2aaaab63d926c370983ad9da5d7cf3d34864b8a5ef1a35b23522ce6f`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:47:20 GMT
ARG AEROSPIKE_EDITION=enterprise
# Wed, 12 Apr 2023 07:47:20 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/6.3.0.1/aerospike-server-enterprise_6.3.0.1_tools-8.2.0_debian11_x86_64.tgz
# Wed, 12 Apr 2023 07:47:20 GMT
ARG AEROSPIKE_SHA_X86_64=43ecd6f3e02fd231d89aec8eaff4e90488bcf72311a0fabd92dd4df7ebffaee7
# Wed, 12 Apr 2023 07:47:20 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/6.3.0.1/aerospike-server-enterprise_6.3.0.1_tools-8.2.0_debian11_aarch64.tgz
# Wed, 12 Apr 2023 07:47:20 GMT
ARG AEROSPIKE_SHA_AARCH64=5793790ee64a5f457f2c226b2f46e9ab0ecdbaea1975dbabf39ec9830d2057cb
# Wed, 12 Apr 2023 07:47:20 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Wed, 12 Apr 2023 07:47:38 GMT
# ARGS: AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/6.3.0.1/aerospike-server-enterprise_6.3.0.1_tools-8.2.0_debian11_aarch64.tgz AEROSPIKE_EDITION=enterprise AEROSPIKE_SHA_AARCH64=5793790ee64a5f457f2c226b2f46e9ab0ecdbaea1975dbabf39ec9830d2057cb AEROSPIKE_SHA_X86_64=43ecd6f3e02fd231d89aec8eaff4e90488bcf72311a0fabd92dd4df7ebffaee7 AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/6.3.0.1/aerospike-server-enterprise_6.3.0.1_tools-8.2.0_debian11_x86_64.tgz
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)*/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/')";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     pushd aerospike/pkg || exit 1;     ar -x ../aerospike-tools*.deb;     popd || exit 1;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done";
# Wed, 12 Apr 2023 07:47:38 GMT
COPY file:c76954551192450f2d9e2a428b0b3a3daeba46fccf29d07ceabb675e275a068e in /etc/aerospike/aerospike.template.conf 
# Wed, 12 Apr 2023 07:47:38 GMT
EXPOSE 3000 3001 3002
# Wed, 12 Apr 2023 07:47:38 GMT
COPY file:57ed4c0390f91371a6d5ddbdf0ecf475b40dc8871b369f3100b157df0d753fc5 in /entrypoint.sh 
# Wed, 12 Apr 2023 07:47:38 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 12 Apr 2023 07:47:38 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d3b776af565f37a8e81ff0368c30fdbe52bfd7b0fc1eae6f89e62315fafd92`  
		Last Modified: Wed, 12 Apr 2023 07:48:15 GMT  
		Size: 49.9 MB (49864083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e317a045c40c64061289255ba3c90fc7fd64ef8bd4194cd5ef7ab24345313f0f`  
		Last Modified: Wed, 12 Apr 2023 07:48:08 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25d689c58a653a595de7cc72a3ba11020f2d0d4d4d2296cd2fa37c1560732dd`  
		Last Modified: Wed, 12 Apr 2023 07:48:08 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `aerospike:ee-6.3.0.1_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:e366ba4715234329d789aa42085b48f0b8788a3d57c9f96ede42856dcb12d70d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79387945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f10e4f82431f65cc4472bde6c88497d3b7d6c6afe506bbb4b402ed5190cfd7`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:02:41 GMT
ARG AEROSPIKE_EDITION=enterprise
# Wed, 12 Apr 2023 01:02:41 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/6.3.0.1/aerospike-server-enterprise_6.3.0.1_tools-8.2.0_debian11_x86_64.tgz
# Wed, 12 Apr 2023 01:02:41 GMT
ARG AEROSPIKE_SHA_X86_64=43ecd6f3e02fd231d89aec8eaff4e90488bcf72311a0fabd92dd4df7ebffaee7
# Wed, 12 Apr 2023 01:02:41 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/6.3.0.1/aerospike-server-enterprise_6.3.0.1_tools-8.2.0_debian11_aarch64.tgz
# Wed, 12 Apr 2023 01:02:41 GMT
ARG AEROSPIKE_SHA_AARCH64=5793790ee64a5f457f2c226b2f46e9ab0ecdbaea1975dbabf39ec9830d2057cb
# Wed, 12 Apr 2023 01:02:41 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Wed, 12 Apr 2023 01:02:57 GMT
# ARGS: AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/6.3.0.1/aerospike-server-enterprise_6.3.0.1_tools-8.2.0_debian11_aarch64.tgz AEROSPIKE_EDITION=enterprise AEROSPIKE_SHA_AARCH64=5793790ee64a5f457f2c226b2f46e9ab0ecdbaea1975dbabf39ec9830d2057cb AEROSPIKE_SHA_X86_64=43ecd6f3e02fd231d89aec8eaff4e90488bcf72311a0fabd92dd4df7ebffaee7 AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/6.3.0.1/aerospike-server-enterprise_6.3.0.1_tools-8.2.0_debian11_x86_64.tgz
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)*/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/')";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     pushd aerospike/pkg || exit 1;     ar -x ../aerospike-tools*.deb;     popd || exit 1;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done";
# Wed, 12 Apr 2023 01:02:58 GMT
COPY file:c76954551192450f2d9e2a428b0b3a3daeba46fccf29d07ceabb675e275a068e in /etc/aerospike/aerospike.template.conf 
# Wed, 12 Apr 2023 01:02:58 GMT
EXPOSE 3000 3001 3002
# Wed, 12 Apr 2023 01:02:58 GMT
COPY file:57ed4c0390f91371a6d5ddbdf0ecf475b40dc8871b369f3100b157df0d753fc5 in /entrypoint.sh 
# Wed, 12 Apr 2023 01:02:58 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 12 Apr 2023 01:02:58 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9a17a6e5006ecb1acb4c525e5a677417ea83ec2798a27bc47a8ddb7d3e863d`  
		Last Modified: Wed, 12 Apr 2023 01:03:31 GMT  
		Size: 49.3 MB (49321934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31c62490bc1486cee3710a59da413f9924099e97636bbcff57f80a7f3893f85`  
		Last Modified: Wed, 12 Apr 2023 01:03:25 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cab6c174ced417c71872a83bacd6551ca3d32ddc4e14d69970d1ccb18fe679b`  
		Last Modified: Wed, 12 Apr 2023 01:03:25 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
