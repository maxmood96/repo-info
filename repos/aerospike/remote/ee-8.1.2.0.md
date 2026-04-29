## `aerospike:ee-8.1.2.0`

```console
$ docker pull aerospike@sha256:abc5dac5a0cd56d9812cf77f8751ef5855b304265383ba4e929ebc18f4157dce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.1.2.0` - linux; amd64

```console
$ docker pull aerospike@sha256:a081991b7c0cff8f55e413e30d240ef0ba8f587471286d1552184e331fe2db12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136150837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5eabfdbfa374a39bf409909221c30c321579f169ab9b4d97777ec79321004e`
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
# Tue, 28 Apr 2026 20:34:06 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.0 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 28 Apr 2026 20:34:06 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 28 Apr 2026 20:34:06 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 28 Apr 2026 20:34:06 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 28 Apr 2026 20:34:06 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 20:34:23 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.0/aerospike-server-enterprise_8.1.2.0_tools-13.0.0_ubuntu24.04_x86_64.tgz';         pkgSha='64397bf042e12c52c9e06189a5fbad86efb7d5c405ba1a4736b55d8ab5ee18b8';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.0/aerospike-server-enterprise_8.1.2.0_tools-13.0.0_ubuntu24.04_aarch64.tgz';         pkgSha='30ebebdd07fe0b7a924433dfde3d6dce6d8fe0841a47cdcf427b14162d83e087';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Tue, 28 Apr 2026 20:34:23 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 28 Apr 2026 20:34:23 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 28 Apr 2026 20:34:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 28 Apr 2026 20:34:23 GMT
STOPSIGNAL SIGTERM
# Tue, 28 Apr 2026 20:34:23 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 28 Apr 2026 20:34:23 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1475438b6d30859f4f37d994fb0af579080c2be2e63e4d0ae1a3fe219cb7c81d`  
		Last Modified: Tue, 28 Apr 2026 20:34:39 GMT  
		Size: 1.1 MB (1050156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0a80e669a2cae94a8cbaa14792a67708713a6091c165d98ff0209b29d1b225`  
		Last Modified: Tue, 28 Apr 2026 20:34:42 GMT  
		Size: 105.4 MB (105365403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd745ecf5078619d41ab93484eecc5c003ee5bbbf4c458db8b9a0cc87f6f376`  
		Last Modified: Tue, 28 Apr 2026 20:34:39 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f5e02e979ee62b514610f0e6ca6f8c0e4d21c25ca75529af37d1186dfaf65`  
		Last Modified: Tue, 28 Apr 2026 20:34:39 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.2.0` - unknown; unknown

```console
$ docker pull aerospike@sha256:59313ed49bd3135853ebf771b97275134e6643bafbc9d946a64b0d4f9922528f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2337878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8587c7695c660283a9443cf7385a45d1aa75712b71596b8732acccfc325d1f2d`

```dockerfile
```

-	Layers:
	-	`sha256:1728f087e559174647376b5dcf0d4d70c92eeb83d8669465f46c14a08738af79`  
		Last Modified: Tue, 28 Apr 2026 20:34:40 GMT  
		Size: 2.3 MB (2316064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bfc54213742a727b5319fc1f63a79cbe9350307b3725997fded37e0d792c3d9`  
		Last Modified: Tue, 28 Apr 2026 20:34:39 GMT  
		Size: 21.8 KB (21814 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.1.2.0` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:ba874b287532b156bfbfd368047b4c96eef5ef8e38d1945b764bf0e8c0137574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132305127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc6165eb24f3d9178f23e1c75442727c9a46945152de9a1fb0a3dee5ee1ecc47`
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
# Tue, 28 Apr 2026 20:33:54 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.0 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 28 Apr 2026 20:33:54 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 28 Apr 2026 20:33:54 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 28 Apr 2026 20:33:54 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 28 Apr 2026 20:33:54 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 20:34:13 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.0/aerospike-server-enterprise_8.1.2.0_tools-13.0.0_ubuntu24.04_x86_64.tgz';         pkgSha='64397bf042e12c52c9e06189a5fbad86efb7d5c405ba1a4736b55d8ab5ee18b8';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.0/aerospike-server-enterprise_8.1.2.0_tools-13.0.0_ubuntu24.04_aarch64.tgz';         pkgSha='30ebebdd07fe0b7a924433dfde3d6dce6d8fe0841a47cdcf427b14162d83e087';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Tue, 28 Apr 2026 20:34:13 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 28 Apr 2026 20:34:13 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 28 Apr 2026 20:34:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 28 Apr 2026 20:34:13 GMT
STOPSIGNAL SIGTERM
# Tue, 28 Apr 2026 20:34:13 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 28 Apr 2026 20:34:13 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83688a58083e5cb7f480ca91dbdfcc52f18fe22f96b05079eb8e794f26da2031`  
		Last Modified: Tue, 28 Apr 2026 20:34:30 GMT  
		Size: 1.0 MB (1032417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1fe71e14355c123163263cc17ea52eb31231f7fd81819d62c9f5002188298f1`  
		Last Modified: Tue, 28 Apr 2026 20:34:32 GMT  
		Size: 102.4 MB (102394626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df0c5b06d60235b99bf8362fbd3fa9c9ce9151c18c370c13a0dc6b38f974961`  
		Last Modified: Tue, 28 Apr 2026 20:34:29 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3b769d08f50270632b9d2ea5cafda417c8426b1a57374cd9a916633d2e572c`  
		Last Modified: Tue, 28 Apr 2026 20:34:29 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.2.0` - unknown; unknown

```console
$ docker pull aerospike@sha256:cff9c54333d021140ac3c8f7a730361575ca95c72a0d5366ca7278b90a8df260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2339083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092c0e057245d68eb7afc4b5f10bcffc11804f25936f0516b50f18901411ef95`

```dockerfile
```

-	Layers:
	-	`sha256:894d7a6242615fdc1a8924302a2ad141ef70242543808b46c84c4e6f1c13157b`  
		Last Modified: Tue, 28 Apr 2026 20:34:29 GMT  
		Size: 2.3 MB (2317174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57cfb87075d0d3431f50f60f8137c61087195eea2ae858046d7795064f8bd654`  
		Last Modified: Tue, 28 Apr 2026 20:34:29 GMT  
		Size: 21.9 KB (21909 bytes)  
		MIME: application/vnd.in-toto+json
