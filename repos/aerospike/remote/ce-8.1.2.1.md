## `aerospike:ce-8.1.2.1`

```console
$ docker pull aerospike@sha256:41b132562620a7e1ea240be3558e9c38988f3f971e4132c3fd6e81b9c6f56d09
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.1.2.1` - linux; amd64

```console
$ docker pull aerospike@sha256:24a89c37cb06b50ec4a27378ca80f0fddc1561e2a0a0ef6efebb2a1cad212d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131793826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec93151fff82f5c60eb4de5f7e0b252dd709b7d2c88f05cc2c447fb64cc7df8`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 13 May 2026 20:47:58 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Wed, 13 May 2026 20:47:58 GMT
ARG AEROSPIKE_EDITION=community
# Wed, 13 May 2026 20:47:58 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Wed, 13 May 2026 20:47:58 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Wed, 13 May 2026 20:47:58 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 20:48:10 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.1/aerospike-server-community_8.1.2.1_tools-13.0.0_ubuntu24.04_x86_64.tgz';         pkgSha='22350b57714fec888705d7dc9fa33e261e36d8dcd24b21d834652450b6009060';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.1/aerospike-server-community_8.1.2.1_tools-13.0.0_ubuntu24.04_aarch64.tgz';         pkgSha='41efbed30b36c9c710a1432939fafdfb413ce7eea4a55e1fbc08e3dea92d3be7';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Wed, 13 May 2026 20:48:10 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Wed, 13 May 2026 20:48:10 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Wed, 13 May 2026 20:48:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 13 May 2026 20:48:10 GMT
STOPSIGNAL SIGTERM
# Wed, 13 May 2026 20:48:10 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 13 May 2026 20:48:10 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d835b9daec529edb1e247b5ddbeac997558a802173f2c7f90394fee9483fd4f0`  
		Last Modified: Wed, 13 May 2026 20:48:25 GMT  
		Size: 1.1 MB (1050159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad077676e812541e7fba29435e52ab7e0ac4c9911511d94ee788c0c788a7b89`  
		Last Modified: Wed, 13 May 2026 20:48:28 GMT  
		Size: 101.0 MB (101008383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0021801082b153c3dc449697eded2ac3f72b1054d79f7b49a3c7dded1755c503`  
		Last Modified: Wed, 13 May 2026 20:48:25 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d9e0627423d0749f9fad466e4b4aba5a10a8ba9b7f1e4bcc7ce144ca3e796f`  
		Last Modified: Wed, 13 May 2026 20:48:25 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.2.1` - unknown; unknown

```console
$ docker pull aerospike@sha256:74bc1ddc5b253bdf99eefbfb9c4516764b30addc6d2f11588f1513481ac29139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2236791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b31485c52d2a1ca225159886db72be9fcb545cff0f6e20498602cea5cf7dc00f`

```dockerfile
```

-	Layers:
	-	`sha256:8115ac7f2122ec93190a1c95a2563af65edd7d0aa9e69f2acd3a2cfac3c19a6e`  
		Last Modified: Wed, 13 May 2026 20:48:25 GMT  
		Size: 2.2 MB (2215000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a27ead53be79fed44db71db93e3000428f5cc58202300c2fe72c4e564a972ac`  
		Last Modified: Wed, 13 May 2026 20:48:25 GMT  
		Size: 21.8 KB (21791 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.1.2.1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:a961e5c3217b0f83d6f911b17ae0187e677a3ee233fef78e66a0e098d75d1d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127914573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4618c3a191f611ddaed65c9e4d9fc69e90decea9352632142fe51a839f1aa1`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 13 May 2026 20:49:42 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Wed, 13 May 2026 20:49:42 GMT
ARG AEROSPIKE_EDITION=community
# Wed, 13 May 2026 20:49:42 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Wed, 13 May 2026 20:49:42 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Wed, 13 May 2026 20:49:42 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 20:50:03 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.1/aerospike-server-community_8.1.2.1_tools-13.0.0_ubuntu24.04_x86_64.tgz';         pkgSha='22350b57714fec888705d7dc9fa33e261e36d8dcd24b21d834652450b6009060';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.1/aerospike-server-community_8.1.2.1_tools-13.0.0_ubuntu24.04_aarch64.tgz';         pkgSha='41efbed30b36c9c710a1432939fafdfb413ce7eea4a55e1fbc08e3dea92d3be7';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Wed, 13 May 2026 20:50:03 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Wed, 13 May 2026 20:50:03 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Wed, 13 May 2026 20:50:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 13 May 2026 20:50:03 GMT
STOPSIGNAL SIGTERM
# Wed, 13 May 2026 20:50:03 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 13 May 2026 20:50:03 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18eac8f8d26b3babe0eab819d5f8db13bd79809192432dc29bf86aaf0560e177`  
		Last Modified: Wed, 13 May 2026 20:50:19 GMT  
		Size: 1.0 MB (1032395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31aca9c9aff6de9bcad4d46994a6e21b2922a24189ea8d59bf8e0c93d1ef4e80`  
		Last Modified: Wed, 13 May 2026 20:50:22 GMT  
		Size: 98.0 MB (98004088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c8f9a8211b2e55f4ec6cb2979ef31b4ad464b1afa54582bf65ed6f4e08537c`  
		Last Modified: Wed, 13 May 2026 20:50:19 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa41f42e5494c9a38c40427e49c57a1ffafce22e80ea7d05642acf8febd15907`  
		Last Modified: Wed, 13 May 2026 20:50:19 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.2.1` - unknown; unknown

```console
$ docker pull aerospike@sha256:1f10d5e71d1e8c9d396bb4c9ebada0128632e9d3cd5423888725f65f6055ce78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2237975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e055c0685588cc5c2e3e7952827086437e8e73845f3fa798a2f98d2ac738f5`

```dockerfile
```

-	Layers:
	-	`sha256:73f99e1d83023eeac41c039517d888e9891428f1e84b8571be727fe2ce7c74ff`  
		Last Modified: Wed, 13 May 2026 20:50:19 GMT  
		Size: 2.2 MB (2216092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f48f474ed22b8aceb4de761ae01326678013e60636d05bccbb68ef09bf75850`  
		Last Modified: Wed, 13 May 2026 20:50:19 GMT  
		Size: 21.9 KB (21883 bytes)  
		MIME: application/vnd.in-toto+json
