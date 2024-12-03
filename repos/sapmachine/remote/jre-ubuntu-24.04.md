## `sapmachine:jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:241f3f3a1b6c07388d67c672d04918505a4c39f4db501649467b84ccbccf71d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:f7a2ee2de3bbc284fabdfdfa01712245a339af6cd745d05e4d7c35a306fe2343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89839993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5be022e12e3c93d83a2b6ad544a2b1614c001c60ac6b8688fac04e06933261b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:19 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:19 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab6e2c88af8dd9b285b7951077ff299e0f1874ad1c14c929fb568a023f6a6f5`  
		Last Modified: Tue, 03 Dec 2024 02:35:05 GMT  
		Size: 60.1 MB (60088025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5bd95f89c15aaed4cf01bab42a4f885890ad0fdbf38377ec19d7d570847c12b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2399046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2671636445a476ec1676526adf39192b21d4c126a4b42ec636726b0fe03d40a8`

```dockerfile
```

-	Layers:
	-	`sha256:b89f84ab31e021ccb386a73c4c1ef1f0b73d0d6db3f29bd00e97fa4771d12987`  
		Last Modified: Tue, 03 Dec 2024 02:35:05 GMT  
		Size: 2.4 MB (2388620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9fbfdec1534ce905ce447349e1baef8b7605e28dc2877cf373fcb2a7b644f1b`  
		Last Modified: Tue, 03 Dec 2024 02:35:04 GMT  
		Size: 10.4 KB (10426 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:5cc678b4756e572a37e45c471997debb31a53a67a2b4b313cf228947e4a24f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (88037339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e3711f20605f59dbc4fb7604387aa89328a5c0f520f648fd01bf8da448ebf7`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8efcd9ec98637cb4984088a807a7c9b24f6a585b4a07480c5cd5ddd2688336`  
		Last Modified: Sat, 16 Nov 2024 03:45:26 GMT  
		Size: 59.1 MB (59144914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1d153072ec8c66641c32e0c0c47b27f29412bab04923adcaaf0a07e7b715179e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2399086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67aaeede76c85dad880b40d0a17f6c99334a07cda7b51f012277f09ef0369dd3`

```dockerfile
```

-	Layers:
	-	`sha256:f8ad8a126b715b68419ca1ec3b058e0d6a97a469f24c9692e95ed0d22c2bf5a4`  
		Last Modified: Sat, 16 Nov 2024 03:45:24 GMT  
		Size: 2.4 MB (2388496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3572daafdf439f465dca9e7dd85a3866b6158ab9ed2a8162e2b63e9e6d2c256`  
		Last Modified: Sat, 16 Nov 2024 03:45:23 GMT  
		Size: 10.6 KB (10590 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f55f4807ea234c2a7e4f9052ac6d1aec4997f66802f3ffe72376acd26f70a002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96032162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9d02d145d7df330c094b52560fd490b7f8dee206d83defe087118774875a4f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 09:26:09 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:26:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:26:12 GMT
ADD file:8427b57c40c05cd946f6695dbd1754b0a521a98decd2cdc16eeb114c7128804a in / 
# Wed, 16 Oct 2024 09:26:12 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:991986948126e836a79c1084e3bee33549a43b83cabfe16234aef5b4b30d86f9`  
		Last Modified: Wed, 16 Oct 2024 12:48:24 GMT  
		Size: 34.4 MB (34388822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df1ff20329df5809bb39900ccbd6c146d7675167009c9d66bba03316ac59091`  
		Last Modified: Sat, 16 Nov 2024 03:43:07 GMT  
		Size: 61.6 MB (61643340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:76a07fb2b9427ede0c4f8809ba873a6d387281bb1851d845eefcd257e4d89722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d38bcc99b179a3ea5afb4fa5f6125f3c78a40607b7a25dffc8c91839d699c1`

```dockerfile
```

-	Layers:
	-	`sha256:9c1b01b86509174f8bef8eb4c06f9c22ba60f4bb08712c1ba80c25bdd99efaed`  
		Last Modified: Sat, 16 Nov 2024 03:43:05 GMT  
		Size: 2.4 MB (2391936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c77ba10aa04b30ca4a4cc3b42904ef934153ddb2aa5ab297aed347ce645522`  
		Last Modified: Sat, 16 Nov 2024 03:43:05 GMT  
		Size: 10.5 KB (10500 bytes)  
		MIME: application/vnd.in-toto+json
