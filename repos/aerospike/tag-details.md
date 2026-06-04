<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-8.1.2.2`](#aerospikece-8122)
-	[`aerospike:ce-8.1.2.2_1`](#aerospikece-8122_1)
-	[`aerospike:ee-8.1.2.2`](#aerospikeee-8122)
-	[`aerospike:ee-8.1.2.2_1`](#aerospikeee-8122_1)

## `aerospike:ce-8.1.2.2`

```console
$ docker pull aerospike@sha256:fe73d88b26299d9e7943b1a3c6bf9690d12dca9f1003a2d00351150b18775ab6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.1.2.2` - linux; amd64

```console
$ docker pull aerospike@sha256:b52361d733e01482f26c7dcd070ae94a6026269e231f4806bd3c090977b3e3ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 MB (134305678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a969c2cdec74dba02f394ce3a99c6f8142707e7db200022a9b57313c15a8172a`
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
# Thu, 04 Jun 2026 17:34:28 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.2 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 04 Jun 2026 17:34:28 GMT
ARG AEROSPIKE_EDITION=community
# Thu, 04 Jun 2026 17:34:28 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Thu, 04 Jun 2026 17:34:28 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 04 Jun 2026 17:34:28 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jun 2026 17:34:43 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.2/aerospike-server-community_8.1.2.2_tools-13.0.1_ubuntu24.04_x86_64.tgz';         pkgSha='3f3e8d1e3727da60323e072c14308a756335a486d0fb951b8421d6445c891eb1';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.2/aerospike-server-community_8.1.2.2_tools-13.0.1_ubuntu24.04_aarch64.tgz';         pkgSha='b216371bd2a0a4ac1c65c6c5887d6f2bc051e83b09a0f8617a0f94fe59c78017';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Thu, 04 Jun 2026 17:34:43 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 04 Jun 2026 17:34:43 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 04 Jun 2026 17:34:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Jun 2026 17:34:43 GMT
STOPSIGNAL SIGTERM
# Thu, 04 Jun 2026 17:34:43 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 04 Jun 2026 17:34:43 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1939da0ef738c0967462a4d1028b6eb26ba5d63973186da390c36827df740dec`  
		Last Modified: Thu, 04 Jun 2026 17:35:00 GMT  
		Size: 1.1 MB (1050314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df6123a9392e64c0ffa8a9e39e56ad53c86d6252d508ed246351a3621c058ea`  
		Last Modified: Thu, 04 Jun 2026 17:35:03 GMT  
		Size: 103.5 MB (103520255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4880a91200a61b32f99b49054b7f561e5a8b6f42b92441b3e299899bccb312`  
		Last Modified: Thu, 04 Jun 2026 17:34:59 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fdd5fea1cb963116b7badca86d50afbd110db14e5190ad5056652995bfa2e6`  
		Last Modified: Thu, 04 Jun 2026 17:35:00 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.2.2` - unknown; unknown

```console
$ docker pull aerospike@sha256:8638d19c4666d758ef90cf613c21d2578d506a59b7a60b7b7fb2ac778aa77101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2238294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91cad6c940c747081e0f6e34e8b80cfca1cc1d2e386902b845077bb733fdc00`

```dockerfile
```

-	Layers:
	-	`sha256:85a8a92b4621f466dd6ef512786d82bd836a2a6ceb907b09108d9ad03c9285e7`  
		Last Modified: Thu, 04 Jun 2026 17:34:59 GMT  
		Size: 2.2 MB (2216497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffcd8b44e156dd77b72eac06c6b65544bafec9cc5140d736581dcc178f3df692`  
		Last Modified: Thu, 04 Jun 2026 17:34:59 GMT  
		Size: 21.8 KB (21797 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.1.2.2` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:e7d384c3db66026c9d7d369770e29afafc756920994f8c368575fe6ff2156916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130531040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d93308cedebf57d6bce10ab80a79b1070bcee68373e26cc529cfa955588848d`
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
# Thu, 04 Jun 2026 17:34:28 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.2 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 04 Jun 2026 17:34:28 GMT
ARG AEROSPIKE_EDITION=community
# Thu, 04 Jun 2026 17:34:28 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Thu, 04 Jun 2026 17:34:28 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 04 Jun 2026 17:34:28 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jun 2026 17:34:44 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.2/aerospike-server-community_8.1.2.2_tools-13.0.1_ubuntu24.04_x86_64.tgz';         pkgSha='3f3e8d1e3727da60323e072c14308a756335a486d0fb951b8421d6445c891eb1';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.2/aerospike-server-community_8.1.2.2_tools-13.0.1_ubuntu24.04_aarch64.tgz';         pkgSha='b216371bd2a0a4ac1c65c6c5887d6f2bc051e83b09a0f8617a0f94fe59c78017';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Thu, 04 Jun 2026 17:34:44 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 04 Jun 2026 17:34:44 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 04 Jun 2026 17:34:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Jun 2026 17:34:44 GMT
STOPSIGNAL SIGTERM
# Thu, 04 Jun 2026 17:34:44 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 04 Jun 2026 17:34:44 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba3dab004775e40735afb9594b0f60aa2ecc9c0dc3f83727cd2266098a3d9cc`  
		Last Modified: Thu, 04 Jun 2026 17:35:00 GMT  
		Size: 1.0 MB (1032461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c791d7983358c9ff26591f56c66ec9dc2e29f7e8cc65e81ebbca72f6f1311e`  
		Last Modified: Thu, 04 Jun 2026 17:35:03 GMT  
		Size: 100.6 MB (100619867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45fb720eb68eb4fe6113963cac33658fceff7a8d2429aa8e62379ae3d6b7d4d`  
		Last Modified: Thu, 04 Jun 2026 17:35:00 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64328f4128159530c240e04f90a28c9ad725be2a40820eaf3614ea85229de90a`  
		Last Modified: Thu, 04 Jun 2026 17:35:00 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.2.2` - unknown; unknown

```console
$ docker pull aerospike@sha256:0d87e53878ab553a841afbfe11ce155d8870e00ebcc55056e8a3f7297ef47746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2239480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200db3c41f2ff982809c55d4b36daf16c9d230ec6572d7733a6549719eba888b`

```dockerfile
```

-	Layers:
	-	`sha256:37b7fd1ba245e319228fde68bec6a5fc666e9ddd29109c9f96d65dabb9627836`  
		Last Modified: Thu, 04 Jun 2026 17:35:00 GMT  
		Size: 2.2 MB (2217589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6262ce5f91ed227c4ec1c283de1949d28560d664fc6feb8bd0c0b924254cc9b1`  
		Last Modified: Thu, 04 Jun 2026 17:35:00 GMT  
		Size: 21.9 KB (21891 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ce-8.1.2.2_1`

```console
$ docker pull aerospike@sha256:fe73d88b26299d9e7943b1a3c6bf9690d12dca9f1003a2d00351150b18775ab6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.1.2.2_1` - linux; amd64

```console
$ docker pull aerospike@sha256:b52361d733e01482f26c7dcd070ae94a6026269e231f4806bd3c090977b3e3ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 MB (134305678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a969c2cdec74dba02f394ce3a99c6f8142707e7db200022a9b57313c15a8172a`
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
# Thu, 04 Jun 2026 17:34:28 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.2 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 04 Jun 2026 17:34:28 GMT
ARG AEROSPIKE_EDITION=community
# Thu, 04 Jun 2026 17:34:28 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Thu, 04 Jun 2026 17:34:28 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 04 Jun 2026 17:34:28 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jun 2026 17:34:43 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.2/aerospike-server-community_8.1.2.2_tools-13.0.1_ubuntu24.04_x86_64.tgz';         pkgSha='3f3e8d1e3727da60323e072c14308a756335a486d0fb951b8421d6445c891eb1';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.2/aerospike-server-community_8.1.2.2_tools-13.0.1_ubuntu24.04_aarch64.tgz';         pkgSha='b216371bd2a0a4ac1c65c6c5887d6f2bc051e83b09a0f8617a0f94fe59c78017';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Thu, 04 Jun 2026 17:34:43 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 04 Jun 2026 17:34:43 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 04 Jun 2026 17:34:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Jun 2026 17:34:43 GMT
STOPSIGNAL SIGTERM
# Thu, 04 Jun 2026 17:34:43 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 04 Jun 2026 17:34:43 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1939da0ef738c0967462a4d1028b6eb26ba5d63973186da390c36827df740dec`  
		Last Modified: Thu, 04 Jun 2026 17:35:00 GMT  
		Size: 1.1 MB (1050314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df6123a9392e64c0ffa8a9e39e56ad53c86d6252d508ed246351a3621c058ea`  
		Last Modified: Thu, 04 Jun 2026 17:35:03 GMT  
		Size: 103.5 MB (103520255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4880a91200a61b32f99b49054b7f561e5a8b6f42b92441b3e299899bccb312`  
		Last Modified: Thu, 04 Jun 2026 17:34:59 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fdd5fea1cb963116b7badca86d50afbd110db14e5190ad5056652995bfa2e6`  
		Last Modified: Thu, 04 Jun 2026 17:35:00 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.2.2_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:8638d19c4666d758ef90cf613c21d2578d506a59b7a60b7b7fb2ac778aa77101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2238294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91cad6c940c747081e0f6e34e8b80cfca1cc1d2e386902b845077bb733fdc00`

```dockerfile
```

-	Layers:
	-	`sha256:85a8a92b4621f466dd6ef512786d82bd836a2a6ceb907b09108d9ad03c9285e7`  
		Last Modified: Thu, 04 Jun 2026 17:34:59 GMT  
		Size: 2.2 MB (2216497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffcd8b44e156dd77b72eac06c6b65544bafec9cc5140d736581dcc178f3df692`  
		Last Modified: Thu, 04 Jun 2026 17:34:59 GMT  
		Size: 21.8 KB (21797 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.1.2.2_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:e7d384c3db66026c9d7d369770e29afafc756920994f8c368575fe6ff2156916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130531040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d93308cedebf57d6bce10ab80a79b1070bcee68373e26cc529cfa955588848d`
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
# Thu, 04 Jun 2026 17:34:28 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.2 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 04 Jun 2026 17:34:28 GMT
ARG AEROSPIKE_EDITION=community
# Thu, 04 Jun 2026 17:34:28 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Thu, 04 Jun 2026 17:34:28 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 04 Jun 2026 17:34:28 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jun 2026 17:34:44 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.2/aerospike-server-community_8.1.2.2_tools-13.0.1_ubuntu24.04_x86_64.tgz';         pkgSha='3f3e8d1e3727da60323e072c14308a756335a486d0fb951b8421d6445c891eb1';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.2/aerospike-server-community_8.1.2.2_tools-13.0.1_ubuntu24.04_aarch64.tgz';         pkgSha='b216371bd2a0a4ac1c65c6c5887d6f2bc051e83b09a0f8617a0f94fe59c78017';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Thu, 04 Jun 2026 17:34:44 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 04 Jun 2026 17:34:44 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 04 Jun 2026 17:34:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Jun 2026 17:34:44 GMT
STOPSIGNAL SIGTERM
# Thu, 04 Jun 2026 17:34:44 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 04 Jun 2026 17:34:44 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba3dab004775e40735afb9594b0f60aa2ecc9c0dc3f83727cd2266098a3d9cc`  
		Last Modified: Thu, 04 Jun 2026 17:35:00 GMT  
		Size: 1.0 MB (1032461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c791d7983358c9ff26591f56c66ec9dc2e29f7e8cc65e81ebbca72f6f1311e`  
		Last Modified: Thu, 04 Jun 2026 17:35:03 GMT  
		Size: 100.6 MB (100619867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45fb720eb68eb4fe6113963cac33658fceff7a8d2429aa8e62379ae3d6b7d4d`  
		Last Modified: Thu, 04 Jun 2026 17:35:00 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64328f4128159530c240e04f90a28c9ad725be2a40820eaf3614ea85229de90a`  
		Last Modified: Thu, 04 Jun 2026 17:35:00 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.2.2_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:0d87e53878ab553a841afbfe11ce155d8870e00ebcc55056e8a3f7297ef47746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2239480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200db3c41f2ff982809c55d4b36daf16c9d230ec6572d7733a6549719eba888b`

```dockerfile
```

-	Layers:
	-	`sha256:37b7fd1ba245e319228fde68bec6a5fc666e9ddd29109c9f96d65dabb9627836`  
		Last Modified: Thu, 04 Jun 2026 17:35:00 GMT  
		Size: 2.2 MB (2217589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6262ce5f91ed227c4ec1c283de1949d28560d664fc6feb8bd0c0b924254cc9b1`  
		Last Modified: Thu, 04 Jun 2026 17:35:00 GMT  
		Size: 21.9 KB (21891 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ee-8.1.2.2`

```console
$ docker pull aerospike@sha256:0a8d29a7720c1c5c449f70e7543be270ec5e4db3a67e00d0c61473695642b79e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.1.2.2` - linux; amd64

```console
$ docker pull aerospike@sha256:1c99e22b687196e877608924910e107d03df546f1574c31d6a4328b462489f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138675903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5d5c7fbb69267d89752ab9142d165e0ba2d7f1205666247ec33ef4fb4edf49`
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
# Thu, 04 Jun 2026 17:33:42 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.2 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 04 Jun 2026 17:33:42 GMT
ARG AEROSPIKE_EDITION=enterprise
# Thu, 04 Jun 2026 17:33:42 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Thu, 04 Jun 2026 17:33:42 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 04 Jun 2026 17:33:42 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jun 2026 17:33:55 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.2/aerospike-server-enterprise_8.1.2.2_tools-13.0.1_ubuntu24.04_x86_64.tgz';         pkgSha='a04ebcb7546ea4bc7e72b71054da58c0fb3aa150a63f3662c655314436ced1a7';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.2/aerospike-server-enterprise_8.1.2.2_tools-13.0.1_ubuntu24.04_aarch64.tgz';         pkgSha='6ed0285d6c81c81689ca408b94c1704317510ced9c01d56b9057fae48ff53fcb';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Thu, 04 Jun 2026 17:33:55 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 04 Jun 2026 17:33:55 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 04 Jun 2026 17:33:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Jun 2026 17:33:55 GMT
STOPSIGNAL SIGTERM
# Thu, 04 Jun 2026 17:33:55 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 04 Jun 2026 17:33:55 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2391e332f9948e1c75e341a452c5d205eacead62107e5b4cbc51232b03c5db1`  
		Last Modified: Thu, 04 Jun 2026 17:34:13 GMT  
		Size: 1.1 MB (1050295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbffa01733a3f820061bd0231f71f494d2a822a628d9db83bb4ed80afbf22c9`  
		Last Modified: Thu, 04 Jun 2026 17:34:15 GMT  
		Size: 107.9 MB (107890500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8117cadeb3d7793473733ba79b60bee221e3c3a7ea59038af8b5fac682c8ab3`  
		Last Modified: Thu, 04 Jun 2026 17:34:13 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf9a846b2eb247c729992464823ed673fd1707045d6a7740c6ee755cd82fc40`  
		Last Modified: Thu, 04 Jun 2026 17:34:11 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.2.2` - unknown; unknown

```console
$ docker pull aerospike@sha256:03cbabd17c7f2a8171a5f3903b81840c8e33d9572b76c660907d926bc62846b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2339375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2944937bc53a37c64f3350884ba9fa80af89c8d894d35c20fc57c245582d25f0`

```dockerfile
```

-	Layers:
	-	`sha256:d39c45b44975e99b1587f6cc0597a9d45c6ba3bb5c7edc1a105f4bd706232099`  
		Last Modified: Thu, 04 Jun 2026 17:34:13 GMT  
		Size: 2.3 MB (2317561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9cb0f25fc0581a268f21166e0f51bbe9ecaeb634b706c77277c203b92364d41`  
		Last Modified: Thu, 04 Jun 2026 17:34:13 GMT  
		Size: 21.8 KB (21814 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.1.2.2` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:ec5439e4d7128e2d448f1519daec78ef9b34764011878d9cca7463be791006a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134927329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53c9db7fe96f5c5ba1812251a29c6eabb91f4fccdec16a161f0e562dd4a2341`
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
# Thu, 04 Jun 2026 17:33:40 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.2 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 04 Jun 2026 17:33:40 GMT
ARG AEROSPIKE_EDITION=enterprise
# Thu, 04 Jun 2026 17:33:40 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Thu, 04 Jun 2026 17:33:40 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 04 Jun 2026 17:33:40 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jun 2026 17:33:54 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.2/aerospike-server-enterprise_8.1.2.2_tools-13.0.1_ubuntu24.04_x86_64.tgz';         pkgSha='a04ebcb7546ea4bc7e72b71054da58c0fb3aa150a63f3662c655314436ced1a7';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.2/aerospike-server-enterprise_8.1.2.2_tools-13.0.1_ubuntu24.04_aarch64.tgz';         pkgSha='6ed0285d6c81c81689ca408b94c1704317510ced9c01d56b9057fae48ff53fcb';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Thu, 04 Jun 2026 17:33:54 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 04 Jun 2026 17:33:54 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 04 Jun 2026 17:33:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Jun 2026 17:33:54 GMT
STOPSIGNAL SIGTERM
# Thu, 04 Jun 2026 17:33:54 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 04 Jun 2026 17:33:54 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a20d6c68c1a3dd6538f24493296fed23e3bbf17a0c390bb8f6bf34f80bdebe`  
		Last Modified: Thu, 04 Jun 2026 17:34:11 GMT  
		Size: 1.0 MB (1032477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec813682bf8c77144d48626844d6485d2c990e5aeba08591eccb863d20b7207`  
		Last Modified: Thu, 04 Jun 2026 17:34:13 GMT  
		Size: 105.0 MB (105016138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf32e423940d6581a1cda0112c49e46496d0b72449388f3cf410b90fe600ea8`  
		Last Modified: Thu, 04 Jun 2026 17:34:10 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf9a846b2eb247c729992464823ed673fd1707045d6a7740c6ee755cd82fc40`  
		Last Modified: Thu, 04 Jun 2026 17:34:11 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.2.2` - unknown; unknown

```console
$ docker pull aerospike@sha256:7d1e18b5ed75c950441da23b3c8d009965411475801b4bf48682ee238594bfd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2340580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c945acc125ed9e5a6156b1da2ebffbb712f8f88bbfafc749c1ba477a22dd9977`

```dockerfile
```

-	Layers:
	-	`sha256:0e0d799834ef403d5083b2274e2c9f4d9d1bab28bcbd804842c01cec84302cd9`  
		Last Modified: Thu, 04 Jun 2026 17:34:11 GMT  
		Size: 2.3 MB (2318671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b18496c0cb5390863b6d4e8e0e7741e019e6c252b65e77e86d6bf4764e3753a`  
		Last Modified: Thu, 04 Jun 2026 17:34:11 GMT  
		Size: 21.9 KB (21909 bytes)  
		MIME: application/vnd.in-toto+json

## `aerospike:ee-8.1.2.2_1`

```console
$ docker pull aerospike@sha256:0a8d29a7720c1c5c449f70e7543be270ec5e4db3a67e00d0c61473695642b79e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ee-8.1.2.2_1` - linux; amd64

```console
$ docker pull aerospike@sha256:1c99e22b687196e877608924910e107d03df546f1574c31d6a4328b462489f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138675903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5d5c7fbb69267d89752ab9142d165e0ba2d7f1205666247ec33ef4fb4edf49`
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
# Thu, 04 Jun 2026 17:33:42 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.2 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 04 Jun 2026 17:33:42 GMT
ARG AEROSPIKE_EDITION=enterprise
# Thu, 04 Jun 2026 17:33:42 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Thu, 04 Jun 2026 17:33:42 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 04 Jun 2026 17:33:42 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jun 2026 17:33:55 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.2/aerospike-server-enterprise_8.1.2.2_tools-13.0.1_ubuntu24.04_x86_64.tgz';         pkgSha='a04ebcb7546ea4bc7e72b71054da58c0fb3aa150a63f3662c655314436ced1a7';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.2/aerospike-server-enterprise_8.1.2.2_tools-13.0.1_ubuntu24.04_aarch64.tgz';         pkgSha='6ed0285d6c81c81689ca408b94c1704317510ced9c01d56b9057fae48ff53fcb';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Thu, 04 Jun 2026 17:33:55 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 04 Jun 2026 17:33:55 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 04 Jun 2026 17:33:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Jun 2026 17:33:55 GMT
STOPSIGNAL SIGTERM
# Thu, 04 Jun 2026 17:33:55 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 04 Jun 2026 17:33:55 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2391e332f9948e1c75e341a452c5d205eacead62107e5b4cbc51232b03c5db1`  
		Last Modified: Thu, 04 Jun 2026 17:34:13 GMT  
		Size: 1.1 MB (1050295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbffa01733a3f820061bd0231f71f494d2a822a628d9db83bb4ed80afbf22c9`  
		Last Modified: Thu, 04 Jun 2026 17:34:15 GMT  
		Size: 107.9 MB (107890500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8117cadeb3d7793473733ba79b60bee221e3c3a7ea59038af8b5fac682c8ab3`  
		Last Modified: Thu, 04 Jun 2026 17:34:13 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf9a846b2eb247c729992464823ed673fd1707045d6a7740c6ee755cd82fc40`  
		Last Modified: Thu, 04 Jun 2026 17:34:11 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.2.2_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:03cbabd17c7f2a8171a5f3903b81840c8e33d9572b76c660907d926bc62846b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2339375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2944937bc53a37c64f3350884ba9fa80af89c8d894d35c20fc57c245582d25f0`

```dockerfile
```

-	Layers:
	-	`sha256:d39c45b44975e99b1587f6cc0597a9d45c6ba3bb5c7edc1a105f4bd706232099`  
		Last Modified: Thu, 04 Jun 2026 17:34:13 GMT  
		Size: 2.3 MB (2317561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9cb0f25fc0581a268f21166e0f51bbe9ecaeb634b706c77277c203b92364d41`  
		Last Modified: Thu, 04 Jun 2026 17:34:13 GMT  
		Size: 21.8 KB (21814 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ee-8.1.2.2_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:ec5439e4d7128e2d448f1519daec78ef9b34764011878d9cca7463be791006a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134927329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53c9db7fe96f5c5ba1812251a29c6eabb91f4fccdec16a161f0e562dd4a2341`
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
# Thu, 04 Jun 2026 17:33:40 GMT
LABEL org.opencontainers.image.title=Aerospike Enterprise Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.2 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Thu, 04 Jun 2026 17:33:40 GMT
ARG AEROSPIKE_EDITION=enterprise
# Thu, 04 Jun 2026 17:33:40 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Thu, 04 Jun 2026 17:33:40 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Thu, 04 Jun 2026 17:33:40 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jun 2026 17:33:54 GMT
# ARGS: AEROSPIKE_EDITION=enterprise
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.2/aerospike-server-enterprise_8.1.2.2_tools-13.0.1_ubuntu24.04_x86_64.tgz';         pkgSha='a04ebcb7546ea4bc7e72b71054da58c0fb3aa150a63f3662c655314436ced1a7';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-enterprise/8.1.2.2/aerospike-server-enterprise_8.1.2.2_tools-13.0.1_ubuntu24.04_aarch64.tgz';         pkgSha='6ed0285d6c81c81689ca408b94c1704317510ced9c01d56b9057fae48ff53fcb';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Thu, 04 Jun 2026 17:33:54 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Thu, 04 Jun 2026 17:33:54 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Thu, 04 Jun 2026 17:33:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Jun 2026 17:33:54 GMT
STOPSIGNAL SIGTERM
# Thu, 04 Jun 2026 17:33:54 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 04 Jun 2026 17:33:54 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a20d6c68c1a3dd6538f24493296fed23e3bbf17a0c390bb8f6bf34f80bdebe`  
		Last Modified: Thu, 04 Jun 2026 17:34:11 GMT  
		Size: 1.0 MB (1032477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec813682bf8c77144d48626844d6485d2c990e5aeba08591eccb863d20b7207`  
		Last Modified: Thu, 04 Jun 2026 17:34:13 GMT  
		Size: 105.0 MB (105016138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf32e423940d6581a1cda0112c49e46496d0b72449388f3cf410b90fe600ea8`  
		Last Modified: Thu, 04 Jun 2026 17:34:10 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf9a846b2eb247c729992464823ed673fd1707045d6a7740c6ee755cd82fc40`  
		Last Modified: Thu, 04 Jun 2026 17:34:11 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ee-8.1.2.2_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:7d1e18b5ed75c950441da23b3c8d009965411475801b4bf48682ee238594bfd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2340580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c945acc125ed9e5a6156b1da2ebffbb712f8f88bbfafc749c1ba477a22dd9977`

```dockerfile
```

-	Layers:
	-	`sha256:0e0d799834ef403d5083b2274e2c9f4d9d1bab28bcbd804842c01cec84302cd9`  
		Last Modified: Thu, 04 Jun 2026 17:34:11 GMT  
		Size: 2.3 MB (2318671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b18496c0cb5390863b6d4e8e0e7741e019e6c252b65e77e86d6bf4764e3753a`  
		Last Modified: Thu, 04 Jun 2026 17:34:11 GMT  
		Size: 21.9 KB (21909 bytes)  
		MIME: application/vnd.in-toto+json
