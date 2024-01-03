## `emqx:latest`

```console
$ docker pull emqx@sha256:b58c03f0e106e1f0e619aa102b3ee51ba09dd60cbf4c109f90290b938c6a48ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:aff5b3f9ce9862eed9c4557f9c6cc3e798843c93ada17b34ccb86ac39b12e27c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118704673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbcd2554aa5aed45a507d0490f69813101a58a02197c172489d6c44f97975b8b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 19:19:56 GMT
ENV EMQX_VERSION=5.4.0
# Wed, 03 Jan 2024 19:19:56 GMT
ENV AMD64_SHA256=5572dccf3704dbd910f145fe19882fa30fdd9132113d0a28110444d4d5685a3f
# Wed, 03 Jan 2024 19:19:56 GMT
ENV ARM64_SHA256=0dbe92966a93054a8dca89762c00b06a44659c7921177feb291a5ddd5340cefc
# Wed, 03 Jan 2024 19:19:57 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 Jan 2024 19:20:13 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 19:20:13 GMT
WORKDIR /opt/emqx
# Wed, 03 Jan 2024 19:20:13 GMT
USER emqx
# Wed, 03 Jan 2024 19:20:13 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 Jan 2024 19:20:14 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 03 Jan 2024 19:20:14 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 03 Jan 2024 19:20:14 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 Jan 2024 19:20:14 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b40ce22fb6882b48b845829080e0fe884a0b6e08ecf4afaac5bc55dc1d4662`  
		Last Modified: Wed, 03 Jan 2024 19:20:38 GMT  
		Size: 87.3 MB (87285898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187072439c197ab4d344bdd676c79e88e5712ba8b2c20f3a0aaa2a2ab7a45d11`  
		Last Modified: Wed, 03 Jan 2024 19:20:28 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:5ccd09ad8dd1320627283fc479a3b760add3a04d32da2cece1eea1718c541f71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108466312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e221710e68ca5dc18d8b139ca8c1f2fb9d9da2aa793cd9b35a0fad72c6f914b5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 19:39:37 GMT
ENV EMQX_VERSION=5.4.0
# Wed, 03 Jan 2024 19:39:37 GMT
ENV AMD64_SHA256=5572dccf3704dbd910f145fe19882fa30fdd9132113d0a28110444d4d5685a3f
# Wed, 03 Jan 2024 19:39:37 GMT
ENV ARM64_SHA256=0dbe92966a93054a8dca89762c00b06a44659c7921177feb291a5ddd5340cefc
# Wed, 03 Jan 2024 19:39:37 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 Jan 2024 19:39:50 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 19:39:51 GMT
WORKDIR /opt/emqx
# Wed, 03 Jan 2024 19:39:51 GMT
USER emqx
# Wed, 03 Jan 2024 19:39:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 Jan 2024 19:39:51 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 03 Jan 2024 19:39:51 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 03 Jan 2024 19:39:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 Jan 2024 19:39:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000db8836b7a4dcf705932e61e11e1c8af7870412c338e39e234bce09ccb3a26`  
		Last Modified: Wed, 03 Jan 2024 19:40:10 GMT  
		Size: 78.4 MB (78401356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f84d1cbfd874e0a6e42d7872df4925361685c19d66d456d85f3b253e6281c6`  
		Last Modified: Wed, 03 Jan 2024 19:40:03 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
