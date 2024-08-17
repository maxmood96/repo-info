## `aerospike:ee-7.1.0.5_1`

```console
$ docker pull aerospike@sha256:86580e9410cefd5b9534fcfde0ab97dae46ab5257fe00db757c58e4efd9ab245
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-7.1.0.5_1` - linux; amd64

```console
$ docker pull aerospike@sha256:8f856f7628b168871995032de379df1b6a7886a578830af4f76c35cb802e95a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80669950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de351e8c0ecf99eab6b4f7df1e72f9fc1ca9ba3f4e6b96fc64b11d8e908274f`
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
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.5 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Wed, 14 Aug 2024 06:09:32 GMT
ARG AEROSPIKE_EDITION=enterprise
# Wed, 14 Aug 2024 06:09:32 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.5/aerospike-server-enterprise_7.1.0.5_tools-11.0.2_ubuntu22.04_x86_64.tgz
# Wed, 14 Aug 2024 06:09:32 GMT
ARG AEROSPIKE_SHA_X86_64=bef2f083ebf55ef57bb333d316763f691f7cb20dea3f82ee086c39731143e580
# Wed, 14 Aug 2024 06:09:32 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.5/aerospike-server-enterprise_7.1.0.5_tools-11.0.2_ubuntu22.04_aarch64.tgz
# Wed, 14 Aug 2024 06:09:32 GMT
ARG AEROSPIKE_SHA_AARCH64=6ae4e5cc3a5705e0291b9c99e5368243fe2bce6a002084b40680cf398c85d8af
# Wed, 14 Aug 2024 06:09:32 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Wed, 14 Aug 2024 06:09:32 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.5/aerospike-server-enterprise_7.1.0.5_tools-11.0.2_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=bef2f083ebf55ef57bb333d316763f691f7cb20dea3f82ee086c39731143e580 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.5/aerospike-server-enterprise_7.1.0.5_tools-11.0.2_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=6ae4e5cc3a5705e0291b9c99e5368243fe2bce6a002084b40680cf398c85d8af
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
	-	`sha256:027ffaeec3a8148ea96dd84f9550190d20b27e0efe395ed4440d8dbc790e87c5`  
		Last Modified: Sat, 17 Aug 2024 01:59:18 GMT  
		Size: 51.1 MB (51131638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5895e2816518b6be4eae30733aaada10f07fdad633ff1ba5272994c586e427e6`  
		Last Modified: Sat, 17 Aug 2024 01:59:16 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4dcdcbfc5e020d095ac71fc80949adc63d006952550c1ea263fa3a64a9131c`  
		Last Modified: Sat, 17 Aug 2024 01:59:16 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.1.0.5_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:a2fdb273bfe1bc695c5bdd3b5dd0dc41677599396ee9e3f73734351cc2c7d77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1970015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b4554791fbb94b1832c1605ade08317898687e016ab8c3e9ddf679222920f38`

```dockerfile
```

-	Layers:
	-	`sha256:9856b4844d21cb06d742d84e4f30410a0bbc962beca469a0b6116a19e43a736a`  
		Last Modified: Sat, 17 Aug 2024 01:59:17 GMT  
		Size: 1.9 MB (1941107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0bfb8dae75f7db041e50953f3a7c30b34ff9a6dea28fe4593fd3be19e6743ac`  
		Last Modified: Sat, 17 Aug 2024 01:59:16 GMT  
		Size: 28.9 KB (28908 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-7.1.0.5_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:4e304d88e62cf07e95225686e0af0fbc0202c1d1ebf8a1972b82e24c9239ac4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77858568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173b9473ff96b06b6d070d6a9cba503a333151bf4a3b01bd8630402551cec97a`
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
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.5 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Wed, 14 Aug 2024 06:09:32 GMT
ARG AEROSPIKE_EDITION=enterprise
# Wed, 14 Aug 2024 06:09:32 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.5/aerospike-server-enterprise_7.1.0.5_tools-11.0.2_ubuntu22.04_x86_64.tgz
# Wed, 14 Aug 2024 06:09:32 GMT
ARG AEROSPIKE_SHA_X86_64=bef2f083ebf55ef57bb333d316763f691f7cb20dea3f82ee086c39731143e580
# Wed, 14 Aug 2024 06:09:32 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.5/aerospike-server-enterprise_7.1.0.5_tools-11.0.2_ubuntu22.04_aarch64.tgz
# Wed, 14 Aug 2024 06:09:32 GMT
ARG AEROSPIKE_SHA_AARCH64=6ae4e5cc3a5705e0291b9c99e5368243fe2bce6a002084b40680cf398c85d8af
# Wed, 14 Aug 2024 06:09:32 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Wed, 14 Aug 2024 06:09:32 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.5/aerospike-server-enterprise_7.1.0.5_tools-11.0.2_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=bef2f083ebf55ef57bb333d316763f691f7cb20dea3f82ee086c39731143e580 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.5/aerospike-server-enterprise_7.1.0.5_tools-11.0.2_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=6ae4e5cc3a5705e0291b9c99e5368243fe2bce6a002084b40680cf398c85d8af
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
	-	`sha256:84fcd3bc5333dfda25c7d6c78906022607e8f5f4a737f6c897ec93e07f638b6c`  
		Last Modified: Sat, 17 Aug 2024 02:13:48 GMT  
		Size: 50.5 MB (50497594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0177e0174e7aa4289cc437c2fa01551b0cbeb458eff0a3be3ab6bc4b2438c552`  
		Last Modified: Sat, 17 Aug 2024 02:13:46 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f535b512a5e8cace135dbfd92de703da24fb898d2a68b743a584fbc0e0b70a85`  
		Last Modified: Sat, 17 Aug 2024 02:13:46 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.1.0.5_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:32a9f5952412f359b1922f939cbbd39c1a99b41e4d6a722ac3d119317e559e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1971663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea8e0585ca43931d31139e7849b09d6c8303ae3660998d74a03df8c6013e93a`

```dockerfile
```

-	Layers:
	-	`sha256:54cd8fa47ccac7ae1ec5cf65d7d5b5641ac58a83efbc1774becfc908b0384196`  
		Last Modified: Sat, 17 Aug 2024 02:13:46 GMT  
		Size: 1.9 MB (1942478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4053a44cedd3fddbd4a3fe040f52be7a34b2e0f8bf10b000aa717672108cba32`  
		Last Modified: Sat, 17 Aug 2024 02:13:46 GMT  
		Size: 29.2 KB (29185 bytes)  
		MIME: application/vnd.in-toto+json
