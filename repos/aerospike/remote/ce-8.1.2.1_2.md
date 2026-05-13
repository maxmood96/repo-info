## `aerospike:ce-8.1.2.1_2`

```console
$ docker pull aerospike@sha256:966e046f8522b02708705e7a3b13fa610934a8d000f21f653efc53b64a293ea6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.1.2.1_2` - linux; amd64

```console
$ docker pull aerospike@sha256:11e42e8bab36e9f1e21badd9c51f1d70615148ddfabbe9bed824580ebdc8da36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131793773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5665b1d3b938e6bb9b9a6622998f33a353ff0071746f098227694df48cae87`
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
# Wed, 13 May 2026 19:04:12 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Wed, 13 May 2026 19:04:12 GMT
ARG AEROSPIKE_EDITION=community
# Wed, 13 May 2026 19:04:12 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Wed, 13 May 2026 19:04:12 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Wed, 13 May 2026 19:04:12 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 19:04:26 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.1/aerospike-server-community_8.1.2.1_tools-13.0.0_ubuntu24.04_x86_64.tgz';         pkgSha='22350b57714fec888705d7dc9fa33e261e36d8dcd24b21d834652450b6009060';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.1/aerospike-server-community_8.1.2.1_tools-13.0.0_ubuntu24.04_aarch64.tgz';         pkgSha='41efbed30b36c9c710a1432939fafdfb413ce7eea4a55e1fbc08e3dea92d3be7';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Wed, 13 May 2026 19:04:26 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Wed, 13 May 2026 19:04:26 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Wed, 13 May 2026 19:04:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 13 May 2026 19:04:26 GMT
STOPSIGNAL SIGTERM
# Wed, 13 May 2026 19:04:26 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 13 May 2026 19:04:26 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c51e9a9f715a472ce3c90bf23e0e5333fec02364f1c030569a0538094ddeb68`  
		Last Modified: Wed, 13 May 2026 19:04:43 GMT  
		Size: 1.1 MB (1050154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a46ca13304bca4f818392a96561f6b97a18eb954b67589e4bcd031ef424b90c`  
		Last Modified: Wed, 13 May 2026 19:04:46 GMT  
		Size: 101.0 MB (101008343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc2d8ae0053a964bb5f6be347aad1744a024e914cd070e68bb849ac996e9c21`  
		Last Modified: Wed, 13 May 2026 19:04:43 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d2923586d9528c8ce0bf4e3825d9b69e868c744b89626ab8e47da322f9c003`  
		Last Modified: Wed, 13 May 2026 19:04:43 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.2.1_2` - unknown; unknown

```console
$ docker pull aerospike@sha256:299bb0260539b294e651cc4ee9ec55ebdecba81b93f090b997e56c89360b7e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2236791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:214750178905b128c3f2df115398e5531ccc2c2ab0a129e574ba9f4ea0f67183`

```dockerfile
```

-	Layers:
	-	`sha256:484b9f022f13ffe5dfdab4845fb17dceabff227389624e4ce62b64d3a28ed3cb`  
		Last Modified: Wed, 13 May 2026 19:04:43 GMT  
		Size: 2.2 MB (2215000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3fb94d9aa940f418e20fe8c1651c676def56c80da4dfcf5801a2a9f52f2c22c`  
		Last Modified: Wed, 13 May 2026 19:04:43 GMT  
		Size: 21.8 KB (21791 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.1.2.1_2` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:8d95b9a48374918360b5e8571b4138cfcd85a3e24b3faf4c59f054f5e37df76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127914552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a641166e030b9b9eab2b89de59c23a0cba87e16590c53ebab714e3913288e7d9`
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
# Wed, 13 May 2026 19:03:50 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Wed, 13 May 2026 19:03:50 GMT
ARG AEROSPIKE_EDITION=community
# Wed, 13 May 2026 19:03:50 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Wed, 13 May 2026 19:03:50 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Wed, 13 May 2026 19:03:50 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 19:04:08 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.1/aerospike-server-community_8.1.2.1_tools-13.0.0_ubuntu24.04_x86_64.tgz';         pkgSha='22350b57714fec888705d7dc9fa33e261e36d8dcd24b21d834652450b6009060';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.1/aerospike-server-community_8.1.2.1_tools-13.0.0_ubuntu24.04_aarch64.tgz';         pkgSha='41efbed30b36c9c710a1432939fafdfb413ce7eea4a55e1fbc08e3dea92d3be7';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Wed, 13 May 2026 19:04:08 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Wed, 13 May 2026 19:04:08 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Wed, 13 May 2026 19:04:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 13 May 2026 19:04:08 GMT
STOPSIGNAL SIGTERM
# Wed, 13 May 2026 19:04:08 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 13 May 2026 19:04:08 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b110d8d61b87f1533afb1da25321bdc862d575416fb04a0f4644d5f2514352fc`  
		Last Modified: Wed, 13 May 2026 19:04:24 GMT  
		Size: 1.0 MB (1032421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6008345ae59a62671b0dca7f0bdc2e8838bbba783607345bdd7cb4fe99e8a1`  
		Last Modified: Wed, 13 May 2026 19:04:27 GMT  
		Size: 98.0 MB (98004045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143ed15837d2986773d268b0c2f4927e709dfc8cb11c0ebf7d23213957e6937f`  
		Last Modified: Wed, 13 May 2026 19:04:24 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a7f7e9855feeba36e6f4ba8eb96e4cabe2e3f10d38936e2347d6b322e3b800`  
		Last Modified: Wed, 13 May 2026 19:04:24 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.2.1_2` - unknown; unknown

```console
$ docker pull aerospike@sha256:6620a9aba8ebcd0424f9c86b730d5c53f37d8e52db487cf6339fc6a165a11ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2237975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7127ba7788824bd91b238b31fece8f4aae3d9f48e50a885d85d24df00c3bc286`

```dockerfile
```

-	Layers:
	-	`sha256:dbe4c0240d79e4f75019ced9f95e39503b0509503c8b6375bb33d64bda4ecb30`  
		Last Modified: Wed, 13 May 2026 19:04:24 GMT  
		Size: 2.2 MB (2216092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d000a78b441c7f84501d5fc1c5b35654f92ac8008df8c62ed85bb3cf03cfdef`  
		Last Modified: Wed, 13 May 2026 19:04:24 GMT  
		Size: 21.9 KB (21883 bytes)  
		MIME: application/vnd.in-toto+json
