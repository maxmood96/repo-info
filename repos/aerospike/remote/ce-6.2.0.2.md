## `aerospike:ce-6.2.0.2`

```console
$ docker pull aerospike@sha256:8e4dd29b5235a308be07ecbaf157342441c9cc90d79a05b33af01c9f2fecbc13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `aerospike:ce-6.2.0.2` - linux; amd64

```console
$ docker pull aerospike@sha256:728f0d721b7f2012b533c77bba9ab244e15c9f0b5d9c94c80e4c93f0a0e7ac4f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76152904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad7d6204df277bf5977ea346dcb2d50ebee307e4bdcebcf3c8210499cd3835e`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 07:15:09 GMT
ARG DEBUG=false
# Sat, 04 Feb 2023 07:15:38 GMT
ARG AEROSPIKE_EDITION=community
# Sat, 04 Feb 2023 07:15:38 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/6.2.0.2/aerospike-server-community_6.2.0.2_tools-8.0.4_debian11_x86_64.tgz
# Sat, 04 Feb 2023 07:15:38 GMT
ARG AEROSPIKE_SHA_X86_64=27a5bdbe844212dff4e319961b9b1387ff16360e9d5544a9de6e1d0e64dbbe78
# Sat, 04 Feb 2023 07:15:38 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/6.2.0.2/aerospike-server-community_6.2.0.2_tools-8.0.4_debian11_aarch64.tgz
# Sat, 04 Feb 2023 07:15:38 GMT
ARG AEROSPIKE_SHA_AARCH64=bdd69acce22e9019e3c662d45f17e787f8570c80fc5dbecc0f8682cb511cb467
# Sat, 04 Feb 2023 07:15:38 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Sat, 04 Feb 2023 07:15:59 GMT
# ARGS: AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/6.2.0.2/aerospike-server-community_6.2.0.2_tools-8.0.4_debian11_aarch64.tgz AEROSPIKE_EDITION=community AEROSPIKE_SHA_AARCH64=bdd69acce22e9019e3c662d45f17e787f8570c80fc5dbecc0f8682cb511cb467 AEROSPIKE_SHA_X86_64=27a5bdbe844212dff4e319961b9b1387ff16360e9d5544a9de6e1d0e64dbbe78 AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/6.2.0.2/aerospike-server-community_6.2.0.2_tools-8.0.4_debian11_x86_64.tgz DEBUG=false
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+([.][0-9]+){2,3}/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/')";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     pushd aerospike/pkg || exit 1;     ar -x ../aerospike-tools*.deb;     popd || exit 1;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done";
# Sat, 04 Feb 2023 07:16:00 GMT
COPY file:c76954551192450f2d9e2a428b0b3a3daeba46fccf29d07ceabb675e275a068e in /etc/aerospike/aerospike.template.conf 
# Sat, 04 Feb 2023 07:16:00 GMT
EXPOSE 3000 3001 3002
# Sat, 04 Feb 2023 07:16:00 GMT
COPY file:d50c4b59c6030f47e41221b7d152a3e0cf299b7e8bf38ea42e3c2e33b1c9cc1f in /entrypoint.sh 
# Sat, 04 Feb 2023 07:16:00 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Sat, 04 Feb 2023 07:16:00 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50fa42afa52b4e3061418010aa409c24720b75a2d793f8f300ce3ed735096c1a`  
		Last Modified: Sat, 04 Feb 2023 07:16:30 GMT  
		Size: 44.8 MB (44753794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ca7eb0567b5f07c64dbf2b9399d57ed339c238f32c36b8d5ce23b16452ad96`  
		Last Modified: Sat, 04 Feb 2023 07:16:24 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3731e7316e32c3481b6a946196d76a0412979936b25a6c00dc9244966d4ad67`  
		Last Modified: Sat, 04 Feb 2023 07:16:24 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `aerospike:ce-6.2.0.2` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:a1eb5ed783ed20f8d81cbbe546fd7923939ce405c2f66c378879b2882db59939
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73509117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1763ef2a7faba9ce774ff1600ae6fc4903fa46fecbbf38dc9d6f8ed39473c37`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 06:41:50 GMT
ARG DEBUG=false
# Sat, 04 Feb 2023 06:42:18 GMT
ARG AEROSPIKE_EDITION=community
# Sat, 04 Feb 2023 06:42:18 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/6.2.0.2/aerospike-server-community_6.2.0.2_tools-8.0.4_debian11_x86_64.tgz
# Sat, 04 Feb 2023 06:42:18 GMT
ARG AEROSPIKE_SHA_X86_64=27a5bdbe844212dff4e319961b9b1387ff16360e9d5544a9de6e1d0e64dbbe78
# Sat, 04 Feb 2023 06:42:18 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/6.2.0.2/aerospike-server-community_6.2.0.2_tools-8.0.4_debian11_aarch64.tgz
# Sat, 04 Feb 2023 06:42:18 GMT
ARG AEROSPIKE_SHA_AARCH64=bdd69acce22e9019e3c662d45f17e787f8570c80fc5dbecc0f8682cb511cb467
# Sat, 04 Feb 2023 06:42:18 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Sat, 04 Feb 2023 06:42:36 GMT
# ARGS: AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/6.2.0.2/aerospike-server-community_6.2.0.2_tools-8.0.4_debian11_aarch64.tgz AEROSPIKE_EDITION=community AEROSPIKE_SHA_AARCH64=bdd69acce22e9019e3c662d45f17e787f8570c80fc5dbecc0f8682cb511cb467 AEROSPIKE_SHA_X86_64=27a5bdbe844212dff4e319961b9b1387ff16360e9d5544a9de6e1d0e64dbbe78 AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/6.2.0.2/aerospike-server-community_6.2.0.2_tools-8.0.4_debian11_x86_64.tgz DEBUG=false
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+([.][0-9]+){2,3}/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/')";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     pushd aerospike/pkg || exit 1;     ar -x ../aerospike-tools*.deb;     popd || exit 1;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done";
# Sat, 04 Feb 2023 06:42:37 GMT
COPY file:c76954551192450f2d9e2a428b0b3a3daeba46fccf29d07ceabb675e275a068e in /etc/aerospike/aerospike.template.conf 
# Sat, 04 Feb 2023 06:42:37 GMT
EXPOSE 3000 3001 3002
# Sat, 04 Feb 2023 06:42:37 GMT
COPY file:d50c4b59c6030f47e41221b7d152a3e0cf299b7e8bf38ea42e3c2e33b1c9cc1f in /entrypoint.sh 
# Sat, 04 Feb 2023 06:42:37 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Sat, 04 Feb 2023 06:42:37 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3dcf09999123e08e25d234a419602b454c9b6f0e624e0e2939aad72eeed4ec1`  
		Last Modified: Sat, 04 Feb 2023 06:43:04 GMT  
		Size: 43.5 MB (43462134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aac4426a300a14b6308305ba1fd005858f51cdbe2873c077ce733652d71791f`  
		Last Modified: Sat, 04 Feb 2023 06:42:59 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4deac992af6e4e275e5e41f20897b424b1576af677dec61e4d0cbc69fe2e11`  
		Last Modified: Sat, 04 Feb 2023 06:42:59 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
