## `aerospike:ee-8.0.0.4_1`

```console
$ docker pull aerospike@sha256:b8e3a1b1931098b0de1f3132490ffdb1877d3680d213a1351501d7eeef651a9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.0.0.4_1` - linux; amd64

```console
$ docker pull aerospike@sha256:fc3a520761ff4ea468f5eaaa0cf5e197a33147b09e2cd536c1362c285182153d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84430724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfa740e0ed5d1fdba0872051c8c2ede3f925956bdc626468737cc5c9e715b88`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2025 20:36:12 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.4 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 21 Feb 2025 20:36:12 GMT
ARG AEROSPIKE_EDITION=enterprise
# Fri, 21 Feb 2025 20:36:12 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.4/aerospike-server-enterprise_8.0.0.4_tools-11.2.0_ubuntu24.04_x86_64.tgz
# Fri, 21 Feb 2025 20:36:12 GMT
ARG AEROSPIKE_SHA_X86_64=f090d89dc2f93175fb8bba0fb1f173448ebe2b3b5f17b2610498dad076b6f508
# Fri, 21 Feb 2025 20:36:12 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.4/aerospike-server-enterprise_8.0.0.4_tools-11.2.0_ubuntu24.04_aarch64.tgz
# Fri, 21 Feb 2025 20:36:12 GMT
ARG AEROSPIKE_SHA_AARCH64=8fa2a101f5b4a9b8720e6c488c375c61bbfb4d20f31c41299da7401790258ddc
# Fri, 21 Feb 2025 20:36:12 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 21 Feb 2025 20:36:12 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.4/aerospike-server-enterprise_8.0.0.4_tools-11.2.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=f090d89dc2f93175fb8bba0fb1f173448ebe2b3b5f17b2610498dad076b6f508 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.4/aerospike-server-enterprise_8.0.0.4_tools-11.2.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=8fa2a101f5b4a9b8720e6c488c375c61bbfb4d20f31c41299da7401790258ddc
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 21 Feb 2025 20:36:12 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 21 Feb 2025 20:36:12 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 21 Feb 2025 20:36:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Feb 2025 20:36:12 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 21 Feb 2025 20:36:12 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17ce73ad287e24943b099608d408d9c45c3beaada83c4c279531eec069f90cd`  
		Last Modified: Fri, 21 Feb 2025 22:27:33 GMT  
		Size: 54.7 MB (54674130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc4eaf0e09b915e39bef8649b3984dc260a38c8058faeaa890a9d3f7ea6a086`  
		Last Modified: Fri, 21 Feb 2025 22:27:32 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba930d566a53cfbc282ca1d83fe095bd57c43992c07ba3828e0c7ec1dffb6de`  
		Last Modified: Fri, 21 Feb 2025 22:27:32 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.0.0.4_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:8ec196c8c5cedeafa57ca4c6bf9bf40a8e512fbf5297fbbacc47146a11d71b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1989320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e15d97b33c737dd931c0b3b383937b730b9be302e3ea2a02cc4c8ac5e32f885`

```dockerfile
```

-	Layers:
	-	`sha256:0f62c2cccb5f92ec52e1b19bc3dbe9a33fc6193a17cec5bd287d3ae69b9b96b5`  
		Last Modified: Fri, 21 Feb 2025 22:27:32 GMT  
		Size: 2.0 MB (1960157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:965b3ab636043da3af007f4ad1335974ae9290de420612122b9eb0ec7f1643e4`  
		Last Modified: Fri, 21 Feb 2025 22:27:32 GMT  
		Size: 29.2 KB (29163 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.0.0.4_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:cc11b4eb207d86c8e24369e8f43cdc1c90346d1ceda970a731e90dba467a9e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82820613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0e38b64ff8661b8a0cfc704e933983b128362d61ce7fa6b3e23a9502151013`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2025 20:36:12 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.4 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Fri, 21 Feb 2025 20:36:12 GMT
ARG AEROSPIKE_EDITION=enterprise
# Fri, 21 Feb 2025 20:36:12 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.4/aerospike-server-enterprise_8.0.0.4_tools-11.2.0_ubuntu24.04_x86_64.tgz
# Fri, 21 Feb 2025 20:36:12 GMT
ARG AEROSPIKE_SHA_X86_64=f090d89dc2f93175fb8bba0fb1f173448ebe2b3b5f17b2610498dad076b6f508
# Fri, 21 Feb 2025 20:36:12 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.4/aerospike-server-enterprise_8.0.0.4_tools-11.2.0_ubuntu24.04_aarch64.tgz
# Fri, 21 Feb 2025 20:36:12 GMT
ARG AEROSPIKE_SHA_AARCH64=8fa2a101f5b4a9b8720e6c488c375c61bbfb4d20f31c41299da7401790258ddc
# Fri, 21 Feb 2025 20:36:12 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Fri, 21 Feb 2025 20:36:12 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.4/aerospike-server-enterprise_8.0.0.4_tools-11.2.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=f090d89dc2f93175fb8bba0fb1f173448ebe2b3b5f17b2610498dad076b6f508 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.0.0.4/aerospike-server-enterprise_8.0.0.4_tools-11.2.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=8fa2a101f5b4a9b8720e6c488c375c61bbfb4d20f31c41299da7401790258ddc
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Fri, 21 Feb 2025 20:36:12 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Fri, 21 Feb 2025 20:36:12 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Fri, 21 Feb 2025 20:36:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Feb 2025 20:36:12 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Fri, 21 Feb 2025 20:36:12 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6932a7a5c6fa63952188cd1f32916165b92a2d0eb77b0f8fb85b9443afec273d`  
		Last Modified: Fri, 21 Feb 2025 22:28:02 GMT  
		Size: 53.9 MB (53924712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11f7c82bc3cc3b1153cdd86aca79e4f59bdff693dca4d4e83129fb0ff40e725`  
		Last Modified: Fri, 21 Feb 2025 22:28:00 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9046f8155fde5a93da6d33f3c55f9e7ce3378b5cb3bc6bd714520f815b0483`  
		Last Modified: Fri, 21 Feb 2025 22:27:37 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.0.0.4_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:68fd86539fd1c4ddbaf8d8c83b19e1c34d437efc68fa885c306357ddbb1edd8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1991680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f52e4c1b24a5e713d3044fc8d40c2ada2fca4a0be33a7328d8cd89393e947e`

```dockerfile
```

-	Layers:
	-	`sha256:da0466b12767a49f1b954f03b12f9fd7b2019b762875698efaa5c73b8035468f`  
		Last Modified: Fri, 21 Feb 2025 22:28:01 GMT  
		Size: 2.0 MB (1962437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60be784ffaa9bc7b7687440534f1447a9eed6e0cefaed37c0452dc656e82760`  
		Last Modified: Fri, 21 Feb 2025 22:28:00 GMT  
		Size: 29.2 KB (29243 bytes)  
		MIME: application/vnd.in-toto+json
