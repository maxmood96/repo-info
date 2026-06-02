<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-8.1.2.1`](#aerospikece-8121)
-	[`aerospike:ce-8.1.2.1_3`](#aerospikece-8121_3)
-	[`aerospike:ee-8.1.2.1`](#aerospikeee-8121)
-	[`aerospike:ee-8.1.2.1_3`](#aerospikeee-8121_3)

## `aerospike:ce-8.1.2.1`

```console
$ docker pull aerospike@sha256:f3ffdb94be7a78e5c7a9f1953b15d48ab29decea2bc5796d24186b936264c7af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.1.2.1` - linux; amd64

```console
$ docker pull aerospike@sha256:5c2da8331981aa702643876671044f715b1e85eafc1233edd6cc834a61e5e6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131793918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b52f8b87ce677480e1df05a8189e539147423f9fd980fc80e89888c2c3b3aae`
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
# Tue, 02 Jun 2026 08:10:51 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 02 Jun 2026 08:10:51 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 02 Jun 2026 08:10:51 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 02 Jun 2026 08:10:51 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 02 Jun 2026 08:10:51 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:11:06 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.1/aerospike-server-community_8.1.2.1_tools-13.0.0_ubuntu24.04_x86_64.tgz';         pkgSha='22350b57714fec888705d7dc9fa33e261e36d8dcd24b21d834652450b6009060';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.1/aerospike-server-community_8.1.2.1_tools-13.0.0_ubuntu24.04_aarch64.tgz';         pkgSha='41efbed30b36c9c710a1432939fafdfb413ce7eea4a55e1fbc08e3dea92d3be7';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Tue, 02 Jun 2026 08:11:06 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 02 Jun 2026 08:11:06 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 02 Jun 2026 08:11:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:11:06 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2026 08:11:06 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 02 Jun 2026 08:11:06 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac06654cd58b06737433e19d4b80093ea281db6a53a2d219fb7a158790df4b5`  
		Last Modified: Tue, 02 Jun 2026 08:11:22 GMT  
		Size: 1.1 MB (1050308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f890a55adf679b2a7fc008b9d09d9d0de46b2252efe37cd0f454808d0ed05a`  
		Last Modified: Tue, 02 Jun 2026 08:11:25 GMT  
		Size: 101.0 MB (101008499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c804c54f947ccb86ec314c7abac6834a45a4c472979450a0dda899f58ff4b881`  
		Last Modified: Tue, 02 Jun 2026 08:11:22 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcf1c650db6b1fb63983800ef7000da9351778cfffa5bcd7794cdf716a18faa`  
		Last Modified: Tue, 02 Jun 2026 08:11:22 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.2.1` - unknown; unknown

```console
$ docker pull aerospike@sha256:b90fc380541dca3ad65d8571a98bf8b9b1c08fca8f182d0e4ea76ee9d22ce1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2236809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef86b88e5a1cac8bbac07d5d3d94751dd778056b3be5c518fea4e7ca570771ff`

```dockerfile
```

-	Layers:
	-	`sha256:c4711014e4de19d9db9e5ab5a2025b0f0154383cb6746fe2fc589d1c8ef6ee02`  
		Last Modified: Tue, 02 Jun 2026 08:11:22 GMT  
		Size: 2.2 MB (2215018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b641d42debbe772420264976f24ec3572e46a7c349b7ea0722ffb02b7fb4a5b5`  
		Last Modified: Tue, 02 Jun 2026 08:11:22 GMT  
		Size: 21.8 KB (21791 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.1.2.1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:13f13be339fde6473f7e7f14439a296a78918ba748fde2f2d9cce4d0fee840e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127915323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfda98b50e8bc2ec965d0cf0ec837e4c9744f2c2fab51532b96b61c2da1b69d`
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
# Tue, 02 Jun 2026 08:10:52 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 02 Jun 2026 08:10:52 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 02 Jun 2026 08:10:52 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 02 Jun 2026 08:10:52 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 02 Jun 2026 08:10:52 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:11:09 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.1/aerospike-server-community_8.1.2.1_tools-13.0.0_ubuntu24.04_x86_64.tgz';         pkgSha='22350b57714fec888705d7dc9fa33e261e36d8dcd24b21d834652450b6009060';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.1/aerospike-server-community_8.1.2.1_tools-13.0.0_ubuntu24.04_aarch64.tgz';         pkgSha='41efbed30b36c9c710a1432939fafdfb413ce7eea4a55e1fbc08e3dea92d3be7';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Tue, 02 Jun 2026 08:11:09 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 02 Jun 2026 08:11:09 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 02 Jun 2026 08:11:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:11:09 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2026 08:11:09 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 02 Jun 2026 08:11:09 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce57ef5098a5ed4e0330577695274e40bd2a6dda16e304659bc3e00f72e49c4a`  
		Last Modified: Tue, 02 Jun 2026 08:11:25 GMT  
		Size: 1.0 MB (1032474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4409c75fa510c7e44ae26e94a74d7bff5748788c27d216eba5a0a2c343185123`  
		Last Modified: Tue, 02 Jun 2026 08:11:28 GMT  
		Size: 98.0 MB (98004138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ee9f82e7ef56159a940c6046765911f7427f69000bf554818f05760c92902`  
		Last Modified: Tue, 02 Jun 2026 08:11:25 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed457fc46cd891b302fa00de893b2ecf407cb4fac3ce49a7a6bb36420f1374f9`  
		Last Modified: Tue, 02 Jun 2026 08:11:25 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.2.1` - unknown; unknown

```console
$ docker pull aerospike@sha256:755a245240cbc8310bdef3bed3f7f13efce431f78aa56a79954f177b670f5293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2237992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1869188b3ee5b503b5381594cd5d5f7f0250503189cd40d9a26b7b96409d3cbe`

```dockerfile
```

-	Layers:
	-	`sha256:7665f1ad7f94642d80b5f7b8301417dd20a447f1e1ce8b0f9eab1a90c7c22fe6`  
		Last Modified: Tue, 02 Jun 2026 08:11:26 GMT  
		Size: 2.2 MB (2216110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e2d4b654f9a4d719ff26672f0207f63c2f50c94598762fab0b8cd7d0990d379`  
		Last Modified: Tue, 02 Jun 2026 08:11:25 GMT  
		Size: 21.9 KB (21882 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ce-8.1.2.1_3`

```console
$ docker pull aerospike@sha256:f3ffdb94be7a78e5c7a9f1953b15d48ab29decea2bc5796d24186b936264c7af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.1.2.1_3` - linux; amd64

```console
$ docker pull aerospike@sha256:5c2da8331981aa702643876671044f715b1e85eafc1233edd6cc834a61e5e6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131793918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b52f8b87ce677480e1df05a8189e539147423f9fd980fc80e89888c2c3b3aae`
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
# Tue, 02 Jun 2026 08:10:51 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 02 Jun 2026 08:10:51 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 02 Jun 2026 08:10:51 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 02 Jun 2026 08:10:51 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 02 Jun 2026 08:10:51 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:11:06 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.1/aerospike-server-community_8.1.2.1_tools-13.0.0_ubuntu24.04_x86_64.tgz';         pkgSha='22350b57714fec888705d7dc9fa33e261e36d8dcd24b21d834652450b6009060';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.1/aerospike-server-community_8.1.2.1_tools-13.0.0_ubuntu24.04_aarch64.tgz';         pkgSha='41efbed30b36c9c710a1432939fafdfb413ce7eea4a55e1fbc08e3dea92d3be7';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Tue, 02 Jun 2026 08:11:06 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 02 Jun 2026 08:11:06 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 02 Jun 2026 08:11:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:11:06 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2026 08:11:06 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 02 Jun 2026 08:11:06 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac06654cd58b06737433e19d4b80093ea281db6a53a2d219fb7a158790df4b5`  
		Last Modified: Tue, 02 Jun 2026 08:11:22 GMT  
		Size: 1.1 MB (1050308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f890a55adf679b2a7fc008b9d09d9d0de46b2252efe37cd0f454808d0ed05a`  
		Last Modified: Tue, 02 Jun 2026 08:11:25 GMT  
		Size: 101.0 MB (101008499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c804c54f947ccb86ec314c7abac6834a45a4c472979450a0dda899f58ff4b881`  
		Last Modified: Tue, 02 Jun 2026 08:11:22 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcf1c650db6b1fb63983800ef7000da9351778cfffa5bcd7794cdf716a18faa`  
		Last Modified: Tue, 02 Jun 2026 08:11:22 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.2.1_3` - unknown; unknown

```console
$ docker pull aerospike@sha256:b90fc380541dca3ad65d8571a98bf8b9b1c08fca8f182d0e4ea76ee9d22ce1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2236809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef86b88e5a1cac8bbac07d5d3d94751dd778056b3be5c518fea4e7ca570771ff`

```dockerfile
```

-	Layers:
	-	`sha256:c4711014e4de19d9db9e5ab5a2025b0f0154383cb6746fe2fc589d1c8ef6ee02`  
		Last Modified: Tue, 02 Jun 2026 08:11:22 GMT  
		Size: 2.2 MB (2215018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b641d42debbe772420264976f24ec3572e46a7c349b7ea0722ffb02b7fb4a5b5`  
		Last Modified: Tue, 02 Jun 2026 08:11:22 GMT  
		Size: 21.8 KB (21791 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.1.2.1_3` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:13f13be339fde6473f7e7f14439a296a78918ba748fde2f2d9cce4d0fee840e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127915323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfda98b50e8bc2ec965d0cf0ec837e4c9744f2c2fab51532b96b61c2da1b69d`
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
# Tue, 02 Jun 2026 08:10:52 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 02 Jun 2026 08:10:52 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 02 Jun 2026 08:10:52 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 02 Jun 2026 08:10:52 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 02 Jun 2026 08:10:52 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:11:09 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.1/aerospike-server-community_8.1.2.1_tools-13.0.0_ubuntu24.04_x86_64.tgz';         pkgSha='22350b57714fec888705d7dc9fa33e261e36d8dcd24b21d834652450b6009060';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.1/aerospike-server-community_8.1.2.1_tools-13.0.0_ubuntu24.04_aarch64.tgz';         pkgSha='41efbed30b36c9c710a1432939fafdfb413ce7eea4a55e1fbc08e3dea92d3be7';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Tue, 02 Jun 2026 08:11:09 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 02 Jun 2026 08:11:09 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 02 Jun 2026 08:11:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:11:09 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2026 08:11:09 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 02 Jun 2026 08:11:09 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce57ef5098a5ed4e0330577695274e40bd2a6dda16e304659bc3e00f72e49c4a`  
		Last Modified: Tue, 02 Jun 2026 08:11:25 GMT  
		Size: 1.0 MB (1032474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4409c75fa510c7e44ae26e94a74d7bff5748788c27d216eba5a0a2c343185123`  
		Last Modified: Tue, 02 Jun 2026 08:11:28 GMT  
		Size: 98.0 MB (98004138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ee9f82e7ef56159a940c6046765911f7427f69000bf554818f05760c92902`  
		Last Modified: Tue, 02 Jun 2026 08:11:25 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed457fc46cd891b302fa00de893b2ecf407cb4fac3ce49a7a6bb36420f1374f9`  
		Last Modified: Tue, 02 Jun 2026 08:11:25 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.2.1_3` - unknown; unknown

```console
$ docker pull aerospike@sha256:755a245240cbc8310bdef3bed3f7f13efce431f78aa56a79954f177b670f5293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2237992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1869188b3ee5b503b5381594cd5d5f7f0250503189cd40d9a26b7b96409d3cbe`

```dockerfile
```

-	Layers:
	-	`sha256:7665f1ad7f94642d80b5f7b8301417dd20a447f1e1ce8b0f9eab1a90c7c22fe6`  
		Last Modified: Tue, 02 Jun 2026 08:11:26 GMT  
		Size: 2.2 MB (2216110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e2d4b654f9a4d719ff26672f0207f63c2f50c94598762fab0b8cd7d0990d379`  
		Last Modified: Tue, 02 Jun 2026 08:11:25 GMT  
		Size: 21.9 KB (21882 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ee-8.1.2.1`

```console
$ docker pull aerospike@sha256:3d45427ef722f9d32a881425338f54054f9265a8feab0606b0bfc36e933a239c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.1.2.1` - linux; amd64

```console
$ docker pull aerospike@sha256:e82257295dd79f7729e4dd0e2415a13489cfdc7278e765995590493ae9b2eae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136152632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553e8acd5c2f8f44127550d21509803cdaf84f089c146db018bd77d74544eb7b`
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
# Tue, 02 Jun 2026 08:10:35 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 02 Jun 2026 08:10:35 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 02 Jun 2026 08:10:35 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 02 Jun 2026 08:10:35 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 02 Jun 2026 08:10:35 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:49 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.1/aerospike-server-enterprise_8.1.2.1_tools-13.0.0_ubuntu24.04_x86_64.tgz';         pkgSha='299916965c5a9959f4159e2b3ba36e55b64bdb63910654735ea96d65e4a38179';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.1/aerospike-server-enterprise_8.1.2.1_tools-13.0.0_ubuntu24.04_aarch64.tgz';         pkgSha='22fa2cec34972bdb9c73c2c3577ba80bb0555855280b6161e6f96d0944503c3c';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Tue, 02 Jun 2026 08:10:49 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 02 Jun 2026 08:10:49 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 02 Jun 2026 08:10:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:10:49 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2026 08:10:49 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 02 Jun 2026 08:10:49 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22dae9d754e14c18c4f91db0d1f3885980c720fd7974e71ed67f97e1083751ee`  
		Last Modified: Tue, 02 Jun 2026 08:11:06 GMT  
		Size: 1.1 MB (1050312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2335af183739fc6721e286c7abfdecc174d9f8bfdf44acc338c3514b6f5e6a11`  
		Last Modified: Tue, 02 Jun 2026 08:11:09 GMT  
		Size: 105.4 MB (105367206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0658ccfb54fc9e3cd3e5251fe19e8fb2cd51b1b7a33e85b8e1504e86c6affde9`  
		Last Modified: Tue, 02 Jun 2026 08:11:06 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053611fc8892a2d5d844deffecd940b2205fe222f933637e493c163ec00a456a`  
		Last Modified: Tue, 02 Jun 2026 08:11:06 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.2.1` - unknown; unknown

```console
$ docker pull aerospike@sha256:ea14b91e26b44f09103b79bbfe96e952acad8a57f05a7b19e1fa75c2715b76f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2337890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7fa7902eabc4f3df2bea138595732948173db50b722f6d6b3fff473c9765df0`

```dockerfile
```

-	Layers:
	-	`sha256:7239bf9f3316261da1724df1635f9e6bd9752502c7ff895f9da535c70846f26a`  
		Last Modified: Tue, 02 Jun 2026 08:11:06 GMT  
		Size: 2.3 MB (2316082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c3fc869de0a60ec203e40ea6778470bc929c169ca8baa5c5915c14df92830d`  
		Last Modified: Tue, 02 Jun 2026 08:11:06 GMT  
		Size: 21.8 KB (21808 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.1.2.1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:2f6f66c7a04828504104e6ae4855a487ea6c89886d6e2d9d6223e15f258c01a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132308725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31ab14eee22a4610d16607344548fcd266f30690bf2b5694e33ef595e008db9`
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
# Tue, 02 Jun 2026 08:10:31 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 02 Jun 2026 08:10:31 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 02 Jun 2026 08:10:31 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 02 Jun 2026 08:10:31 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 02 Jun 2026 08:10:31 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:46 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.1/aerospike-server-enterprise_8.1.2.1_tools-13.0.0_ubuntu24.04_x86_64.tgz';         pkgSha='299916965c5a9959f4159e2b3ba36e55b64bdb63910654735ea96d65e4a38179';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.1/aerospike-server-enterprise_8.1.2.1_tools-13.0.0_ubuntu24.04_aarch64.tgz';         pkgSha='22fa2cec34972bdb9c73c2c3577ba80bb0555855280b6161e6f96d0944503c3c';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Tue, 02 Jun 2026 08:10:46 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 02 Jun 2026 08:10:46 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 02 Jun 2026 08:10:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:10:46 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2026 08:10:46 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 02 Jun 2026 08:10:46 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead44134ef261ef485bb0a3d90813fa6f7497345bd261adf508baa7546517a45`  
		Last Modified: Tue, 02 Jun 2026 08:11:03 GMT  
		Size: 1.0 MB (1032462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638fe0d9ea1c8c38c76a21032b6346f69ef4877b84e313c64aedb39c2dfdde8c`  
		Last Modified: Tue, 02 Jun 2026 08:11:06 GMT  
		Size: 102.4 MB (102397552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9b778263aa36212c34626626ac1614bb2f3c665754c0afa34ac8a0236bf788`  
		Last Modified: Tue, 02 Jun 2026 08:11:03 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ffb2077c751e5dda7dc3724d2696aa0060892f8db2724ce245cfa0e9fd8e77`  
		Last Modified: Tue, 02 Jun 2026 08:11:03 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.2.1` - unknown; unknown

```console
$ docker pull aerospike@sha256:54486e497fd7b79eaba86b970504aaa0d39ba75e9fcbee72b0eb3a99010cf5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2339095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8454d873925de98ab7c1671ddd57fc27efca8aa6192874e413ff89aca32dc2b9`

```dockerfile
```

-	Layers:
	-	`sha256:84a1b2867d5fbb15f317de4da6cb33a453f1c4e30787eb13c9cc55d5366830f2`  
		Last Modified: Tue, 02 Jun 2026 08:11:03 GMT  
		Size: 2.3 MB (2317192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e1c0f7d787c6930d8735a37ad7c0b822f7c1a41c299b5b37d6e9951bb1d1e8`  
		Last Modified: Tue, 02 Jun 2026 08:11:03 GMT  
		Size: 21.9 KB (21903 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ee-8.1.2.1_3`

```console
$ docker pull aerospike@sha256:3d45427ef722f9d32a881425338f54054f9265a8feab0606b0bfc36e933a239c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.1.2.1_3` - linux; amd64

```console
$ docker pull aerospike@sha256:e82257295dd79f7729e4dd0e2415a13489cfdc7278e765995590493ae9b2eae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136152632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553e8acd5c2f8f44127550d21509803cdaf84f089c146db018bd77d74544eb7b`
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
# Tue, 02 Jun 2026 08:10:35 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 02 Jun 2026 08:10:35 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 02 Jun 2026 08:10:35 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 02 Jun 2026 08:10:35 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 02 Jun 2026 08:10:35 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:49 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.1/aerospike-server-enterprise_8.1.2.1_tools-13.0.0_ubuntu24.04_x86_64.tgz';         pkgSha='299916965c5a9959f4159e2b3ba36e55b64bdb63910654735ea96d65e4a38179';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.1/aerospike-server-enterprise_8.1.2.1_tools-13.0.0_ubuntu24.04_aarch64.tgz';         pkgSha='22fa2cec34972bdb9c73c2c3577ba80bb0555855280b6161e6f96d0944503c3c';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Tue, 02 Jun 2026 08:10:49 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 02 Jun 2026 08:10:49 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 02 Jun 2026 08:10:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:10:49 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2026 08:10:49 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 02 Jun 2026 08:10:49 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22dae9d754e14c18c4f91db0d1f3885980c720fd7974e71ed67f97e1083751ee`  
		Last Modified: Tue, 02 Jun 2026 08:11:06 GMT  
		Size: 1.1 MB (1050312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2335af183739fc6721e286c7abfdecc174d9f8bfdf44acc338c3514b6f5e6a11`  
		Last Modified: Tue, 02 Jun 2026 08:11:09 GMT  
		Size: 105.4 MB (105367206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0658ccfb54fc9e3cd3e5251fe19e8fb2cd51b1b7a33e85b8e1504e86c6affde9`  
		Last Modified: Tue, 02 Jun 2026 08:11:06 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053611fc8892a2d5d844deffecd940b2205fe222f933637e493c163ec00a456a`  
		Last Modified: Tue, 02 Jun 2026 08:11:06 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.2.1_3` - unknown; unknown

```console
$ docker pull aerospike@sha256:ea14b91e26b44f09103b79bbfe96e952acad8a57f05a7b19e1fa75c2715b76f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2337890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7fa7902eabc4f3df2bea138595732948173db50b722f6d6b3fff473c9765df0`

```dockerfile
```

-	Layers:
	-	`sha256:7239bf9f3316261da1724df1635f9e6bd9752502c7ff895f9da535c70846f26a`  
		Last Modified: Tue, 02 Jun 2026 08:11:06 GMT  
		Size: 2.3 MB (2316082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c3fc869de0a60ec203e40ea6778470bc929c169ca8baa5c5915c14df92830d`  
		Last Modified: Tue, 02 Jun 2026 08:11:06 GMT  
		Size: 21.8 KB (21808 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.1.2.1_3` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:2f6f66c7a04828504104e6ae4855a487ea6c89886d6e2d9d6223e15f258c01a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132308725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31ab14eee22a4610d16607344548fcd266f30690bf2b5694e33ef595e008db9`
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
# Tue, 02 Jun 2026 08:10:31 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.1 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 02 Jun 2026 08:10:31 GMT
ARG AEROSPIKE_EDITION=enterprise
# Tue, 02 Jun 2026 08:10:31 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 02 Jun 2026 08:10:31 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 02 Jun 2026 08:10:31 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:10:46 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.1/aerospike-server-enterprise_8.1.2.1_tools-13.0.0_ubuntu24.04_x86_64.tgz';         pkgSha='299916965c5a9959f4159e2b3ba36e55b64bdb63910654735ea96d65e4a38179';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.1/aerospike-server-enterprise_8.1.2.1_tools-13.0.0_ubuntu24.04_aarch64.tgz';         pkgSha='22fa2cec34972bdb9c73c2c3577ba80bb0555855280b6161e6f96d0944503c3c';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Tue, 02 Jun 2026 08:10:46 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 02 Jun 2026 08:10:46 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 02 Jun 2026 08:10:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:10:46 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2026 08:10:46 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 02 Jun 2026 08:10:46 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead44134ef261ef485bb0a3d90813fa6f7497345bd261adf508baa7546517a45`  
		Last Modified: Tue, 02 Jun 2026 08:11:03 GMT  
		Size: 1.0 MB (1032462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638fe0d9ea1c8c38c76a21032b6346f69ef4877b84e313c64aedb39c2dfdde8c`  
		Last Modified: Tue, 02 Jun 2026 08:11:06 GMT  
		Size: 102.4 MB (102397552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9b778263aa36212c34626626ac1614bb2f3c665754c0afa34ac8a0236bf788`  
		Last Modified: Tue, 02 Jun 2026 08:11:03 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ffb2077c751e5dda7dc3724d2696aa0060892f8db2724ce245cfa0e9fd8e77`  
		Last Modified: Tue, 02 Jun 2026 08:11:03 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.2.1_3` - unknown; unknown

```console
$ docker pull aerospike@sha256:54486e497fd7b79eaba86b970504aaa0d39ba75e9fcbee72b0eb3a99010cf5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2339095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8454d873925de98ab7c1671ddd57fc27efca8aa6192874e413ff89aca32dc2b9`

```dockerfile
```

-	Layers:
	-	`sha256:84a1b2867d5fbb15f317de4da6cb33a453f1c4e30787eb13c9cc55d5366830f2`  
		Last Modified: Tue, 02 Jun 2026 08:11:03 GMT  
		Size: 2.3 MB (2317192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e1c0f7d787c6930d8735a37ad7c0b822f7c1a41c299b5b37d6e9951bb1d1e8`  
		Last Modified: Tue, 02 Jun 2026 08:11:03 GMT  
		Size: 21.9 KB (21903 bytes)  
		MIME: application/vnd.in-toto+json
