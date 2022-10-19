<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `sapmachine`

-	[`sapmachine:11`](#sapmachine11)
-	[`sapmachine:11.0.17`](#sapmachine11017)
-	[`sapmachine:17`](#sapmachine17)
-	[`sapmachine:17.0.5`](#sapmachine1705)
-	[`sapmachine:19`](#sapmachine19)
-	[`sapmachine:19.0.1`](#sapmachine1901)
-	[`sapmachine:latest`](#sapmachinelatest)
-	[`sapmachine:lts`](#sapmachinelts)

## `sapmachine:11`

```console
$ docker pull sapmachine@sha256:0004dc37f1d0b9667c37f219395fe0690261dd75a56363cc14011df65ad06c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:11` - linux; amd64

```console
$ docker pull sapmachine@sha256:7f7670e1caa5de4bc001e09b204086174bebe82da7d20181196b6d46c952683a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235119904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3df038a66947a8562f5665f39d3120013d22e93302109f847cd1c19100c8bf3`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:09:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:47:26 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.17     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:47:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 19 Oct 2022 19:47:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0b13da87099833442bbfa96ea98ecb8c17f08743ed487859d5091012fa27a9`  
		Last Modified: Wed, 05 Oct 2022 18:11:18 GMT  
		Size: 7.9 MB (7920113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c58044bde1e64fa917308c3ee47dba5e1fdca2dd52763a2fd00a1f332d84e33`  
		Last Modified: Wed, 19 Oct 2022 19:49:08 GMT  
		Size: 198.6 MB (198625340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:11.0.17`

```console
$ docker pull sapmachine@sha256:0004dc37f1d0b9667c37f219395fe0690261dd75a56363cc14011df65ad06c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:11.0.17` - linux; amd64

```console
$ docker pull sapmachine@sha256:7f7670e1caa5de4bc001e09b204086174bebe82da7d20181196b6d46c952683a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235119904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3df038a66947a8562f5665f39d3120013d22e93302109f847cd1c19100c8bf3`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:09:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:47:26 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.17     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:47:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 19 Oct 2022 19:47:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0b13da87099833442bbfa96ea98ecb8c17f08743ed487859d5091012fa27a9`  
		Last Modified: Wed, 05 Oct 2022 18:11:18 GMT  
		Size: 7.9 MB (7920113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c58044bde1e64fa917308c3ee47dba5e1fdca2dd52763a2fd00a1f332d84e33`  
		Last Modified: Wed, 19 Oct 2022 19:49:08 GMT  
		Size: 198.6 MB (198625340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17`

```console
$ docker pull sapmachine@sha256:755aec1f288bb2c6129d16e85c2ec4af41fd3365ab812dd908d20ce1bda287c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:17` - linux; amd64

```console
$ docker pull sapmachine@sha256:cf10b0582a7b5408e8d95266169b428f8cd62653286cebd139583a3512fd2562
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.5 MB (234532649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285290ea9b8813926cfdf9f200a39e9b1b6277a0963e5a1b83d07aaedc2e601b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:09:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:48:03 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.5     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:48:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 19 Oct 2022 19:48:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0b13da87099833442bbfa96ea98ecb8c17f08743ed487859d5091012fa27a9`  
		Last Modified: Wed, 05 Oct 2022 18:11:18 GMT  
		Size: 7.9 MB (7920113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c35b7ead18b0a4008063e88686ff48525270ed2d5e8d75a98a485a1fab1e32`  
		Last Modified: Wed, 19 Oct 2022 19:49:33 GMT  
		Size: 198.0 MB (198038085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17.0.5`

```console
$ docker pull sapmachine@sha256:755aec1f288bb2c6129d16e85c2ec4af41fd3365ab812dd908d20ce1bda287c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:17.0.5` - linux; amd64

```console
$ docker pull sapmachine@sha256:cf10b0582a7b5408e8d95266169b428f8cd62653286cebd139583a3512fd2562
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.5 MB (234532649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285290ea9b8813926cfdf9f200a39e9b1b6277a0963e5a1b83d07aaedc2e601b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:09:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:48:03 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.5     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:48:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 19 Oct 2022 19:48:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0b13da87099833442bbfa96ea98ecb8c17f08743ed487859d5091012fa27a9`  
		Last Modified: Wed, 05 Oct 2022 18:11:18 GMT  
		Size: 7.9 MB (7920113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c35b7ead18b0a4008063e88686ff48525270ed2d5e8d75a98a485a1fab1e32`  
		Last Modified: Wed, 19 Oct 2022 19:49:33 GMT  
		Size: 198.0 MB (198038085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:19`

```console
$ docker pull sapmachine@sha256:8cac064ac11e626b124f0d081dd7f85c17d0925e1c2ef768ca5c98bbb58d8007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:19` - linux; amd64

```console
$ docker pull sapmachine@sha256:4bc993088086c4c245942726371ce3cf38bab56883f0dd7e1ff6f30c60ec6fce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242921163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510d8bb401632ac2a260973d4f4a8f75d616fb4bca9ec6b4f5342c44cbb309f2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:09:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:48:38 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19.0.1     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:48:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Wed, 19 Oct 2022 19:48:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0b13da87099833442bbfa96ea98ecb8c17f08743ed487859d5091012fa27a9`  
		Last Modified: Wed, 05 Oct 2022 18:11:18 GMT  
		Size: 7.9 MB (7920113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994bdc4c603a252d3d427fbb2731f10f2ec4c2e382c5f95faaf78893e034a95f`  
		Last Modified: Wed, 19 Oct 2022 19:50:00 GMT  
		Size: 206.4 MB (206426599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:19.0.1`

```console
$ docker pull sapmachine@sha256:8cac064ac11e626b124f0d081dd7f85c17d0925e1c2ef768ca5c98bbb58d8007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:19.0.1` - linux; amd64

```console
$ docker pull sapmachine@sha256:4bc993088086c4c245942726371ce3cf38bab56883f0dd7e1ff6f30c60ec6fce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242921163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510d8bb401632ac2a260973d4f4a8f75d616fb4bca9ec6b4f5342c44cbb309f2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:09:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:48:38 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19.0.1     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:48:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Wed, 19 Oct 2022 19:48:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0b13da87099833442bbfa96ea98ecb8c17f08743ed487859d5091012fa27a9`  
		Last Modified: Wed, 05 Oct 2022 18:11:18 GMT  
		Size: 7.9 MB (7920113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994bdc4c603a252d3d427fbb2731f10f2ec4c2e382c5f95faaf78893e034a95f`  
		Last Modified: Wed, 19 Oct 2022 19:50:00 GMT  
		Size: 206.4 MB (206426599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:8cac064ac11e626b124f0d081dd7f85c17d0925e1c2ef768ca5c98bbb58d8007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:4bc993088086c4c245942726371ce3cf38bab56883f0dd7e1ff6f30c60ec6fce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242921163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510d8bb401632ac2a260973d4f4a8f75d616fb4bca9ec6b4f5342c44cbb309f2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:09:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:48:38 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19.0.1     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:48:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Wed, 19 Oct 2022 19:48:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0b13da87099833442bbfa96ea98ecb8c17f08743ed487859d5091012fa27a9`  
		Last Modified: Wed, 05 Oct 2022 18:11:18 GMT  
		Size: 7.9 MB (7920113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994bdc4c603a252d3d427fbb2731f10f2ec4c2e382c5f95faaf78893e034a95f`  
		Last Modified: Wed, 19 Oct 2022 19:50:00 GMT  
		Size: 206.4 MB (206426599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:lts`

```console
$ docker pull sapmachine@sha256:755aec1f288bb2c6129d16e85c2ec4af41fd3365ab812dd908d20ce1bda287c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:lts` - linux; amd64

```console
$ docker pull sapmachine@sha256:cf10b0582a7b5408e8d95266169b428f8cd62653286cebd139583a3512fd2562
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.5 MB (234532649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285290ea9b8813926cfdf9f200a39e9b1b6277a0963e5a1b83d07aaedc2e601b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:09:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:48:03 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.5     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:48:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 19 Oct 2022 19:48:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0b13da87099833442bbfa96ea98ecb8c17f08743ed487859d5091012fa27a9`  
		Last Modified: Wed, 05 Oct 2022 18:11:18 GMT  
		Size: 7.9 MB (7920113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c35b7ead18b0a4008063e88686ff48525270ed2d5e8d75a98a485a1fab1e32`  
		Last Modified: Wed, 19 Oct 2022 19:49:33 GMT  
		Size: 198.0 MB (198038085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
