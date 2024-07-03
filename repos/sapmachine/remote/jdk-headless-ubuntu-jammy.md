## `sapmachine:jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:5ea841000187f359b2f4f37ca4f124148d34e2a39bbe81f9fb3cc65912d73c6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:c836c6a90f08885663f6ad48d9539905f857c9987f48f86811cc2a7b977eb4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241727780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1283560733434a968a43c8e418faccd11b328f498ac5f2898100f8a98d58739a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b8af7642807b74e4fd4d9c7788a74056e9e4bf5d04481f93ba0bf200c07ed3`  
		Last Modified: Tue, 02 Jul 2024 03:31:51 GMT  
		Size: 212.2 MB (212193725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e90b7c3d560c721898b0825d93de04e8e8767a27c8519bf18b7d52f19a4b32e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25651a9491d58e6bcab5186e27cd1f9ff64455db03ea2ca891bea3713845ba74`

```dockerfile
```

-	Layers:
	-	`sha256:ec646ff7e35b7ca636a82f24ca31cecf003b12c9c35f219f881c60c4932d40ed`  
		Last Modified: Tue, 02 Jul 2024 03:31:48 GMT  
		Size: 2.2 MB (2204978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a0ee32f3c1b2e428ae1db24c856372374f0d3c210b4930df5167dafaa86c113`  
		Last Modified: Tue, 02 Jul 2024 03:31:48 GMT  
		Size: 9.4 KB (9376 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:eef03cd809f0426a92c3b2cc9d106b7c3ccb92ebc57243d8ba591377300e197e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237487368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998fd45d2e2eed5b6c1463b6e0b032a6044ccc5e7a9723147a9616a0adf142be`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3598e6d036efab8571f1b0e31e2a09c2314932b8a59e6956ff41f245532fd192`  
		Last Modified: Tue, 25 Jun 2024 23:55:34 GMT  
		Size: 210.1 MB (210125586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c04c9475cda11a2def6e3b41705fb54016863c6ea040c9787afb44d09fac10d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2213742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c07f9775add389e9422f7ba57d50e987cdc78e6d4f7aa47a547ace52738a38`

```dockerfile
```

-	Layers:
	-	`sha256:0a4cdc77f7f1a826a522b5d86de160e14bd79114aa7d31d26a110b31ceba33ba`  
		Last Modified: Tue, 25 Jun 2024 23:55:29 GMT  
		Size: 2.2 MB (2204041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:594e6528f4bc7d8fe562ece37ce8fb412bfd57ad5b47eb6cbaf253839ebbfec6`  
		Last Modified: Tue, 25 Jun 2024 23:55:28 GMT  
		Size: 9.7 KB (9701 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:eb31d8482fe491ecfd6fb46e28e323093063886d3fea39ae2553c066605b44d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.5 MB (247549225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5877868dd6cdf7ced38ddf48e9726b48b3d44b0437327a9686c79555f44386d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6799c90a640e44998365b1a0a6aa44c129fa3db23f0ed07565b2cd6b3138bde6`  
		Last Modified: Tue, 02 Jul 2024 21:21:19 GMT  
		Size: 213.1 MB (213088144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9e019bea472f98cc4fefedb1cf95e0e469295295749bcd01180e79fbf50c73db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2215752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146da4f9e7eabef218de39828166aefef81c1c804e22a0873350ab5565c10816`

```dockerfile
```

-	Layers:
	-	`sha256:70e8eea04165df21e31866075abc66c67494899663ba0b24afa7792f3004facc`  
		Last Modified: Tue, 02 Jul 2024 21:21:14 GMT  
		Size: 2.2 MB (2206331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8dd07e19695f4fea8be1c9128c6c189c40ae497c094ee6041c928d660b90a04`  
		Last Modified: Tue, 02 Jul 2024 21:21:14 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.in-toto+json
