## `aerospike:ee-8.1.2.1_3`

```console
$ docker pull aerospike@sha256:9f68bb0ab82960b7bdb6f2bcc8921d1529461d9c34b235915d55fe23e0de27ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.1.2.1_3` - linux; amd64

```console
$ docker pull aerospike@sha256:4cfce48c4d4978d3e8a7dddf7a797f248e28f92166f38d63759dd590ed259355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136152579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:334eb9766780542807c3787ad4901c6af2816e63136b95a450174757ef9a2b06`
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
# Wed, 13 May 2026 20:47:54 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Wed, 13 May 2026 20:47:54 GMT
ARG AEROSPIKE_EDITION=enterprise
# Wed, 13 May 2026 20:47:54 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Wed, 13 May 2026 20:47:54 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Wed, 13 May 2026 20:47:54 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 20:48:07 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.1/aerospike-server-enterprise_8.1.2.1_tools-13.0.0_ubuntu24.04_x86_64.tgz';         pkgSha='299916965c5a9959f4159e2b3ba36e55b64bdb63910654735ea96d65e4a38179';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.1/aerospike-server-enterprise_8.1.2.1_tools-13.0.0_ubuntu24.04_aarch64.tgz';         pkgSha='22fa2cec34972bdb9c73c2c3577ba80bb0555855280b6161e6f96d0944503c3c';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Wed, 13 May 2026 20:48:07 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Wed, 13 May 2026 20:48:07 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Wed, 13 May 2026 20:48:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 13 May 2026 20:48:07 GMT
STOPSIGNAL SIGTERM
# Wed, 13 May 2026 20:48:07 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 13 May 2026 20:48:07 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492e292359928806cdb42331d48e29c9084824bbefc76c67f1b3ecf6c82c78ed`  
		Last Modified: Wed, 13 May 2026 20:48:23 GMT  
		Size: 1.1 MB (1050161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc52a0361e44e2819773eca1a303bb88944ae3808fed41c39836cf79d4af2b6c`  
		Last Modified: Wed, 13 May 2026 20:48:26 GMT  
		Size: 105.4 MB (105367136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e012b68af67bbb1a20f1b5edbdf7d27047bf2476897f3ad55f2c2f8e8ace927`  
		Last Modified: Wed, 13 May 2026 20:48:23 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7133d9074630346a8c0ab0cca18e14ee5ddd09021ed633fbb630916b08bea51`  
		Last Modified: Wed, 13 May 2026 20:48:23 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.2.1_3` - unknown; unknown

```console
$ docker pull aerospike@sha256:95d327eb23c7810abf7ccef7983ab068e2c81c8fff16bd1a67e66dd6ee5391d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2337872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec62e68a44f772f1b2f6a22a051f1377e29c1b2a13531bf3d2ef7b5c34a7515`

```dockerfile
```

-	Layers:
	-	`sha256:c5f180b5259e5d076b2ad08f1e13ec23a7e248f2c81091598d17aed78b3da4c1`  
		Last Modified: Wed, 13 May 2026 20:48:23 GMT  
		Size: 2.3 MB (2316064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9f79ffeea7304a2a043913fdd910310fda7e1e2782e94b7273bd91fe18f0b9a`  
		Last Modified: Wed, 13 May 2026 20:48:23 GMT  
		Size: 21.8 KB (21808 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.1.2.1_3` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:2fa9a59a9711e65ade1485b134b26fd4e21e5192abeaf4139ad7ed138ae17236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132307962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1651b9991e394b3467ef658a751fa2e078f8927eaa7dcd244753000c1943d9b0`
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
# Wed, 13 May 2026 20:48:46 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Wed, 13 May 2026 20:48:46 GMT
ARG AEROSPIKE_EDITION=enterprise
# Wed, 13 May 2026 20:48:46 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Wed, 13 May 2026 20:48:46 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Wed, 13 May 2026 20:48:46 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 20:49:07 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.1/aerospike-server-enterprise_8.1.2.1_tools-13.0.0_ubuntu24.04_x86_64.tgz';         pkgSha='299916965c5a9959f4159e2b3ba36e55b64bdb63910654735ea96d65e4a38179';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.1/aerospike-server-enterprise_8.1.2.1_tools-13.0.0_ubuntu24.04_aarch64.tgz';         pkgSha='22fa2cec34972bdb9c73c2c3577ba80bb0555855280b6161e6f96d0944503c3c';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Wed, 13 May 2026 20:49:07 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Wed, 13 May 2026 20:49:07 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Wed, 13 May 2026 20:49:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 13 May 2026 20:49:07 GMT
STOPSIGNAL SIGTERM
# Wed, 13 May 2026 20:49:07 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 13 May 2026 20:49:07 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c711ef33fafbf85df8f73430f4bb952de824c76a205a95fdcd0f8dcce7b2cd28`  
		Last Modified: Wed, 13 May 2026 20:49:24 GMT  
		Size: 1.0 MB (1032405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981daf888fdf3878f8a68978519f5a602cfc43f7d9da21db65e18e225ace1a72`  
		Last Modified: Wed, 13 May 2026 20:49:26 GMT  
		Size: 102.4 MB (102397465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d15aa6964c73e1aaaedf0ea83eeab45bf09df2272ee7faa0853e3c5c0bc40e6`  
		Last Modified: Wed, 13 May 2026 20:49:23 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf017655c9f8994b979dfdaf20394e9da496e8ca6d2f63037c23fecfc3b406e7`  
		Last Modified: Wed, 13 May 2026 20:49:24 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.2.1_3` - unknown; unknown

```console
$ docker pull aerospike@sha256:ee32f3e0b04fe51c0f6bb1c8c39814e1ae69f5c560cdeee1c552f22329957423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2339077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae63c74870778c4fd9a6d3f71c65e60ce705d0a768cf0302e0b16ffff2b42839`

```dockerfile
```

-	Layers:
	-	`sha256:b3a966c8dd3c9705518cfa77f685221e445c924ff4cc76c9dd8c3d848b07d8ac`  
		Last Modified: Wed, 13 May 2026 20:49:24 GMT  
		Size: 2.3 MB (2317174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06bf94bc7da71d3ca79bcbc3d2c6c0f555ffbc4fc87182457b13884d0c4b88cc`  
		Last Modified: Wed, 13 May 2026 20:49:23 GMT  
		Size: 21.9 KB (21903 bytes)  
		MIME: application/vnd.in-toto+json
