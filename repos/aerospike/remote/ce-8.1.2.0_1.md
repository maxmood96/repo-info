## `aerospike:ce-8.1.2.0_1`

```console
$ docker pull aerospike@sha256:908bec2c151d6da51425d275e174ae2a63622ee7eaf74dea04e40865337ad970
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `aerospike:ce-8.1.2.0_1` - linux; amd64

```console
$ docker pull aerospike@sha256:229d5829e187084adf3bbd531992e3ae3c8ac94bb418c55f2cce12fd9da3788a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131793322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c2e0c8190af9d7225e572993d356e08495e3dbd9302e85adf5e5f3abde47f5`
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
# Tue, 28 Apr 2026 20:34:56 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.0 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 28 Apr 2026 20:34:56 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 28 Apr 2026 20:34:56 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 28 Apr 2026 20:34:56 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 28 Apr 2026 20:34:56 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 20:35:12 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.0/aerospike-server-community_8.1.2.0_tools-13.0.0_ubuntu24.04_x86_64.tgz';         pkgSha='bef8a6acf697837d037a8608b913d61ee01e4d03c22a986eafe5d56289aaa91e';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.0/aerospike-server-community_8.1.2.0_tools-13.0.0_ubuntu24.04_aarch64.tgz';         pkgSha='f8859425a8a6a4a3cca8dd3728dd154c45ba9f42529f079b1182b5d428d0c54c';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Tue, 28 Apr 2026 20:35:12 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 28 Apr 2026 20:35:12 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 28 Apr 2026 20:35:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 28 Apr 2026 20:35:12 GMT
STOPSIGNAL SIGTERM
# Tue, 28 Apr 2026 20:35:12 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 28 Apr 2026 20:35:12 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dba69c08784572ef33c2bba7bda71f7dbdb0532c69fdcdd703274aa78a589e`  
		Last Modified: Tue, 28 Apr 2026 20:35:27 GMT  
		Size: 1.1 MB (1050146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fd4c25185e8dc4aaf8b71d7a2dec10faf02590682229e1aec7340834fd128d`  
		Last Modified: Tue, 28 Apr 2026 20:35:30 GMT  
		Size: 101.0 MB (101007902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c82c383cd28fd3f94175a34db462a6a56dab30fcaee6c61ee5e39a3caf1269c`  
		Last Modified: Tue, 28 Apr 2026 20:35:27 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c7fac996f9ad8592f911b8acb78f80e6e017a8a86d42db2bbe9510b434f2d3`  
		Last Modified: Tue, 28 Apr 2026 20:35:28 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.2.0_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:cc17601cfe22b7d832f0fbd03af66cc5e159109967b7b00f1fd4471027ac3b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2236796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00b0bf0aa9d70388a677c10472eba1ee261f2a4203c99bb9624a659ebfb7c37`

```dockerfile
```

-	Layers:
	-	`sha256:7297d31afad08bb61f6134e8958c24cd23a37d4d92513a44d018561cf6b544ae`  
		Last Modified: Tue, 28 Apr 2026 20:35:28 GMT  
		Size: 2.2 MB (2215000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbdc5b69ec58263dffd997a0f934bae61a126ed2f0e948100139ebb8bceb4d8c`  
		Last Modified: Tue, 28 Apr 2026 20:35:27 GMT  
		Size: 21.8 KB (21796 bytes)  
		MIME: application/vnd.in-toto+json

### `aerospike:ce-8.1.2.0_1` - linux; arm64 variant v8

```console
$ docker pull aerospike@sha256:4cba79b4ec588b0f5c871010cce67c41cda23bbb2a23879911806521a61cebc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127915261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be5aba1d3874c68cd497030e066e80d8b6632f875d541b3513a9dd58b3b9368`
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
# Tue, 28 Apr 2026 20:34:48 GMT
LABEL org.opencontainers.image.title=Aerospike Community Server org.opencontainers.image.description=Aerospike is a real-time database with predictable performance at petabyte scale with microsecond latency over billions of transactions. org.opencontainers.image.documentation=https://hub.docker.com/_/aerospike org.opencontainers.image.base.name=docker.io/library/ubuntu:24.04 org.opencontainers.image.source=https://github.com/aerospike/aerospike-server.docker org.opencontainers.image.vendor=Aerospike org.opencontainers.image.version=8.1.2.0 org.opencontainers.image.url=https://github.com/aerospike/aerospike-server.docker
# Tue, 28 Apr 2026 20:34:48 GMT
ARG AEROSPIKE_EDITION=community
# Tue, 28 Apr 2026 20:34:48 GMT
ENV AEROSPIKE_LINUX_BASE=ubuntu:24.04
# Tue, 28 Apr 2026 20:34:48 GMT
SHELL [/bin/bash -Eeuo pipefail -c]
# Tue, 28 Apr 2026 20:34:48 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN apt-get update;   apt-get install -y --no-install-recommends     ca-certificates     procps   ;   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 20:35:07 GMT
# ARGS: AEROSPIKE_EDITION=community
RUN {     apt-get update;     apt-get install -y --no-install-recommends curl;     ARCH="$(dpkg --print-architecture)";     if [ "${ARCH}" = "amd64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static';         tiniSha='d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.0/aerospike-server-community_8.1.2.0_tools-13.0.0_ubuntu24.04_x86_64.tgz';         pkgSha='bef8a6acf697837d037a8608b913d61ee01e4d03c22a986eafe5d56289aaa91e';     elif [ "${ARCH}" = "arm64" ]; then         tiniUrl='https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static-arm64';         tiniSha='1c398e5283af2f33888b7d8ac5b01ac89f777ea27c85d25866a40d1e64d0341b';         pkgLink='https://download.aerospike.com/artifacts/aerospike-server-community/8.1.2.0/aerospike-server-community_8.1.2.0_tools-13.0.0_ubuntu24.04_aarch64.tgz';         pkgSha='f8859425a8a6a4a3cca8dd3728dd154c45ba9f42529f079b1182b5d428d0c54c';     else         echo >&2 "error: unsupported architecture '${ARCH}'";         exit 1;     fi;   };   {     curl -fL -o /usr/bin/as-tini-static "${tiniUrl}";     echo "${tiniSha} */usr/bin/as-tini-static" | sha256sum --strict --check -;     chmod +x /usr/bin/as-tini-static;   };   {     mkdir -p /tmp/aerospike;     curl -fL -o /tmp/aerospike/pkg.tgz "${pkgLink}";     echo "${pkgSha} */tmp/aerospike/pkg.tgz" | sha256sum --strict --check -;     tar -xzf /tmp/aerospike/pkg.tgz --strip-components=1 -C /tmp/aerospike;   };   {     apt-get install -y --no-install-recommends         /tmp/aerospike/aerospike-server-*.deb         /tmp/aerospike/aerospike-tools*.deb;   };   {     mkdir -p /etc/aerospike /licenses /var/log/aerospike /var/run/aerospike;     cp /tmp/aerospike/LICENSE /licenses/;     if [ "${AEROSPIKE_EDITION}" = "enterprise" ] || [ "${AEROSPIKE_EDITION}" = "federal" ]; then         if [ -f /tmp/aerospike/features.conf ]; then             cp /tmp/aerospike/features.conf /etc/aerospike/features.conf;         fi;     fi;     rm -rf /tmp/aerospike;     apt-mark auto curl;     apt-get autoremove -y --purge;     rm -rf /var/lib/apt/lists/*;   };   echo "done"; # buildkit
# Tue, 28 Apr 2026 20:35:07 GMT
COPY aerospike.template.conf /etc/aerospike/aerospike.template.conf # buildkit
# Tue, 28 Apr 2026 20:35:07 GMT
EXPOSE map[3000/tcp:{} 3001/tcp:{} 3002/tcp:{}]
# Tue, 28 Apr 2026 20:35:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 28 Apr 2026 20:35:07 GMT
STOPSIGNAL SIGTERM
# Tue, 28 Apr 2026 20:35:07 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 28 Apr 2026 20:35:07 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac3cf76d394f68d87a7ed438aebce621f6faf8de4915a80965f5e4f1d78308c`  
		Last Modified: Tue, 28 Apr 2026 20:35:22 GMT  
		Size: 1.0 MB (1032405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be26fd59b1620665d8838f97f1ef62b9a88101e74540dc5037b679838519857`  
		Last Modified: Tue, 28 Apr 2026 20:35:25 GMT  
		Size: 98.0 MB (98004771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63b9b49453662d4f67cf17a9d2345159ab29ff26b9ef38f6883daeeae930de7`  
		Last Modified: Tue, 28 Apr 2026 20:35:22 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e41458a767188921723f4c3ab7240066cf8b46d89bbd9ae797f46926b0a028e`  
		Last Modified: Tue, 28 Apr 2026 20:35:22 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `aerospike:ce-8.1.2.0_1` - unknown; unknown

```console
$ docker pull aerospike@sha256:fad8f8f2bf74ce2107449a8c32f8d263cd2d054f9d0030343f154a2a75f1d496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2237981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17f35ee55d1dcf4063f300aeb19d28922a3e1fef9574e9e3770beec0bac8391`

```dockerfile
```

-	Layers:
	-	`sha256:96a0d927f25bd134a790b702fa54f371fdb33de7b4d1aa4825cf5d605b5b5c10`  
		Last Modified: Tue, 28 Apr 2026 20:35:22 GMT  
		Size: 2.2 MB (2216092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30d904a88a2b39c2df4c5e483b1cba5fea3ff985c4f0a1cb5431c863633af742`  
		Last Modified: Tue, 28 Apr 2026 20:35:22 GMT  
		Size: 21.9 KB (21889 bytes)  
		MIME: application/vnd.in-toto+json
