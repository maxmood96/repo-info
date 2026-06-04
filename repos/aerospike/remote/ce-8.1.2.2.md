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
