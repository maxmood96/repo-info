<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `sapmachine`

-	[`sapmachine:11`](#sapmachine11)
-	[`sapmachine:11.0.15.0.1`](#sapmachine1101501)
-	[`sapmachine:17`](#sapmachine17)
-	[`sapmachine:17.0.3.0.1`](#sapmachine170301)
-	[`sapmachine:18`](#sapmachine18)
-	[`sapmachine:18.0.1.1`](#sapmachine18011)
-	[`sapmachine:latest`](#sapmachinelatest)
-	[`sapmachine:lts`](#sapmachinelts)

## `sapmachine:11`

```console
$ docker pull sapmachine@sha256:588daa78f86dd3ddedc8838cfafec269d11444f7ca409281a358f4adfe662605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:11` - linux; amd64

```console
$ docker pull sapmachine@sha256:7c3afcdebcb3851109b100952a85e96a5afe6c8ff1a3dda56660b449ecd6fe45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234342106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8dca7428f5006e9c5a35c38dccf3a5166dd6f731d44025951c5e1fe97316c0`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:58:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:59:30 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.15.0.1     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:59:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 07 Jun 2022 01:59:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe776cde7ad2a2b7a4d2c92bae129822b7fe24c87f0491eb7c7e449bf80c59a`  
		Last Modified: Tue, 07 Jun 2022 02:01:02 GMT  
		Size: 7.9 MB (7926360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790b0a9db3568d78bbfc61f35ef38f0c3c1a46e435d4956d6ab90a29997e5f7a`  
		Last Modified: Tue, 07 Jun 2022 02:01:15 GMT  
		Size: 197.8 MB (197843114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:11.0.15.0.1`

```console
$ docker pull sapmachine@sha256:588daa78f86dd3ddedc8838cfafec269d11444f7ca409281a358f4adfe662605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:11.0.15.0.1` - linux; amd64

```console
$ docker pull sapmachine@sha256:7c3afcdebcb3851109b100952a85e96a5afe6c8ff1a3dda56660b449ecd6fe45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234342106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8dca7428f5006e9c5a35c38dccf3a5166dd6f731d44025951c5e1fe97316c0`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:58:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:59:30 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.15.0.1     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:59:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 07 Jun 2022 01:59:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe776cde7ad2a2b7a4d2c92bae129822b7fe24c87f0491eb7c7e449bf80c59a`  
		Last Modified: Tue, 07 Jun 2022 02:01:02 GMT  
		Size: 7.9 MB (7926360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790b0a9db3568d78bbfc61f35ef38f0c3c1a46e435d4956d6ab90a29997e5f7a`  
		Last Modified: Tue, 07 Jun 2022 02:01:15 GMT  
		Size: 197.8 MB (197843114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17`

```console
$ docker pull sapmachine@sha256:17a3555664e43e5b1ab818b28a25501273b13a33db289f02502d73aa3628a7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:17` - linux; amd64

```console
$ docker pull sapmachine@sha256:bf6bb34526844521788394a6effaa89285e12da0e8deb6a7dc7ccc9e84bc92af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234278304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a9ca25fa81085c0da18e385adfe53b1caa59575ab4f0316a6d7b2eacf09e1b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:58:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 02:00:02 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.3.0.1     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 02:00:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 07 Jun 2022 02:00:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe776cde7ad2a2b7a4d2c92bae129822b7fe24c87f0491eb7c7e449bf80c59a`  
		Last Modified: Tue, 07 Jun 2022 02:01:02 GMT  
		Size: 7.9 MB (7926360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df80882928ff58941ceb49d0ab69d77503c243f2135390a07aadea5ea7f3462`  
		Last Modified: Tue, 07 Jun 2022 02:01:51 GMT  
		Size: 197.8 MB (197779312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17.0.3.0.1`

```console
$ docker pull sapmachine@sha256:17a3555664e43e5b1ab818b28a25501273b13a33db289f02502d73aa3628a7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:17.0.3.0.1` - linux; amd64

```console
$ docker pull sapmachine@sha256:bf6bb34526844521788394a6effaa89285e12da0e8deb6a7dc7ccc9e84bc92af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234278304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a9ca25fa81085c0da18e385adfe53b1caa59575ab4f0316a6d7b2eacf09e1b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:58:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 02:00:02 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.3.0.1     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 02:00:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 07 Jun 2022 02:00:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe776cde7ad2a2b7a4d2c92bae129822b7fe24c87f0491eb7c7e449bf80c59a`  
		Last Modified: Tue, 07 Jun 2022 02:01:02 GMT  
		Size: 7.9 MB (7926360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df80882928ff58941ceb49d0ab69d77503c243f2135390a07aadea5ea7f3462`  
		Last Modified: Tue, 07 Jun 2022 02:01:51 GMT  
		Size: 197.8 MB (197779312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:18`

```console
$ docker pull sapmachine@sha256:497fd9b36f9f108f83a841b5a1190c13a1cc9817e31613f80bda738c65a4d069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:18` - linux; amd64

```console
$ docker pull sapmachine@sha256:596fad7aa95f6a6d1e7794659fd41508afc1744b7d54b35a79a8ac7b44b02e65
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235243730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599cc5383b23f2e74915056180ff942a41de27f7fa672845d608c35541b734be`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:58:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 02:00:39 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-18-jdk=18.0.1.1     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 02:00:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-18
# Tue, 07 Jun 2022 02:00:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe776cde7ad2a2b7a4d2c92bae129822b7fe24c87f0491eb7c7e449bf80c59a`  
		Last Modified: Tue, 07 Jun 2022 02:01:02 GMT  
		Size: 7.9 MB (7926360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766f3d6639478ad881be8dff4e22ff2f73f889301c1e45b41063f37daff048c2`  
		Last Modified: Tue, 07 Jun 2022 02:02:18 GMT  
		Size: 198.7 MB (198744738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:18.0.1.1`

```console
$ docker pull sapmachine@sha256:497fd9b36f9f108f83a841b5a1190c13a1cc9817e31613f80bda738c65a4d069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:18.0.1.1` - linux; amd64

```console
$ docker pull sapmachine@sha256:596fad7aa95f6a6d1e7794659fd41508afc1744b7d54b35a79a8ac7b44b02e65
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235243730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599cc5383b23f2e74915056180ff942a41de27f7fa672845d608c35541b734be`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:58:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 02:00:39 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-18-jdk=18.0.1.1     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 02:00:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-18
# Tue, 07 Jun 2022 02:00:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe776cde7ad2a2b7a4d2c92bae129822b7fe24c87f0491eb7c7e449bf80c59a`  
		Last Modified: Tue, 07 Jun 2022 02:01:02 GMT  
		Size: 7.9 MB (7926360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766f3d6639478ad881be8dff4e22ff2f73f889301c1e45b41063f37daff048c2`  
		Last Modified: Tue, 07 Jun 2022 02:02:18 GMT  
		Size: 198.7 MB (198744738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:497fd9b36f9f108f83a841b5a1190c13a1cc9817e31613f80bda738c65a4d069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:596fad7aa95f6a6d1e7794659fd41508afc1744b7d54b35a79a8ac7b44b02e65
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235243730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599cc5383b23f2e74915056180ff942a41de27f7fa672845d608c35541b734be`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:58:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 02:00:39 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-18-jdk=18.0.1.1     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 02:00:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-18
# Tue, 07 Jun 2022 02:00:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe776cde7ad2a2b7a4d2c92bae129822b7fe24c87f0491eb7c7e449bf80c59a`  
		Last Modified: Tue, 07 Jun 2022 02:01:02 GMT  
		Size: 7.9 MB (7926360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766f3d6639478ad881be8dff4e22ff2f73f889301c1e45b41063f37daff048c2`  
		Last Modified: Tue, 07 Jun 2022 02:02:18 GMT  
		Size: 198.7 MB (198744738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:lts`

```console
$ docker pull sapmachine@sha256:17a3555664e43e5b1ab818b28a25501273b13a33db289f02502d73aa3628a7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:lts` - linux; amd64

```console
$ docker pull sapmachine@sha256:bf6bb34526844521788394a6effaa89285e12da0e8deb6a7dc7ccc9e84bc92af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234278304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a9ca25fa81085c0da18e385adfe53b1caa59575ab4f0316a6d7b2eacf09e1b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:58:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 02:00:02 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.3.0.1     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 02:00:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 07 Jun 2022 02:00:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe776cde7ad2a2b7a4d2c92bae129822b7fe24c87f0491eb7c7e449bf80c59a`  
		Last Modified: Tue, 07 Jun 2022 02:01:02 GMT  
		Size: 7.9 MB (7926360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df80882928ff58941ceb49d0ab69d77503c243f2135390a07aadea5ea7f3462`  
		Last Modified: Tue, 07 Jun 2022 02:01:51 GMT  
		Size: 197.8 MB (197779312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
