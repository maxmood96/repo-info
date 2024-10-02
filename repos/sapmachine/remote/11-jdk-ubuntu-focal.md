## `sapmachine:11-jdk-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:60a4cf297213b4936cf7a98ddb2711c6fcf72a2e1bc9a9a827f87f12babf01c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:e917cccc01ef6b1bf4910266a7b78d59446e38a587decb831f999e65be37e80d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227794350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9f6fc552ff19e326ceab933dc6c255a8fb2fd5c2a4fdb729ff8644ed57c4f4`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9c3b9b07dc76ac0d24a1f87dac8e956141073301fd25d4eeac25913530a101`  
		Last Modified: Wed, 02 Oct 2024 02:00:23 GMT  
		Size: 200.3 MB (200283298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d8bf72f3282c0fc15e5fcf02e9d58f4a3fe88d80a3d4289a79b4db22f8c184fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2391833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfedef0702fdb41a57204b9e0847aa6cae0adda6cc227afe5d4103205b41d5c`

```dockerfile
```

-	Layers:
	-	`sha256:b37c1d9af874292b9b805f387b9d61a37d0f98bbc4e16541f113b6ebc8d888a2`  
		Last Modified: Wed, 02 Oct 2024 02:00:20 GMT  
		Size: 2.4 MB (2381944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac740fe99dd390ddc0273489eca91faea36c59cb3e834a578a053520e6d9497c`  
		Last Modified: Wed, 02 Oct 2024 02:00:20 GMT  
		Size: 9.9 KB (9889 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c730885a49184e1157ffac2deda3bacabd3ebaaca63e17fcc20fa1e2800e9026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224742674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf990be867baa799b02ea997f0246dfef9459511948045f20aa455c63cc8fb4`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f5597480e4e51ecb81f6638c73f36699bdc9abc216c2db9f36fef7af7241ff`  
		Last Modified: Wed, 02 Oct 2024 04:08:08 GMT  
		Size: 198.8 MB (198769082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7345df93c6a901e418791350c2c9c2332a0466f861e59405f5ddd6b7f41b41e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2392291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49101bb19ef50c0d6ff245baab98c6936022b5bcd5a04fb64175502fee35236c`

```dockerfile
```

-	Layers:
	-	`sha256:9d3072efc5f7c1401c0a43a6e6eb39c4ce51ab542026d57f61ac2a9c1e9d4a1e`  
		Last Modified: Wed, 02 Oct 2024 04:08:04 GMT  
		Size: 2.4 MB (2382256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3994374386520459a78ea8de60580018d4c59cb6a70cf8b46eb287a3176ce966`  
		Last Modified: Wed, 02 Oct 2024 04:08:03 GMT  
		Size: 10.0 KB (10035 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9cfdaee3aa051a635f3d1fb04e962afb7485d8ac82c8706becf83efbf530445c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218625266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d961fccb55483e7eee0ce8d5fc4d1c197a582f10dba03336edcdfe9e58d5c32b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cafd57629abc05d597016161b87b83b544a17d39d1016cfb289a60295fc7d492`  
		Last Modified: Wed, 18 Sep 2024 05:32:58 GMT  
		Size: 32.1 MB (32076334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c741981745350fd3be0b37a47417dd68b8ef67baed3f4dc44729f68e11ffca4`  
		Last Modified: Wed, 02 Oct 2024 03:26:19 GMT  
		Size: 186.5 MB (186548932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a179762882c79ae0e57f8a646d3feeb23fbb7effa51fbc7620bb5e1d4eacddeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2393110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a74f4455a78bc77d60cd200cf32f012c25e1dcf7b98526e3bd13dc66ea664c`

```dockerfile
```

-	Layers:
	-	`sha256:817296582e1238dbf3c53550cfe3dd0e061a8ed10c67c71c7053d91d66b14238`  
		Last Modified: Wed, 02 Oct 2024 03:26:15 GMT  
		Size: 2.4 MB (2383159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17db6dbf0c2f9bce79e11d9735d7f9cb2fb9c4b30c423ff646a205d2587fc933`  
		Last Modified: Wed, 02 Oct 2024 03:26:14 GMT  
		Size: 10.0 KB (9951 bytes)  
		MIME: application/vnd.in-toto+json
