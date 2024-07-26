## `aerospike:ce-7.1.0.4_1`

```console
$ docker pull aerospike@sha256:9db550e16bcfe787ca194208ae32bda77b9cb47a6d48e98aad21b88fc748c4e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `aerospike:ce-7.1.0.4_1` - linux; amd64

```console
$ docker pull aerospike@sha256:4600d37d5a19a7ee48ed2ce5744cfc33c47d5496d5c3024fc503ef4311716427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77365967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac026d95dd87a39d3315e611b583d04dbc29fac5e7784cdab1a3881f57114005`
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
# Thu, 25 Jul 2024 02:10:16 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:22.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=7.1.0.4 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 25 Jul 2024 02:10:16 GMT
ARG AEROSPIKE_EDITION=community
# Thu, 25 Jul 2024 02:10:16 GMT
ARG AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.4/aerospike-server-community_7.1.0.4_tools-11.0.2_ubuntu22.04_x86_64.tgz
# Thu, 25 Jul 2024 02:10:16 GMT
ARG AEROSPIKE_SHA_X86_64=57095d4300357664e1c4947bdb81fb0fff0d1a740cb4809491f314b787d02af1
# Thu, 25 Jul 2024 02:10:16 GMT
ARG AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.4/aerospike-server-community_7.1.0.4_tools-11.0.2_ubuntu22.04_aarch64.tgz
# Thu, 25 Jul 2024 02:10:16 GMT
ARG AEROSPIKE_SHA_AARCH64=626d96783d7cff2baceb27286d2765ae846b07faf06d073fa98519f47207bbd3
# Thu, 25 Jul 2024 02:10:16 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 25 Jul 2024 02:10:16 GMT
# ARGS: AEROSPIKE_EDITION=community AEROSPIKE_X86_64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.4/aerospike-server-community_7.1.0.4_tools-11.0.2_ubuntu22.04_x86_64.tgz AEROSPIKE_SHA_X86_64=57095d4300357664e1c4947bdb81fb0fff0d1a740cb4809491f314b787d02af1 AEROSPIKE_AARCH64_LINK=https://artifacts.aerospike.com/aerospike-server-community/7.1.0.4/aerospike-server-community_7.1.0.4_tools-11.0.2_ubuntu22.04_aarch64.tgz AEROSPIKE_SHA_AARCH64=626d96783d7cff2baceb27286d2765ae846b07faf06d073fa98519f47207bbd3
RUN {     export DEBIAN_FRONTEND=noninteractive;     apt-get update -y;     apt-get install -y --no-install-recommends apt-utils;     apt-get install -y --no-install-recommends       binutils       ca-certificates       curl       xz-utils;   };   {     apt-get install -y --no-install-recommends procps;   };   {     VERSION="$(grep -oE "/[0-9]+[.][0-9]+[.][0-9]+([.][0-9]+)+(-rc[0-9]+)?([-][0-9]+[-]g[0-9a-z]*)?/" <<<"${AEROSPIKE_X86_64_LINK}" | tr -d '/' | tail -1)";   };   {     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then       sha256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940;       suffix="";     elif [ "${ARCH}" = "arm64" ]; then       sha256=1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b;       suffix="-arm64";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     curl -fsSL "https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static${suffix}" --output /usr/bin/as-tini-static;     echo "${sha256} /usr/bin/as-tini-static" | sha256sum -c -;     chmod +x /usr/bin/as-tini-static;   };   {     ARCH="$(dpkg --print-architecture)";     mkdir -p aerospike/pkg;     if [ "${ARCH}" = "amd64" ]; then       pkg_link="${AEROSPIKE_X86_64_LINK}";       sha256="${AEROSPIKE_SHA_X86_64}";     elif [ "${ARCH}" = "arm64" ]; then       pkg_link="${AEROSPIKE_AARCH64_LINK}";       sha256="${AEROSPIKE_SHA_AARCH64}";     else       echo "Unsuported architecture - ${ARCH}" >&2;       exit 1;     fi;     if ! curl -fsSL "${pkg_link}" --output aerospike-server.tgz; then       echo "Could not fetch pkg - ${pkg_link}" >&2;       exit 1;     fi;     echo "${sha256} aerospike-server.tgz" | sha256sum -c -;     tar xzf aerospike-server.tgz --strip-components=1 -C aerospike;     rm aerospike-server.tgz;     mkdir -p /var/{log,run}/aerospike;     mkdir -p /licenses;     cp aerospike/LICENSE /licenses;   };   {     if [ "${AEROSPIKE_EDITION}" = "enterprise" ]; then       apt-get install -y --no-install-recommends         libcurl4         libldap-2.4.2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.0" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         libcurl4;     fi;     dpkg -i aerospike/aerospike-server-*.deb;     rm -rf /opt/aerospike/bin;   };   {     if ! [ "$(printf "%s\n%s" "${VERSION}" "5.1" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python2;     elif ! [ "$(printf "%s\n%s" "${VERSION}" "6.2.0.3" | sort -V | head -1)" != "${VERSION}" ]; then       apt-get install -y --no-install-recommends         python3         python3-distutils;     fi;   };   {     ar -x aerospike/aerospike-tools*.deb --output aerospike/pkg;     tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/;   };   {     find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +;     mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike;     if ! [ "$(printf "%s\n%s" "${VERSION}" "6.2" | sort -V | head -1)" != "${VERSION}" ]; then        mv aerospike/pkg/opt/aerospike/bin/aql /usr/bin;     fi;     if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     else       mkdir /usr/lib/asadm;       mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f 'aerospike/pkg/opt/aerospike/bin/asinfo' ]; then       mv aerospike/pkg/opt/aerospike/bin/asinfo /usr/lib/asadm/;     fi;     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;   };   {     rm -rf aerospike;   };   {     rm -rf /var/lib/apt/lists/*;     dpkg --purge       apt-utils       binutils       ca-certificates       curl       xz-utils 2>&1;     apt-get purge -y;     apt-get autoremove -y;     unset DEBIAN_FRONTEND;   };   echo "done"; # buildkit
# Thu, 25 Jul 2024 02:10:16 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 25 Jul 2024 02:10:16 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 25 Jul 2024 02:10:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Jul 2024 02:10:16 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 25 Jul 2024 02:10:16 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97104dbfe31b504d0e082c80a35d38b1ad36987a59100c98d8dfb8f352b606ae`  
		Last Modified: Thu, 25 Jul 2024 20:08:38 GMT  
		Size: 47.8 MB (47829625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacdf59daeff2437a6de02a63a859f13ca9b816236bcce0715a45551d7d541a6`  
		Last Modified: Thu, 25 Jul 2024 20:08:37 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496ab79783122062329bb3338eb7e388390dcd72e060c37b1b39e53fe5e7ee00`  
		Last Modified: Thu, 25 Jul 2024 20:08:37 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-7.1.0.4_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:b14cee8b198b8d11abe6bfd9b09354a14cf6a4aa5eef9c2c74c4f37cbac6ca81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1905580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785fea1133452254410dfa533c3a043629b7ce4cd5b93c3922a408f142804a9e`

```dockerfile
```

-	Layers:
	-	`sha256:63dbbe764e724a0e85e8c7a08d29a0ca2fd1301217e3aceeae199452458b0e87`  
		Last Modified: Thu, 25 Jul 2024 20:08:37 GMT  
		Size: 1.9 MB (1876690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6452fe1ec3813dc55b3fcebd8762077f6a6212993a843f7ea7ca85e9c58c21c5`  
		Last Modified: Thu, 25 Jul 2024 20:08:37 GMT  
		Size: 28.9 KB (28890 bytes)  
		MIME: application/vnd.in-toto+json
