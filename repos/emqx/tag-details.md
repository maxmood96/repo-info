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
-	[`emqx:5.7`](#emqx57)
-	[`emqx:5.7.1`](#emqx571)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:51c39f5995f6aedd292707e73c7dbfbe8b72b82a5d0e2be5f2ef1c14df09c599
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:66c1f31561788effe34d9804299758d4927b7e11d8467297de202a96835f925f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126238122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fdc5370bf923bab8c90743b24666bca939fd1f2874c786e47d23fa1fbbfd87b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jun 2024 06:50:32 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 06:50:32 GMT
ENV EMQX_VERSION=5.7.1
# Thu, 27 Jun 2024 06:50:32 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Thu, 27 Jun 2024 06:50:32 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Thu, 27 Jun 2024 06:50:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Jun 2024 06:50:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
WORKDIR /opt/emqx
# Thu, 27 Jun 2024 06:50:32 GMT
USER emqx
# Thu, 27 Jun 2024 06:50:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Jun 2024 06:50:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 27 Jun 2024 06:50:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ea6242b71c16ce1352fcf57a0d11687c2bd0b9fd496834fd62f76dd8f5ebf2`  
		Last Modified: Tue, 23 Jul 2024 07:19:54 GMT  
		Size: 97.1 MB (97110772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312a74d0107a3ee33685af3838ac090917b45e87cb3006fc6192781d92482b4c`  
		Last Modified: Tue, 23 Jul 2024 07:19:51 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:8e4ad0134f93a3a02b2167fa3392b9b80c19466227b895ce27358ee2077c37ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2612062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f34cd44ade291f177d0677daa06c10214702867382053ae2ca28173d626e3f8`

```dockerfile
```

-	Layers:
	-	`sha256:7c83086fd6007886c99a90d7d357091c7e561d320beb2faba0c8bbcc497c6298`  
		Last Modified: Tue, 23 Jul 2024 07:19:51 GMT  
		Size: 2.6 MB (2599757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4740c9a8c3c0fdbc38c099b4759c70dc685a1bdf61a78e9702f2e6540074d6fb`  
		Last Modified: Tue, 23 Jul 2024 07:19:51 GMT  
		Size: 12.3 KB (12305 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:074ff8d864916263abc6e8c42120a7efa67fea641cb6a3a070a3614a2c5b66d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122815523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:573da311dffd01ef129754dc5a68bc6494d88d070bb031800b6881927091e973`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jun 2024 06:50:32 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 06:50:32 GMT
ENV EMQX_VERSION=5.7.1
# Thu, 27 Jun 2024 06:50:32 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Thu, 27 Jun 2024 06:50:32 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Thu, 27 Jun 2024 06:50:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Jun 2024 06:50:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
WORKDIR /opt/emqx
# Thu, 27 Jun 2024 06:50:32 GMT
USER emqx
# Thu, 27 Jun 2024 06:50:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Jun 2024 06:50:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 27 Jun 2024 06:50:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b31646db1381832e88900fde1500ba647e8458191411a4d10dcc4c8becfe406`  
		Last Modified: Mon, 08 Jul 2024 19:14:23 GMT  
		Size: 93.7 MB (93657896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762d975f3920ce02bd4da5ca7a8fdc83b4f8f921649f9451c80a10c3edccf678`  
		Last Modified: Mon, 08 Jul 2024 19:14:20 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:dd3bbbb96dcc4b68baf65342c6a21b9823d447ab4b1885e31b16f99167788509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb517a98e5b34cd172b0be13bd95c2cf36068984db6969a8c563accb9a671403`

```dockerfile
```

-	Layers:
	-	`sha256:5dd0ef27adb8bfba84a8a3bbd60855144597953b9ee86a6b30793bdc44cdb30c`  
		Last Modified: Mon, 08 Jul 2024 19:14:21 GMT  
		Size: 2.6 MB (2559768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b57ba143a92dd352085be44c5cc683e7846827132d92ab0aa6c287b80b3d3ac`  
		Last Modified: Mon, 08 Jul 2024 19:14:20 GMT  
		Size: 12.6 KB (12607 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.1`

```console
$ docker pull emqx@sha256:2cfb3d965ccd9ed0fef08811647e1e4091b02dd398ffdd0a4d7e436aad01e824
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.1` - linux; amd64

```console
$ docker pull emqx@sha256:dbd0ac96beea6a7b58282e863f6d4387911d4afdcfe0acb61fe88a5c7fe7f6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102401399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c4b47dc0cf4028485ba4b3282946b530f6b17c3ebd6da0a20836f84e5b23b2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 05 Sep 2023 13:05:03 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["bash"]
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 05 Sep 2023 13:05:03 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 05 Sep 2023 13:05:03 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 05 Sep 2023 13:05:03 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
WORKDIR /opt/emqx
# Tue, 05 Sep 2023 13:05:03 GMT
USER emqx
# Tue, 05 Sep 2023 13:05:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 05 Sep 2023 13:05:03 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 05 Sep 2023 13:05:03 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c29eb70beca3a9d65a22162f8772e56435d546ff0276c086630e4c28ed0567e`  
		Last Modified: Tue, 23 Jul 2024 07:19:21 GMT  
		Size: 3.0 MB (2987574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab66c95b99483ae60045e516ec652067ea908c43d5b0d5ecfd38439fb8968fe7`  
		Last Modified: Tue, 23 Jul 2024 07:19:21 GMT  
		Size: 4.0 KB (3987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9a35cf555d7da20558a61409d839a9703de7a44df4826b7b7d7c2f1bb642ac`  
		Last Modified: Tue, 23 Jul 2024 07:19:23 GMT  
		Size: 68.0 MB (67980576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb005464fd444dafd24404013e16d680b6837ce0101f39aee07987b4cd3b1556`  
		Last Modified: Tue, 23 Jul 2024 07:19:21 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.1` - unknown; unknown

```console
$ docker pull emqx@sha256:09007f288dacdde2c458dda7643dfb04fb76f62bd41eed24bf790801e549f182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2876794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffb95c9945f66313d3e51d217bab2058e20e1227d04af334ce8d867bb9a94b0`

```dockerfile
```

-	Layers:
	-	`sha256:148d4052ae97cc5a36434cec0ab64b3b43fb8824c3cca687f7755ecb0ac2ea20`  
		Last Modified: Tue, 23 Jul 2024 07:19:21 GMT  
		Size: 2.9 MB (2861668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0109e7f9d0e071578e49ad062bb7dab1793c7abf98094079eb6998ffb3931a11`  
		Last Modified: Tue, 23 Jul 2024 07:19:20 GMT  
		Size: 15.1 KB (15126 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:cada4e0bebc80733ea8b2deaaa4c17b8b89b7ecae41eb72037d86975677b7b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92698712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb76131bb270212955ab13689d623955acc25a8bad1f4b6ff667d46ee4c122c2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 05 Sep 2023 13:05:03 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["bash"]
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 05 Sep 2023 13:05:03 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 05 Sep 2023 13:05:03 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 05 Sep 2023 13:05:03 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
WORKDIR /opt/emqx
# Tue, 05 Sep 2023 13:05:03 GMT
USER emqx
# Tue, 05 Sep 2023 13:05:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 05 Sep 2023 13:05:03 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 05 Sep 2023 13:05:03 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47fc32e1771420c513826f66af1965425d7fde637f9df85e79c88abcf9df8f4`  
		Last Modified: Mon, 08 Jul 2024 19:10:27 GMT  
		Size: 3.0 MB (3003825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30abb6da25a89b034369ea57a7b6f06a4b59035a842b59538e0b0c9b70412159`  
		Last Modified: Mon, 08 Jul 2024 19:10:27 GMT  
		Size: 4.0 KB (3998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcbc9c4ef2388a1d129a01b42394a636072b082259312c8de48ca08ec4341e4`  
		Last Modified: Mon, 08 Jul 2024 19:10:28 GMT  
		Size: 59.6 MB (59620341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442fe0e0448c7bbd97e338110a8b195ab0aa51764677f1519f6e668b821d7d97`  
		Last Modified: Mon, 08 Jul 2024 19:10:27 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.1` - unknown; unknown

```console
$ docker pull emqx@sha256:a7758fa95ff78651af4b5807080d88ecb614e10124348dc840d3627821a3ab03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2837769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb74e25ec6582b18ce5c04a69587822c751bd640c95ac9ff32b440b4b16d3c3`

```dockerfile
```

-	Layers:
	-	`sha256:39de6641d6a29c6221c008ff83be6625a111c57ee1f3a985bf449f2ad286e61c`  
		Last Modified: Mon, 08 Jul 2024 19:10:27 GMT  
		Size: 2.8 MB (2822362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04f67d2af5dcf43b040dba313ee19eab8ac3fb660a57d74e6a50c72efc1580e2`  
		Last Modified: Mon, 08 Jul 2024 19:10:26 GMT  
		Size: 15.4 KB (15407 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.1.6`

```console
$ docker pull emqx@sha256:2cfb3d965ccd9ed0fef08811647e1e4091b02dd398ffdd0a4d7e436aad01e824
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.1.6` - linux; amd64

```console
$ docker pull emqx@sha256:dbd0ac96beea6a7b58282e863f6d4387911d4afdcfe0acb61fe88a5c7fe7f6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102401399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c4b47dc0cf4028485ba4b3282946b530f6b17c3ebd6da0a20836f84e5b23b2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 05 Sep 2023 13:05:03 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["bash"]
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 05 Sep 2023 13:05:03 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 05 Sep 2023 13:05:03 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 05 Sep 2023 13:05:03 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
WORKDIR /opt/emqx
# Tue, 05 Sep 2023 13:05:03 GMT
USER emqx
# Tue, 05 Sep 2023 13:05:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 05 Sep 2023 13:05:03 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 05 Sep 2023 13:05:03 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c29eb70beca3a9d65a22162f8772e56435d546ff0276c086630e4c28ed0567e`  
		Last Modified: Tue, 23 Jul 2024 07:19:21 GMT  
		Size: 3.0 MB (2987574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab66c95b99483ae60045e516ec652067ea908c43d5b0d5ecfd38439fb8968fe7`  
		Last Modified: Tue, 23 Jul 2024 07:19:21 GMT  
		Size: 4.0 KB (3987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9a35cf555d7da20558a61409d839a9703de7a44df4826b7b7d7c2f1bb642ac`  
		Last Modified: Tue, 23 Jul 2024 07:19:23 GMT  
		Size: 68.0 MB (67980576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb005464fd444dafd24404013e16d680b6837ce0101f39aee07987b4cd3b1556`  
		Last Modified: Tue, 23 Jul 2024 07:19:21 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.1.6` - unknown; unknown

```console
$ docker pull emqx@sha256:09007f288dacdde2c458dda7643dfb04fb76f62bd41eed24bf790801e549f182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2876794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffb95c9945f66313d3e51d217bab2058e20e1227d04af334ce8d867bb9a94b0`

```dockerfile
```

-	Layers:
	-	`sha256:148d4052ae97cc5a36434cec0ab64b3b43fb8824c3cca687f7755ecb0ac2ea20`  
		Last Modified: Tue, 23 Jul 2024 07:19:21 GMT  
		Size: 2.9 MB (2861668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0109e7f9d0e071578e49ad062bb7dab1793c7abf98094079eb6998ffb3931a11`  
		Last Modified: Tue, 23 Jul 2024 07:19:20 GMT  
		Size: 15.1 KB (15126 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.1.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:cada4e0bebc80733ea8b2deaaa4c17b8b89b7ecae41eb72037d86975677b7b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92698712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb76131bb270212955ab13689d623955acc25a8bad1f4b6ff667d46ee4c122c2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 05 Sep 2023 13:05:03 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["bash"]
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 05 Sep 2023 13:05:03 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 05 Sep 2023 13:05:03 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 05 Sep 2023 13:05:03 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
WORKDIR /opt/emqx
# Tue, 05 Sep 2023 13:05:03 GMT
USER emqx
# Tue, 05 Sep 2023 13:05:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 05 Sep 2023 13:05:03 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 05 Sep 2023 13:05:03 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47fc32e1771420c513826f66af1965425d7fde637f9df85e79c88abcf9df8f4`  
		Last Modified: Mon, 08 Jul 2024 19:10:27 GMT  
		Size: 3.0 MB (3003825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30abb6da25a89b034369ea57a7b6f06a4b59035a842b59538e0b0c9b70412159`  
		Last Modified: Mon, 08 Jul 2024 19:10:27 GMT  
		Size: 4.0 KB (3998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcbc9c4ef2388a1d129a01b42394a636072b082259312c8de48ca08ec4341e4`  
		Last Modified: Mon, 08 Jul 2024 19:10:28 GMT  
		Size: 59.6 MB (59620341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442fe0e0448c7bbd97e338110a8b195ab0aa51764677f1519f6e668b821d7d97`  
		Last Modified: Mon, 08 Jul 2024 19:10:27 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.1.6` - unknown; unknown

```console
$ docker pull emqx@sha256:a7758fa95ff78651af4b5807080d88ecb614e10124348dc840d3627821a3ab03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2837769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb74e25ec6582b18ce5c04a69587822c751bd640c95ac9ff32b440b4b16d3c3`

```dockerfile
```

-	Layers:
	-	`sha256:39de6641d6a29c6221c008ff83be6625a111c57ee1f3a985bf449f2ad286e61c`  
		Last Modified: Mon, 08 Jul 2024 19:10:27 GMT  
		Size: 2.8 MB (2822362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04f67d2af5dcf43b040dba313ee19eab8ac3fb660a57d74e6a50c72efc1580e2`  
		Last Modified: Mon, 08 Jul 2024 19:10:26 GMT  
		Size: 15.4 KB (15407 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.2`

```console
$ docker pull emqx@sha256:13c6cc061887742ca485f67a6e4a119ce8f7873850770402cdffce9ff9badbd3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.2` - linux; amd64

```console
$ docker pull emqx@sha256:a0849341eebb70b49fee29b693f9f123565dc4691a06de9e044459e467389e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (100956082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7a55867b2cd375ce93ac98c4df13776b6e900607d423711ebd61cf58188e64`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["bash"]
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENV EMQX_VERSION=5.2.1
# Mon, 25 Sep 2023 09:53:58 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Mon, 25 Sep 2023 09:53:58 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Mon, 25 Sep 2023 09:53:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
WORKDIR /opt/emqx
# Mon, 25 Sep 2023 09:53:58 GMT
USER emqx
# Mon, 25 Sep 2023 09:53:58 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 25 Sep 2023 09:53:58 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 25 Sep 2023 09:53:58 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e189bca6085d98f7f8cbed0ab1b2102a4d2aac5a5e572323ccefc7fbe5ecdd3`  
		Last Modified: Tue, 23 Jul 2024 07:19:39 GMT  
		Size: 1.6 MB (1629027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba433d75d4bd1f3423515cbba9d3255248e2c6341dda4b1d9c38d0f22e9d822c`  
		Last Modified: Tue, 23 Jul 2024 07:19:38 GMT  
		Size: 4.0 KB (3989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf15f68a2f2cd2e73ad2aea4fd6c47b28de391809b83cec9471e70a213944302`  
		Last Modified: Tue, 23 Jul 2024 07:19:41 GMT  
		Size: 67.9 MB (67893807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bbc4ae6f356e392cb815fd42aba13d9a9f36c4436fb275354e2f197b00d07a`  
		Last Modified: Tue, 23 Jul 2024 07:19:39 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2` - unknown; unknown

```console
$ docker pull emqx@sha256:e2c3cab821f3f894eec87ae1863d037cc10322134d716547549343cbffa53cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2821478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa1c15416fb1786bc7543097c7f7b8010d8c8cbc54e12942b6753629dd03d03`

```dockerfile
```

-	Layers:
	-	`sha256:d5cf5699c22d1a5b4d40ae217257d78a85cdec49ea0c6b53870da496b9539ea9`  
		Last Modified: Tue, 23 Jul 2024 07:19:39 GMT  
		Size: 2.8 MB (2805848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bf7cff96c7e01c881669b333a116bc618e611c3c531cd121ed3f096ff4484e4`  
		Last Modified: Tue, 23 Jul 2024 07:19:38 GMT  
		Size: 15.6 KB (15630 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:2262eef51d4a9f61be2b7407b21706a2465c050cc30110b0d9e7d6dc7cb380f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91255514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d4f0cc3734ca61ac76aa974e1346421d7668cdf39ee0b57c0f37f847f96d93`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["bash"]
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENV EMQX_VERSION=5.2.1
# Mon, 25 Sep 2023 09:53:58 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Mon, 25 Sep 2023 09:53:58 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Mon, 25 Sep 2023 09:53:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
WORKDIR /opt/emqx
# Mon, 25 Sep 2023 09:53:58 GMT
USER emqx
# Mon, 25 Sep 2023 09:53:58 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 25 Sep 2023 09:53:58 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 25 Sep 2023 09:53:58 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47f685676a84b42ad28e83cc2288b58817812479b9f78a84df26fc6d2ba6d58`  
		Last Modified: Mon, 08 Jul 2024 19:11:05 GMT  
		Size: 1.6 MB (1643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9667ea51efb76fc783c11b275ac32c60c19eba9d80c6d79a52c63654793225e6`  
		Last Modified: Mon, 08 Jul 2024 19:11:04 GMT  
		Size: 4.0 KB (3998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1143fda4d658df0d453ccde0405de6a0cec03673cc964e9ce07dd4fe12b187`  
		Last Modified: Mon, 08 Jul 2024 19:11:07 GMT  
		Size: 59.5 MB (59537226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797b4d2cd4c0f7c62b169286fa88cdc4b702f8cf2dae5e2c08a8d2d8e06563a2`  
		Last Modified: Mon, 08 Jul 2024 19:11:05 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2` - unknown; unknown

```console
$ docker pull emqx@sha256:0bca6dd2d4e8601122ae7e30393d3ec62b9d1911176784ec1e078b2bab02ac10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2784870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad7b4e33e396474881ae0eade18c058b76ad76d2a125d8d95f9f7d4871297ee`

```dockerfile
```

-	Layers:
	-	`sha256:778f56810c422ec9c701dfede4ad8c5fc809fcf52caf1b3bd455a5e87526f293`  
		Last Modified: Mon, 08 Jul 2024 19:11:05 GMT  
		Size: 2.8 MB (2768961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:030b4d71e411dc20c6c2a709f33103035822397592f6a8cc4bdb3444ea9e5e46`  
		Last Modified: Mon, 08 Jul 2024 19:11:06 GMT  
		Size: 15.9 KB (15909 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.2.1`

```console
$ docker pull emqx@sha256:13c6cc061887742ca485f67a6e4a119ce8f7873850770402cdffce9ff9badbd3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.2.1` - linux; amd64

```console
$ docker pull emqx@sha256:a0849341eebb70b49fee29b693f9f123565dc4691a06de9e044459e467389e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (100956082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7a55867b2cd375ce93ac98c4df13776b6e900607d423711ebd61cf58188e64`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["bash"]
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENV EMQX_VERSION=5.2.1
# Mon, 25 Sep 2023 09:53:58 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Mon, 25 Sep 2023 09:53:58 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Mon, 25 Sep 2023 09:53:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
WORKDIR /opt/emqx
# Mon, 25 Sep 2023 09:53:58 GMT
USER emqx
# Mon, 25 Sep 2023 09:53:58 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 25 Sep 2023 09:53:58 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 25 Sep 2023 09:53:58 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e189bca6085d98f7f8cbed0ab1b2102a4d2aac5a5e572323ccefc7fbe5ecdd3`  
		Last Modified: Tue, 23 Jul 2024 07:19:39 GMT  
		Size: 1.6 MB (1629027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba433d75d4bd1f3423515cbba9d3255248e2c6341dda4b1d9c38d0f22e9d822c`  
		Last Modified: Tue, 23 Jul 2024 07:19:38 GMT  
		Size: 4.0 KB (3989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf15f68a2f2cd2e73ad2aea4fd6c47b28de391809b83cec9471e70a213944302`  
		Last Modified: Tue, 23 Jul 2024 07:19:41 GMT  
		Size: 67.9 MB (67893807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bbc4ae6f356e392cb815fd42aba13d9a9f36c4436fb275354e2f197b00d07a`  
		Last Modified: Tue, 23 Jul 2024 07:19:39 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2.1` - unknown; unknown

```console
$ docker pull emqx@sha256:e2c3cab821f3f894eec87ae1863d037cc10322134d716547549343cbffa53cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2821478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa1c15416fb1786bc7543097c7f7b8010d8c8cbc54e12942b6753629dd03d03`

```dockerfile
```

-	Layers:
	-	`sha256:d5cf5699c22d1a5b4d40ae217257d78a85cdec49ea0c6b53870da496b9539ea9`  
		Last Modified: Tue, 23 Jul 2024 07:19:39 GMT  
		Size: 2.8 MB (2805848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bf7cff96c7e01c881669b333a116bc618e611c3c531cd121ed3f096ff4484e4`  
		Last Modified: Tue, 23 Jul 2024 07:19:38 GMT  
		Size: 15.6 KB (15630 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.2.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:2262eef51d4a9f61be2b7407b21706a2465c050cc30110b0d9e7d6dc7cb380f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91255514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d4f0cc3734ca61ac76aa974e1346421d7668cdf39ee0b57c0f37f847f96d93`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["bash"]
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENV EMQX_VERSION=5.2.1
# Mon, 25 Sep 2023 09:53:58 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Mon, 25 Sep 2023 09:53:58 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Mon, 25 Sep 2023 09:53:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
WORKDIR /opt/emqx
# Mon, 25 Sep 2023 09:53:58 GMT
USER emqx
# Mon, 25 Sep 2023 09:53:58 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 25 Sep 2023 09:53:58 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 25 Sep 2023 09:53:58 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47f685676a84b42ad28e83cc2288b58817812479b9f78a84df26fc6d2ba6d58`  
		Last Modified: Mon, 08 Jul 2024 19:11:05 GMT  
		Size: 1.6 MB (1643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9667ea51efb76fc783c11b275ac32c60c19eba9d80c6d79a52c63654793225e6`  
		Last Modified: Mon, 08 Jul 2024 19:11:04 GMT  
		Size: 4.0 KB (3998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1143fda4d658df0d453ccde0405de6a0cec03673cc964e9ce07dd4fe12b187`  
		Last Modified: Mon, 08 Jul 2024 19:11:07 GMT  
		Size: 59.5 MB (59537226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797b4d2cd4c0f7c62b169286fa88cdc4b702f8cf2dae5e2c08a8d2d8e06563a2`  
		Last Modified: Mon, 08 Jul 2024 19:11:05 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2.1` - unknown; unknown

```console
$ docker pull emqx@sha256:0bca6dd2d4e8601122ae7e30393d3ec62b9d1911176784ec1e078b2bab02ac10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2784870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad7b4e33e396474881ae0eade18c058b76ad76d2a125d8d95f9f7d4871297ee`

```dockerfile
```

-	Layers:
	-	`sha256:778f56810c422ec9c701dfede4ad8c5fc809fcf52caf1b3bd455a5e87526f293`  
		Last Modified: Mon, 08 Jul 2024 19:11:05 GMT  
		Size: 2.8 MB (2768961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:030b4d71e411dc20c6c2a709f33103035822397592f6a8cc4bdb3444ea9e5e46`  
		Last Modified: Mon, 08 Jul 2024 19:11:06 GMT  
		Size: 15.9 KB (15909 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.3`

```console
$ docker pull emqx@sha256:7c6ade6d4204e5dd8b5f4d1436953825f84bfec7ea99119c38f783b74e62e5e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.3` - linux; amd64

```console
$ docker pull emqx@sha256:a6fe3c0c2168a117cd1fb144446715cae592b1d40b4f7d83506cdb78bec151ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101788638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd370770950487b90d8130e5dafe4a0462c21838af82ba085470a4f07613446e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["bash"]
# Fri, 01 Dec 2023 10:27:11 GMT
ENV EMQX_VERSION=5.3.2
# Fri, 01 Dec 2023 10:27:11 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Fri, 01 Dec 2023 10:27:11 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Fri, 01 Dec 2023 10:27:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 01 Dec 2023 10:27:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
WORKDIR /opt/emqx
# Fri, 01 Dec 2023 10:27:11 GMT
USER emqx
# Fri, 01 Dec 2023 10:27:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 01 Dec 2023 10:27:11 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 01 Dec 2023 10:27:11 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e331474f7851debe45007e158fdcd7f49976b79070bec20e5ceba179bf9aaca3`  
		Last Modified: Tue, 23 Jul 2024 07:19:37 GMT  
		Size: 70.4 MB (70359376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2899f845418245006d6927a3b61d29a1693efc77385165598ad5e6292b474337`  
		Last Modified: Tue, 23 Jul 2024 07:19:34 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3` - unknown; unknown

```console
$ docker pull emqx@sha256:f645d17309997cf898cd4906ea20f63db739510f07911f1abe96e943229bda5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2829750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7517e06fe5c6e863ad826476f4b4927bbdf7316b3d01dc3f441a9643748828f`

```dockerfile
```

-	Layers:
	-	`sha256:71c51d352ef22c8160dffbd058bf8adf08a3698941e1b2b92565f07b5a3100e2`  
		Last Modified: Tue, 23 Jul 2024 07:19:35 GMT  
		Size: 2.8 MB (2817191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58a131d85add3520004ebfadb1510e09b8349b2e71e0a257ee843531f808aa7e`  
		Last Modified: Tue, 23 Jul 2024 07:19:34 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:988f5d343469d557bdea7c43791cbe2d3c80a4c5d338c2e978da1020e9429592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92081158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b75fe113027384d5d77071c49148c048ce843069161fcf8e37bb77e3b2e683`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["bash"]
# Fri, 01 Dec 2023 10:27:11 GMT
ENV EMQX_VERSION=5.3.2
# Fri, 01 Dec 2023 10:27:11 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Fri, 01 Dec 2023 10:27:11 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Fri, 01 Dec 2023 10:27:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 01 Dec 2023 10:27:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
WORKDIR /opt/emqx
# Fri, 01 Dec 2023 10:27:11 GMT
USER emqx
# Fri, 01 Dec 2023 10:27:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 01 Dec 2023 10:27:11 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 01 Dec 2023 10:27:11 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cab82329c1e3ef265821322daff0415d83d5f27f461c80fdad1e800cf38ba3`  
		Last Modified: Mon, 08 Jul 2024 19:11:42 GMT  
		Size: 62.0 MB (62010610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0566a31872da74abd788a5bc34c298683d3f97d9d6037f09f5640668abb81838`  
		Last Modified: Mon, 08 Jul 2024 19:11:38 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3` - unknown; unknown

```console
$ docker pull emqx@sha256:810b9f82ca5926ef2b4127348ca0085a3fe6ceab1ba7122e29d28d622e2e885f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2791712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2411b2201c7bff828cf1ebcf64108f9c56db164e3448bc2f321e5aaec038fcdc`

```dockerfile
```

-	Layers:
	-	`sha256:0f99375ac7482efa306d1d270621d0c5ae5038208124da1d66f0a0b7830dcbb3`  
		Last Modified: Mon, 08 Jul 2024 19:11:38 GMT  
		Size: 2.8 MB (2778874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a3a98bbe060291962b24b8d2ee9eee82015834014427d2ec016a04a023e566`  
		Last Modified: Mon, 08 Jul 2024 19:11:38 GMT  
		Size: 12.8 KB (12838 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.3.2`

```console
$ docker pull emqx@sha256:7c6ade6d4204e5dd8b5f4d1436953825f84bfec7ea99119c38f783b74e62e5e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.3.2` - linux; amd64

```console
$ docker pull emqx@sha256:a6fe3c0c2168a117cd1fb144446715cae592b1d40b4f7d83506cdb78bec151ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101788638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd370770950487b90d8130e5dafe4a0462c21838af82ba085470a4f07613446e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["bash"]
# Fri, 01 Dec 2023 10:27:11 GMT
ENV EMQX_VERSION=5.3.2
# Fri, 01 Dec 2023 10:27:11 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Fri, 01 Dec 2023 10:27:11 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Fri, 01 Dec 2023 10:27:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 01 Dec 2023 10:27:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
WORKDIR /opt/emqx
# Fri, 01 Dec 2023 10:27:11 GMT
USER emqx
# Fri, 01 Dec 2023 10:27:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 01 Dec 2023 10:27:11 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 01 Dec 2023 10:27:11 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e331474f7851debe45007e158fdcd7f49976b79070bec20e5ceba179bf9aaca3`  
		Last Modified: Tue, 23 Jul 2024 07:19:37 GMT  
		Size: 70.4 MB (70359376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2899f845418245006d6927a3b61d29a1693efc77385165598ad5e6292b474337`  
		Last Modified: Tue, 23 Jul 2024 07:19:34 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3.2` - unknown; unknown

```console
$ docker pull emqx@sha256:f645d17309997cf898cd4906ea20f63db739510f07911f1abe96e943229bda5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2829750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7517e06fe5c6e863ad826476f4b4927bbdf7316b3d01dc3f441a9643748828f`

```dockerfile
```

-	Layers:
	-	`sha256:71c51d352ef22c8160dffbd058bf8adf08a3698941e1b2b92565f07b5a3100e2`  
		Last Modified: Tue, 23 Jul 2024 07:19:35 GMT  
		Size: 2.8 MB (2817191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58a131d85add3520004ebfadb1510e09b8349b2e71e0a257ee843531f808aa7e`  
		Last Modified: Tue, 23 Jul 2024 07:19:34 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.3.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:988f5d343469d557bdea7c43791cbe2d3c80a4c5d338c2e978da1020e9429592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92081158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b75fe113027384d5d77071c49148c048ce843069161fcf8e37bb77e3b2e683`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["bash"]
# Fri, 01 Dec 2023 10:27:11 GMT
ENV EMQX_VERSION=5.3.2
# Fri, 01 Dec 2023 10:27:11 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Fri, 01 Dec 2023 10:27:11 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Fri, 01 Dec 2023 10:27:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 01 Dec 2023 10:27:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
WORKDIR /opt/emqx
# Fri, 01 Dec 2023 10:27:11 GMT
USER emqx
# Fri, 01 Dec 2023 10:27:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 01 Dec 2023 10:27:11 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 01 Dec 2023 10:27:11 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cab82329c1e3ef265821322daff0415d83d5f27f461c80fdad1e800cf38ba3`  
		Last Modified: Mon, 08 Jul 2024 19:11:42 GMT  
		Size: 62.0 MB (62010610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0566a31872da74abd788a5bc34c298683d3f97d9d6037f09f5640668abb81838`  
		Last Modified: Mon, 08 Jul 2024 19:11:38 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3.2` - unknown; unknown

```console
$ docker pull emqx@sha256:810b9f82ca5926ef2b4127348ca0085a3fe6ceab1ba7122e29d28d622e2e885f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2791712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2411b2201c7bff828cf1ebcf64108f9c56db164e3448bc2f321e5aaec038fcdc`

```dockerfile
```

-	Layers:
	-	`sha256:0f99375ac7482efa306d1d270621d0c5ae5038208124da1d66f0a0b7830dcbb3`  
		Last Modified: Mon, 08 Jul 2024 19:11:38 GMT  
		Size: 2.8 MB (2778874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a3a98bbe060291962b24b8d2ee9eee82015834014427d2ec016a04a023e566`  
		Last Modified: Mon, 08 Jul 2024 19:11:38 GMT  
		Size: 12.8 KB (12838 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.4`

```console
$ docker pull emqx@sha256:8ebd0fffea3c061551d3433d5fae7241ad5febd60cea1421eaa3ba8c3c21e741
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.4` - linux; amd64

```console
$ docker pull emqx@sha256:262777adf23fd79cd9ad8483c944e75f066a5350f084cfa81c1a0544496653f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118702428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18197ba4751815032809d286a6188ab366c189483c8183136296c2c2fbede8a6`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 14:13:45 GMT
ENV EMQX_VERSION=5.4.1
# Fri, 12 Jan 2024 14:13:45 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Fri, 12 Jan 2024 14:13:45 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Fri, 12 Jan 2024 14:13:45 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 12 Jan 2024 14:13:45 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
WORKDIR /opt/emqx
# Fri, 12 Jan 2024 14:13:45 GMT
USER emqx
# Fri, 12 Jan 2024 14:13:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 12 Jan 2024 14:13:45 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 12 Jan 2024 14:13:45 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea714ba9b9d35e53b7b7b219714cd5d47d607621fbe17f648e006cd41997bacd`  
		Last Modified: Tue, 23 Jul 2024 07:19:41 GMT  
		Size: 87.3 MB (87273168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e491635fe7358b221ac87cec318fe90c38d981d1214a2908d5c62c37c5dd1e8d`  
		Last Modified: Tue, 23 Jul 2024 07:19:40 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4` - unknown; unknown

```console
$ docker pull emqx@sha256:26e70fe1933e641c84e20bfe6bc2ace9db7f7b719a375f7e48082edd21f22706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbbed9f965307bd8bf1d792e340d0b97df8f44ebec6ad308fb4d89affc44d046`

```dockerfile
```

-	Layers:
	-	`sha256:4301c76f3e24f16ab4fc68b97bc25902ffa96c7a13a4e0118b04bc85fb5d15dd`  
		Last Modified: Tue, 23 Jul 2024 07:19:40 GMT  
		Size: 2.8 MB (2810516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82d3c7f0f2b38e8b4470a688648ee89239ea7da80f39dcc0288de81937f01d89`  
		Last Modified: Tue, 23 Jul 2024 07:19:40 GMT  
		Size: 12.5 KB (12502 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:372129587039fb4d05a7b1f092a5cb01fd403a02ad00156e3ebd04f577dea18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108479553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c629d363e9597a0fc94034631d9cc2831df884201a6bcf81644116287ea32a5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 14:13:45 GMT
ENV EMQX_VERSION=5.4.1
# Fri, 12 Jan 2024 14:13:45 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Fri, 12 Jan 2024 14:13:45 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Fri, 12 Jan 2024 14:13:45 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 12 Jan 2024 14:13:45 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
WORKDIR /opt/emqx
# Fri, 12 Jan 2024 14:13:45 GMT
USER emqx
# Fri, 12 Jan 2024 14:13:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 12 Jan 2024 14:13:45 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 12 Jan 2024 14:13:45 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3602325be2f03896f21a1b18ec916d00c20d1d0d4ff357ea418b351ddfc993b7`  
		Last Modified: Mon, 08 Jul 2024 19:12:18 GMT  
		Size: 78.4 MB (78409005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a443efe216cff55e388643f0246e1746bde91e197528a31e4a5f5109c29ff585`  
		Last Modified: Mon, 08 Jul 2024 19:12:15 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4` - unknown; unknown

```console
$ docker pull emqx@sha256:a23fd6dc2af4f850b35bdd7e407b53bf1c0a51186b5b1664d910a5ec74580def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2785839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88ab692e308275b2fdcef7f96f5e805f0af93a0b98992f7a6d0c05ea084ae6a`

```dockerfile
```

-	Layers:
	-	`sha256:7ebad33375cb3eb1724f405536bce35e2b65b667071a82abcb0ddb31ac31b7cd`  
		Last Modified: Mon, 08 Jul 2024 19:12:16 GMT  
		Size: 2.8 MB (2773057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c54a86be65a75bb9a55e0e2ecedb678e8fa8801603ed8ee8e5b262bcc3d6617`  
		Last Modified: Mon, 08 Jul 2024 19:12:15 GMT  
		Size: 12.8 KB (12782 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.4.1`

```console
$ docker pull emqx@sha256:8ebd0fffea3c061551d3433d5fae7241ad5febd60cea1421eaa3ba8c3c21e741
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.4.1` - linux; amd64

```console
$ docker pull emqx@sha256:262777adf23fd79cd9ad8483c944e75f066a5350f084cfa81c1a0544496653f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118702428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18197ba4751815032809d286a6188ab366c189483c8183136296c2c2fbede8a6`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 14:13:45 GMT
ENV EMQX_VERSION=5.4.1
# Fri, 12 Jan 2024 14:13:45 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Fri, 12 Jan 2024 14:13:45 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Fri, 12 Jan 2024 14:13:45 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 12 Jan 2024 14:13:45 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
WORKDIR /opt/emqx
# Fri, 12 Jan 2024 14:13:45 GMT
USER emqx
# Fri, 12 Jan 2024 14:13:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 12 Jan 2024 14:13:45 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 12 Jan 2024 14:13:45 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea714ba9b9d35e53b7b7b219714cd5d47d607621fbe17f648e006cd41997bacd`  
		Last Modified: Tue, 23 Jul 2024 07:19:41 GMT  
		Size: 87.3 MB (87273168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e491635fe7358b221ac87cec318fe90c38d981d1214a2908d5c62c37c5dd1e8d`  
		Last Modified: Tue, 23 Jul 2024 07:19:40 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4.1` - unknown; unknown

```console
$ docker pull emqx@sha256:26e70fe1933e641c84e20bfe6bc2ace9db7f7b719a375f7e48082edd21f22706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbbed9f965307bd8bf1d792e340d0b97df8f44ebec6ad308fb4d89affc44d046`

```dockerfile
```

-	Layers:
	-	`sha256:4301c76f3e24f16ab4fc68b97bc25902ffa96c7a13a4e0118b04bc85fb5d15dd`  
		Last Modified: Tue, 23 Jul 2024 07:19:40 GMT  
		Size: 2.8 MB (2810516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82d3c7f0f2b38e8b4470a688648ee89239ea7da80f39dcc0288de81937f01d89`  
		Last Modified: Tue, 23 Jul 2024 07:19:40 GMT  
		Size: 12.5 KB (12502 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.4.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:372129587039fb4d05a7b1f092a5cb01fd403a02ad00156e3ebd04f577dea18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108479553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c629d363e9597a0fc94034631d9cc2831df884201a6bcf81644116287ea32a5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 14:13:45 GMT
ENV EMQX_VERSION=5.4.1
# Fri, 12 Jan 2024 14:13:45 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Fri, 12 Jan 2024 14:13:45 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Fri, 12 Jan 2024 14:13:45 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 12 Jan 2024 14:13:45 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
WORKDIR /opt/emqx
# Fri, 12 Jan 2024 14:13:45 GMT
USER emqx
# Fri, 12 Jan 2024 14:13:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 12 Jan 2024 14:13:45 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 12 Jan 2024 14:13:45 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3602325be2f03896f21a1b18ec916d00c20d1d0d4ff357ea418b351ddfc993b7`  
		Last Modified: Mon, 08 Jul 2024 19:12:18 GMT  
		Size: 78.4 MB (78409005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a443efe216cff55e388643f0246e1746bde91e197528a31e4a5f5109c29ff585`  
		Last Modified: Mon, 08 Jul 2024 19:12:15 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4.1` - unknown; unknown

```console
$ docker pull emqx@sha256:a23fd6dc2af4f850b35bdd7e407b53bf1c0a51186b5b1664d910a5ec74580def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2785839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88ab692e308275b2fdcef7f96f5e805f0af93a0b98992f7a6d0c05ea084ae6a`

```dockerfile
```

-	Layers:
	-	`sha256:7ebad33375cb3eb1724f405536bce35e2b65b667071a82abcb0ddb31ac31b7cd`  
		Last Modified: Mon, 08 Jul 2024 19:12:16 GMT  
		Size: 2.8 MB (2773057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c54a86be65a75bb9a55e0e2ecedb678e8fa8801603ed8ee8e5b262bcc3d6617`  
		Last Modified: Mon, 08 Jul 2024 19:12:15 GMT  
		Size: 12.8 KB (12782 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.5`

```console
$ docker pull emqx@sha256:b5544437f21180a829af7ed5950910c06282414337a176c5e0ccdfb59bf84fee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.5` - linux; amd64

```console
$ docker pull emqx@sha256:d5f2cb2a5502757eba734c225cdb184cc6a8730bb511157e3bbe2e056e0d3024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121268622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d314375323dde3608b960c3945617a227981386ab755843f8398202ebb7819`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["bash"]
# Wed, 03 Apr 2024 12:49:39 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 03 Apr 2024 12:49:39 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 03 Apr 2024 12:49:39 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 03 Apr 2024 12:49:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 Apr 2024 12:49:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
WORKDIR /opt/emqx
# Wed, 03 Apr 2024 12:49:39 GMT
USER emqx
# Wed, 03 Apr 2024 12:49:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 Apr 2024 12:49:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 03 Apr 2024 12:49:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6404f8ff86888fd6c35089c5bd704c38ef0605c8a8ce905a3524b656003fe8b5`  
		Last Modified: Tue, 23 Jul 2024 07:19:39 GMT  
		Size: 89.8 MB (89839229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef18a9365b7f384b5e01a202bbba4d12664d019282cc89130608da8f1e4dad0d`  
		Last Modified: Tue, 23 Jul 2024 07:19:37 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5` - unknown; unknown

```console
$ docker pull emqx@sha256:7baffabd412d6360aaf075abf42876c48d64785fc6ee447e6cdde5f9337b6e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0adb12e0ab236b5bacc29103cc97f6640aee8ffa6a43395270d4ea841f92b08`

```dockerfile
```

-	Layers:
	-	`sha256:b378b471d429c4426abbd08382ef61722d20dc5092766ee7354839fd18a9c0f5`  
		Last Modified: Tue, 23 Jul 2024 07:19:37 GMT  
		Size: 2.8 MB (2810477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea5a377f056dfec42047ac3dfdd3075d88964aa8f502faf12e8316b40f7e9b04`  
		Last Modified: Tue, 23 Jul 2024 07:19:37 GMT  
		Size: 12.6 KB (12605 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:ac7bf171d1a3642d64769d50db4aaa1da31af3078465c6336c600485d37daf23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116777814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5258c409483366dae6b03bb495f5ca837095616adc4eb76abc9648884ddb83e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["bash"]
# Wed, 03 Apr 2024 12:49:39 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 03 Apr 2024 12:49:39 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 03 Apr 2024 12:49:39 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 03 Apr 2024 12:49:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 Apr 2024 12:49:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
WORKDIR /opt/emqx
# Wed, 03 Apr 2024 12:49:39 GMT
USER emqx
# Wed, 03 Apr 2024 12:49:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 Apr 2024 12:49:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 03 Apr 2024 12:49:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683d31784681b627bf9d7a783bdd8234bd2e23eb72007310cfbd93ccb01ca839`  
		Last Modified: Mon, 08 Jul 2024 19:12:54 GMT  
		Size: 86.7 MB (86707135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d443b25a39e53134295d1fbc3ffaecb74826d01b2d2bbc0e630c27ade7c64057`  
		Last Modified: Mon, 08 Jul 2024 19:12:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5` - unknown; unknown

```console
$ docker pull emqx@sha256:46e79cb810438a94f5c4465c05e12ecf07d3b5f87d0cc037d53ff4980d54e0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2785901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9787d744429f183b66f26754b4a33a6169c2b5ed796bea91655b2e86e78648`

```dockerfile
```

-	Layers:
	-	`sha256:aef6b69a7208c02e2b911d26c930fd16fc7074b491330289101ec477407b3a19`  
		Last Modified: Mon, 08 Jul 2024 19:12:52 GMT  
		Size: 2.8 MB (2773018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e816758d0759f99074fb60904d9e203c2b52b50cea7267960c27cde890b1fe7`  
		Last Modified: Mon, 08 Jul 2024 19:12:51 GMT  
		Size: 12.9 KB (12883 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.5.1`

```console
$ docker pull emqx@sha256:b5544437f21180a829af7ed5950910c06282414337a176c5e0ccdfb59bf84fee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.5.1` - linux; amd64

```console
$ docker pull emqx@sha256:d5f2cb2a5502757eba734c225cdb184cc6a8730bb511157e3bbe2e056e0d3024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121268622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d314375323dde3608b960c3945617a227981386ab755843f8398202ebb7819`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["bash"]
# Wed, 03 Apr 2024 12:49:39 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 03 Apr 2024 12:49:39 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 03 Apr 2024 12:49:39 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 03 Apr 2024 12:49:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 Apr 2024 12:49:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
WORKDIR /opt/emqx
# Wed, 03 Apr 2024 12:49:39 GMT
USER emqx
# Wed, 03 Apr 2024 12:49:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 Apr 2024 12:49:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 03 Apr 2024 12:49:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6404f8ff86888fd6c35089c5bd704c38ef0605c8a8ce905a3524b656003fe8b5`  
		Last Modified: Tue, 23 Jul 2024 07:19:39 GMT  
		Size: 89.8 MB (89839229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef18a9365b7f384b5e01a202bbba4d12664d019282cc89130608da8f1e4dad0d`  
		Last Modified: Tue, 23 Jul 2024 07:19:37 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5.1` - unknown; unknown

```console
$ docker pull emqx@sha256:7baffabd412d6360aaf075abf42876c48d64785fc6ee447e6cdde5f9337b6e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0adb12e0ab236b5bacc29103cc97f6640aee8ffa6a43395270d4ea841f92b08`

```dockerfile
```

-	Layers:
	-	`sha256:b378b471d429c4426abbd08382ef61722d20dc5092766ee7354839fd18a9c0f5`  
		Last Modified: Tue, 23 Jul 2024 07:19:37 GMT  
		Size: 2.8 MB (2810477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea5a377f056dfec42047ac3dfdd3075d88964aa8f502faf12e8316b40f7e9b04`  
		Last Modified: Tue, 23 Jul 2024 07:19:37 GMT  
		Size: 12.6 KB (12605 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:ac7bf171d1a3642d64769d50db4aaa1da31af3078465c6336c600485d37daf23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116777814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5258c409483366dae6b03bb495f5ca837095616adc4eb76abc9648884ddb83e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["bash"]
# Wed, 03 Apr 2024 12:49:39 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 03 Apr 2024 12:49:39 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 03 Apr 2024 12:49:39 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 03 Apr 2024 12:49:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 Apr 2024 12:49:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
WORKDIR /opt/emqx
# Wed, 03 Apr 2024 12:49:39 GMT
USER emqx
# Wed, 03 Apr 2024 12:49:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 Apr 2024 12:49:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 03 Apr 2024 12:49:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683d31784681b627bf9d7a783bdd8234bd2e23eb72007310cfbd93ccb01ca839`  
		Last Modified: Mon, 08 Jul 2024 19:12:54 GMT  
		Size: 86.7 MB (86707135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d443b25a39e53134295d1fbc3ffaecb74826d01b2d2bbc0e630c27ade7c64057`  
		Last Modified: Mon, 08 Jul 2024 19:12:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5.1` - unknown; unknown

```console
$ docker pull emqx@sha256:46e79cb810438a94f5c4465c05e12ecf07d3b5f87d0cc037d53ff4980d54e0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2785901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9787d744429f183b66f26754b4a33a6169c2b5ed796bea91655b2e86e78648`

```dockerfile
```

-	Layers:
	-	`sha256:aef6b69a7208c02e2b911d26c930fd16fc7074b491330289101ec477407b3a19`  
		Last Modified: Mon, 08 Jul 2024 19:12:52 GMT  
		Size: 2.8 MB (2773018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e816758d0759f99074fb60904d9e203c2b52b50cea7267960c27cde890b1fe7`  
		Last Modified: Mon, 08 Jul 2024 19:12:51 GMT  
		Size: 12.9 KB (12883 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.6`

```console
$ docker pull emqx@sha256:aac6d71e2100d0201492bbcb11c144c60467d5cea59f7b50b570104d8c7f1bb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.6` - linux; amd64

```console
$ docker pull emqx@sha256:675686d706f0bc997abdf76c0acfb619a638ce47d9f0e28b790dc77e587a6ec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124180948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23cce53894a9ea27727dc3c93f3baa6f56d37e4458355bcf3dcef8f69d4c7b71`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 06:31:42 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 06:31:42 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 06:31:42 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 06:31:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 06:31:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 06:31:42 GMT
USER emqx
# Mon, 22 Apr 2024 06:31:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 06:31:42 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 22 Apr 2024 06:31:42 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461dd64345866487ebdf19993bae617d70db890df0434a3236814f9021d81316`  
		Last Modified: Tue, 23 Jul 2024 07:19:46 GMT  
		Size: 95.1 MB (95053598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14f3a6b5697a0da8dc4f0b4d143f40a276048a4a7637ae73ee9edcb1df171cc`  
		Last Modified: Tue, 23 Jul 2024 07:19:45 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6` - unknown; unknown

```console
$ docker pull emqx@sha256:de786f8388623ea594e1575de843456177d34f6817d6f4021670e2d8165246d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2603152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc028b2643d7b121b3ab23b5b9c73b23a0fd8c2ee9ce4f5bdde5bd8f398a919`

```dockerfile
```

-	Layers:
	-	`sha256:e0f0104ada8dbe65bbbeec15e8402083574a9f6a69d055750a8630150a2c348c`  
		Last Modified: Tue, 23 Jul 2024 07:19:45 GMT  
		Size: 2.6 MB (2591425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a13de0cd6cfd5dc1496ce8183ba1f42f05776c3ebc0c75ba4f36d16e95351e7`  
		Last Modified: Tue, 23 Jul 2024 07:19:45 GMT  
		Size: 11.7 KB (11727 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:3672b7c05cce1e4925fd46a8bda3a5c1584f222d42e408a35048264d743d71f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120775029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e6d072aa51b5aaf239a941c72b3ec197802b764183f48127a6321c99fdc7dd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 06:31:42 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 06:31:42 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 06:31:42 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 06:31:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 06:31:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 06:31:42 GMT
USER emqx
# Mon, 22 Apr 2024 06:31:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 06:31:42 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 22 Apr 2024 06:31:42 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43835f8cf5b229f55d9c7b439ff9d127fe655be4b2bd9e4d9e5ed35271314631`  
		Last Modified: Mon, 08 Jul 2024 19:13:41 GMT  
		Size: 91.6 MB (91617405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5679dd221f9633c40dc1c6987afed73d67588bd6649bee99983230043238e7e0`  
		Last Modified: Mon, 08 Jul 2024 19:13:39 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6` - unknown; unknown

```console
$ docker pull emqx@sha256:9345065322dae3f338d4ac8a509937978b4580c83359bbd369328036e524684a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2564419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c2ade3b0c32f55629eca99573bc25cc300b71421082cd5f9184fc49148d718`

```dockerfile
```

-	Layers:
	-	`sha256:e3cb7cb3dcf0adccbe9d4689b327b5b1e893d797d115eeacfa3cbf85c54f944c`  
		Last Modified: Mon, 08 Jul 2024 19:13:39 GMT  
		Size: 2.6 MB (2552413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb734b3bd3151a422e104ddf51890260a2f9be4dcbede4614c180993038d1d40`  
		Last Modified: Mon, 08 Jul 2024 19:13:38 GMT  
		Size: 12.0 KB (12006 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.6.1`

```console
$ docker pull emqx@sha256:aac6d71e2100d0201492bbcb11c144c60467d5cea59f7b50b570104d8c7f1bb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.6.1` - linux; amd64

```console
$ docker pull emqx@sha256:675686d706f0bc997abdf76c0acfb619a638ce47d9f0e28b790dc77e587a6ec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124180948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23cce53894a9ea27727dc3c93f3baa6f56d37e4458355bcf3dcef8f69d4c7b71`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 06:31:42 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 06:31:42 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 06:31:42 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 06:31:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 06:31:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 06:31:42 GMT
USER emqx
# Mon, 22 Apr 2024 06:31:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 06:31:42 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 22 Apr 2024 06:31:42 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461dd64345866487ebdf19993bae617d70db890df0434a3236814f9021d81316`  
		Last Modified: Tue, 23 Jul 2024 07:19:46 GMT  
		Size: 95.1 MB (95053598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14f3a6b5697a0da8dc4f0b4d143f40a276048a4a7637ae73ee9edcb1df171cc`  
		Last Modified: Tue, 23 Jul 2024 07:19:45 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6.1` - unknown; unknown

```console
$ docker pull emqx@sha256:de786f8388623ea594e1575de843456177d34f6817d6f4021670e2d8165246d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2603152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc028b2643d7b121b3ab23b5b9c73b23a0fd8c2ee9ce4f5bdde5bd8f398a919`

```dockerfile
```

-	Layers:
	-	`sha256:e0f0104ada8dbe65bbbeec15e8402083574a9f6a69d055750a8630150a2c348c`  
		Last Modified: Tue, 23 Jul 2024 07:19:45 GMT  
		Size: 2.6 MB (2591425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a13de0cd6cfd5dc1496ce8183ba1f42f05776c3ebc0c75ba4f36d16e95351e7`  
		Last Modified: Tue, 23 Jul 2024 07:19:45 GMT  
		Size: 11.7 KB (11727 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.6.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:3672b7c05cce1e4925fd46a8bda3a5c1584f222d42e408a35048264d743d71f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120775029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e6d072aa51b5aaf239a941c72b3ec197802b764183f48127a6321c99fdc7dd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 06:31:42 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 06:31:42 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 06:31:42 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 06:31:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 06:31:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 06:31:42 GMT
USER emqx
# Mon, 22 Apr 2024 06:31:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 06:31:42 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 22 Apr 2024 06:31:42 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43835f8cf5b229f55d9c7b439ff9d127fe655be4b2bd9e4d9e5ed35271314631`  
		Last Modified: Mon, 08 Jul 2024 19:13:41 GMT  
		Size: 91.6 MB (91617405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5679dd221f9633c40dc1c6987afed73d67588bd6649bee99983230043238e7e0`  
		Last Modified: Mon, 08 Jul 2024 19:13:39 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6.1` - unknown; unknown

```console
$ docker pull emqx@sha256:9345065322dae3f338d4ac8a509937978b4580c83359bbd369328036e524684a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2564419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c2ade3b0c32f55629eca99573bc25cc300b71421082cd5f9184fc49148d718`

```dockerfile
```

-	Layers:
	-	`sha256:e3cb7cb3dcf0adccbe9d4689b327b5b1e893d797d115eeacfa3cbf85c54f944c`  
		Last Modified: Mon, 08 Jul 2024 19:13:39 GMT  
		Size: 2.6 MB (2552413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb734b3bd3151a422e104ddf51890260a2f9be4dcbede4614c180993038d1d40`  
		Last Modified: Mon, 08 Jul 2024 19:13:38 GMT  
		Size: 12.0 KB (12006 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:51c39f5995f6aedd292707e73c7dbfbe8b72b82a5d0e2be5f2ef1c14df09c599
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:66c1f31561788effe34d9804299758d4927b7e11d8467297de202a96835f925f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126238122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fdc5370bf923bab8c90743b24666bca939fd1f2874c786e47d23fa1fbbfd87b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jun 2024 06:50:32 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 06:50:32 GMT
ENV EMQX_VERSION=5.7.1
# Thu, 27 Jun 2024 06:50:32 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Thu, 27 Jun 2024 06:50:32 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Thu, 27 Jun 2024 06:50:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Jun 2024 06:50:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
WORKDIR /opt/emqx
# Thu, 27 Jun 2024 06:50:32 GMT
USER emqx
# Thu, 27 Jun 2024 06:50:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Jun 2024 06:50:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 27 Jun 2024 06:50:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ea6242b71c16ce1352fcf57a0d11687c2bd0b9fd496834fd62f76dd8f5ebf2`  
		Last Modified: Tue, 23 Jul 2024 07:19:54 GMT  
		Size: 97.1 MB (97110772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312a74d0107a3ee33685af3838ac090917b45e87cb3006fc6192781d92482b4c`  
		Last Modified: Tue, 23 Jul 2024 07:19:51 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:8e4ad0134f93a3a02b2167fa3392b9b80c19466227b895ce27358ee2077c37ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2612062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f34cd44ade291f177d0677daa06c10214702867382053ae2ca28173d626e3f8`

```dockerfile
```

-	Layers:
	-	`sha256:7c83086fd6007886c99a90d7d357091c7e561d320beb2faba0c8bbcc497c6298`  
		Last Modified: Tue, 23 Jul 2024 07:19:51 GMT  
		Size: 2.6 MB (2599757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4740c9a8c3c0fdbc38c099b4759c70dc685a1bdf61a78e9702f2e6540074d6fb`  
		Last Modified: Tue, 23 Jul 2024 07:19:51 GMT  
		Size: 12.3 KB (12305 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:074ff8d864916263abc6e8c42120a7efa67fea641cb6a3a070a3614a2c5b66d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122815523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:573da311dffd01ef129754dc5a68bc6494d88d070bb031800b6881927091e973`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jun 2024 06:50:32 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 06:50:32 GMT
ENV EMQX_VERSION=5.7.1
# Thu, 27 Jun 2024 06:50:32 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Thu, 27 Jun 2024 06:50:32 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Thu, 27 Jun 2024 06:50:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Jun 2024 06:50:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
WORKDIR /opt/emqx
# Thu, 27 Jun 2024 06:50:32 GMT
USER emqx
# Thu, 27 Jun 2024 06:50:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Jun 2024 06:50:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 27 Jun 2024 06:50:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b31646db1381832e88900fde1500ba647e8458191411a4d10dcc4c8becfe406`  
		Last Modified: Mon, 08 Jul 2024 19:14:23 GMT  
		Size: 93.7 MB (93657896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762d975f3920ce02bd4da5ca7a8fdc83b4f8f921649f9451c80a10c3edccf678`  
		Last Modified: Mon, 08 Jul 2024 19:14:20 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:dd3bbbb96dcc4b68baf65342c6a21b9823d447ab4b1885e31b16f99167788509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb517a98e5b34cd172b0be13bd95c2cf36068984db6969a8c563accb9a671403`

```dockerfile
```

-	Layers:
	-	`sha256:5dd0ef27adb8bfba84a8a3bbd60855144597953b9ee86a6b30793bdc44cdb30c`  
		Last Modified: Mon, 08 Jul 2024 19:14:21 GMT  
		Size: 2.6 MB (2559768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b57ba143a92dd352085be44c5cc683e7846827132d92ab0aa6c287b80b3d3ac`  
		Last Modified: Mon, 08 Jul 2024 19:14:20 GMT  
		Size: 12.6 KB (12607 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.1`

```console
$ docker pull emqx@sha256:51c39f5995f6aedd292707e73c7dbfbe8b72b82a5d0e2be5f2ef1c14df09c599
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.1` - linux; amd64

```console
$ docker pull emqx@sha256:66c1f31561788effe34d9804299758d4927b7e11d8467297de202a96835f925f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126238122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fdc5370bf923bab8c90743b24666bca939fd1f2874c786e47d23fa1fbbfd87b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jun 2024 06:50:32 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 06:50:32 GMT
ENV EMQX_VERSION=5.7.1
# Thu, 27 Jun 2024 06:50:32 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Thu, 27 Jun 2024 06:50:32 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Thu, 27 Jun 2024 06:50:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Jun 2024 06:50:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
WORKDIR /opt/emqx
# Thu, 27 Jun 2024 06:50:32 GMT
USER emqx
# Thu, 27 Jun 2024 06:50:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Jun 2024 06:50:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 27 Jun 2024 06:50:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ea6242b71c16ce1352fcf57a0d11687c2bd0b9fd496834fd62f76dd8f5ebf2`  
		Last Modified: Tue, 23 Jul 2024 07:19:54 GMT  
		Size: 97.1 MB (97110772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312a74d0107a3ee33685af3838ac090917b45e87cb3006fc6192781d92482b4c`  
		Last Modified: Tue, 23 Jul 2024 07:19:51 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.1` - unknown; unknown

```console
$ docker pull emqx@sha256:8e4ad0134f93a3a02b2167fa3392b9b80c19466227b895ce27358ee2077c37ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2612062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f34cd44ade291f177d0677daa06c10214702867382053ae2ca28173d626e3f8`

```dockerfile
```

-	Layers:
	-	`sha256:7c83086fd6007886c99a90d7d357091c7e561d320beb2faba0c8bbcc497c6298`  
		Last Modified: Tue, 23 Jul 2024 07:19:51 GMT  
		Size: 2.6 MB (2599757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4740c9a8c3c0fdbc38c099b4759c70dc685a1bdf61a78e9702f2e6540074d6fb`  
		Last Modified: Tue, 23 Jul 2024 07:19:51 GMT  
		Size: 12.3 KB (12305 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:074ff8d864916263abc6e8c42120a7efa67fea641cb6a3a070a3614a2c5b66d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122815523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:573da311dffd01ef129754dc5a68bc6494d88d070bb031800b6881927091e973`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jun 2024 06:50:32 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 06:50:32 GMT
ENV EMQX_VERSION=5.7.1
# Thu, 27 Jun 2024 06:50:32 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Thu, 27 Jun 2024 06:50:32 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Thu, 27 Jun 2024 06:50:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Jun 2024 06:50:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
WORKDIR /opt/emqx
# Thu, 27 Jun 2024 06:50:32 GMT
USER emqx
# Thu, 27 Jun 2024 06:50:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Jun 2024 06:50:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 27 Jun 2024 06:50:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b31646db1381832e88900fde1500ba647e8458191411a4d10dcc4c8becfe406`  
		Last Modified: Mon, 08 Jul 2024 19:14:23 GMT  
		Size: 93.7 MB (93657896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762d975f3920ce02bd4da5ca7a8fdc83b4f8f921649f9451c80a10c3edccf678`  
		Last Modified: Mon, 08 Jul 2024 19:14:20 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.1` - unknown; unknown

```console
$ docker pull emqx@sha256:dd3bbbb96dcc4b68baf65342c6a21b9823d447ab4b1885e31b16f99167788509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb517a98e5b34cd172b0be13bd95c2cf36068984db6969a8c563accb9a671403`

```dockerfile
```

-	Layers:
	-	`sha256:5dd0ef27adb8bfba84a8a3bbd60855144597953b9ee86a6b30793bdc44cdb30c`  
		Last Modified: Mon, 08 Jul 2024 19:14:21 GMT  
		Size: 2.6 MB (2559768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b57ba143a92dd352085be44c5cc683e7846827132d92ab0aa6c287b80b3d3ac`  
		Last Modified: Mon, 08 Jul 2024 19:14:20 GMT  
		Size: 12.6 KB (12607 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:51c39f5995f6aedd292707e73c7dbfbe8b72b82a5d0e2be5f2ef1c14df09c599
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:66c1f31561788effe34d9804299758d4927b7e11d8467297de202a96835f925f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126238122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fdc5370bf923bab8c90743b24666bca939fd1f2874c786e47d23fa1fbbfd87b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jun 2024 06:50:32 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 06:50:32 GMT
ENV EMQX_VERSION=5.7.1
# Thu, 27 Jun 2024 06:50:32 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Thu, 27 Jun 2024 06:50:32 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Thu, 27 Jun 2024 06:50:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Jun 2024 06:50:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
WORKDIR /opt/emqx
# Thu, 27 Jun 2024 06:50:32 GMT
USER emqx
# Thu, 27 Jun 2024 06:50:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Jun 2024 06:50:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 27 Jun 2024 06:50:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ea6242b71c16ce1352fcf57a0d11687c2bd0b9fd496834fd62f76dd8f5ebf2`  
		Last Modified: Tue, 23 Jul 2024 07:19:54 GMT  
		Size: 97.1 MB (97110772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312a74d0107a3ee33685af3838ac090917b45e87cb3006fc6192781d92482b4c`  
		Last Modified: Tue, 23 Jul 2024 07:19:51 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:8e4ad0134f93a3a02b2167fa3392b9b80c19466227b895ce27358ee2077c37ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2612062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f34cd44ade291f177d0677daa06c10214702867382053ae2ca28173d626e3f8`

```dockerfile
```

-	Layers:
	-	`sha256:7c83086fd6007886c99a90d7d357091c7e561d320beb2faba0c8bbcc497c6298`  
		Last Modified: Tue, 23 Jul 2024 07:19:51 GMT  
		Size: 2.6 MB (2599757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4740c9a8c3c0fdbc38c099b4759c70dc685a1bdf61a78e9702f2e6540074d6fb`  
		Last Modified: Tue, 23 Jul 2024 07:19:51 GMT  
		Size: 12.3 KB (12305 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:074ff8d864916263abc6e8c42120a7efa67fea641cb6a3a070a3614a2c5b66d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122815523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:573da311dffd01ef129754dc5a68bc6494d88d070bb031800b6881927091e973`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jun 2024 06:50:32 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 06:50:32 GMT
ENV EMQX_VERSION=5.7.1
# Thu, 27 Jun 2024 06:50:32 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Thu, 27 Jun 2024 06:50:32 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Thu, 27 Jun 2024 06:50:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Jun 2024 06:50:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
WORKDIR /opt/emqx
# Thu, 27 Jun 2024 06:50:32 GMT
USER emqx
# Thu, 27 Jun 2024 06:50:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Jun 2024 06:50:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 27 Jun 2024 06:50:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b31646db1381832e88900fde1500ba647e8458191411a4d10dcc4c8becfe406`  
		Last Modified: Mon, 08 Jul 2024 19:14:23 GMT  
		Size: 93.7 MB (93657896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762d975f3920ce02bd4da5ca7a8fdc83b4f8f921649f9451c80a10c3edccf678`  
		Last Modified: Mon, 08 Jul 2024 19:14:20 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:dd3bbbb96dcc4b68baf65342c6a21b9823d447ab4b1885e31b16f99167788509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb517a98e5b34cd172b0be13bd95c2cf36068984db6969a8c563accb9a671403`

```dockerfile
```

-	Layers:
	-	`sha256:5dd0ef27adb8bfba84a8a3bbd60855144597953b9ee86a6b30793bdc44cdb30c`  
		Last Modified: Mon, 08 Jul 2024 19:14:21 GMT  
		Size: 2.6 MB (2559768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b57ba143a92dd352085be44c5cc683e7846827132d92ab0aa6c287b80b3d3ac`  
		Last Modified: Mon, 08 Jul 2024 19:14:20 GMT  
		Size: 12.6 KB (12607 bytes)  
		MIME: application/vnd.in-toto+json
