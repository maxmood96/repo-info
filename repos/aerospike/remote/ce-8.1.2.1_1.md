## `aerospike:ce-8.1.2.1_1`

```console
$ docker pull aerospike@sha256:0e512fb0a7235d6f9295e09d17e9de375e3959d6b308af836b5e782393fec4ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.1.2.1_1` - linux; amd64

```console
$ docker pull aerospike@sha256:7ef1b0b28a7bf1fdcca3ed79aacb265cf461548644124b7e228d342d6ef9a35a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131793800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c9cca98eaaddef9a18e600fcea295af0eae91af9081122f4f52382ee9fd4ee`
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
# Tue, 05 May 2026 20:44:03 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 05 May 2026 20:44:03 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 05 May 2026 20:44:03 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 05 May 2026 20:44:03 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 05 May 2026 20:44:03 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 20:44:15 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.1/aerospike-server-community_8.1.2.1_tools-13.0.0_ubuntu24.04_x86_64.tgz';         pkgSha='22350b57714fec888705d7dc9fa33e261e36d8dcd24b21d834652450b6009060';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.1/aerospike-server-community_8.1.2.1_tools-13.0.0_ubuntu24.04_aarch64.tgz';         pkgSha='41efbed30b36c9c710a1432939fafdfb413ce7eea4a55e1fbc08e3dea92d3be7';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Tue, 05 May 2026 20:44:15 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 05 May 2026 20:44:15 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 05 May 2026 20:44:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 05 May 2026 20:44:15 GMT
STOPSIGNAL SIGTERM
# Tue, 05 May 2026 20:44:15 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 05 May 2026 20:44:15 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e2a21155ed41d9d428ad3a2aeef0f2df8bbd7011c4a683d368413476f2d190`  
		Last Modified: Tue, 05 May 2026 20:44:32 GMT  
		Size: 1.1 MB (1050141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39073a212aa5fedf56c814175367fc8b2f5f4d1f439265dd9a203e513dc47b67`  
		Last Modified: Tue, 05 May 2026 20:44:35 GMT  
		Size: 101.0 MB (101008383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca84d452cdbea426ef3ef7c900700cbcfc1a1f55d38ff184beb010426b7c2a2e`  
		Last Modified: Tue, 05 May 2026 20:44:32 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67accf4eb0cf9f885d89146b836af947caeb9e28c6f6be35ebbf5399625047fd`  
		Last Modified: Tue, 05 May 2026 20:44:32 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.2.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:571695df3646dd224a0f42065c082e59aad4a02384891021cef78cac6c79e9c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2236797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9dbb89ccf4066ef998eabbbce9d1d002308adb218156f5701cb2dd8c43b251`

```dockerfile
```

-	Layers:
	-	`sha256:40918945971512c7cd9950dba0d4a2787c2eac69b38363db36c3ba7b0b5fdd45`  
		Last Modified: Tue, 05 May 2026 20:44:32 GMT  
		Size: 2.2 MB (2215000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:021f1e6a804a1e96b826fda28f5f0e59050802758becf93e817a8be6aa9ebed3`  
		Last Modified: Tue, 05 May 2026 20:44:32 GMT  
		Size: 21.8 KB (21797 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.1.2.1_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:d3217e2709b1ed7e40d47b89987e721532c5cede855c3d60ae118600f41f7e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127914616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ce3618ff92c2f9efbfe0e62473214fa7b2e8862969d0c647373c6c886d8796`
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
# Tue, 05 May 2026 20:43:58 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 05 May 2026 20:43:58 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 05 May 2026 20:43:58 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 05 May 2026 20:43:58 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 05 May 2026 20:43:58 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 20:44:15 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.1/aerospike-server-community_8.1.2.1_tools-13.0.0_ubuntu24.04_x86_64.tgz';         pkgSha='22350b57714fec888705d7dc9fa33e261e36d8dcd24b21d834652450b6009060';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.1/aerospike-server-community_8.1.2.1_tools-13.0.0_ubuntu24.04_aarch64.tgz';         pkgSha='41efbed30b36c9c710a1432939fafdfb413ce7eea4a55e1fbc08e3dea92d3be7';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Tue, 05 May 2026 20:44:15 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 05 May 2026 20:44:15 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 05 May 2026 20:44:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 05 May 2026 20:44:15 GMT
STOPSIGNAL SIGTERM
# Tue, 05 May 2026 20:44:15 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 05 May 2026 20:44:15 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1fd8ff4563cae0644e283b027afde65ad5f02a331d9da989315ddce7b521189`  
		Last Modified: Tue, 05 May 2026 20:44:31 GMT  
		Size: 1.0 MB (1032439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0b5e3522e517505c509a008dfe9fb1ef1c88937e40fa0bd3127c10c40e5955`  
		Last Modified: Tue, 05 May 2026 20:44:34 GMT  
		Size: 98.0 MB (98004091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8de801b8bc69ff91407cb3ee008a5821e66e3a9c109f3803fc5e3a7c22030e`  
		Last Modified: Tue, 05 May 2026 20:44:31 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bfc4d03885e946968b1d99d2036f065dbdd8d6ca1e281ef471997c7b154578`  
		Last Modified: Tue, 05 May 2026 20:44:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.2.1_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:d2b21721f0db514eb2bb57bdd6888d10cfbfdcec8aa494e5a6bc9fec3f65d42e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2237981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c1646964672b1f57eec4b12c9c42ce5c6f5c3ba957344c442585170b534006`

```dockerfile
```

-	Layers:
	-	`sha256:5050e7ec8d8463ad9e1ba55ff0cdeaf478645fabcbfddbe24e008017bb9d22f5`  
		Last Modified: Tue, 05 May 2026 20:44:31 GMT  
		Size: 2.2 MB (2216092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:848e78b4256fa2d4d6111c7d911327f3d19d36df5fcf23ef78738cd16a93f0e3`  
		Last Modified: Tue, 05 May 2026 20:44:31 GMT  
		Size: 21.9 KB (21889 bytes)  
		MIME: application/vnd.in-toto+json
