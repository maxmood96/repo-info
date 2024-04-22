<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.1`](#emqx51)
-	[`emqx:5.1.6`](#emqx516)
-	[`emqx:5.2`](#emqx52)
-	[`emqx:5.2.1`](#emqx521)
-	[`emqx:5.3`](#emqx53)
-	[`emqx:5.3.2`](#emqx532)
-	[`emqx:5.4`](#emqx54)
-	[`emqx:5.4.1`](#emqx541)
-	[`emqx:5.5`](#emqx55)
-	[`emqx:5.5.1`](#emqx551)
-	[`emqx:5.6`](#emqx56)
-	[`emqx:5.6.1`](#emqx561)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:edb27d4b20dfc466393cd352d8cdc55a369136f307fb19586b021f8708a92698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:30881c725b75da9f0d89a10366ffa8bf0ae749cda098b530a2f641000942f0e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124184594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d269f2003c9d50e119df8a24963e50f4bb7c3fe974be6287c666388ed268f15`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 18:24:41 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 18:24:41 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 18:24:42 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 18:24:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 18:24:57 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 22 Apr 2024 18:24:57 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 18:24:57 GMT
USER emqx
# Mon, 22 Apr 2024 18:24:57 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 18:24:57 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Mon, 22 Apr 2024 18:24:58 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Mon, 22 Apr 2024 18:24:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 18:24:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99faa8eeb4e25dfc780ba176527f797072c71b1fd864ebbf986547567c2b1acc`  
		Last Modified: Mon, 22 Apr 2024 18:25:27 GMT  
		Size: 95.1 MB (95052202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d58b6d6c1d7d342e1eddf4c4ab2068f5b4088cf1831a617d9700205bee2dbe5`  
		Last Modified: Mon, 22 Apr 2024 18:25:17 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:4d7e9f32d5dccf6faf2d23fca41df6b427825a542c278601458853790fbe0cfc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120775975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75b0b6066bd0a469d2953b967242684ba353813deed6b9825611f90934e9cd1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 17:41:57 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 17:41:57 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 17:41:57 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 17:41:57 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 17:42:10 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 22 Apr 2024 17:42:11 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 17:42:12 GMT
USER emqx
# Mon, 22 Apr 2024 17:42:12 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 17:42:12 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Mon, 22 Apr 2024 17:42:12 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Mon, 22 Apr 2024 17:42:12 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 17:42:12 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469c7f8258b8fcbca771d436a752dc7fb67eed640784f665297450001139a320`  
		Last Modified: Mon, 22 Apr 2024 17:42:40 GMT  
		Size: 91.6 MB (91612782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3fc26722d2c686504c8cf5bea418f9b63e85934d164e33c86e8cda55d36946`  
		Last Modified: Mon, 22 Apr 2024 17:42:32 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1`

```console
$ docker pull emqx@sha256:6b7d1a0b4e5721ddc2e6721095c961821efb5e60932e04a18c9fe94edb9ab02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1` - linux; amd64

```console
$ docker pull emqx@sha256:0643ee036a68c68147288e58613e595e5e5ccc4338d8f834d50bcd14c6008363
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102402310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76180abb30b2557a88028bcf792b092096879c3daea9071052e8254a7f1d244b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:09:22 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:09:23 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 10 Apr 2024 07:09:23 GMT
ENV EMQX_VERSION=5.1.6
# Wed, 10 Apr 2024 07:09:23 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Wed, 10 Apr 2024 07:09:23 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Wed, 10 Apr 2024 07:09:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 07:09:30 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 10 Apr 2024 07:09:31 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 07:09:31 GMT
USER emqx
# Wed, 10 Apr 2024 07:09:31 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 07:09:31 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 07:09:31 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 10 Apr 2024 07:09:31 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:09:31 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb75347c57d452dccf220e908f0594851a6a0af43ebc5cdbc2218cbb7b8e045`  
		Last Modified: Wed, 10 Apr 2024 07:11:30 GMT  
		Size: 3.0 MB (2988332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e37a9e4690a29cfeaf903962d665f4dcf7f9cec23880039e62e3fb4e3c7ef9`  
		Last Modified: Wed, 10 Apr 2024 07:11:30 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15ae4f84de9e5883c178ab5efae48ce4bc4fae3560e9a2dca47dd3103acd765`  
		Last Modified: Wed, 10 Apr 2024 07:11:37 GMT  
		Size: 68.0 MB (67981233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77fb989d7d6376a44f9adaa549cb50e768fadd243db9827b1cad74ee3898c97`  
		Last Modified: Wed, 10 Apr 2024 07:11:30 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:ee40939f497418615d39efc4c1d77a6460887d8d2bcd3a5eb9da929ab60163fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92710406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa84f628673a0a323214f478f3abba1f381e9aebd8d1eed0abc040c3ff6a04a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 10:35:48 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 10:35:48 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 10 Apr 2024 10:35:48 GMT
ENV EMQX_VERSION=5.1.6
# Wed, 10 Apr 2024 10:35:48 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Wed, 10 Apr 2024 10:35:48 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Wed, 10 Apr 2024 10:35:48 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 10:35:54 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 10 Apr 2024 10:35:55 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 10:35:55 GMT
USER emqx
# Wed, 10 Apr 2024 10:35:55 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 10:35:55 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 10:35:55 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 10 Apr 2024 10:35:55 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 10:35:55 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d5805c7ae4428de3ad92547a1a8550cb6e409961c06499c4d3a4251b944895`  
		Last Modified: Wed, 10 Apr 2024 10:37:33 GMT  
		Size: 3.0 MB (3004459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64032c0c3350a8edd116cd062dbb79adbc8a6e9f2e467502611cc4d3d8b5d48`  
		Last Modified: Wed, 10 Apr 2024 10:37:33 GMT  
		Size: 4.1 KB (4108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c59b75b2fbba7db827ac680bdcb13277f769f78372c4728d50fbea35e95102`  
		Last Modified: Wed, 10 Apr 2024 10:37:38 GMT  
		Size: 59.6 MB (59624629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7c9a9866fb4ce3f0821bac867ad140b2af4deda924d41cf26836986b210795`  
		Last Modified: Wed, 10 Apr 2024 10:37:33 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1.6`

```console
$ docker pull emqx@sha256:6b7d1a0b4e5721ddc2e6721095c961821efb5e60932e04a18c9fe94edb9ab02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1.6` - linux; amd64

```console
$ docker pull emqx@sha256:0643ee036a68c68147288e58613e595e5e5ccc4338d8f834d50bcd14c6008363
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102402310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76180abb30b2557a88028bcf792b092096879c3daea9071052e8254a7f1d244b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:09:22 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:09:23 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 10 Apr 2024 07:09:23 GMT
ENV EMQX_VERSION=5.1.6
# Wed, 10 Apr 2024 07:09:23 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Wed, 10 Apr 2024 07:09:23 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Wed, 10 Apr 2024 07:09:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 07:09:30 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 10 Apr 2024 07:09:31 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 07:09:31 GMT
USER emqx
# Wed, 10 Apr 2024 07:09:31 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 07:09:31 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 07:09:31 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 10 Apr 2024 07:09:31 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:09:31 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb75347c57d452dccf220e908f0594851a6a0af43ebc5cdbc2218cbb7b8e045`  
		Last Modified: Wed, 10 Apr 2024 07:11:30 GMT  
		Size: 3.0 MB (2988332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e37a9e4690a29cfeaf903962d665f4dcf7f9cec23880039e62e3fb4e3c7ef9`  
		Last Modified: Wed, 10 Apr 2024 07:11:30 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15ae4f84de9e5883c178ab5efae48ce4bc4fae3560e9a2dca47dd3103acd765`  
		Last Modified: Wed, 10 Apr 2024 07:11:37 GMT  
		Size: 68.0 MB (67981233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77fb989d7d6376a44f9adaa549cb50e768fadd243db9827b1cad74ee3898c97`  
		Last Modified: Wed, 10 Apr 2024 07:11:30 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.1.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:ee40939f497418615d39efc4c1d77a6460887d8d2bcd3a5eb9da929ab60163fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92710406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa84f628673a0a323214f478f3abba1f381e9aebd8d1eed0abc040c3ff6a04a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 10:35:48 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 10:35:48 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 10 Apr 2024 10:35:48 GMT
ENV EMQX_VERSION=5.1.6
# Wed, 10 Apr 2024 10:35:48 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Wed, 10 Apr 2024 10:35:48 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Wed, 10 Apr 2024 10:35:48 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 10:35:54 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 10 Apr 2024 10:35:55 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 10:35:55 GMT
USER emqx
# Wed, 10 Apr 2024 10:35:55 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 10:35:55 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 10:35:55 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 10 Apr 2024 10:35:55 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 10:35:55 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d5805c7ae4428de3ad92547a1a8550cb6e409961c06499c4d3a4251b944895`  
		Last Modified: Wed, 10 Apr 2024 10:37:33 GMT  
		Size: 3.0 MB (3004459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64032c0c3350a8edd116cd062dbb79adbc8a6e9f2e467502611cc4d3d8b5d48`  
		Last Modified: Wed, 10 Apr 2024 10:37:33 GMT  
		Size: 4.1 KB (4108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c59b75b2fbba7db827ac680bdcb13277f769f78372c4728d50fbea35e95102`  
		Last Modified: Wed, 10 Apr 2024 10:37:38 GMT  
		Size: 59.6 MB (59624629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7c9a9866fb4ce3f0821bac867ad140b2af4deda924d41cf26836986b210795`  
		Last Modified: Wed, 10 Apr 2024 10:37:33 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2`

```console
$ docker pull emqx@sha256:828ba7df3eea964a80f66a5ee01aa1abd9e4566bfc03f39e68224eeb515c7859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2` - linux; amd64

```console
$ docker pull emqx@sha256:c7842d4a63d6f2ac6d385f714f382c5ee2a63b4454840674814a6abda6bfc4cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101172431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02cf8be8d7d1856c4cb09c41522e9d94fa6f4da7038b735cd19a94c251a09748`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:09:41 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:09:42 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 10 Apr 2024 07:09:42 GMT
ENV EMQX_VERSION=5.2.1
# Wed, 10 Apr 2024 07:09:42 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Wed, 10 Apr 2024 07:09:42 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Wed, 10 Apr 2024 07:09:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 07:09:53 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Wed, 10 Apr 2024 07:09:54 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 07:09:54 GMT
USER emqx
# Wed, 10 Apr 2024 07:09:54 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 07:09:54 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 07:09:54 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 10 Apr 2024 07:09:54 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:09:54 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659bee472f61e6a5c34eeeeb6b52574444c8f0f00fee74a8d7647be4feec6332`  
		Last Modified: Wed, 10 Apr 2024 07:11:47 GMT  
		Size: 1.6 MB (1629581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e3164039a5500ecd1b07faccf899e4c31871251f9733ec1948fc78fe32e305`  
		Last Modified: Wed, 10 Apr 2024 07:11:46 GMT  
		Size: 4.1 KB (4100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0db93238eabe5784aacd12eb497a576d4b67a8f47b2b042c2e8157f463086d6`  
		Last Modified: Wed, 10 Apr 2024 07:11:53 GMT  
		Size: 68.1 MB (68110109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a22bc1c301f31f63c12ddb59c936825db2a363474fbad4e8a497997d838905`  
		Last Modified: Wed, 10 Apr 2024 07:11:46 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:180e19ff6a98a0e30faf3befc99e1e60e89df91b53a520e7f48037c6ce856ab2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91476457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d55c20a67323bff87778e18cba0650cd1e24ffd59302e70e02a5bad6846cb6`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 10:36:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 10:36:04 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 10 Apr 2024 10:36:04 GMT
ENV EMQX_VERSION=5.2.1
# Wed, 10 Apr 2024 10:36:04 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Wed, 10 Apr 2024 10:36:04 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Wed, 10 Apr 2024 10:36:04 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 10:36:13 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Wed, 10 Apr 2024 10:36:13 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 10:36:13 GMT
USER emqx
# Wed, 10 Apr 2024 10:36:13 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 10:36:14 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 10:36:14 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 10 Apr 2024 10:36:14 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 10:36:14 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d572ff4a3f92d27f016982c3850c9d19bfc77f901d6c17499c392008564d27`  
		Last Modified: Wed, 10 Apr 2024 10:37:46 GMT  
		Size: 1.6 MB (1644150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019fa610161bfd0ddc70c244a2ef9eda05f0f9c719bdf727b21779855f52c055`  
		Last Modified: Wed, 10 Apr 2024 10:37:46 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9fdb72ee1aed6a850cebd3fa8248cd5c46592553a05abb48a010da5c7aa52c`  
		Last Modified: Wed, 10 Apr 2024 10:37:51 GMT  
		Size: 59.8 MB (59750987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af773b332edbe5a9743f32302e30e69f498716a0cfce080d78b8ea18d1caee76`  
		Last Modified: Wed, 10 Apr 2024 10:37:46 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2.1`

```console
$ docker pull emqx@sha256:828ba7df3eea964a80f66a5ee01aa1abd9e4566bfc03f39e68224eeb515c7859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2.1` - linux; amd64

```console
$ docker pull emqx@sha256:c7842d4a63d6f2ac6d385f714f382c5ee2a63b4454840674814a6abda6bfc4cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101172431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02cf8be8d7d1856c4cb09c41522e9d94fa6f4da7038b735cd19a94c251a09748`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:09:41 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:09:42 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 10 Apr 2024 07:09:42 GMT
ENV EMQX_VERSION=5.2.1
# Wed, 10 Apr 2024 07:09:42 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Wed, 10 Apr 2024 07:09:42 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Wed, 10 Apr 2024 07:09:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 07:09:53 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Wed, 10 Apr 2024 07:09:54 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 07:09:54 GMT
USER emqx
# Wed, 10 Apr 2024 07:09:54 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 07:09:54 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 07:09:54 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 10 Apr 2024 07:09:54 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:09:54 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659bee472f61e6a5c34eeeeb6b52574444c8f0f00fee74a8d7647be4feec6332`  
		Last Modified: Wed, 10 Apr 2024 07:11:47 GMT  
		Size: 1.6 MB (1629581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e3164039a5500ecd1b07faccf899e4c31871251f9733ec1948fc78fe32e305`  
		Last Modified: Wed, 10 Apr 2024 07:11:46 GMT  
		Size: 4.1 KB (4100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0db93238eabe5784aacd12eb497a576d4b67a8f47b2b042c2e8157f463086d6`  
		Last Modified: Wed, 10 Apr 2024 07:11:53 GMT  
		Size: 68.1 MB (68110109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a22bc1c301f31f63c12ddb59c936825db2a363474fbad4e8a497997d838905`  
		Last Modified: Wed, 10 Apr 2024 07:11:46 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.2.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:180e19ff6a98a0e30faf3befc99e1e60e89df91b53a520e7f48037c6ce856ab2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91476457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d55c20a67323bff87778e18cba0650cd1e24ffd59302e70e02a5bad6846cb6`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 10:36:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 10:36:04 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 10 Apr 2024 10:36:04 GMT
ENV EMQX_VERSION=5.2.1
# Wed, 10 Apr 2024 10:36:04 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Wed, 10 Apr 2024 10:36:04 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Wed, 10 Apr 2024 10:36:04 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 10:36:13 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Wed, 10 Apr 2024 10:36:13 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 10:36:13 GMT
USER emqx
# Wed, 10 Apr 2024 10:36:13 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 10:36:14 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 10:36:14 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 10 Apr 2024 10:36:14 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 10:36:14 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d572ff4a3f92d27f016982c3850c9d19bfc77f901d6c17499c392008564d27`  
		Last Modified: Wed, 10 Apr 2024 10:37:46 GMT  
		Size: 1.6 MB (1644150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019fa610161bfd0ddc70c244a2ef9eda05f0f9c719bdf727b21779855f52c055`  
		Last Modified: Wed, 10 Apr 2024 10:37:46 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9fdb72ee1aed6a850cebd3fa8248cd5c46592553a05abb48a010da5c7aa52c`  
		Last Modified: Wed, 10 Apr 2024 10:37:51 GMT  
		Size: 59.8 MB (59750987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af773b332edbe5a9743f32302e30e69f498716a0cfce080d78b8ea18d1caee76`  
		Last Modified: Wed, 10 Apr 2024 10:37:46 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3`

```console
$ docker pull emqx@sha256:6a580fce9aeeda4259ee8f204eae0b87ee1d155b7b47d1566d8d07d9747af557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3` - linux; amd64

```console
$ docker pull emqx@sha256:e5f1af09cac9d50e42fd97cc2e93ee9f9cc118f09803a4f5fd74827ed2362a31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101788561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600c659e067ff96b2bff11f1c964d80e643f7a88dc65b322fb7c8c4147823fc1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:09:57 GMT
ENV EMQX_VERSION=5.3.2
# Wed, 10 Apr 2024 07:09:57 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Wed, 10 Apr 2024 07:09:57 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Wed, 10 Apr 2024 07:09:57 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 07:10:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:10:11 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 07:10:11 GMT
USER emqx
# Wed, 10 Apr 2024 07:10:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 07:10:12 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 07:10:12 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 10 Apr 2024 07:10:12 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:10:12 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a97575f9a741c04405eaf409f32f3383756408e452b1f8254eadfa1818cbe5`  
		Last Modified: Wed, 10 Apr 2024 07:12:09 GMT  
		Size: 70.4 MB (70359921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db5db75a5d47b30115b1cea0d499181edd6019befbfdec1c5d74f93f80e273b`  
		Last Modified: Wed, 10 Apr 2024 07:12:01 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b8eb69c00ef0fd90d5bf3c7ed423dba1423dfe1e587c5d16c53eff8eb1c4ff2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92091111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4315d7deb5a748f9f7a895c1525619158b4b0cc486bd863d4ab23cd4115ef694`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 10:36:16 GMT
ENV EMQX_VERSION=5.3.2
# Wed, 10 Apr 2024 10:36:16 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Wed, 10 Apr 2024 10:36:16 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Wed, 10 Apr 2024 10:36:16 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 10:36:27 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 10:36:27 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 10:36:27 GMT
USER emqx
# Wed, 10 Apr 2024 10:36:27 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 10:36:28 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 10:36:28 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 10 Apr 2024 10:36:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 10:36:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18facfbf0c2daf24d35a575d53926bddb0a04d9a10c96fde60690ec773c7be9`  
		Last Modified: Wed, 10 Apr 2024 10:38:04 GMT  
		Size: 62.0 MB (62013903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872d05c30441c2536cc7fc4d8c67bee79799051ab1a9c52ae524d881cd8783d5`  
		Last Modified: Wed, 10 Apr 2024 10:37:58 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3.2`

```console
$ docker pull emqx@sha256:6a580fce9aeeda4259ee8f204eae0b87ee1d155b7b47d1566d8d07d9747af557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3.2` - linux; amd64

```console
$ docker pull emqx@sha256:e5f1af09cac9d50e42fd97cc2e93ee9f9cc118f09803a4f5fd74827ed2362a31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101788561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600c659e067ff96b2bff11f1c964d80e643f7a88dc65b322fb7c8c4147823fc1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:09:57 GMT
ENV EMQX_VERSION=5.3.2
# Wed, 10 Apr 2024 07:09:57 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Wed, 10 Apr 2024 07:09:57 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Wed, 10 Apr 2024 07:09:57 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 07:10:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:10:11 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 07:10:11 GMT
USER emqx
# Wed, 10 Apr 2024 07:10:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 07:10:12 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 07:10:12 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 10 Apr 2024 07:10:12 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:10:12 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a97575f9a741c04405eaf409f32f3383756408e452b1f8254eadfa1818cbe5`  
		Last Modified: Wed, 10 Apr 2024 07:12:09 GMT  
		Size: 70.4 MB (70359921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db5db75a5d47b30115b1cea0d499181edd6019befbfdec1c5d74f93f80e273b`  
		Last Modified: Wed, 10 Apr 2024 07:12:01 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.3.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b8eb69c00ef0fd90d5bf3c7ed423dba1423dfe1e587c5d16c53eff8eb1c4ff2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92091111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4315d7deb5a748f9f7a895c1525619158b4b0cc486bd863d4ab23cd4115ef694`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 10:36:16 GMT
ENV EMQX_VERSION=5.3.2
# Wed, 10 Apr 2024 10:36:16 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Wed, 10 Apr 2024 10:36:16 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Wed, 10 Apr 2024 10:36:16 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 10:36:27 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 10:36:27 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 10:36:27 GMT
USER emqx
# Wed, 10 Apr 2024 10:36:27 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 10:36:28 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 10:36:28 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 10 Apr 2024 10:36:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 10:36:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18facfbf0c2daf24d35a575d53926bddb0a04d9a10c96fde60690ec773c7be9`  
		Last Modified: Wed, 10 Apr 2024 10:38:04 GMT  
		Size: 62.0 MB (62013903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872d05c30441c2536cc7fc4d8c67bee79799051ab1a9c52ae524d881cd8783d5`  
		Last Modified: Wed, 10 Apr 2024 10:37:58 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.4`

```console
$ docker pull emqx@sha256:a1bc848fbc31496c16469d52e543eda47fb1c2bbff138aa91b93fe118d0b6e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.4` - linux; amd64

```console
$ docker pull emqx@sha256:b0d4142d8610b259f3d06044083bc2e42fabb6ea4d122b35807508d44fb0c2ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118703418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815f4b8e2c23d2099c7132ced8342732b6e7d8354c9abea90f7f37526cad2176`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:10:18 GMT
ENV EMQX_VERSION=5.4.1
# Wed, 10 Apr 2024 07:10:18 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Wed, 10 Apr 2024 07:10:18 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Wed, 10 Apr 2024 07:10:18 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 07:10:33 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:10:33 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 07:10:34 GMT
USER emqx
# Wed, 10 Apr 2024 07:10:34 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 07:10:34 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 07:10:34 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 10 Apr 2024 07:10:34 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:10:34 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00106a8a1247286972b6d5b4b36692ee17ea2d97c5f334ec7736971208573f8`  
		Last Modified: Wed, 10 Apr 2024 07:12:26 GMT  
		Size: 87.3 MB (87274778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be8c9fc1c2ef13a842fbf6aff2874b9fbc105340b9a6b7eb9d61754fc7fa714`  
		Last Modified: Wed, 10 Apr 2024 07:12:17 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:a11fad2583b88e55d190d3e01ba9d56a377b93e988c22825e847b8d63a86ccca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108486488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86d1cd40e85eae374b8b2eaea22635c94f12953a6f4d8346527f452e7a78c23`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 10:36:30 GMT
ENV EMQX_VERSION=5.4.1
# Wed, 10 Apr 2024 10:36:30 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Wed, 10 Apr 2024 10:36:30 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Wed, 10 Apr 2024 10:36:30 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 10:36:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 10:36:42 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 10:36:42 GMT
USER emqx
# Wed, 10 Apr 2024 10:36:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 10:36:42 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 10:36:42 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 10 Apr 2024 10:36:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 10:36:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13c46b2b0718c8fbcd711d9ee48ea5404a8f951c4b003f3986682831a731f27`  
		Last Modified: Wed, 10 Apr 2024 10:38:18 GMT  
		Size: 78.4 MB (78409279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c851788443bcbdca3cbab1991bab68ad35649e55bba07caa093149cce68ed8`  
		Last Modified: Wed, 10 Apr 2024 10:38:11 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.4.1`

```console
$ docker pull emqx@sha256:a1bc848fbc31496c16469d52e543eda47fb1c2bbff138aa91b93fe118d0b6e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.4.1` - linux; amd64

```console
$ docker pull emqx@sha256:b0d4142d8610b259f3d06044083bc2e42fabb6ea4d122b35807508d44fb0c2ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118703418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815f4b8e2c23d2099c7132ced8342732b6e7d8354c9abea90f7f37526cad2176`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:10:18 GMT
ENV EMQX_VERSION=5.4.1
# Wed, 10 Apr 2024 07:10:18 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Wed, 10 Apr 2024 07:10:18 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Wed, 10 Apr 2024 07:10:18 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 07:10:33 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:10:33 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 07:10:34 GMT
USER emqx
# Wed, 10 Apr 2024 07:10:34 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 07:10:34 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 07:10:34 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 10 Apr 2024 07:10:34 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:10:34 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00106a8a1247286972b6d5b4b36692ee17ea2d97c5f334ec7736971208573f8`  
		Last Modified: Wed, 10 Apr 2024 07:12:26 GMT  
		Size: 87.3 MB (87274778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be8c9fc1c2ef13a842fbf6aff2874b9fbc105340b9a6b7eb9d61754fc7fa714`  
		Last Modified: Wed, 10 Apr 2024 07:12:17 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.4.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:a11fad2583b88e55d190d3e01ba9d56a377b93e988c22825e847b8d63a86ccca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108486488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86d1cd40e85eae374b8b2eaea22635c94f12953a6f4d8346527f452e7a78c23`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 10:36:30 GMT
ENV EMQX_VERSION=5.4.1
# Wed, 10 Apr 2024 10:36:30 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Wed, 10 Apr 2024 10:36:30 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Wed, 10 Apr 2024 10:36:30 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 10:36:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 10:36:42 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 10:36:42 GMT
USER emqx
# Wed, 10 Apr 2024 10:36:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 10:36:42 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 10:36:42 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 10 Apr 2024 10:36:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 10:36:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13c46b2b0718c8fbcd711d9ee48ea5404a8f951c4b003f3986682831a731f27`  
		Last Modified: Wed, 10 Apr 2024 10:38:18 GMT  
		Size: 78.4 MB (78409279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c851788443bcbdca3cbab1991bab68ad35649e55bba07caa093149cce68ed8`  
		Last Modified: Wed, 10 Apr 2024 10:38:11 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.5`

```console
$ docker pull emqx@sha256:79af25fcf47f51dbf5c44ef162ce37404c38a6908bd88255f24f51c250644995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.5` - linux; amd64

```console
$ docker pull emqx@sha256:5efce21eced38b8faa9e37088511728d05e4065b5e279d096a1b61edaebdc68b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121268493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac34f32f6c6596b90f03a6eec508c1fbde04f7171e60d1c7e60583e92b20cd77`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:10:38 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 10 Apr 2024 07:10:38 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 10 Apr 2024 07:10:38 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 10 Apr 2024 07:10:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 07:10:54 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 10 Apr 2024 07:10:54 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 07:10:54 GMT
USER emqx
# Wed, 10 Apr 2024 07:10:54 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 07:10:55 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 07:10:55 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 10 Apr 2024 07:10:55 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:10:55 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135438a2d2de091ce5a0d87c8afd5a17e05038759ea9d60b1dc2464757c901fd`  
		Last Modified: Wed, 10 Apr 2024 07:12:44 GMT  
		Size: 89.8 MB (89839721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94547f34bc606d0b03a2f12b19f212f9195a4ef5b3ebf35f87fc966b849bfaa`  
		Last Modified: Wed, 10 Apr 2024 07:12:34 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:f48aa9eefc1b3c419ceaec8ea13efcef043d26cd3e1f8704674694748e49f977
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116784469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93852e5f41ce7b886a09323c3c692fef9099c97e1b94e2ba5dfe8ee35d5e5dd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 10:36:46 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 10 Apr 2024 10:36:46 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 10 Apr 2024 10:36:46 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 10 Apr 2024 10:36:46 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 10:36:59 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 10 Apr 2024 10:37:00 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 10:37:00 GMT
USER emqx
# Wed, 10 Apr 2024 10:37:00 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 10:37:00 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 10:37:00 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 10 Apr 2024 10:37:00 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 10:37:00 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4608d68733b0a539f557f23f7c63f81cbe7a5ea64fe02fb5ae440f8e40a54b6`  
		Last Modified: Wed, 10 Apr 2024 10:38:33 GMT  
		Size: 86.7 MB (86707129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63eda8f691fea5363d602730fc1f38c3373c757b8bccba97f7cbf890110df586`  
		Last Modified: Wed, 10 Apr 2024 10:38:26 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.5.1`

```console
$ docker pull emqx@sha256:79af25fcf47f51dbf5c44ef162ce37404c38a6908bd88255f24f51c250644995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.5.1` - linux; amd64

```console
$ docker pull emqx@sha256:5efce21eced38b8faa9e37088511728d05e4065b5e279d096a1b61edaebdc68b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121268493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac34f32f6c6596b90f03a6eec508c1fbde04f7171e60d1c7e60583e92b20cd77`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:10:38 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 10 Apr 2024 07:10:38 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 10 Apr 2024 07:10:38 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 10 Apr 2024 07:10:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 07:10:54 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 10 Apr 2024 07:10:54 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 07:10:54 GMT
USER emqx
# Wed, 10 Apr 2024 07:10:54 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 07:10:55 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 07:10:55 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 10 Apr 2024 07:10:55 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:10:55 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135438a2d2de091ce5a0d87c8afd5a17e05038759ea9d60b1dc2464757c901fd`  
		Last Modified: Wed, 10 Apr 2024 07:12:44 GMT  
		Size: 89.8 MB (89839721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94547f34bc606d0b03a2f12b19f212f9195a4ef5b3ebf35f87fc966b849bfaa`  
		Last Modified: Wed, 10 Apr 2024 07:12:34 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:f48aa9eefc1b3c419ceaec8ea13efcef043d26cd3e1f8704674694748e49f977
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116784469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93852e5f41ce7b886a09323c3c692fef9099c97e1b94e2ba5dfe8ee35d5e5dd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 10:36:46 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 10 Apr 2024 10:36:46 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 10 Apr 2024 10:36:46 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 10 Apr 2024 10:36:46 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 10:36:59 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 10 Apr 2024 10:37:00 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 10:37:00 GMT
USER emqx
# Wed, 10 Apr 2024 10:37:00 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 10:37:00 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 10:37:00 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 10 Apr 2024 10:37:00 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 10:37:00 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4608d68733b0a539f557f23f7c63f81cbe7a5ea64fe02fb5ae440f8e40a54b6`  
		Last Modified: Wed, 10 Apr 2024 10:38:33 GMT  
		Size: 86.7 MB (86707129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63eda8f691fea5363d602730fc1f38c3373c757b8bccba97f7cbf890110df586`  
		Last Modified: Wed, 10 Apr 2024 10:38:26 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.6`

```console
$ docker pull emqx@sha256:edb27d4b20dfc466393cd352d8cdc55a369136f307fb19586b021f8708a92698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.6` - linux; amd64

```console
$ docker pull emqx@sha256:30881c725b75da9f0d89a10366ffa8bf0ae749cda098b530a2f641000942f0e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124184594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d269f2003c9d50e119df8a24963e50f4bb7c3fe974be6287c666388ed268f15`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 18:24:41 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 18:24:41 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 18:24:42 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 18:24:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 18:24:57 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 22 Apr 2024 18:24:57 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 18:24:57 GMT
USER emqx
# Mon, 22 Apr 2024 18:24:57 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 18:24:57 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Mon, 22 Apr 2024 18:24:58 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Mon, 22 Apr 2024 18:24:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 18:24:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99faa8eeb4e25dfc780ba176527f797072c71b1fd864ebbf986547567c2b1acc`  
		Last Modified: Mon, 22 Apr 2024 18:25:27 GMT  
		Size: 95.1 MB (95052202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d58b6d6c1d7d342e1eddf4c4ab2068f5b4088cf1831a617d9700205bee2dbe5`  
		Last Modified: Mon, 22 Apr 2024 18:25:17 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:4d7e9f32d5dccf6faf2d23fca41df6b427825a542c278601458853790fbe0cfc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120775975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75b0b6066bd0a469d2953b967242684ba353813deed6b9825611f90934e9cd1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 17:41:57 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 17:41:57 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 17:41:57 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 17:41:57 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 17:42:10 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 22 Apr 2024 17:42:11 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 17:42:12 GMT
USER emqx
# Mon, 22 Apr 2024 17:42:12 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 17:42:12 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Mon, 22 Apr 2024 17:42:12 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Mon, 22 Apr 2024 17:42:12 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 17:42:12 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469c7f8258b8fcbca771d436a752dc7fb67eed640784f665297450001139a320`  
		Last Modified: Mon, 22 Apr 2024 17:42:40 GMT  
		Size: 91.6 MB (91612782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3fc26722d2c686504c8cf5bea418f9b63e85934d164e33c86e8cda55d36946`  
		Last Modified: Mon, 22 Apr 2024 17:42:32 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.6.1`

```console
$ docker pull emqx@sha256:edb27d4b20dfc466393cd352d8cdc55a369136f307fb19586b021f8708a92698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.6.1` - linux; amd64

```console
$ docker pull emqx@sha256:30881c725b75da9f0d89a10366ffa8bf0ae749cda098b530a2f641000942f0e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124184594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d269f2003c9d50e119df8a24963e50f4bb7c3fe974be6287c666388ed268f15`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 18:24:41 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 18:24:41 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 18:24:42 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 18:24:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 18:24:57 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 22 Apr 2024 18:24:57 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 18:24:57 GMT
USER emqx
# Mon, 22 Apr 2024 18:24:57 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 18:24:57 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Mon, 22 Apr 2024 18:24:58 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Mon, 22 Apr 2024 18:24:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 18:24:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99faa8eeb4e25dfc780ba176527f797072c71b1fd864ebbf986547567c2b1acc`  
		Last Modified: Mon, 22 Apr 2024 18:25:27 GMT  
		Size: 95.1 MB (95052202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d58b6d6c1d7d342e1eddf4c4ab2068f5b4088cf1831a617d9700205bee2dbe5`  
		Last Modified: Mon, 22 Apr 2024 18:25:17 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.6.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:4d7e9f32d5dccf6faf2d23fca41df6b427825a542c278601458853790fbe0cfc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120775975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75b0b6066bd0a469d2953b967242684ba353813deed6b9825611f90934e9cd1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 17:41:57 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 17:41:57 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 17:41:57 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 17:41:57 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 17:42:10 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 22 Apr 2024 17:42:11 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 17:42:12 GMT
USER emqx
# Mon, 22 Apr 2024 17:42:12 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 17:42:12 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Mon, 22 Apr 2024 17:42:12 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Mon, 22 Apr 2024 17:42:12 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 17:42:12 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469c7f8258b8fcbca771d436a752dc7fb67eed640784f665297450001139a320`  
		Last Modified: Mon, 22 Apr 2024 17:42:40 GMT  
		Size: 91.6 MB (91612782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3fc26722d2c686504c8cf5bea418f9b63e85934d164e33c86e8cda55d36946`  
		Last Modified: Mon, 22 Apr 2024 17:42:32 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:edb27d4b20dfc466393cd352d8cdc55a369136f307fb19586b021f8708a92698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:30881c725b75da9f0d89a10366ffa8bf0ae749cda098b530a2f641000942f0e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124184594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d269f2003c9d50e119df8a24963e50f4bb7c3fe974be6287c666388ed268f15`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 18:24:41 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 18:24:41 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 18:24:42 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 18:24:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 18:24:57 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 22 Apr 2024 18:24:57 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 18:24:57 GMT
USER emqx
# Mon, 22 Apr 2024 18:24:57 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 18:24:57 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Mon, 22 Apr 2024 18:24:58 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Mon, 22 Apr 2024 18:24:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 18:24:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99faa8eeb4e25dfc780ba176527f797072c71b1fd864ebbf986547567c2b1acc`  
		Last Modified: Mon, 22 Apr 2024 18:25:27 GMT  
		Size: 95.1 MB (95052202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d58b6d6c1d7d342e1eddf4c4ab2068f5b4088cf1831a617d9700205bee2dbe5`  
		Last Modified: Mon, 22 Apr 2024 18:25:17 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:4d7e9f32d5dccf6faf2d23fca41df6b427825a542c278601458853790fbe0cfc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120775975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75b0b6066bd0a469d2953b967242684ba353813deed6b9825611f90934e9cd1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 17:41:57 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 17:41:57 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 17:41:57 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 17:41:57 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 17:42:10 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 22 Apr 2024 17:42:11 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 17:42:12 GMT
USER emqx
# Mon, 22 Apr 2024 17:42:12 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 17:42:12 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Mon, 22 Apr 2024 17:42:12 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Mon, 22 Apr 2024 17:42:12 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 17:42:12 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469c7f8258b8fcbca771d436a752dc7fb67eed640784f665297450001139a320`  
		Last Modified: Mon, 22 Apr 2024 17:42:40 GMT  
		Size: 91.6 MB (91612782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3fc26722d2c686504c8cf5bea418f9b63e85934d164e33c86e8cda55d36946`  
		Last Modified: Mon, 22 Apr 2024 17:42:32 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
