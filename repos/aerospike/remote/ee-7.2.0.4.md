## `aerospike:ee-7.2.0.4`

```console
$ docker pull aerospike@sha256:347b744591472649e25a109bc04bb3c1bf598fc9c1a519c081d105ffbb6e1f0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-7.2.0.4` - linux; amd64

```console
$ docker pull aerospike@sha256:45c8ff51b118a83ed5134174e96f0aa1bc2d7adf1a85b8b029466c328cf0ae88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81692643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b117d77118ab8a58e808bbd5ada19a465deef9a455fbcf849255cbdb60a7581`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:54 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:57 GMT
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
# Wed, 16 Oct 2024 09:25:57 GMT
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
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4970f096bd94e8fea65e3e04abd7757438e3e1ac94b8b3a0a8b60a955744a7d7`  
		Last Modified: Thu, 21 Nov 2024 19:28:08 GMT  
		Size: 51.9 MB (51938557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847ce8a39d3d8cf0359a510be428c3578d7cad21790ffa1c1aa3cf182c6a78b7`  
		Last Modified: Thu, 21 Nov 2024 19:28:06 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9606a0a96b8a27a75d8ae4f483756cb084c787d861214d707539f9aebd76e1`  
		Last Modified: Thu, 21 Nov 2024 19:28:06 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.2.0.4` - unknown; unknown

```console
$ docker pull aerospike@sha256:e64a2062258f98b6d0dc160cdc2016b1c49b4274ab571c1114a63bc00089cbfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1986394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daec3a1848d2d9bbfa01fa797522a4a40c54f13e9b016ae556269fae1c18f012`

```dockerfile
```

-	Layers:
	-	`sha256:9895d2aac2a89439d329b700a85cd6eb96c689e9baf0cc1e611a0b25fd93fba5`  
		Last Modified: Thu, 21 Nov 2024 19:28:06 GMT  
		Size: 2.0 MB (1957231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50555b31916d2ed3753cc32141b097a503114dd22fd7a902353fa3ba137316f5`  
		Last Modified: Thu, 21 Nov 2024 19:28:06 GMT  
		Size: 29.2 KB (29163 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-7.2.0.4` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:ec681f3471c9513c26c1aa53decefcafd61efa1bff1a750b34acdc03dcafc09b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80274483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d140eefeb422949dd538cec457dea17dad2d17589a9dcea2a6f2fd7029ec0b95`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
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
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a05a292ef9b9a219ea92756545cba8c5ff8e8622e446556a37b644032b1bbda`  
		Last Modified: Thu, 21 Nov 2024 22:13:29 GMT  
		Size: 51.4 MB (51379758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9884891c4e6d0c9b8518f764ff17a925ebb434a98042d5a1518c1219fcc139ad`  
		Last Modified: Thu, 21 Nov 2024 22:13:27 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e96cf04205e6443e8a2d76d41e50be816997bbf4af5414b85246459a2b48758`  
		Last Modified: Thu, 21 Nov 2024 22:13:27 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.2.0.4` - unknown; unknown

```console
$ docker pull aerospike@sha256:7e4f5c3920616df9a2ace86ebd369db84ec72947a44b00425f501588bd4b837f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1988745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80cd530bab3f0ca667e2c6225a5804a38d86077d41f92242e411558458a7acbe`

```dockerfile
```

-	Layers:
	-	`sha256:229304d15f841f966ae77b0f5a808106ff74329542194b11506b081903700cd6`  
		Last Modified: Thu, 21 Nov 2024 22:13:27 GMT  
		Size: 2.0 MB (1959502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:138a402bc5817646a14a81c38e5e96fa55dde619cca678064b0a5a8fe83e1bc9`  
		Last Modified: Thu, 21 Nov 2024 22:13:27 GMT  
		Size: 29.2 KB (29243 bytes)  
		MIME: application/vnd.in-toto+json
