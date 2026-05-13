## `aerospike:ee-8.1.2.1_2`

```console
$ docker pull aerospike@sha256:3071f77205336879ed2992688804368322a3bcab843c9a19772c417746f7225a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.1.2.1_2` - linux; amd64

```console
$ docker pull aerospike@sha256:d90161f19dad1174ddac44d425723c9f3a6b42c10bc5be8d2dae326fc306f7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136152504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b84f32247b6949182285378104f22afc81a19b2c047f793f5c7922e4e0fb0ca`
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
# Wed, 13 May 2026 19:03:16 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Wed, 13 May 2026 19:03:16 GMT
ARG AEROSPIKE_EDITION=enterprise
# Wed, 13 May 2026 19:03:16 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Wed, 13 May 2026 19:03:16 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Wed, 13 May 2026 19:03:16 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 19:03:34 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.1/aerospike-server-enterprise_8.1.2.1_tools-13.0.0_ubuntu24.04_x86_64.tgz';         pkgSha='299916965c5a9959f4159e2b3ba36e55b64bdb63910654735ea96d65e4a38179';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.1/aerospike-server-enterprise_8.1.2.1_tools-13.0.0_ubuntu24.04_aarch64.tgz';         pkgSha='22fa2cec34972bdb9c73c2c3577ba80bb0555855280b6161e6f96d0944503c3c';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Wed, 13 May 2026 19:03:34 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Wed, 13 May 2026 19:03:34 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Wed, 13 May 2026 19:03:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 13 May 2026 19:03:34 GMT
STOPSIGNAL SIGTERM
# Wed, 13 May 2026 19:03:34 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 13 May 2026 19:03:34 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa77eb59bbce749f2b2b945a8c4f3df1033ca04b86a37953408e92d1c46b6dd`  
		Last Modified: Wed, 13 May 2026 19:03:53 GMT  
		Size: 1.1 MB (1050125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c283f82a31076446fa3feebabbe9e4dd04de5b0d97cf2d605b62ffc9b5ef94`  
		Last Modified: Wed, 13 May 2026 19:03:56 GMT  
		Size: 105.4 MB (105367100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7074b454a99d54233e96bacf04cf02d8a2d5684ff8bf38a5c3578f55a7a5bde8`  
		Last Modified: Wed, 13 May 2026 19:03:53 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3a75b25ebc3a9284eda6c71d9639e9d47e44d24634fd1a7a056aab18311ffe`  
		Last Modified: Wed, 13 May 2026 19:03:53 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.2.1_2` - unknown; unknown

```console
$ docker pull aerospike@sha256:21b6f880544a6491f4a07cfa5c34e6966bb92f41a4f8ca84955cd0d3f91ff9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2337872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98128a9be4440a001e34a2bfdb55fad6cb0ab4bd7d8037bc145cca1f35c4e6d5`

```dockerfile
```

-	Layers:
	-	`sha256:20d5e863d334fd57dbf2e0cab5a45e474d2dd35a9b7c35b05cc6412afe29226e`  
		Last Modified: Wed, 13 May 2026 19:03:53 GMT  
		Size: 2.3 MB (2316064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d9957f7de3a48f03475f8c345c606a68eb3816c2cbede31c811d5aeb74bb4b4`  
		Last Modified: Wed, 13 May 2026 19:03:53 GMT  
		Size: 21.8 KB (21808 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.1.2.1_2` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:dd6bf74101b61dcf2711c3b29292e8ef05de9d7bcc1fff08c3aed8749a551920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132308026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3c5f487b2b994dea01c205024dadbdae5e98a4e71ae3e7b4abbc81c424ab2d`
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
# Wed, 13 May 2026 19:02:54 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Wed, 13 May 2026 19:02:54 GMT
ARG AEROSPIKE_EDITION=enterprise
# Wed, 13 May 2026 19:02:54 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Wed, 13 May 2026 19:02:54 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Wed, 13 May 2026 19:02:54 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 19:03:13 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.1/aerospike-server-enterprise_8.1.2.1_tools-13.0.0_ubuntu24.04_x86_64.tgz';         pkgSha='299916965c5a9959f4159e2b3ba36e55b64bdb63910654735ea96d65e4a38179';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.1/aerospike-server-enterprise_8.1.2.1_tools-13.0.0_ubuntu24.04_aarch64.tgz';         pkgSha='22fa2cec34972bdb9c73c2c3577ba80bb0555855280b6161e6f96d0944503c3c';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Wed, 13 May 2026 19:03:13 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Wed, 13 May 2026 19:03:13 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Wed, 13 May 2026 19:03:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 13 May 2026 19:03:13 GMT
STOPSIGNAL SIGTERM
# Wed, 13 May 2026 19:03:13 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 13 May 2026 19:03:13 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2674ebc5b27386af3d6ff2e068eaaad90e12678e30819f66cc5098394239bf36`  
		Last Modified: Wed, 13 May 2026 19:03:29 GMT  
		Size: 1.0 MB (1032415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1c3299171394e738561d826f815aa68f6a3549074e1b3c127afd8c2c747e2c`  
		Last Modified: Wed, 13 May 2026 19:03:32 GMT  
		Size: 102.4 MB (102397525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e563d556d71dac53f8edb0b6da9d536e02b23669d16638b2c93021c04cdc4e18`  
		Last Modified: Wed, 13 May 2026 19:03:29 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb90ed2018efeeaba269aeae3e2b795f8ceedf44f8851c2389b24051fdfb71e2`  
		Last Modified: Wed, 13 May 2026 19:03:29 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.2.1_2` - unknown; unknown

```console
$ docker pull aerospike@sha256:93a447a032df4056851d619c9061b4244c9072497638cd2f79ddb35e723853f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2339077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a35d20a8f9b1b9022948fd742cc861110d5bc81752d6027f0af4842513934c9`

```dockerfile
```

-	Layers:
	-	`sha256:3a255e921fe5d70a6b6d7fe4cfafded011b46ee1e16be005a99dfdca0cd0043f`  
		Last Modified: Wed, 13 May 2026 19:03:30 GMT  
		Size: 2.3 MB (2317174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81da136ee719876ce052ebc7082a530efb3bd6af65f17e39387452d1ca267057`  
		Last Modified: Wed, 13 May 2026 19:03:29 GMT  
		Size: 21.9 KB (21903 bytes)  
		MIME: application/vnd.in-toto+json
