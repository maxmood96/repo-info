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
$ docker pull emqx@sha256:e87784d6043f89f4a430bef4acdf28a22dc0d62e4a3de02a145b7f851dc21368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:45f51914bc6b28d0e23bea555679bd070a23277cd121e69f5ae5a2027655b417
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124206533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a6a473df1836e785190f4778273218fb396bf89c01b14f22523409d3126f2e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:28:20 GMT
ENV EMQX_VERSION=5.6.1
# Wed, 24 Apr 2024 04:28:20 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Wed, 24 Apr 2024 04:28:20 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Wed, 24 Apr 2024 04:28:20 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:28:36 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 24 Apr 2024 04:28:36 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:28:36 GMT
USER emqx
# Wed, 24 Apr 2024 04:28:37 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:28:37 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:28:37 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 24 Apr 2024 04:28:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:28:37 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb78d9b1d11aea4e48b11cf101ca79b8d05e2a6afeb220013793b7fc5bcfc7f`  
		Last Modified: Wed, 24 Apr 2024 04:30:21 GMT  
		Size: 95.1 MB (95055018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c721fad0602a66b21da5d838df97aa2132862eb7528e29342e2106e67029f6`  
		Last Modified: Wed, 24 Apr 2024 04:30:11 GMT  
		Size: 1.0 KB (1036 bytes)  
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
$ docker pull emqx@sha256:26bf799a173a6125d5a99b5a0c1590fa6ba6f5fc03282c33ec3694f8ee142411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1` - linux; amd64

```console
$ docker pull emqx@sha256:003b4648e0d1b1e2c5aa897995391007eb54ac8b2ab977a4ef4ee3f2e5367c44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102410084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8e5e57fa4348fa42babe5411aff4e1cbee418d7811873667652a380bb98003`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:26:46 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:26:46 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 24 Apr 2024 04:26:47 GMT
ENV EMQX_VERSION=5.1.6
# Wed, 24 Apr 2024 04:26:47 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Wed, 24 Apr 2024 04:26:47 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Wed, 24 Apr 2024 04:26:47 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:26:54 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 24 Apr 2024 04:26:54 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:26:54 GMT
USER emqx
# Wed, 24 Apr 2024 04:26:55 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:26:55 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:26:55 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 24 Apr 2024 04:26:55 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:26:55 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45976b5fe7010690f90ffafb4e0238f46242f6d04abbb8b9e1f0af5b1d0a1c11`  
		Last Modified: Wed, 24 Apr 2024 04:28:51 GMT  
		Size: 3.0 MB (2989557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c0a3ba50ab1ac8902be9b5a546bf7c63f86aa47f495593cca165a263e1ab62`  
		Last Modified: Wed, 24 Apr 2024 04:28:50 GMT  
		Size: 4.1 KB (4110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692af07376113d51e6d2184cede678855da97260624d5f88a3ba32c93e0283ae`  
		Last Modified: Wed, 24 Apr 2024 04:28:58 GMT  
		Size: 68.0 MB (67981252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592be638672b7afe71cfa5a79337f2c460c4f25a53eb838507bf667daaa5dd1b`  
		Last Modified: Wed, 24 Apr 2024 04:28:51 GMT  
		Size: 902.0 B  
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
$ docker pull emqx@sha256:26bf799a173a6125d5a99b5a0c1590fa6ba6f5fc03282c33ec3694f8ee142411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1.6` - linux; amd64

```console
$ docker pull emqx@sha256:003b4648e0d1b1e2c5aa897995391007eb54ac8b2ab977a4ef4ee3f2e5367c44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102410084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8e5e57fa4348fa42babe5411aff4e1cbee418d7811873667652a380bb98003`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:26:46 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:26:46 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 24 Apr 2024 04:26:47 GMT
ENV EMQX_VERSION=5.1.6
# Wed, 24 Apr 2024 04:26:47 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Wed, 24 Apr 2024 04:26:47 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Wed, 24 Apr 2024 04:26:47 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:26:54 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 24 Apr 2024 04:26:54 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:26:54 GMT
USER emqx
# Wed, 24 Apr 2024 04:26:55 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:26:55 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:26:55 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 24 Apr 2024 04:26:55 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:26:55 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45976b5fe7010690f90ffafb4e0238f46242f6d04abbb8b9e1f0af5b1d0a1c11`  
		Last Modified: Wed, 24 Apr 2024 04:28:51 GMT  
		Size: 3.0 MB (2989557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c0a3ba50ab1ac8902be9b5a546bf7c63f86aa47f495593cca165a263e1ab62`  
		Last Modified: Wed, 24 Apr 2024 04:28:50 GMT  
		Size: 4.1 KB (4110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692af07376113d51e6d2184cede678855da97260624d5f88a3ba32c93e0283ae`  
		Last Modified: Wed, 24 Apr 2024 04:28:58 GMT  
		Size: 68.0 MB (67981252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592be638672b7afe71cfa5a79337f2c460c4f25a53eb838507bf667daaa5dd1b`  
		Last Modified: Wed, 24 Apr 2024 04:28:51 GMT  
		Size: 902.0 B  
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
$ docker pull emqx@sha256:e8f469041521f6a4c69ea5c45a4525ec39163636a698a2ad58e74870cbf480fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2` - linux; amd64

```console
$ docker pull emqx@sha256:995d3751fd4368091c838b98b180715eaadf94a6c718c9a5f41939e870bbb87c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101181640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5283b60dedc3b9998377c9c1c31ac9d342dac8d9a21d443a28a4af747144287`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:27:06 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:27:06 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 24 Apr 2024 04:27:06 GMT
ENV EMQX_VERSION=5.2.1
# Wed, 24 Apr 2024 04:27:06 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Wed, 24 Apr 2024 04:27:07 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Wed, 24 Apr 2024 04:27:07 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:27:17 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 04:27:18 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:27:18 GMT
USER emqx
# Wed, 24 Apr 2024 04:27:18 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:27:18 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:27:18 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 24 Apr 2024 04:27:18 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:27:18 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75790383ce9e9813e8d074e7dbb333b898e94c8cb92522050935fb77fa0f90aa`  
		Last Modified: Wed, 24 Apr 2024 04:29:07 GMT  
		Size: 1.6 MB (1631415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28049f7bce9a304fcdb3ebc51a65cfb6f3df3f829da9d33d8c94c4a27cb89ef9`  
		Last Modified: Wed, 24 Apr 2024 04:29:07 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfcf27c5f29fcb7a5137bf1fa47b6dae66f05e1f0037d2a48dbfba8a7843220`  
		Last Modified: Wed, 24 Apr 2024 04:29:14 GMT  
		Size: 68.1 MB (68110948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30057c45291b51de1b91c0f716d2a5766ebc4403946282bec750ee6ff26f125`  
		Last Modified: Wed, 24 Apr 2024 04:29:07 GMT  
		Size: 905.0 B  
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
$ docker pull emqx@sha256:e8f469041521f6a4c69ea5c45a4525ec39163636a698a2ad58e74870cbf480fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2.1` - linux; amd64

```console
$ docker pull emqx@sha256:995d3751fd4368091c838b98b180715eaadf94a6c718c9a5f41939e870bbb87c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101181640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5283b60dedc3b9998377c9c1c31ac9d342dac8d9a21d443a28a4af747144287`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:27:06 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:27:06 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 24 Apr 2024 04:27:06 GMT
ENV EMQX_VERSION=5.2.1
# Wed, 24 Apr 2024 04:27:06 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Wed, 24 Apr 2024 04:27:07 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Wed, 24 Apr 2024 04:27:07 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:27:17 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 04:27:18 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:27:18 GMT
USER emqx
# Wed, 24 Apr 2024 04:27:18 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:27:18 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:27:18 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 24 Apr 2024 04:27:18 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:27:18 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75790383ce9e9813e8d074e7dbb333b898e94c8cb92522050935fb77fa0f90aa`  
		Last Modified: Wed, 24 Apr 2024 04:29:07 GMT  
		Size: 1.6 MB (1631415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28049f7bce9a304fcdb3ebc51a65cfb6f3df3f829da9d33d8c94c4a27cb89ef9`  
		Last Modified: Wed, 24 Apr 2024 04:29:07 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfcf27c5f29fcb7a5137bf1fa47b6dae66f05e1f0037d2a48dbfba8a7843220`  
		Last Modified: Wed, 24 Apr 2024 04:29:14 GMT  
		Size: 68.1 MB (68110948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30057c45291b51de1b91c0f716d2a5766ebc4403946282bec750ee6ff26f125`  
		Last Modified: Wed, 24 Apr 2024 04:29:07 GMT  
		Size: 905.0 B  
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
$ docker pull emqx@sha256:d6adc492015a019c9d3e4fec6450f2bee6f85c2035b26ca5b88f32040bf2fe83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3` - linux; amd64

```console
$ docker pull emqx@sha256:f245db650f41c1aa7704dce0b2ba8508e71fe733f89633319d756ddea7eda48d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101797010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ce8bd3480b902853aeb4d7201881ee8a275212d2c4543835d2b65531da37b1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:27:21 GMT
ENV EMQX_VERSION=5.3.2
# Wed, 24 Apr 2024 04:27:21 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Wed, 24 Apr 2024 04:27:22 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Wed, 24 Apr 2024 04:27:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:27:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:27:35 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:27:35 GMT
USER emqx
# Wed, 24 Apr 2024 04:27:35 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:27:36 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:27:36 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 24 Apr 2024 04:27:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:27:36 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d73b737ffc0a772c1834b3343f18e8c065b4f1cfc3ab9dac0dd4e063afc552`  
		Last Modified: Wed, 24 Apr 2024 04:29:29 GMT  
		Size: 70.4 MB (70361843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9b106549774436fdf9f9cc7adbfeb8a409b98aabf141b2e244355a78b88d9f`  
		Last Modified: Wed, 24 Apr 2024 04:29:22 GMT  
		Size: 904.0 B  
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
$ docker pull emqx@sha256:d6adc492015a019c9d3e4fec6450f2bee6f85c2035b26ca5b88f32040bf2fe83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3.2` - linux; amd64

```console
$ docker pull emqx@sha256:f245db650f41c1aa7704dce0b2ba8508e71fe733f89633319d756ddea7eda48d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101797010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ce8bd3480b902853aeb4d7201881ee8a275212d2c4543835d2b65531da37b1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:27:21 GMT
ENV EMQX_VERSION=5.3.2
# Wed, 24 Apr 2024 04:27:21 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Wed, 24 Apr 2024 04:27:22 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Wed, 24 Apr 2024 04:27:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:27:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:27:35 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:27:35 GMT
USER emqx
# Wed, 24 Apr 2024 04:27:35 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:27:36 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:27:36 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 24 Apr 2024 04:27:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:27:36 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d73b737ffc0a772c1834b3343f18e8c065b4f1cfc3ab9dac0dd4e063afc552`  
		Last Modified: Wed, 24 Apr 2024 04:29:29 GMT  
		Size: 70.4 MB (70361843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9b106549774436fdf9f9cc7adbfeb8a409b98aabf141b2e244355a78b88d9f`  
		Last Modified: Wed, 24 Apr 2024 04:29:22 GMT  
		Size: 904.0 B  
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
$ docker pull emqx@sha256:0aee743ca11afacf6451c19d806c15aac969e2428d383482f8fb6c21f8824498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.4` - linux; amd64

```console
$ docker pull emqx@sha256:744a46964365cfaf1d1e54aa8c1d422ff63d8ee38518b37867ff2805ac8b225d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118711283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a1c27c576ef23e02a7cd1f3a0f7ef133c13de78f3deb8454f4edf9a8d43d555`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:27:39 GMT
ENV EMQX_VERSION=5.4.1
# Wed, 24 Apr 2024 04:27:39 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Wed, 24 Apr 2024 04:27:39 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Wed, 24 Apr 2024 04:27:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:27:53 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:27:54 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:27:54 GMT
USER emqx
# Wed, 24 Apr 2024 04:27:54 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:27:54 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:27:54 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 24 Apr 2024 04:27:54 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:27:54 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bf5b439acfbd6136715e0bf5598af603b7e76bc5eedf4c8294a470adfbaed0`  
		Last Modified: Wed, 24 Apr 2024 04:29:46 GMT  
		Size: 87.3 MB (87276116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45852421f49784c3e3d49bd5db714deb4f6e57cecb5efb9852554184c7d01f52`  
		Last Modified: Wed, 24 Apr 2024 04:29:37 GMT  
		Size: 904.0 B  
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
$ docker pull emqx@sha256:0aee743ca11afacf6451c19d806c15aac969e2428d383482f8fb6c21f8824498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.4.1` - linux; amd64

```console
$ docker pull emqx@sha256:744a46964365cfaf1d1e54aa8c1d422ff63d8ee38518b37867ff2805ac8b225d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118711283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a1c27c576ef23e02a7cd1f3a0f7ef133c13de78f3deb8454f4edf9a8d43d555`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:27:39 GMT
ENV EMQX_VERSION=5.4.1
# Wed, 24 Apr 2024 04:27:39 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Wed, 24 Apr 2024 04:27:39 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Wed, 24 Apr 2024 04:27:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:27:53 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:27:54 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:27:54 GMT
USER emqx
# Wed, 24 Apr 2024 04:27:54 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:27:54 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:27:54 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 24 Apr 2024 04:27:54 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:27:54 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bf5b439acfbd6136715e0bf5598af603b7e76bc5eedf4c8294a470adfbaed0`  
		Last Modified: Wed, 24 Apr 2024 04:29:46 GMT  
		Size: 87.3 MB (87276116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45852421f49784c3e3d49bd5db714deb4f6e57cecb5efb9852554184c7d01f52`  
		Last Modified: Wed, 24 Apr 2024 04:29:37 GMT  
		Size: 904.0 B  
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
$ docker pull emqx@sha256:b73e098152ee036c66e354e0a3ec8d2ee259bb6613923077adccec30d5be8961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.5` - linux; amd64

```console
$ docker pull emqx@sha256:4414026061ac91ba5e7530cb6cbd59ff169ea521f67496893fa5a70884b39ae7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121276344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a7d2abf39e0bd7b5f2a27acb040e8ae63c8fa18a472b543cc253bf455c4f76`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:27:59 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 24 Apr 2024 04:27:59 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 24 Apr 2024 04:27:59 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 24 Apr 2024 04:28:00 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:28:14 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 24 Apr 2024 04:28:15 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:28:15 GMT
USER emqx
# Wed, 24 Apr 2024 04:28:15 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:28:15 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:28:15 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 24 Apr 2024 04:28:15 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:28:15 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1473ab5946a2647810af01e92b9b740a67d435fbb6d0b22e7eaf0cc310a5f96e`  
		Last Modified: Wed, 24 Apr 2024 04:30:03 GMT  
		Size: 89.8 MB (89841047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54901cafd7674d3aaf7f5e367ab76ff45b764e0b68ae821126a6c417a34efe5`  
		Last Modified: Wed, 24 Apr 2024 04:29:53 GMT  
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
$ docker pull emqx@sha256:b73e098152ee036c66e354e0a3ec8d2ee259bb6613923077adccec30d5be8961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.5.1` - linux; amd64

```console
$ docker pull emqx@sha256:4414026061ac91ba5e7530cb6cbd59ff169ea521f67496893fa5a70884b39ae7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121276344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a7d2abf39e0bd7b5f2a27acb040e8ae63c8fa18a472b543cc253bf455c4f76`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:27:59 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 24 Apr 2024 04:27:59 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 24 Apr 2024 04:27:59 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 24 Apr 2024 04:28:00 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:28:14 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 24 Apr 2024 04:28:15 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:28:15 GMT
USER emqx
# Wed, 24 Apr 2024 04:28:15 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:28:15 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:28:15 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 24 Apr 2024 04:28:15 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:28:15 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1473ab5946a2647810af01e92b9b740a67d435fbb6d0b22e7eaf0cc310a5f96e`  
		Last Modified: Wed, 24 Apr 2024 04:30:03 GMT  
		Size: 89.8 MB (89841047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54901cafd7674d3aaf7f5e367ab76ff45b764e0b68ae821126a6c417a34efe5`  
		Last Modified: Wed, 24 Apr 2024 04:29:53 GMT  
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
$ docker pull emqx@sha256:e87784d6043f89f4a430bef4acdf28a22dc0d62e4a3de02a145b7f851dc21368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.6` - linux; amd64

```console
$ docker pull emqx@sha256:45f51914bc6b28d0e23bea555679bd070a23277cd121e69f5ae5a2027655b417
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124206533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a6a473df1836e785190f4778273218fb396bf89c01b14f22523409d3126f2e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:28:20 GMT
ENV EMQX_VERSION=5.6.1
# Wed, 24 Apr 2024 04:28:20 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Wed, 24 Apr 2024 04:28:20 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Wed, 24 Apr 2024 04:28:20 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:28:36 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 24 Apr 2024 04:28:36 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:28:36 GMT
USER emqx
# Wed, 24 Apr 2024 04:28:37 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:28:37 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:28:37 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 24 Apr 2024 04:28:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:28:37 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb78d9b1d11aea4e48b11cf101ca79b8d05e2a6afeb220013793b7fc5bcfc7f`  
		Last Modified: Wed, 24 Apr 2024 04:30:21 GMT  
		Size: 95.1 MB (95055018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c721fad0602a66b21da5d838df97aa2132862eb7528e29342e2106e67029f6`  
		Last Modified: Wed, 24 Apr 2024 04:30:11 GMT  
		Size: 1.0 KB (1036 bytes)  
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
$ docker pull emqx@sha256:e87784d6043f89f4a430bef4acdf28a22dc0d62e4a3de02a145b7f851dc21368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.6.1` - linux; amd64

```console
$ docker pull emqx@sha256:45f51914bc6b28d0e23bea555679bd070a23277cd121e69f5ae5a2027655b417
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124206533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a6a473df1836e785190f4778273218fb396bf89c01b14f22523409d3126f2e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:28:20 GMT
ENV EMQX_VERSION=5.6.1
# Wed, 24 Apr 2024 04:28:20 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Wed, 24 Apr 2024 04:28:20 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Wed, 24 Apr 2024 04:28:20 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:28:36 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 24 Apr 2024 04:28:36 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:28:36 GMT
USER emqx
# Wed, 24 Apr 2024 04:28:37 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:28:37 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:28:37 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 24 Apr 2024 04:28:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:28:37 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb78d9b1d11aea4e48b11cf101ca79b8d05e2a6afeb220013793b7fc5bcfc7f`  
		Last Modified: Wed, 24 Apr 2024 04:30:21 GMT  
		Size: 95.1 MB (95055018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c721fad0602a66b21da5d838df97aa2132862eb7528e29342e2106e67029f6`  
		Last Modified: Wed, 24 Apr 2024 04:30:11 GMT  
		Size: 1.0 KB (1036 bytes)  
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
$ docker pull emqx@sha256:e87784d6043f89f4a430bef4acdf28a22dc0d62e4a3de02a145b7f851dc21368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:45f51914bc6b28d0e23bea555679bd070a23277cd121e69f5ae5a2027655b417
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124206533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a6a473df1836e785190f4778273218fb396bf89c01b14f22523409d3126f2e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:28:20 GMT
ENV EMQX_VERSION=5.6.1
# Wed, 24 Apr 2024 04:28:20 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Wed, 24 Apr 2024 04:28:20 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Wed, 24 Apr 2024 04:28:20 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:28:36 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 24 Apr 2024 04:28:36 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:28:36 GMT
USER emqx
# Wed, 24 Apr 2024 04:28:37 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:28:37 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:28:37 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 24 Apr 2024 04:28:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:28:37 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb78d9b1d11aea4e48b11cf101ca79b8d05e2a6afeb220013793b7fc5bcfc7f`  
		Last Modified: Wed, 24 Apr 2024 04:30:21 GMT  
		Size: 95.1 MB (95055018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c721fad0602a66b21da5d838df97aa2132862eb7528e29342e2106e67029f6`  
		Last Modified: Wed, 24 Apr 2024 04:30:11 GMT  
		Size: 1.0 KB (1036 bytes)  
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
