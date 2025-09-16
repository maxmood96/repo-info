## `aerospike:ce-8.1.0.0_2`

```console
$ docker pull aerospike@sha256:386122b0a4fed4373accfa8bd93c1dba2271d7e5e2177995dfda6ff8c98a9765
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.1.0.0_2` - linux; amd64

```console
$ docker pull aerospike@sha256:5f2ead82d4538732b2ef38a096570f47db8a32f105db067b04f299e66d179f4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81477045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1339374ee5fcfe4bcca3dc6c166ae74970e39ad64a5fc50de8c1b8d46d69d4fb`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Thu, 04 Sep 2025 23:57:21 GMT
ARG RELEASE
# Thu, 04 Sep 2025 23:57:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 04 Sep 2025 23:57:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 04 Sep 2025 23:57:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 04 Sep 2025 23:57:21 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Thu, 04 Sep 2025 23:57:21 GMT
CMD ["/bin/bash"]
# Thu, 04 Sep 2025 23:57:21 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.0.0 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 04 Sep 2025 23:57:21 GMT
ARG AEROSPIKE_EDITION=community
# Thu, 04 Sep 2025 23:57:21 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Thu, 04 Sep 2025 23:57:21 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.0/aerospike-server-community_8.1.0.0_tools-12.0.1_ubuntu24.04_x86_64.tgz
# Thu, 04 Sep 2025 23:57:21 GMT
ARG AEROSPIKE_SHA_X86_64=32e63cf0e83a0ee559984505b6cb069c2218da97b621ff63dd58e55993392c2b
# Thu, 04 Sep 2025 23:57:21 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.0/aerospike-server-community_8.1.0.0_tools-12.0.1_ubuntu24.04_aarch64.tgz
# Thu, 04 Sep 2025 23:57:21 GMT
ARG AEROSPIKE_SHA_AARCH64=fc29743dd6a098eb5bd11b55bf76491cc5a2252792fdf366224fdcd755cc079b
# Thu, 04 Sep 2025 23:57:21 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 04 Sep 2025 23:57:21 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.0/aerospike-server-community_8.1.0.0_tools-12.0.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=32e63cf0e83a0ee559984505b6cb069c2218da97b621ff63dd58e55993392c2b AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.0/aerospike-server-community_8.1.0.0_tools-12.0.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=fc29743dd6a098eb5bd11b55bf76491cc5a2252792fdf366224fdcd755cc079b
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 04 Sep 2025 23:57:21 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 04 Sep 2025 23:57:21 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 04 Sep 2025 23:57:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 23:57:21 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 04 Sep 2025 23:57:21 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c7b94538e57517aed45ba7e975c072316af9e70162b4c890d88a45da51ca12`  
		Last Modified: Mon, 15 Sep 2025 22:12:01 GMT  
		Size: 51.8 MB (51751296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091c804bc1bc21a782c2c00de6b706708fa9d5036ef3746bcd573588cc5b30ce`  
		Last Modified: Mon, 15 Sep 2025 22:11:57 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88f2e7de10b5be44da57c069be7e533f41542ff57b1e1337862516f0523233b`  
		Last Modified: Mon, 15 Sep 2025 22:11:57 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.0.0_2` - unknown; unknown

```console
$ docker pull aerospike@sha256:500bca236658fd41f33645c6d92d92db01f557dfdab72cf9296009aafbadadcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424ab9e15f9b68056eb45acc6ed89f3d4716aa418332616eb8c66a0dfa4a7ff9`

```dockerfile
```

-	Layers:
	-	`sha256:f52e9d234adf58d58f2c60351e6007932fbe5fadd3e5c36fafa3f24657d13433`  
		Last Modified: Mon, 15 Sep 2025 23:25:20 GMT  
		Size: 2.2 MB (2182312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd66e690654efc99821da0dcb81274ff096e6c1edce5a8b3b99e1d807076fc11`  
		Last Modified: Mon, 15 Sep 2025 23:25:21 GMT  
		Size: 29.0 KB (29012 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.1.0.0_2` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:7a6e19e0ace730c11cf971698408479b077a50d53b9f222cd85ea7b5536b0d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79845062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d2ee015b9495601bdfc9c93db827d73d36a052b1bf1851183afca5288368e5`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Thu, 04 Sep 2025 23:57:21 GMT
ARG RELEASE
# Thu, 04 Sep 2025 23:57:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 04 Sep 2025 23:57:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 04 Sep 2025 23:57:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 04 Sep 2025 23:57:21 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Thu, 04 Sep 2025 23:57:21 GMT
CMD ["/bin/bash"]
# Thu, 04 Sep 2025 23:57:21 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.0.0 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 04 Sep 2025 23:57:21 GMT
ARG AEROSPIKE_EDITION=community
# Thu, 04 Sep 2025 23:57:21 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Thu, 04 Sep 2025 23:57:21 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.0/aerospike-server-community_8.1.0.0_tools-12.0.1_ubuntu24.04_x86_64.tgz
# Thu, 04 Sep 2025 23:57:21 GMT
ARG AEROSPIKE_SHA_X86_64=32e63cf0e83a0ee559984505b6cb069c2218da97b621ff63dd58e55993392c2b
# Thu, 04 Sep 2025 23:57:21 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.0/aerospike-server-community_8.1.0.0_tools-12.0.1_ubuntu24.04_aarch64.tgz
# Thu, 04 Sep 2025 23:57:21 GMT
ARG AEROSPIKE_SHA_AARCH64=fc29743dd6a098eb5bd11b55bf76491cc5a2252792fdf366224fdcd755cc079b
# Thu, 04 Sep 2025 23:57:21 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 04 Sep 2025 23:57:21 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.0/aerospike-server-community_8.1.0.0_tools-12.0.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=32e63cf0e83a0ee559984505b6cb069c2218da97b621ff63dd58e55993392c2b AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.1.0.0/aerospike-server-community_8.1.0.0_tools-12.0.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=fc29743dd6a098eb5bd11b55bf76491cc5a2252792fdf366224fdcd755cc079b
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       xz-utils;   };   {     apt-get install -y --no-install-recommends ca-certificates curl procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 04 Sep 2025 23:57:21 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 04 Sep 2025 23:57:21 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 04 Sep 2025 23:57:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 23:57:21 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 04 Sep 2025 23:57:21 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828c892ec1306c0756cd942c0879f2bcf66ca238662091c9f115e84af4274d76`  
		Last Modified: Mon, 15 Sep 2025 22:11:45 GMT  
		Size: 51.0 MB (50981445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b01b273d3e1828b779238a3bb4b993fa876ace99333506e749a6ce9d122341`  
		Last Modified: Mon, 15 Sep 2025 22:11:38 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c27c9ceb53d6400212ce6e826bcb02e16cd3fa1ddbfbe0676c698cf417ebce3`  
		Last Modified: Mon, 15 Sep 2025 22:11:38 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.0.0_2` - unknown; unknown

```console
$ docker pull aerospike@sha256:df088b5c419829c53f065df8e90a4470413b3a4ca48f12e6873114c4764e872b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2213684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f19add592e5ce71d513d4303b9e6d2ef3d405fb96eea2698beef70c643171d6`

```dockerfile
```

-	Layers:
	-	`sha256:23b2e621e4c2a84693d3c049a35386d7b261dbae7d7171466454f25388d09d5f`  
		Last Modified: Mon, 15 Sep 2025 23:25:25 GMT  
		Size: 2.2 MB (2184592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52f2ef1ee7a8a1affd0ac888df4200f0ddb437df217a443215e01e8467cb8c66`  
		Last Modified: Mon, 15 Sep 2025 23:25:26 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json
