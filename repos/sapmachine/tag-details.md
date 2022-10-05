<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `sapmachine`

-	[`sapmachine:11`](#sapmachine11)
-	[`sapmachine:11.0.16.1`](#sapmachine110161)
-	[`sapmachine:17`](#sapmachine17)
-	[`sapmachine:17.0.4.1`](#sapmachine17041)
-	[`sapmachine:19`](#sapmachine19)
-	[`sapmachine:latest`](#sapmachinelatest)
-	[`sapmachine:lts`](#sapmachinelts)

## `sapmachine:11`

```console
$ docker pull sapmachine@sha256:1c1e9b7c66d83fa58d072a941d9cd01819f0cb1ffe02ba34b0bb24586e7eac32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:11` - linux; amd64

```console
$ docker pull sapmachine@sha256:6c6914f0483ea3dcca7123f4458c97f8b4bbc98dad3e96430ce442bf0bb9e977
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234785791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2426f09bf856e6b84b1f424b5e895c0f31cb2c79e440632bacf6619932892a05`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:09:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 18:09:43 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.16.1     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 18:09:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 05 Oct 2022 18:09:44 GMT
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
	-	`sha256:da2c881841450ee0ba843d135c5160f5e990daac5df5603786b17973d09eab72`  
		Last Modified: Wed, 05 Oct 2022 18:11:32 GMT  
		Size: 198.3 MB (198291227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:11.0.16.1`

```console
$ docker pull sapmachine@sha256:1c1e9b7c66d83fa58d072a941d9cd01819f0cb1ffe02ba34b0bb24586e7eac32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:11.0.16.1` - linux; amd64

```console
$ docker pull sapmachine@sha256:6c6914f0483ea3dcca7123f4458c97f8b4bbc98dad3e96430ce442bf0bb9e977
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234785791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2426f09bf856e6b84b1f424b5e895c0f31cb2c79e440632bacf6619932892a05`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:09:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 18:09:43 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.16.1     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 18:09:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 05 Oct 2022 18:09:44 GMT
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
	-	`sha256:da2c881841450ee0ba843d135c5160f5e990daac5df5603786b17973d09eab72`  
		Last Modified: Wed, 05 Oct 2022 18:11:32 GMT  
		Size: 198.3 MB (198291227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17`

```console
$ docker pull sapmachine@sha256:79dc41def81e896744ff43ebaf51827cc8bee5dd06e3844dbd093f0bcb9525f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:17` - linux; amd64

```console
$ docker pull sapmachine@sha256:9a325b6a9ff00813e79fd180f564ae075a3e51a8f42979d03fd439b4070ed237
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234258801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f711251a816890d8131d291378f2039f574b0aafcf14ac296db3da70d72e2fb3`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:09:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 18:10:23 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.4.1     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 18:10:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 05 Oct 2022 18:10:25 GMT
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
	-	`sha256:897b09c52e9c3c0090d0a17bb00c88daf0b5ff8c10d40087dd5f1fd895bd349a`  
		Last Modified: Wed, 05 Oct 2022 18:11:56 GMT  
		Size: 197.8 MB (197764237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17.0.4.1`

```console
$ docker pull sapmachine@sha256:79dc41def81e896744ff43ebaf51827cc8bee5dd06e3844dbd093f0bcb9525f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:17.0.4.1` - linux; amd64

```console
$ docker pull sapmachine@sha256:9a325b6a9ff00813e79fd180f564ae075a3e51a8f42979d03fd439b4070ed237
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234258801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f711251a816890d8131d291378f2039f574b0aafcf14ac296db3da70d72e2fb3`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:09:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 18:10:23 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.4.1     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 18:10:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 05 Oct 2022 18:10:25 GMT
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
	-	`sha256:897b09c52e9c3c0090d0a17bb00c88daf0b5ff8c10d40087dd5f1fd895bd349a`  
		Last Modified: Wed, 05 Oct 2022 18:11:56 GMT  
		Size: 197.8 MB (197764237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:19`

```console
$ docker pull sapmachine@sha256:38f62d1f316099659fea47a694ebc4ced919efc18e413bf73ea08edd7fc800ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:19` - linux; amd64

```console
$ docker pull sapmachine@sha256:954aea26e2daf0b37f8e6a881d8bedeab16373b0d990ebeeda96a726da765d8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.7 MB (242658131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c980783df16adbdce5e7ef29c498d1761043cbdf3cc940b6633db7e93e49b2c6`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:09:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 18:11:02 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 18:11:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Wed, 05 Oct 2022 18:11:03 GMT
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
	-	`sha256:6273b3fdc30cf2f78ba8fcd6518ab12af5faa5c3aa25c31c20f6f2c9368e1702`  
		Last Modified: Wed, 05 Oct 2022 18:12:25 GMT  
		Size: 206.2 MB (206163567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:38f62d1f316099659fea47a694ebc4ced919efc18e413bf73ea08edd7fc800ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:954aea26e2daf0b37f8e6a881d8bedeab16373b0d990ebeeda96a726da765d8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.7 MB (242658131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c980783df16adbdce5e7ef29c498d1761043cbdf3cc940b6633db7e93e49b2c6`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:09:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 18:11:02 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 18:11:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Wed, 05 Oct 2022 18:11:03 GMT
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
	-	`sha256:6273b3fdc30cf2f78ba8fcd6518ab12af5faa5c3aa25c31c20f6f2c9368e1702`  
		Last Modified: Wed, 05 Oct 2022 18:12:25 GMT  
		Size: 206.2 MB (206163567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:lts`

```console
$ docker pull sapmachine@sha256:79dc41def81e896744ff43ebaf51827cc8bee5dd06e3844dbd093f0bcb9525f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:lts` - linux; amd64

```console
$ docker pull sapmachine@sha256:9a325b6a9ff00813e79fd180f564ae075a3e51a8f42979d03fd439b4070ed237
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234258801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f711251a816890d8131d291378f2039f574b0aafcf14ac296db3da70d72e2fb3`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:09:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 18:10:23 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.4.1     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 18:10:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 05 Oct 2022 18:10:25 GMT
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
	-	`sha256:897b09c52e9c3c0090d0a17bb00c88daf0b5ff8c10d40087dd5f1fd895bd349a`  
		Last Modified: Wed, 05 Oct 2022 18:11:56 GMT  
		Size: 197.8 MB (197764237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
