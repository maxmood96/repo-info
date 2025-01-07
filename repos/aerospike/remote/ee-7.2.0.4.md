## `aerospike:ee-7.2.0.4`

```console
$ docker pull aerospike@sha256:3de876e61aed9db6de4e74313103a8d20cc43b6777bd687b659e20f63d949235
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-7.2.0.4` - linux; amd64

```console
$ docker pull aerospike@sha256:b27e69037e07863088279f358ed20ecd437ef9443b13afb23131058808a63374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81692986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b94065e1a1ddb3b68c50e5143b10cf022e0b4be274d54783603a0edcbb72643`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Thu, 21 Nov 2024 04:27:43 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.2.0.4 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 21 Nov 2024 04:27:43 GMT
ARG AEROSPIKE_EDITION=enterprise
# Thu, 21 Nov 2024 04:27:43 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.4/aerospike-server-enterprise_7.2.0.4_tools-11.1.1_ubuntu24.04_x86_64.tgz
# Thu, 21 Nov 2024 04:27:43 GMT
ARG AEROSPIKE_SHA_X86_64=56b9d435b7ad1cabb6ae2af5e3a25d82937bbbce9807f7b54234a41a8b1252ef
# Thu, 21 Nov 2024 04:27:43 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.4/aerospike-server-enterprise_7.2.0.4_tools-11.1.1_ubuntu24.04_aarch64.tgz
# Thu, 21 Nov 2024 04:27:43 GMT
ARG AEROSPIKE_SHA_AARCH64=16bc0a9d9a181ab84fafafcc54849b3de7587522ff279f5ff897c73c953cc068
# Thu, 21 Nov 2024 04:27:43 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 21 Nov 2024 04:27:43 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.4/aerospike-server-enterprise_7.2.0.4_tools-11.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=56b9d435b7ad1cabb6ae2af5e3a25d82937bbbce9807f7b54234a41a8b1252ef AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.4/aerospike-server-enterprise_7.2.0.4_tools-11.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=16bc0a9d9a181ab84fafafcc54849b3de7587522ff279f5ff897c73c953cc068
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 21 Nov 2024 04:27:43 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 21 Nov 2024 04:27:43 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 21 Nov 2024 04:27:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 21 Nov 2024 04:27:43 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 21 Nov 2024 04:27:43 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972e69c538f28f29a487245b15489d37a39f2b87cd21da9b0c04b5342562eb39`  
		Last Modified: Tue, 03 Dec 2024 02:15:47 GMT  
		Size: 51.9 MB (51938715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c31220b40c155714a42b9cdc78e640641f3639d087e4f30dd5805113e62250`  
		Last Modified: Tue, 03 Dec 2024 02:15:46 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de3fee3a919bd81fb722b4429c8191e32da1b8d05e385d25d89dad0358e8ef4`  
		Last Modified: Tue, 03 Dec 2024 02:15:46 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.2.0.4` - unknown; unknown

```console
$ docker pull aerospike@sha256:09b475f454a6791e7d5a162135365dee529b91a2e29cbf94750422586c572e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1986414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef86a0b21d158fb9be948c20444c43501ba755ca7794f2f906c634c9220e9d8`

```dockerfile
```

-	Layers:
	-	`sha256:fe9ee30b9083b7bf8d2dedb49b05e5907843d3776b83d6126ca02fea2baf166f`  
		Last Modified: Tue, 03 Dec 2024 02:15:46 GMT  
		Size: 2.0 MB (1957251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ff996512b67a54be1997a161f5bb31e4bc33a2297884795688e4c2e3c14f596`  
		Last Modified: Tue, 03 Dec 2024 02:15:46 GMT  
		Size: 29.2 KB (29163 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-7.2.0.4` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:9ba3751aee6125da065306876125cdf545759a80988314c5237a893d9fdf4d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80275044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f478f98324c517a69b4f8e2ada14abd50dc95faae7231747d77395fe4cd7318`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Thu, 21 Nov 2024 04:27:43 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.2.0.4 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 21 Nov 2024 04:27:43 GMT
ARG AEROSPIKE_EDITION=enterprise
# Thu, 21 Nov 2024 04:27:43 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.4/aerospike-server-enterprise_7.2.0.4_tools-11.1.1_ubuntu24.04_x86_64.tgz
# Thu, 21 Nov 2024 04:27:43 GMT
ARG AEROSPIKE_SHA_X86_64=56b9d435b7ad1cabb6ae2af5e3a25d82937bbbce9807f7b54234a41a8b1252ef
# Thu, 21 Nov 2024 04:27:43 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.4/aerospike-server-enterprise_7.2.0.4_tools-11.1.1_ubuntu24.04_aarch64.tgz
# Thu, 21 Nov 2024 04:27:43 GMT
ARG AEROSPIKE_SHA_AARCH64=16bc0a9d9a181ab84fafafcc54849b3de7587522ff279f5ff897c73c953cc068
# Thu, 21 Nov 2024 04:27:43 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 21 Nov 2024 04:27:43 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.4/aerospike-server-enterprise_7.2.0.4_tools-11.1.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=56b9d435b7ad1cabb6ae2af5e3a25d82937bbbce9807f7b54234a41a8b1252ef AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.2.0.4/aerospike-server-enterprise_7.2.0.4_tools-11.1.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=16bc0a9d9a181ab84fafafcc54849b3de7587522ff279f5ff897c73c953cc068
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 21 Nov 2024 04:27:43 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 21 Nov 2024 04:27:43 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 21 Nov 2024 04:27:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 21 Nov 2024 04:27:43 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 21 Nov 2024 04:27:43 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d479c431296cfa67b42627d6e5762f86161e2d60cd67cf95b31b93079a65c2`  
		Last Modified: Tue, 03 Dec 2024 05:37:46 GMT  
		Size: 51.4 MB (51380071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6420c19d9909118068b7cfd2cb19818bcc869f7e0bbfdc4e4dab5f070371d3f1`  
		Last Modified: Tue, 03 Dec 2024 05:37:44 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30084fb2780b4b63dc37a51579d32d39cc9d57a747f3c899d89330593f36515`  
		Last Modified: Tue, 03 Dec 2024 05:37:44 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.2.0.4` - unknown; unknown

```console
$ docker pull aerospike@sha256:c986563265207bfc853b175472359a5134fa8bc308b59e83d47cdac99202ae74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1988765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527a49b4f5c016b83241a4294d4077bffbf9a43a896936d5aeb6bc22c27de8db`

```dockerfile
```

-	Layers:
	-	`sha256:88880498b02135c05227166c3f553d468388b18b0ecc42ae27888ee5ec1a9ddb`  
		Last Modified: Tue, 03 Dec 2024 05:37:45 GMT  
		Size: 2.0 MB (1959522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40e8027a16412ba3a6aa4dc29e8905f0232f82570ee30ecd2abbe8d0d1cb8412`  
		Last Modified: Tue, 03 Dec 2024 05:37:44 GMT  
		Size: 29.2 KB (29243 bytes)  
		MIME: application/vnd.in-toto+json
