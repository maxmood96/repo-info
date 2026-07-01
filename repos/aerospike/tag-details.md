<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-8.1.2.3`](#aerospikece-8123)
-	[`aerospike:ce-8.1.2.3_1`](#aerospikece-8123_1)
-	[`aerospike:ee-8.1.2.3`](#aerospikeee-8123)
-	[`aerospike:ee-8.1.2.3_1`](#aerospikeee-8123_1)

## `aerospike:ce-8.1.2.3`

```console
$ docker pull aerospike@sha256:b90f34b998851acd1a96c7b2b3931adef9dbce7a9766fb177c0918b9f195e27f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.1.2.3` - linux; amd64

```console
$ docker pull aerospike@sha256:58f6ffe5cc070726a977552ad2aa003992bd67b9425d7087627db4f079eeef26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136683158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39af118d206b6793f746bb6c3763559f2a3732d6465137d75b68b141fbeaf99e`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Wed, 01 Jul 2026 00:18:50 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.3 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Wed, 01 Jul 2026 00:18:50 GMT
ARG AEROSPIKE_EDITION=community
# Wed, 01 Jul 2026 00:18:50 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Wed, 01 Jul 2026 00:18:50 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Wed, 01 Jul 2026 00:18:50 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Jul 2026 00:19:01 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.3/aerospike-server-community_8.1.2.3_tools-13.0.1_ubuntu24.04_x86_64.tgz';         pkgSha='676cbf17e11f6f3919a27a693fc7d8129734ab4878c0b91990bd6d437eafa8dd';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.3/aerospike-server-community_8.1.2.3_tools-13.0.1_ubuntu24.04_aarch64.tgz';         pkgSha='19b380d17586f23b736e346a3855796a155a3e9f3bb242c5e8ec6622f6dc6744';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Wed, 01 Jul 2026 00:19:01 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Wed, 01 Jul 2026 00:19:01 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Wed, 01 Jul 2026 00:19:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Jul 2026 00:19:01 GMT
STOPSIGNAL SIGTERM
# Wed, 01 Jul 2026 00:19:01 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 01 Jul 2026 00:19:01 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ed9dd3812bae17dbe6892246be268d9db388dd4418094e7953674018c4fc96`  
		Last Modified: Wed, 01 Jul 2026 00:19:17 GMT  
		Size: 3.4 MB (3418118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd343dabf4632753bcf596d800c90d5c1d66c164f6a29345ef3825c92ee5bc3d`  
		Last Modified: Wed, 01 Jul 2026 00:19:20 GMT  
		Size: 103.5 MB (103529931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8cc6f5c6a6a0ddf628ac954e9bcf3f61437ee6ad49be61ac1779ff56191102`  
		Last Modified: Wed, 01 Jul 2026 00:19:16 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98eaab54413e0c820181fe9596f8506d6cdf02772dfca0db8cadfc48c46027c`  
		Last Modified: Wed, 01 Jul 2026 00:19:16 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.2.3` - unknown; unknown

```console
$ docker pull aerospike@sha256:61a809100a527473690792b74b4c3d22b47cbbd5d48b26bbffd063bbcf9fc114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2222040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d3cbf5d3429f6050f76505c78b7468b3c4188b7ef9b7ed8daad036a80cc261`

```dockerfile
```

-	Layers:
	-	`sha256:35d9737d894377288456c086f2c01fe5350928addb8947c0ab8ddfc585a6c921`  
		Last Modified: Wed, 01 Jul 2026 00:19:16 GMT  
		Size: 2.2 MB (2200243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3eee5ff03919bfc97e134d2078e0ce587eff556f98e1d28ad9d4c61ce5002a9a`  
		Last Modified: Wed, 01 Jul 2026 00:19:16 GMT  
		Size: 21.8 KB (21797 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.1.2.3` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:3e89be0a69cc987df2c77ec626a85787fb89a2c70e46ffa02f3bd443a168f28a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132714267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c70cda52804bd3602a6ecfee46f24b011276ce267a8026a7e8144503ace75b`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Wed, 01 Jul 2026 00:26:46 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.3 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Wed, 01 Jul 2026 00:26:46 GMT
ARG AEROSPIKE_EDITION=community
# Wed, 01 Jul 2026 00:26:46 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Wed, 01 Jul 2026 00:26:46 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Wed, 01 Jul 2026 00:26:46 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Jul 2026 00:26:58 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.3/aerospike-server-community_8.1.2.3_tools-13.0.1_ubuntu24.04_x86_64.tgz';         pkgSha='676cbf17e11f6f3919a27a693fc7d8129734ab4878c0b91990bd6d437eafa8dd';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.3/aerospike-server-community_8.1.2.3_tools-13.0.1_ubuntu24.04_aarch64.tgz';         pkgSha='19b380d17586f23b736e346a3855796a155a3e9f3bb242c5e8ec6622f6dc6744';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Wed, 01 Jul 2026 00:26:59 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Wed, 01 Jul 2026 00:26:59 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Wed, 01 Jul 2026 00:26:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Jul 2026 00:26:59 GMT
STOPSIGNAL SIGTERM
# Wed, 01 Jul 2026 00:26:59 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 01 Jul 2026 00:26:59 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04c1c7a9ba6aa38e93702ca0623de73b9bb1abe9bfd25eb369e538dd768f24c`  
		Last Modified: Wed, 01 Jul 2026 00:27:15 GMT  
		Size: 3.2 MB (3211918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b242bf7ca62fa33634c2adb90294ee17a9ec244c02689b33eb71f1b456f58e`  
		Last Modified: Wed, 01 Jul 2026 00:27:17 GMT  
		Size: 100.6 MB (100623635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d140a09f165e27632e73ebf7c6360cc5c04a780d02bf2e4554f9a06bd4e6ad59`  
		Last Modified: Wed, 01 Jul 2026 00:27:14 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989527cc352395090c465abed07279585c7ad1ccc9a3eb9be1b533ff5e49dc1f`  
		Last Modified: Wed, 01 Jul 2026 00:27:14 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.2.3` - unknown; unknown

```console
$ docker pull aerospike@sha256:40852db669b0cbbfde597c75e3e2f9dc3b5a26babfcfb42bc8a35d209f16f47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2223227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea9f001d3ee646293daca10749a535c06eafa69ce6c19003608c6f70def9817`

```dockerfile
```

-	Layers:
	-	`sha256:c4c6c9e866fb7ddbe0e5bf8f8436e09eda76e28862c5efff023539465ceacc64`  
		Last Modified: Wed, 01 Jul 2026 00:27:14 GMT  
		Size: 2.2 MB (2201335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d2e8f080a8e212b1169b169c24e527dd0919ff2d0aa1f8f50f814f197d4705`  
		Last Modified: Wed, 01 Jul 2026 00:27:14 GMT  
		Size: 21.9 KB (21892 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ce-8.1.2.3_1`

```console
$ docker pull aerospike@sha256:b90f34b998851acd1a96c7b2b3931adef9dbce7a9766fb177c0918b9f195e27f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.1.2.3_1` - linux; amd64

```console
$ docker pull aerospike@sha256:58f6ffe5cc070726a977552ad2aa003992bd67b9425d7087627db4f079eeef26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136683158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39af118d206b6793f746bb6c3763559f2a3732d6465137d75b68b141fbeaf99e`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Wed, 01 Jul 2026 00:18:50 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.3 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Wed, 01 Jul 2026 00:18:50 GMT
ARG AEROSPIKE_EDITION=community
# Wed, 01 Jul 2026 00:18:50 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Wed, 01 Jul 2026 00:18:50 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Wed, 01 Jul 2026 00:18:50 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Jul 2026 00:19:01 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.3/aerospike-server-community_8.1.2.3_tools-13.0.1_ubuntu24.04_x86_64.tgz';         pkgSha='676cbf17e11f6f3919a27a693fc7d8129734ab4878c0b91990bd6d437eafa8dd';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.3/aerospike-server-community_8.1.2.3_tools-13.0.1_ubuntu24.04_aarch64.tgz';         pkgSha='19b380d17586f23b736e346a3855796a155a3e9f3bb242c5e8ec6622f6dc6744';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Wed, 01 Jul 2026 00:19:01 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Wed, 01 Jul 2026 00:19:01 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Wed, 01 Jul 2026 00:19:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Jul 2026 00:19:01 GMT
STOPSIGNAL SIGTERM
# Wed, 01 Jul 2026 00:19:01 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 01 Jul 2026 00:19:01 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ed9dd3812bae17dbe6892246be268d9db388dd4418094e7953674018c4fc96`  
		Last Modified: Wed, 01 Jul 2026 00:19:17 GMT  
		Size: 3.4 MB (3418118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd343dabf4632753bcf596d800c90d5c1d66c164f6a29345ef3825c92ee5bc3d`  
		Last Modified: Wed, 01 Jul 2026 00:19:20 GMT  
		Size: 103.5 MB (103529931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8cc6f5c6a6a0ddf628ac954e9bcf3f61437ee6ad49be61ac1779ff56191102`  
		Last Modified: Wed, 01 Jul 2026 00:19:16 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98eaab54413e0c820181fe9596f8506d6cdf02772dfca0db8cadfc48c46027c`  
		Last Modified: Wed, 01 Jul 2026 00:19:16 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.2.3_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:61a809100a527473690792b74b4c3d22b47cbbd5d48b26bbffd063bbcf9fc114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2222040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d3cbf5d3429f6050f76505c78b7468b3c4188b7ef9b7ed8daad036a80cc261`

```dockerfile
```

-	Layers:
	-	`sha256:35d9737d894377288456c086f2c01fe5350928addb8947c0ab8ddfc585a6c921`  
		Last Modified: Wed, 01 Jul 2026 00:19:16 GMT  
		Size: 2.2 MB (2200243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3eee5ff03919bfc97e134d2078e0ce587eff556f98e1d28ad9d4c61ce5002a9a`  
		Last Modified: Wed, 01 Jul 2026 00:19:16 GMT  
		Size: 21.8 KB (21797 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.1.2.3_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:3e89be0a69cc987df2c77ec626a85787fb89a2c70e46ffa02f3bd443a168f28a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132714267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c70cda52804bd3602a6ecfee46f24b011276ce267a8026a7e8144503ace75b`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Wed, 01 Jul 2026 00:26:46 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.3 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Wed, 01 Jul 2026 00:26:46 GMT
ARG AEROSPIKE_EDITION=community
# Wed, 01 Jul 2026 00:26:46 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Wed, 01 Jul 2026 00:26:46 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Wed, 01 Jul 2026 00:26:46 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Jul 2026 00:26:58 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.3/aerospike-server-community_8.1.2.3_tools-13.0.1_ubuntu24.04_x86_64.tgz';         pkgSha='676cbf17e11f6f3919a27a693fc7d8129734ab4878c0b91990bd6d437eafa8dd';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.3/aerospike-server-community_8.1.2.3_tools-13.0.1_ubuntu24.04_aarch64.tgz';         pkgSha='19b380d17586f23b736e346a3855796a155a3e9f3bb242c5e8ec6622f6dc6744';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Wed, 01 Jul 2026 00:26:59 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Wed, 01 Jul 2026 00:26:59 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Wed, 01 Jul 2026 00:26:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Jul 2026 00:26:59 GMT
STOPSIGNAL SIGTERM
# Wed, 01 Jul 2026 00:26:59 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 01 Jul 2026 00:26:59 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04c1c7a9ba6aa38e93702ca0623de73b9bb1abe9bfd25eb369e538dd768f24c`  
		Last Modified: Wed, 01 Jul 2026 00:27:15 GMT  
		Size: 3.2 MB (3211918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b242bf7ca62fa33634c2adb90294ee17a9ec244c02689b33eb71f1b456f58e`  
		Last Modified: Wed, 01 Jul 2026 00:27:17 GMT  
		Size: 100.6 MB (100623635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d140a09f165e27632e73ebf7c6360cc5c04a780d02bf2e4554f9a06bd4e6ad59`  
		Last Modified: Wed, 01 Jul 2026 00:27:14 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989527cc352395090c465abed07279585c7ad1ccc9a3eb9be1b533ff5e49dc1f`  
		Last Modified: Wed, 01 Jul 2026 00:27:14 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.2.3_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:40852db669b0cbbfde597c75e3e2f9dc3b5a26babfcfb42bc8a35d209f16f47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2223227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea9f001d3ee646293daca10749a535c06eafa69ce6c19003608c6f70def9817`

```dockerfile
```

-	Layers:
	-	`sha256:c4c6c9e866fb7ddbe0e5bf8f8436e09eda76e28862c5efff023539465ceacc64`  
		Last Modified: Wed, 01 Jul 2026 00:27:14 GMT  
		Size: 2.2 MB (2201335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d2e8f080a8e212b1169b169c24e527dd0919ff2d0aa1f8f50f814f197d4705`  
		Last Modified: Wed, 01 Jul 2026 00:27:14 GMT  
		Size: 21.9 KB (21892 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ee-8.1.2.3`

```console
$ docker pull aerospike@sha256:27559feabace5d8c31b6d124c3ce6dc88b5c97e06cd5a74093ccbbd56641debb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.1.2.3` - linux; amd64

```console
$ docker pull aerospike@sha256:c34baaad25f08acaeead64ad93cfff428292fe6768ddf963506586317811c5f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141058152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190f99ccb4219b5d28cfd2b91cdf50cad9c866aa9f7a919a7e45e6097585ba1e`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Wed, 01 Jul 2026 00:18:53 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.3 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Wed, 01 Jul 2026 00:18:53 GMT
ARG AEROSPIKE_EDITION=enterprise
# Wed, 01 Jul 2026 00:18:53 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Wed, 01 Jul 2026 00:18:53 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Wed, 01 Jul 2026 00:18:53 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Jul 2026 00:19:05 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.3/aerospike-server-enterprise_8.1.2.3_tools-13.0.1_ubuntu24.04_x86_64.tgz';         pkgSha='e065f91d1d1acdc807f347b888b85ee9c6695f64b772b8455374fa492c8f59cd';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.3/aerospike-server-enterprise_8.1.2.3_tools-13.0.1_ubuntu24.04_aarch64.tgz';         pkgSha='80d193462128a70d43a37d716ca57f896ce3b6cf6dc95daec9a079f8338c3869';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Wed, 01 Jul 2026 00:19:05 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Wed, 01 Jul 2026 00:19:05 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Wed, 01 Jul 2026 00:19:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Jul 2026 00:19:05 GMT
STOPSIGNAL SIGTERM
# Wed, 01 Jul 2026 00:19:05 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 01 Jul 2026 00:19:05 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff28819c92c74e84dffa9b798fa2085d66ed01eeb29ef6761dfd6c886ddede2`  
		Last Modified: Wed, 01 Jul 2026 00:19:24 GMT  
		Size: 3.4 MB (3418135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad20f0e1a43456e7fe5450947c0d1127b62769e113c3dc96a3cefe2ca064c297`  
		Last Modified: Wed, 01 Jul 2026 00:19:26 GMT  
		Size: 107.9 MB (107904906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fc89011f85a4585a46280f2587db4499c68da4f0e5efb59a2d6742cf310f42`  
		Last Modified: Wed, 01 Jul 2026 00:19:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22ecc194881cc7a129c2e85b6471bc3994d43f70cb468a0e41e6f7ef072ae98`  
		Last Modified: Wed, 01 Jul 2026 00:19:23 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.2.3` - unknown; unknown

```console
$ docker pull aerospike@sha256:c2adbdffdc2ff55c84ea4757d1fb95a2b3a748976d3ddc67d1383e6b745a7c3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2323121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c9079bd6ca8a0cab960f5c05f24a7523917ce5d4e87074dc2d48398997b25fc`

```dockerfile
```

-	Layers:
	-	`sha256:16d6deb23596fbbcd880d6c40c09f8505189b7c5d8d4e0a608cb660451c38db0`  
		Last Modified: Wed, 01 Jul 2026 00:19:24 GMT  
		Size: 2.3 MB (2301307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ec8f68282590f28416b03559e9616cd6b94ba6dd982b21b5f68cd0d960a220c`  
		Last Modified: Wed, 01 Jul 2026 00:19:24 GMT  
		Size: 21.8 KB (21814 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.1.2.3` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:ba9bad82732dec92c5625fc9d35ca3b1f3f0b2c0138a19e98f1da9615ba17cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137121852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95c9f1b825a348e2c5e592da260f5030fd7ac11cc200f0d0e89a13388f32d8f`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Wed, 01 Jul 2026 00:26:40 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.3 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Wed, 01 Jul 2026 00:26:40 GMT
ARG AEROSPIKE_EDITION=enterprise
# Wed, 01 Jul 2026 00:26:40 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Wed, 01 Jul 2026 00:26:40 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Wed, 01 Jul 2026 00:26:40 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Jul 2026 00:26:53 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.3/aerospike-server-enterprise_8.1.2.3_tools-13.0.1_ubuntu24.04_x86_64.tgz';         pkgSha='e065f91d1d1acdc807f347b888b85ee9c6695f64b772b8455374fa492c8f59cd';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.3/aerospike-server-enterprise_8.1.2.3_tools-13.0.1_ubuntu24.04_aarch64.tgz';         pkgSha='80d193462128a70d43a37d716ca57f896ce3b6cf6dc95daec9a079f8338c3869';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Wed, 01 Jul 2026 00:26:53 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Wed, 01 Jul 2026 00:26:53 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Wed, 01 Jul 2026 00:26:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Jul 2026 00:26:53 GMT
STOPSIGNAL SIGTERM
# Wed, 01 Jul 2026 00:26:53 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 01 Jul 2026 00:26:53 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58fde573d43a3b5511d6eccfe40140bab70e8808684e7d588a86e5fd1fd255a`  
		Last Modified: Wed, 01 Jul 2026 00:27:09 GMT  
		Size: 3.2 MB (3211948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8c891b3fc20a8c3736b7fcdd12f4482840dab176db150c577a585309fb2aa6`  
		Last Modified: Wed, 01 Jul 2026 00:27:12 GMT  
		Size: 105.0 MB (105031193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b1c273dbd6c07292e50a9e3ee964941f4c7ea38b3457bb5a2deec839ca27f8`  
		Last Modified: Wed, 01 Jul 2026 00:27:09 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d126535bcbdbb8ef267cfef97e55e27fbef2715bc8f94c2b9380b3988ab5ae2`  
		Last Modified: Wed, 01 Jul 2026 00:27:09 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.2.3` - unknown; unknown

```console
$ docker pull aerospike@sha256:6ef7a5829f7b5bc455530549b661c8b2238ae95a01b377e73ae463d85352eb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2324330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b40b4ac6a337e7fc0b19e7e3cbadc597962cc322b1b5577f036435ed7afbf893`

```dockerfile
```

-	Layers:
	-	`sha256:1d600e74292bd1867de168385ea12346cdaf636135fd4fbfd1d27f9fac69391f`  
		Last Modified: Wed, 01 Jul 2026 00:27:09 GMT  
		Size: 2.3 MB (2302421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1db47182e48f2bac3a9d91458a322d3dc04cac7fc879f62c92b7a7ec3f1921f`  
		Last Modified: Wed, 01 Jul 2026 00:27:09 GMT  
		Size: 21.9 KB (21909 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ee-8.1.2.3_1`

```console
$ docker pull aerospike@sha256:27559feabace5d8c31b6d124c3ce6dc88b5c97e06cd5a74093ccbbd56641debb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.1.2.3_1` - linux; amd64

```console
$ docker pull aerospike@sha256:c34baaad25f08acaeead64ad93cfff428292fe6768ddf963506586317811c5f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141058152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190f99ccb4219b5d28cfd2b91cdf50cad9c866aa9f7a919a7e45e6097585ba1e`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Wed, 01 Jul 2026 00:18:53 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.3 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Wed, 01 Jul 2026 00:18:53 GMT
ARG AEROSPIKE_EDITION=enterprise
# Wed, 01 Jul 2026 00:18:53 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Wed, 01 Jul 2026 00:18:53 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Wed, 01 Jul 2026 00:18:53 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Jul 2026 00:19:05 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.3/aerospike-server-enterprise_8.1.2.3_tools-13.0.1_ubuntu24.04_x86_64.tgz';         pkgSha='e065f91d1d1acdc807f347b888b85ee9c6695f64b772b8455374fa492c8f59cd';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.3/aerospike-server-enterprise_8.1.2.3_tools-13.0.1_ubuntu24.04_aarch64.tgz';         pkgSha='80d193462128a70d43a37d716ca57f896ce3b6cf6dc95daec9a079f8338c3869';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Wed, 01 Jul 2026 00:19:05 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Wed, 01 Jul 2026 00:19:05 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Wed, 01 Jul 2026 00:19:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Jul 2026 00:19:05 GMT
STOPSIGNAL SIGTERM
# Wed, 01 Jul 2026 00:19:05 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 01 Jul 2026 00:19:05 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff28819c92c74e84dffa9b798fa2085d66ed01eeb29ef6761dfd6c886ddede2`  
		Last Modified: Wed, 01 Jul 2026 00:19:24 GMT  
		Size: 3.4 MB (3418135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad20f0e1a43456e7fe5450947c0d1127b62769e113c3dc96a3cefe2ca064c297`  
		Last Modified: Wed, 01 Jul 2026 00:19:26 GMT  
		Size: 107.9 MB (107904906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fc89011f85a4585a46280f2587db4499c68da4f0e5efb59a2d6742cf310f42`  
		Last Modified: Wed, 01 Jul 2026 00:19:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22ecc194881cc7a129c2e85b6471bc3994d43f70cb468a0e41e6f7ef072ae98`  
		Last Modified: Wed, 01 Jul 2026 00:19:23 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.2.3_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:c2adbdffdc2ff55c84ea4757d1fb95a2b3a748976d3ddc67d1383e6b745a7c3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2323121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c9079bd6ca8a0cab960f5c05f24a7523917ce5d4e87074dc2d48398997b25fc`

```dockerfile
```

-	Layers:
	-	`sha256:16d6deb23596fbbcd880d6c40c09f8505189b7c5d8d4e0a608cb660451c38db0`  
		Last Modified: Wed, 01 Jul 2026 00:19:24 GMT  
		Size: 2.3 MB (2301307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ec8f68282590f28416b03559e9616cd6b94ba6dd982b21b5f68cd0d960a220c`  
		Last Modified: Wed, 01 Jul 2026 00:19:24 GMT  
		Size: 21.8 KB (21814 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.1.2.3_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:ba9bad82732dec92c5625fc9d35ca3b1f3f0b2c0138a19e98f1da9615ba17cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137121852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95c9f1b825a348e2c5e592da260f5030fd7ac11cc200f0d0e89a13388f32d8f`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-Eeuo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Wed, 01 Jul 2026 00:26:40 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.3 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Wed, 01 Jul 2026 00:26:40 GMT
ARG AEROSPIKE_EDITION=enterprise
# Wed, 01 Jul 2026 00:26:40 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Wed, 01 Jul 2026 00:26:40 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Wed, 01 Jul 2026 00:26:40 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Jul 2026 00:26:53 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.3/aerospike-server-enterprise_8.1.2.3_tools-13.0.1_ubuntu24.04_x86_64.tgz';         pkgSha='e065f91d1d1acdc807f347b888b85ee9c6695f64b772b8455374fa492c8f59cd';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.3/aerospike-server-enterprise_8.1.2.3_tools-13.0.1_ubuntu24.04_aarch64.tgz';         pkgSha='80d193462128a70d43a37d716ca57f896ce3b6cf6dc95daec9a079f8338c3869';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Wed, 01 Jul 2026 00:26:53 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Wed, 01 Jul 2026 00:26:53 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Wed, 01 Jul 2026 00:26:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Jul 2026 00:26:53 GMT
STOPSIGNAL SIGTERM
# Wed, 01 Jul 2026 00:26:53 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 01 Jul 2026 00:26:53 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58fde573d43a3b5511d6eccfe40140bab70e8808684e7d588a86e5fd1fd255a`  
		Last Modified: Wed, 01 Jul 2026 00:27:09 GMT  
		Size: 3.2 MB (3211948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8c891b3fc20a8c3736b7fcdd12f4482840dab176db150c577a585309fb2aa6`  
		Last Modified: Wed, 01 Jul 2026 00:27:12 GMT  
		Size: 105.0 MB (105031193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b1c273dbd6c07292e50a9e3ee964941f4c7ea38b3457bb5a2deec839ca27f8`  
		Last Modified: Wed, 01 Jul 2026 00:27:09 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d126535bcbdbb8ef267cfef97e55e27fbef2715bc8f94c2b9380b3988ab5ae2`  
		Last Modified: Wed, 01 Jul 2026 00:27:09 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.2.3_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:6ef7a5829f7b5bc455530549b661c8b2238ae95a01b377e73ae463d85352eb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2324330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b40b4ac6a337e7fc0b19e7e3cbadc597962cc322b1b5577f036435ed7afbf893`

```dockerfile
```

-	Layers:
	-	`sha256:1d600e74292bd1867de168385ea12346cdaf636135fd4fbfd1d27f9fac69391f`  
		Last Modified: Wed, 01 Jul 2026 00:27:09 GMT  
		Size: 2.3 MB (2302421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1db47182e48f2bac3a9d91458a322d3dc04cac7fc879f62c92b7a7ec3f1921f`  
		Last Modified: Wed, 01 Jul 2026 00:27:09 GMT  
		Size: 21.9 KB (21909 bytes)  
		MIME: application/vnd.in-toto+json
