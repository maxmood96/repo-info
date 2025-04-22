## `aerospike:ce-8.0.0.6`

```console
$ docker pull aerospike@sha256:6748cf0d97afc2134e9e33d7bfc8fbe52cffb29b9a3a9599554942dc925138e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.0.0.6` - linux; amd64

```console
$ docker pull aerospike@sha256:c3be517de035fb7495207b66443285dcd96257c1ae8402a3c822a8677b7f1c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81063724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817b295b17b0de30f4dad0abca65c46a60e62ff1c573258b5d55422833b5dcc7`
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
# Sat, 19 Apr 2025 09:34:41 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.6 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Sat, 19 Apr 2025 09:34:41 GMT
ARG AEROSPIKE_EDITION=community
# Sat, 19 Apr 2025 09:34:41 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.6/aerospike-server-community_8.0.0.6_tools-11.2.2_ubuntu24.04_x86_64.tgz
# Sat, 19 Apr 2025 09:34:41 GMT
ARG AEROSPIKE_SHA_X86_64=efe60dde195d7865ffae749243c81b8f2ba7c6362ca6653ec3ffab51c40ae1f2
# Sat, 19 Apr 2025 09:34:41 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.6/aerospike-server-community_8.0.0.6_tools-11.2.2_ubuntu24.04_aarch64.tgz
# Sat, 19 Apr 2025 09:34:41 GMT
ARG AEROSPIKE_SHA_AARCH64=10dbc7988cbcc7d78d4d74ecc6919c6de73619826e4eeaacfbe2620c724df33f
# Sat, 19 Apr 2025 09:34:41 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Sat, 19 Apr 2025 09:34:41 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.6/aerospike-server-community_8.0.0.6_tools-11.2.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=efe60dde195d7865ffae749243c81b8f2ba7c6362ca6653ec3ffab51c40ae1f2 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.6/aerospike-server-community_8.0.0.6_tools-11.2.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=10dbc7988cbcc7d78d4d74ecc6919c6de73619826e4eeaacfbe2620c724df33f
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Sat, 19 Apr 2025 09:34:41 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Sat, 19 Apr 2025 09:34:41 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Sat, 19 Apr 2025 09:34:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 19 Apr 2025 09:34:41 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Sat, 19 Apr 2025 09:34:41 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d900ba63c9b99378ceff40235bc0f76490b194ceb11fe423ffad5817b4ac732`  
		Last Modified: Mon, 21 Apr 2025 22:34:08 GMT  
		Size: 51.3 MB (51343768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa41a4bc99b2b72b9b00b011f1c91d1279ab8269ac1b02c6e5bc7c938536bd3`  
		Last Modified: Mon, 21 Apr 2025 22:34:07 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8537aaf5725c04c90887e6dec76039726a537bdf7b89c22c8060468c18276352`  
		Last Modified: Mon, 21 Apr 2025 22:34:07 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.0.0.6` - unknown; unknown

```console
$ docker pull aerospike@sha256:8b27a6dcd04eb4f59f414ad237f7cb9cb7d0eb015867af1047f6daac148690c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1893175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ad43420934f23b2f839a9b36b4f3f6787e7db638aa9b15d93f66a7efcd984d`

```dockerfile
```

-	Layers:
	-	`sha256:221a36c5698c651c77095ca87c04c8d7b0245d636c3ce2f99cd30e207f32563e`  
		Last Modified: Mon, 21 Apr 2025 22:34:07 GMT  
		Size: 1.9 MB (1864028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a8618ff63fe0506715fc9317346980a857d5d8407fb5bc7cc2487dd71a25117`  
		Last Modified: Mon, 21 Apr 2025 22:34:07 GMT  
		Size: 29.1 KB (29147 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.0.0.6` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:004ef25f11692bfc7f8a78cfb2f9c8a5c77d640337965bee38e400e7fbf72d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79615726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0324908bfe0dac70505700a47fbbc53306814d90e05c097ba8b9710a83844681`
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
# Sat, 19 Apr 2025 09:34:41 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.6 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Sat, 19 Apr 2025 09:34:41 GMT
ARG AEROSPIKE_EDITION=community
# Sat, 19 Apr 2025 09:34:41 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.6/aerospike-server-community_8.0.0.6_tools-11.2.2_ubuntu24.04_x86_64.tgz
# Sat, 19 Apr 2025 09:34:41 GMT
ARG AEROSPIKE_SHA_X86_64=efe60dde195d7865ffae749243c81b8f2ba7c6362ca6653ec3ffab51c40ae1f2
# Sat, 19 Apr 2025 09:34:41 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.6/aerospike-server-community_8.0.0.6_tools-11.2.2_ubuntu24.04_aarch64.tgz
# Sat, 19 Apr 2025 09:34:41 GMT
ARG AEROSPIKE_SHA_AARCH64=10dbc7988cbcc7d78d4d74ecc6919c6de73619826e4eeaacfbe2620c724df33f
# Sat, 19 Apr 2025 09:34:41 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Sat, 19 Apr 2025 09:34:41 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.6/aerospike-server-community_8.0.0.6_tools-11.2.2_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=efe60dde195d7865ffae749243c81b8f2ba7c6362ca6653ec3ffab51c40ae1f2 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.6/aerospike-server-community_8.0.0.6_tools-11.2.2_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=10dbc7988cbcc7d78d4d74ecc6919c6de73619826e4eeaacfbe2620c724df33f
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Sat, 19 Apr 2025 09:34:41 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Sat, 19 Apr 2025 09:34:41 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Sat, 19 Apr 2025 09:34:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 19 Apr 2025 09:34:41 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Sat, 19 Apr 2025 09:34:41 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a668baef76a06ef2b7fc89377131ad102160c1f40947cd7f073124ff5a1978`  
		Last Modified: Mon, 21 Apr 2025 22:49:36 GMT  
		Size: 50.8 MB (50766469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139ae3d94f3b7df9c6c49e3a1726b9686cd6ef54a4216d2b73b831b5e4d7fa23`  
		Last Modified: Mon, 21 Apr 2025 22:49:34 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5d8e6c16b74814bd1339f1c3a9cf0486f6a26b85ee8e542aa4fc9d22596000`  
		Last Modified: Mon, 21 Apr 2025 22:49:34 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.0.0.6` - unknown; unknown

```console
$ docker pull aerospike@sha256:dc370c5845bc85547665f9e42ef1e1f255279d658a30f90b2fb0b090cead9c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1895517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d73de4e6d3b819d77eec2263fdb93e7bfa43c4f0f9374db9996179bac872f31`

```dockerfile
```

-	Layers:
	-	`sha256:5698869cc7d4a05162fee23b64b9affb77d58f7be062e1e565084b46e2adedb3`  
		Last Modified: Mon, 21 Apr 2025 22:49:35 GMT  
		Size: 1.9 MB (1866290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcb63248a648cc4c2911c895665ddee702b66b7190eda84467db7ff159f0a856`  
		Last Modified: Mon, 21 Apr 2025 22:49:34 GMT  
		Size: 29.2 KB (29227 bytes)  
		MIME: application/vnd.in-toto+json
