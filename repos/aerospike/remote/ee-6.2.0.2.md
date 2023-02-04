## `aerospike:ee-6.2.0.2`

```console
$ docker pull aerospike@sha256:e0ee3debe01cc2f411e03356d9880959cf0f3612f283c07e642468a892e067f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `aerospike:ee-6.2.0.2` - linux; amd64

```console
$ docker pull aerospike@sha256:d28059668284a0640bff3bb8a8a2d3622b6422502a5d6f0103428daab74c8cea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79160298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c96ac5c3a31f6e8a8913e8a108a13389c4d297d737b4fea2fb7c15ddf6afdaf0`
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
# Sat, 04 Feb 2023 07:15:09 GMT
ARG AEROSPIKE_EDITION=enterprise
# Sat, 04 Feb 2023 07:15:09 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/6.2.0.2/aerospike-server-enterprise_6.2.0.2_tools-8.0.4_debian11_x86_64.tgz
# Sat, 04 Feb 2023 07:15:09 GMT
ARG AEROSPIKE_SHA_X86_64=0eeb32a9b5da70dcc9f9e155e57ec0d8dfcc17c471ba6e844b2d7449cf577c34
# Sat, 04 Feb 2023 07:15:10 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/6.2.0.2/aerospike-server-enterprise_6.2.0.2_tools-8.0.4_debian11_aarch64.tgz
# Sat, 04 Feb 2023 07:15:10 GMT
ARG AEROSPIKE_SHA_AARCH64=2d250ca285a7c5b30b9534888a462ce742b0d812f4f97b954a554884e8ede122
# Sat, 04 Feb 2023 07:15:10 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Sat, 04 Feb 2023 07:15:33 GMT
# ARGS: AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/6.2.0.2/aerospike-server-enterprise_6.2.0.2_tools-8.0.4_debian11_aarch64.tgz AEROSPIKE_EDITION=enterprise AEROSPIKE_SHA_AARCH64=2d250ca285a7c5b30b9534888a462ce742b0d812f4f97b954a554884e8ede122 AEROSPIKE_SHA_X86_64=0eeb32a9b5da70dcc9f9e155e57ec0d8dfcc17c471ba6e844b2d7449cf577c34 AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/6.2.0.2/aerospike-server-enterprise_6.2.0.2_tools-8.0.4_debian11_x86_64.tgz DEBUG=false
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+([.][0-9]+){2,3}/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/')";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     pushd aerospike/pkg || exit 1;     ar -x ../aerospike-tools*.deb;     popd || exit 1;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done";
# Sat, 04 Feb 2023 07:15:33 GMT
COPY file:c76954551192450f2d9e2a428b0b3a3daeba46fccf29d07ceabb675e275a068e in /etc/aerospike/aerospike.template.conf 
# Sat, 04 Feb 2023 07:15:33 GMT
EXPOSE 3000 3001 3002
# Sat, 04 Feb 2023 07:15:33 GMT
COPY file:d50c4b59c6030f47e41221b7d152a3e0cf299b7e8bf38ea42e3c2e33b1c9cc1f in /entrypoint.sh 
# Sat, 04 Feb 2023 07:15:34 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Sat, 04 Feb 2023 07:15:34 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3372dca7f0bc726c320966fa88c91bd63a409dba6cae8a9dd8a6f13a9a80380f`  
		Last Modified: Sat, 04 Feb 2023 07:16:18 GMT  
		Size: 47.8 MB (47761194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:967e1d4e5b57e415d077ed761aec8ae7aeb1a63ebc838e258d731710af7fc93d`  
		Last Modified: Sat, 04 Feb 2023 07:16:11 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca0edadcfd0d7fb8c3edc6c683ed3298ea4a25963cf80c28d55413f4871036d`  
		Last Modified: Sat, 04 Feb 2023 07:16:11 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `aerospike:ee-6.2.0.2` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:4284820d07143d0b77eb37c48e601643c8d0e39cc1aef681de36aa4999c32333
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76523934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb5489f523a242b922e43191e27edb4575303cb871c20d3baf1e6d0c24c9f0a`
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
# Sat, 04 Feb 2023 06:41:50 GMT
ARG AEROSPIKE_EDITION=enterprise
# Sat, 04 Feb 2023 06:41:50 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/6.2.0.2/aerospike-server-enterprise_6.2.0.2_tools-8.0.4_debian11_x86_64.tgz
# Sat, 04 Feb 2023 06:41:50 GMT
ARG AEROSPIKE_SHA_X86_64=0eeb32a9b5da70dcc9f9e155e57ec0d8dfcc17c471ba6e844b2d7449cf577c34
# Sat, 04 Feb 2023 06:41:50 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/6.2.0.2/aerospike-server-enterprise_6.2.0.2_tools-8.0.4_debian11_aarch64.tgz
# Sat, 04 Feb 2023 06:41:50 GMT
ARG AEROSPIKE_SHA_AARCH64=2d250ca285a7c5b30b9534888a462ce742b0d812f4f97b954a554884e8ede122
# Sat, 04 Feb 2023 06:41:50 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Sat, 04 Feb 2023 06:42:11 GMT
# ARGS: AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/6.2.0.2/aerospike-server-enterprise_6.2.0.2_tools-8.0.4_debian11_aarch64.tgz AEROSPIKE_EDITION=enterprise AEROSPIKE_SHA_AARCH64=2d250ca285a7c5b30b9534888a462ce742b0d812f4f97b954a554884e8ede122 AEROSPIKE_SHA_X86_64=0eeb32a9b5da70dcc9f9e155e57ec0d8dfcc17c471ba6e844b2d7449cf577c34 AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/6.2.0.2/aerospike-server-enterprise_6.2.0.2_tools-8.0.4_debian11_x86_64.tgz DEBUG=false
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+([.][0-9]+){2,3}/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/')";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     pushd aerospike/pkg || exit 1;     ar -x ../aerospike-tools*.deb;     popd || exit 1;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done";
# Sat, 04 Feb 2023 06:42:11 GMT
COPY file:c76954551192450f2d9e2a428b0b3a3daeba46fccf29d07ceabb675e275a068e in /etc/aerospike/aerospike.template.conf 
# Sat, 04 Feb 2023 06:42:11 GMT
EXPOSE 3000 3001 3002
# Sat, 04 Feb 2023 06:42:12 GMT
COPY file:d50c4b59c6030f47e41221b7d152a3e0cf299b7e8bf38ea42e3c2e33b1c9cc1f in /entrypoint.sh 
# Sat, 04 Feb 2023 06:42:12 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Sat, 04 Feb 2023 06:42:12 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287d565aecaaff55e9f365d50001e9f326b9bcc927b576947a9a7a0375a1ec14`  
		Last Modified: Sat, 04 Feb 2023 06:42:53 GMT  
		Size: 46.5 MB (46476952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb0b61ff7ce0132e1a70cc16121f2e2723db0e1177cf4783113a1b0887ac5ff`  
		Last Modified: Sat, 04 Feb 2023 06:42:47 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ab00ef483359b9b9c63bd79a53bfd50a08414d323578c2da23e0a6072f5256`  
		Last Modified: Sat, 04 Feb 2023 06:42:47 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
