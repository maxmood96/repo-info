## `aerospike:ee-8.1.0.0_2`

```console
$ docker pull aerospike@sha256:8e0bd2d593f628cad3c7e6bc965e9f60c4c79724a5375bd79b95add1f93c4f58
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.1.0.0_2` - linux; amd64

```console
$ docker pull aerospike@sha256:9a66e8974c4a636797057e0601cf9f0d1d1771ccf2567c1383db60d9b7e2eafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83579775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788eb33c1929974aacdfb5ccc594f204ef93538e56add978a87b153d12b50186`
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
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.0.0 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 04 Sep 2025 23:57:21 GMT
ARG AEROSPIKE_EDITION=enterprise
# Thu, 04 Sep 2025 23:57:21 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Thu, 04 Sep 2025 23:57:21 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.0/aerospike-server-enterprise_8.1.0.0_tools-12.0.1_ubuntu24.04_x86_64.tgz
# Thu, 04 Sep 2025 23:57:21 GMT
ARG AEROSPIKE_SHA_X86_64=29b23377443c5c81346f09db2545c47cb4b6f27fc23efccc470bd5f22dc090c6
# Thu, 04 Sep 2025 23:57:21 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.0/aerospike-server-enterprise_8.1.0.0_tools-12.0.1_ubuntu24.04_aarch64.tgz
# Thu, 04 Sep 2025 23:57:21 GMT
ARG AEROSPIKE_SHA_AARCH64=1296963d3edd9a533ef8031c4c3f56c02a758a28ba3265cd0b4ffcd22450f8a2
# Thu, 04 Sep 2025 23:57:21 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 04 Sep 2025 23:57:21 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.0/aerospike-server-enterprise_8.1.0.0_tools-12.0.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=29b23377443c5c81346f09db2545c47cb4b6f27fc23efccc470bd5f22dc090c6 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.0/aerospike-server-enterprise_8.1.0.0_tools-12.0.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=1296963d3edd9a533ef8031c4c3f56c02a758a28ba3265cd0b4ffcd22450f8a2
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
	-	`sha256:9eefa6cdff250119be305db3e77d18e8d0b47a42695e3b9d3f91f156876b9a43`  
		Last Modified: Mon, 15 Sep 2025 22:12:04 GMT  
		Size: 53.9 MB (53854024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538709acf66f087a4c9c579f940c68c22350b7a8b9e19756009c439c8d2f3cee`  
		Last Modified: Mon, 15 Sep 2025 22:11:57 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afe5c3369f4e527e96564ecc362fa922c6456fbc1c8e173ae87e3145d9b69f7`  
		Last Modified: Mon, 15 Sep 2025 22:11:57 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.0.0_2` - unknown; unknown

```console
$ docker pull aerospike@sha256:8861423c1c9d087fb6207863867bc7ce25e7a71f0d516c984ad9d07c922e1ea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40929c2b68076ba41e10d1431e1d86648f5c5ec046409450e78696fc9e41e906`

```dockerfile
```

-	Layers:
	-	`sha256:c41c314ef84588ee27b4c4c472d96f32d3215a8a1fc6dab9e76a7773bd189687`  
		Last Modified: Mon, 15 Sep 2025 23:25:29 GMT  
		Size: 2.2 MB (2182953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db3a77408302c018297bc96cad4d4f015622aaea7c894e73ca98ad5245307c3b`  
		Last Modified: Mon, 15 Sep 2025 23:25:30 GMT  
		Size: 29.0 KB (29028 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.1.0.0_2` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:4c3145ec094ed459111c0202906988f2c814be5e96f17136efc68cce74eb23ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81933509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3155765af6a67799ede4b54b57e80ed95ea3a75efce88782494f2ef4aecf7ef`
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
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.0.0 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 04 Sep 2025 23:57:21 GMT
ARG AEROSPIKE_EDITION=enterprise
# Thu, 04 Sep 2025 23:57:21 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Thu, 04 Sep 2025 23:57:21 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.0/aerospike-server-enterprise_8.1.0.0_tools-12.0.1_ubuntu24.04_x86_64.tgz
# Thu, 04 Sep 2025 23:57:21 GMT
ARG AEROSPIKE_SHA_X86_64=29b23377443c5c81346f09db2545c47cb4b6f27fc23efccc470bd5f22dc090c6
# Thu, 04 Sep 2025 23:57:21 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.0/aerospike-server-enterprise_8.1.0.0_tools-12.0.1_ubuntu24.04_aarch64.tgz
# Thu, 04 Sep 2025 23:57:21 GMT
ARG AEROSPIKE_SHA_AARCH64=1296963d3edd9a533ef8031c4c3f56c02a758a28ba3265cd0b4ffcd22450f8a2
# Thu, 04 Sep 2025 23:57:21 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 04 Sep 2025 23:57:21 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.0/aerospike-server-enterprise_8.1.0.0_tools-12.0.1_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=29b23377443c5c81346f09db2545c47cb4b6f27fc23efccc470bd5f22dc090c6 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/8.1.0.0/aerospike-server-enterprise_8.1.0.0_tools-12.0.1_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=1296963d3edd9a533ef8031c4c3f56c02a758a28ba3265cd0b4ffcd22450f8a2
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
	-	`sha256:5cd1d979fe8e01665bcb2251df94256875f6ecd413322e8e4f1ee328094940d2`  
		Last Modified: Mon, 15 Sep 2025 22:10:59 GMT  
		Size: 53.1 MB (53069894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179094830dbc46dd54d588a5cc1e0e54d7877cd4077cf8c999425f55126da6cb`  
		Last Modified: Mon, 15 Sep 2025 22:10:55 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d807a578d6b045460745a920eafee0c1dc5e5f890bb912ecfe285b3fc455c858`  
		Last Modified: Mon, 15 Sep 2025 22:10:55 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.0.0_2` - unknown; unknown

```console
$ docker pull aerospike@sha256:fcfd94a78b1dcdec94098af0f3ad5184aeb492137e75dff47f121e36d3c6ba07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b234c83a331f1e13a42a24c76ed0bcb74f177e54d1d27f790f2934899f1432`

```dockerfile
```

-	Layers:
	-	`sha256:f12663ee2e8a526038ffea730e4941e10995d8674fd8312468e54f64c86eae62`  
		Last Modified: Mon, 15 Sep 2025 23:25:34 GMT  
		Size: 2.2 MB (2185233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4cfebcf09f3ec0f0e791be37b27cfe942911975eadf8f411cf0a2bdba1b0075`  
		Last Modified: Mon, 15 Sep 2025 23:25:35 GMT  
		Size: 29.1 KB (29108 bytes)  
		MIME: application/vnd.in-toto+json
