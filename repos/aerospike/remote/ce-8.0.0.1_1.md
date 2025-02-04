## `aerospike:ce-8.0.0.1_1`

```console
$ docker pull aerospike@sha256:0fcae99d4bbb24567baf69a61555b49d3a9d567e6c922b59edeb136e76801cc9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.0.0.1_1` - linux; amd64

```console
$ docker pull aerospike@sha256:6f0139b01948776dfd955921f3f991ae2a98b28faa6d5eb061cf6cbc97472e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77746666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca651a246dcf263eb30a253d46ded044be2751c6e816e0fa93311cbc4013124`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Thu, 23 Jan 2025 07:00:10 GMT
ARG RELEASE
# Thu, 23 Jan 2025 07:00:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 Jan 2025 07:00:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 Jan 2025 07:00:10 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 23 Jan 2025 07:00:10 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Thu, 23 Jan 2025 07:00:10 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 07:00:10 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 23 Jan 2025 07:00:10 GMT
ARG AEROSPIKE_EDITION=community
# Thu, 23 Jan 2025 07:00:10 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.1/aerospike-server-community_8.0.0.1_tools-11.2.0_ubuntu24.04_x86_64.tgz
# Thu, 23 Jan 2025 07:00:10 GMT
ARG AEROSPIKE_SHA_X86_64=f1bfa2f3f630b2a6154f245ddd3a9189673d0edecb1059f92b5596f82cac0788
# Thu, 23 Jan 2025 07:00:10 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.1/aerospike-server-community_8.0.0.1_tools-11.2.0_ubuntu24.04_aarch64.tgz
# Thu, 23 Jan 2025 07:00:10 GMT
ARG AEROSPIKE_SHA_AARCH64=6b427d8e8046c608061db23ab6ce93ae9972d7693ce68dc3caebef82e53cfa47
# Thu, 23 Jan 2025 07:00:10 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 23 Jan 2025 07:00:10 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.1/aerospike-server-community_8.0.0.1_tools-11.2.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=f1bfa2f3f630b2a6154f245ddd3a9189673d0edecb1059f92b5596f82cac0788 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.1/aerospike-server-community_8.0.0.1_tools-11.2.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=6b427d8e8046c608061db23ab6ce93ae9972d7693ce68dc3caebef82e53cfa47
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 23 Jan 2025 07:00:10 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 23 Jan 2025 07:00:10 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 23 Jan 2025 07:00:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 23 Jan 2025 07:00:10 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 23 Jan 2025 07:00:10 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102f16b9b3c9363435933fd7e324f1b3ff351c2ab0ca3cdb98a56d54d97af898`  
		Last Modified: Tue, 04 Feb 2025 04:37:28 GMT  
		Size: 48.0 MB (47990073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf93528ef43a3cc51386bbc106b27f3367bd19866061226fbaa0da7bbe5f866`  
		Last Modified: Tue, 04 Feb 2025 04:37:27 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33647932fc8d09ca4d0b850141619c4420a93e767d49ff17efac505903e48462`  
		Last Modified: Tue, 04 Feb 2025 04:37:27 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.0.0.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:161c00bc44f37589695e994fcdf37f06999ad4661fc5e8c63d6b3e9764793ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1895422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78201211b0b08ae3f853e96c091e0b2a38883533f00a460593e6b238dafb8a19`

```dockerfile
```

-	Layers:
	-	`sha256:2da2c4d3f4f188da0f5780165141f6da3fbc7da330c3d36a5636ae03de68b829`  
		Last Modified: Tue, 04 Feb 2025 04:37:27 GMT  
		Size: 1.9 MB (1866275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:673d7a2cf17949270037e1dcb466908e87adff98edfe8807396b123b2191902c`  
		Last Modified: Tue, 04 Feb 2025 04:37:27 GMT  
		Size: 29.1 KB (29147 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.0.0.1_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:e921bf697852216bf0f2fb414ed3def7bd8ae5013bdcec741c4845ac25459163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76308149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f6465fe09cb34728229087c1946ee0139d94fcf2440614d4dda24af510bc491`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Thu, 23 Jan 2025 07:00:10 GMT
ARG RELEASE
# Thu, 23 Jan 2025 07:00:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 Jan 2025 07:00:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 Jan 2025 07:00:10 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 23 Jan 2025 07:00:10 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Thu, 23 Jan 2025 07:00:10 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 07:00:10 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.0.0.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 23 Jan 2025 07:00:10 GMT
ARG AEROSPIKE_EDITION=community
# Thu, 23 Jan 2025 07:00:10 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.1/aerospike-server-community_8.0.0.1_tools-11.2.0_ubuntu24.04_x86_64.tgz
# Thu, 23 Jan 2025 07:00:10 GMT
ARG AEROSPIKE_SHA_X86_64=f1bfa2f3f630b2a6154f245ddd3a9189673d0edecb1059f92b5596f82cac0788
# Thu, 23 Jan 2025 07:00:10 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.1/aerospike-server-community_8.0.0.1_tools-11.2.0_ubuntu24.04_aarch64.tgz
# Thu, 23 Jan 2025 07:00:10 GMT
ARG AEROSPIKE_SHA_AARCH64=6b427d8e8046c608061db23ab6ce93ae9972d7693ce68dc3caebef82e53cfa47
# Thu, 23 Jan 2025 07:00:10 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 23 Jan 2025 07:00:10 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.1/aerospike-server-community_8.0.0.1_tools-11.2.0_ubuntu24.04_x86_64.tgz AEROSPIKE_SHA_X86_64=f1bfa2f3f630b2a6154f245ddd3a9189673d0edecb1059f92b5596f82cac0788 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/8.0.0.1/aerospike-server-community_8.0.0.1_tools-11.2.0_ubuntu24.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=6b427d8e8046c608061db23ab6ce93ae9972d7693ce68dc3caebef82e53cfa47
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-[a-z0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 23 Jan 2025 07:00:10 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 23 Jan 2025 07:00:10 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 23 Jan 2025 07:00:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 23 Jan 2025 07:00:10 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 23 Jan 2025 07:00:10 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa190db51c1bae5a90a5c0bf69388122cab0f1cd1ba4c085fe1a800fe3f93ee`  
		Last Modified: Tue, 04 Feb 2025 08:59:31 GMT  
		Size: 47.4 MB (47412247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fdb5eaa0f7e0c44b8e8d4b517b7050ebc8ed90dc6b03d2fc22a020f58b9bd3`  
		Last Modified: Tue, 04 Feb 2025 08:59:29 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716f488692cbf9517398685020e90b5970041652a0ccdd019e4caf78a2bcdc27`  
		Last Modified: Tue, 04 Feb 2025 08:59:29 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.0.0.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:7770308d5caf4c558ace1395edbe94975bc782f018387b2771601fc764c520ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1897764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8eeab85a73b8d7c825f4876812110ce7d69dd7a041fa3c450761c97fe365b17`

```dockerfile
```

-	Layers:
	-	`sha256:810269bca836c4d2a1bfc37abe146ab9cbdaa9595dfe45a6ed643a42a7bef7af`  
		Last Modified: Tue, 04 Feb 2025 08:59:30 GMT  
		Size: 1.9 MB (1868537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a411e2d60e57444cbbff635c9b8e6cfe733d2716f5d1063fb175fc5f0f0d6511`  
		Last Modified: Tue, 04 Feb 2025 08:59:29 GMT  
		Size: 29.2 KB (29227 bytes)  
		MIME: application/vnd.in-toto+json
