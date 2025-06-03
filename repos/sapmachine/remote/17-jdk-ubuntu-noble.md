## `sapmachine:17-jdk-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:9abe0aa2c1b1f4b66b25edc7516c47c0a6c778673540289fe79d42917721cedf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:94cc21a285e3992576942f46c9a34d1b607620a1d961075e76dcf436fd220ce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230119249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f44c51ecf22cf0df674ddf9badddd35170849adb65ca9f6c1e5f9d51ff9b376`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9ed21bf16d010109638fdb04fb6f85601b38565ea6e4713380e1c10f66d362`  
		Last Modified: Tue, 03 Jun 2025 13:36:10 GMT  
		Size: 200.4 MB (200403912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:82c5a5c53e601c7faa6dbc528f03cfc5dcf2d4ef9bdbe77d5297ded69364f8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2506016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a473ce3a66f1196480bea0d1ba6cd539cd4f066692279752d9fb0e711b825b5`

```dockerfile
```

-	Layers:
	-	`sha256:d96f989fa2bdc0aaafafaedceffc131ece2a9440da4ecc00d8ebed56a85846db`  
		Last Modified: Tue, 03 Jun 2025 17:21:44 GMT  
		Size: 2.5 MB (2494622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc37c407d4ba7b1e5ef2b810098ad7a7026faa0f42aca334e8646825f15db8ac`  
		Last Modified: Tue, 03 Jun 2025 17:21:42 GMT  
		Size: 11.4 KB (11394 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3e398ae3a473fcc5a6ef616458ae57bf8e023b41a078677c5408865db6d3deb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228011764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b70d77a7513495da31e14c46981a11e7168ebf647f0fdcf9c8ba038f69702ab`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78af24ea68b2c2dbda63a9cc98e6286719db1bcb545d1b053b0dd9faeb870ed1`  
		Last Modified: Tue, 03 Jun 2025 14:40:33 GMT  
		Size: 199.2 MB (199159865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:abd99cb2311f697548ea7c8180680d7cd5f0e68f45694fdea911130d7173b26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2506780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2553ea3a7f72d7c16825c567a56cd066c45e70cf68c19af768bde993cf3455`

```dockerfile
```

-	Layers:
	-	`sha256:d4728fc79a9d1591a3cc6cfec268e8c5a2dbf8f9e565dad84cf6a3faae8e588c`  
		Last Modified: Tue, 03 Jun 2025 17:21:43 GMT  
		Size: 2.5 MB (2495186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2630e19e4f4c6e842bbab262ba912b252f0be5c8a1f3008555d21368c4fc3e0d`  
		Last Modified: Tue, 03 Jun 2025 17:21:43 GMT  
		Size: 11.6 KB (11594 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8c54546c2eaa5530760f1b4b74df5cc60036b8355c137b06e51b419552e3edf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235917031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5005c58114d89048b95f4e1f95152a46d02f34cffc845d5dff510fd5e97779`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74596d1c35eb463e5bc9e393d197b58daf08688bf438293ca27d2070bfeda15`  
		Last Modified: Tue, 03 Jun 2025 17:21:53 GMT  
		Size: 201.6 MB (201591821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a36e690ed88569948a532c1b81e38cd527acf1a47f9c663219b7ae27e81fbe20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2508282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4beab065a632b9af6e527a0225dbb7a4bfccc0eb4bd83b1b842525beb7f77b`

```dockerfile
```

-	Layers:
	-	`sha256:d0b9949ffc669c4482eca9894fbe824193f30703d30de5328ae70e70cebc3f94`  
		Last Modified: Tue, 03 Jun 2025 17:21:43 GMT  
		Size: 2.5 MB (2496797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61c6231f3d06bd3a2f021a6fdb938d3dc41f6429e28227c3c284cecc27d72f35`  
		Last Modified: Tue, 03 Jun 2025 17:21:42 GMT  
		Size: 11.5 KB (11485 bytes)  
		MIME: application/vnd.in-toto+json
