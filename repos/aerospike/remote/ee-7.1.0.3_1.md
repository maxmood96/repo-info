## `aerospike:ee-7.1.0.3_1`

```console
$ docker pull aerospike@sha256:c72edb3e8e99fe27524c78a50fe9df7c558fdea0d6de894b1e1e1efe55bb74e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `aerospike:ee-7.1.0.3_1` - linux; amd64

```console
$ docker pull aerospike@sha256:7ffc273429842e7a21c85f01fd9b67e3124e16024e421f721c8bffef3b04b9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80667994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a958e8b029a79a01c527005b6a9f2b4c79078124101579d27df8d3b5e0723ac`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 03:36:37 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.3 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 18 Jul 2024 03:36:37 GMT
ARG AEROSPIKE_EDITION=enterprise
# Thu, 18 Jul 2024 03:36:37 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.3/aerospike-server-enterprise_7.1.0.3_tools-11.0.2_ubuntu22.04_x86_64.tgz
# Thu, 18 Jul 2024 03:36:37 GMT
ARG AEROSPIKE_SHA_X86_64=a17f79fc8204a52bd556dfe009911a77c19f31306036807243a0458a8ff54656
# Thu, 18 Jul 2024 03:36:37 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.3/aerospike-server-enterprise_7.1.0.3_tools-11.0.2_ubuntu22.04_aarch64.tgz
# Thu, 18 Jul 2024 03:36:37 GMT
ARG AEROSPIKE_SHA_AARCH64=95e1990ef29716bd5d19266ed9a4550f78315907bc196154f57277e0503bb400
# Thu, 18 Jul 2024 03:36:37 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 18 Jul 2024 03:36:37 GMT
# ARGS: AEROSPIKE_EDITION=enterprise AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.3/aerospike-server-enterprise_7.1.0.3_tools-11.0.2_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=a17f79fc8204a52bd556dfe009911a77c19f31306036807243a0458a8ff54656 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-enterprise/7.1.0.3/aerospike-server-enterprise_7.1.0.3_tools-11.0.2_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=95e1990ef29716bd5d19266ed9a4550f78315907bc196154f57277e0503bb400
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 18 Jul 2024 03:36:37 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 18 Jul 2024 03:36:37 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 18 Jul 2024 03:36:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Jul 2024 03:36:37 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 18 Jul 2024 03:36:37 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3429a1cddd18fe9063f1052d6a5d0d0b484806ff730aa3b5193912947afa7a`  
		Last Modified: Thu, 18 Jul 2024 18:55:52 GMT  
		Size: 51.1 MB (51131653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9675a6f6986eff3a7e462ebd98fd3aa7db7f832879db04aaf0656407005f4545`  
		Last Modified: Thu, 18 Jul 2024 18:55:50 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f777190bebba24315871617950d46dce88cac5610ba79f2eda6f59ab7f31e137`  
		Last Modified: Thu, 18 Jul 2024 18:55:50 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-7.1.0.3_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:089264e0f3fc0e2c163372043adce52ce9561392bfddd79ca6b9f6d9ae5ad3bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1970015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b013d95d0b121d6ff01bc250b1dcf6d9e18bec79cd64d800c9bea7c2fae2df74`

```dockerfile
```

-	Layers:
	-	`sha256:8c20976e6d1cca119e02c7884666a75b34fc1d0a7666be8bb06acab929c311bd`  
		Last Modified: Thu, 18 Jul 2024 18:55:50 GMT  
		Size: 1.9 MB (1941107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a9c2ab2b92c399aaf03b0d1487524a0acaf865a85c7908e326917c1999c560a`  
		Last Modified: Thu, 18 Jul 2024 18:55:50 GMT  
		Size: 28.9 KB (28908 bytes)  
		MIME: application/vnd.in-toto+json
