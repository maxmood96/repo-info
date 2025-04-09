## `aerospike:ee-8.0.0.5`

```console
$ docker pull aerospike@sha256:c40b40c5f65cab45bc83e3d0246c5f7acaf800db224ac01d08758f6060b55d29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.0.0.5` - linux; amd64

```console
$ docker pull aerospike@sha256:cc062244104f68496e7fb47a973567f1e7d01da7c59130d98687237f67ea52a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81993194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996d604ef2860f0f37c33cc75c73c972374d86774143149ac6cf2a807292304d`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 25 Feb 2025 21:03:12 GMT
ARG RELEASE
# Tue, 25 Feb 2025 21:03:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Feb 2025 21:03:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Feb 2025 21:03:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 25 Feb 2025 21:03:12 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 25 Feb 2025 21:03:12 GMT
CMD ["/bin/bash"]
# Tue, 25 Feb 2025 21:03:12 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.5 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 25 Feb 2025 21:03:12 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 25 Feb 2025 21:03:12 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.5/aerospike-server-enterprise_8.0.0.5_tools-11.2.0_ubuntu24.04_x86_64.tgz
# Tue, 25 Feb 2025 21:03:12 GMT
ARG AEROSPIKE_SHA_X86_64=534ffa934469b39ee8b91b13f6ecd221f8b38001b8483118f14cc28dffefa314
# Tue, 25 Feb 2025 21:03:12 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.5/aerospike-server-enterprise_8.0.0.5_tools-11.2.0_ubuntu24.04_aarch64.tgz
# Tue, 25 Feb 2025 21:03:12 GMT
ARG AEROSPIKE_SHA_AARCH64=57c13ac199b4206089938b9ebef3a92af4e74a0d7d0a7e4ab5e8aac6d25d529a
# Tue, 25 Feb 2025 21:03:12 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 25 Feb 2025 21:03:12 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.5/aerospike-server-enterprise_8.0.0.5_tools-11.2.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=534ffa934469b39ee8b91b13f6ecd221f8b38001b8483118f14cc28dffefa314 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.5/aerospike-server-enterprise_8.0.0.5_tools-11.2.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=57c13ac199b4206089938b9ebef3a92af4e74a0d7d0a7e4ab5e8aac6d25d529a
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 25 Feb 2025 21:03:12 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 25 Feb 2025 21:03:12 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 25 Feb 2025 21:03:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 25 Feb 2025 21:03:12 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 25 Feb 2025 21:03:12 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c153da37969196e630629a8125d1a39f416a12533072ff0db2ff282795920e`  
		Last Modified: Wed, 09 Apr 2025 01:11:43 GMT  
		Size: 52.3 MB (52273241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ade459eefe248898216da08bae7499a90e22fed7323f182e495308006e0775`  
		Last Modified: Wed, 09 Apr 2025 01:11:42 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d88a4826675825295cb618d63e1af2fb5fff8d1316b435460483b99bbd9ce5c`  
		Last Modified: Wed, 09 Apr 2025 01:11:42 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.0.0.5` - unknown; unknown

```console
$ docker pull aerospike@sha256:01671bf0b5e273d48b1fba2c67fa530845ff5fd3797f54e297f18968d764d5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1987093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67865e89091bcc7d1262e4b8806795b0545cf6ff8f9e4f8acb6cc3beba64c3d5`

```dockerfile
```

-	Layers:
	-	`sha256:98ad1cf1671763495b11bc71fdd351dda63906e654b366bd0a907e099e2ba7d9`  
		Last Modified: Wed, 09 Apr 2025 01:11:42 GMT  
		Size: 2.0 MB (1957930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0732aead4acb9cf35cb2d4b1553fb268ff16afff5d6698ac727022abecc3c73b`  
		Last Modified: Wed, 09 Apr 2025 01:11:42 GMT  
		Size: 29.2 KB (29163 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.0.0.5` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:6918bd84aea9a175677794a5e8629d0593fb590fecab4fcbf537607d729abb94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80566573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b787b5fd6b0df208e2f1860e8564c0a0a6a1e8aead8ea7be39e5f8501addc0`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 25 Feb 2025 21:03:12 GMT
ARG RELEASE
# Tue, 25 Feb 2025 21:03:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Feb 2025 21:03:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Feb 2025 21:03:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 25 Feb 2025 21:03:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 25 Feb 2025 21:03:12 GMT
CMD ["/bin/bash"]
# Tue, 25 Feb 2025 21:03:12 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.5 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 25 Feb 2025 21:03:12 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 25 Feb 2025 21:03:12 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.5/aerospike-server-enterprise_8.0.0.5_tools-11.2.0_ubuntu24.04_x86_64.tgz
# Tue, 25 Feb 2025 21:03:12 GMT
ARG AEROSPIKE_SHA_X86_64=534ffa934469b39ee8b91b13f6ecd221f8b38001b8483118f14cc28dffefa314
# Tue, 25 Feb 2025 21:03:12 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.5/aerospike-server-enterprise_8.0.0.5_tools-11.2.0_ubuntu24.04_aarch64.tgz
# Tue, 25 Feb 2025 21:03:12 GMT
ARG AEROSPIKE_SHA_AARCH64=57c13ac199b4206089938b9ebef3a92af4e74a0d7d0a7e4ab5e8aac6d25d529a
# Tue, 25 Feb 2025 21:03:12 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 25 Feb 2025 21:03:12 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.5/aerospike-server-enterprise_8.0.0.5_tools-11.2.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=534ffa934469b39ee8b91b13f6ecd221f8b38001b8483118f14cc28dffefa314 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.5/aerospike-server-enterprise_8.0.0.5_tools-11.2.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=57c13ac199b4206089938b9ebef3a92af4e74a0d7d0a7e4ab5e8aac6d25d529a
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 25 Feb 2025 21:03:12 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 25 Feb 2025 21:03:12 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 25 Feb 2025 21:03:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 25 Feb 2025 21:03:12 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 25 Feb 2025 21:03:12 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21243cb63e383562fe9162057070457241a72f5cfa16c0c83b0aa0263c9ca0c0`  
		Last Modified: Wed, 09 Apr 2025 06:06:44 GMT  
		Size: 51.7 MB (51717314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae4e612904a50b4dea1891114168bb4ed5f004124fb039ba4c203bd43ac0fa5`  
		Last Modified: Wed, 09 Apr 2025 06:06:42 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0509bdd42ba78544f57fb329ea3aea3617dfaacd07f8a493050b8eefd26af45e`  
		Last Modified: Wed, 09 Apr 2025 06:06:42 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.0.0.5` - unknown; unknown

```console
$ docker pull aerospike@sha256:db0d868bc72260ecb868935f24f89c9e960aaa6d283c8ae7386f978cffb79ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1989452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf716b74b60adadf856aadddd866324ad2be304b0bc36701c1e30561cf28f51`

```dockerfile
```

-	Layers:
	-	`sha256:6c430722593eac6b8f59c6a0df08f286a8b60857c2eb1b6e689478dc2485b05d`  
		Last Modified: Wed, 09 Apr 2025 06:06:43 GMT  
		Size: 2.0 MB (1960210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:211077a3e8162177709d352ae581844d3b21cde9e1fd7e49cbd3d2857547f243`  
		Last Modified: Wed, 09 Apr 2025 06:06:42 GMT  
		Size: 29.2 KB (29242 bytes)  
		MIME: application/vnd.in-toto+json
