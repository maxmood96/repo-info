## `aerospike:ee-7.1.0.1`

```console
$ docker pull aerospike@sha256:adb69b56b6c4d85682f633b947b81ed0c3049c79e0675081e253c1e74c131625
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `aerospike:ee-7.1.0.1` - linux; amd64

```console
$ docker pull aerospike@sha256:4bf55450d681088b449dcac8c5d969de08a49cec6fa68ec63836ade0b105bd89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81987572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d1c5d9e99a24648a0fed43620084295cd5e8c13f2b8d7adc71e783d2572271`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 02:22:43 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 04 Jun 2024 02:22:43 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 04 Jun 2024 02:22:43 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.1/aerospike-server-enterprise_7.1.0.1_tools-11.0.1_ubuntu22.04_x86_64.tgz
# Tue, 04 Jun 2024 02:22:43 GMT
ARG AEROSPIKE_SHA_X86_64=8e73af5aaed00d25ec57289e1429a5b8e933fec3d7ff29b5bc7659c500677c49
# Tue, 04 Jun 2024 02:22:43 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.1/aerospike-server-enterprise_7.1.0.1_tools-11.0.1_ubuntu22.04_aarch64.tgz
# Tue, 04 Jun 2024 02:22:43 GMT
ARG AEROSPIKE_SHA_AARCH64=1ea83b77615bb39e88c87ca3cfa5d7a456bda3e2ba0be3124eb678c897718a5f
# Tue, 04 Jun 2024 02:22:43 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 04 Jun 2024 02:22:43 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.1/aerospike-server-enterprise_7.1.0.1_tools-11.0.1_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=8e73af5aaed00d25ec57289e1429a5b8e933fec3d7ff29b5bc7659c500677c49 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.1/aerospike-server-enterprise_7.1.0.1_tools-11.0.1_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=1ea83b77615bb39e88c87ca3cfa5d7a456bda3e2ba0be3124eb678c897718a5f
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Tue, 04 Jun 2024 02:22:43 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 04 Jun 2024 02:22:43 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 04 Jun 2024 02:22:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Jun 2024 02:22:43 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 04 Jun 2024 02:22:43 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f716391d5bc08dc1c77cbb5098c693ecc6ed76455512dd13408b8740b5913208`  
		Last Modified: Wed, 05 Jun 2024 02:24:17 GMT  
		Size: 52.5 MB (52451530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedec7a0e65dd5a5bac6ab94f11d61d4364b14b8307ca90eae69d3532872ac20`  
		Last Modified: Wed, 05 Jun 2024 02:24:16 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49c77e51e6875eefb648a066bd00e4b40eec886e382eade3232b0945d5ef370`  
		Last Modified: Wed, 05 Jun 2024 02:24:17 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.1.0.1` - unknown; unknown

```console
$ docker pull aerospike@sha256:23c072e88f8623645f8c5f873b1ad2a42da9c830279577da441407371d8ecc22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1945999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c228b3b8964bfd1588262ec0a059b4c3d574f27288597cda8be2260cd9c585`

```dockerfile
```

-	Layers:
	-	`sha256:a293b84827cef8954cbcc6e5de048e51d84a40e8b0b32612e83579097684b259`  
		Last Modified: Wed, 05 Jun 2024 02:24:17 GMT  
		Size: 1.9 MB (1917140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f35f10abe30477d41d6290af00ec1bbf45d1d05e1aa14373d57b9c6ce5e8d2dc`  
		Last Modified: Wed, 05 Jun 2024 02:24:16 GMT  
		Size: 28.9 KB (28859 bytes)  
		MIME: application/vnd.in-toto+json
