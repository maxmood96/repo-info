## `sapmachine:11-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:02478f9a9bbe8d74238aaef282155cae2fac240f20f924eebce351f81d9605bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:1f2ea9427379b5596f765a44a0423f53e74ee8ff4953606878099d29c7d35af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78951368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7659e50809adfb7d0561d2748fd04ddbd58fab52a282e85b1d6388548266a583`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:16 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:16 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:16 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f67f328e874b3f75ccbcce2054236311f1c707d60e41a5185797054bda9b59`  
		Last Modified: Tue, 03 Dec 2024 02:37:23 GMT  
		Size: 49.2 MB (49199400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ef0bfdf59f9ec914990453d8d7ec980c02910998e24608e8974dc25a5f5707f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2163428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46eb3d43e200dd9e070ac1f01a22d75283bb3a10d64b536a7fd8ddbbef5b6278`

```dockerfile
```

-	Layers:
	-	`sha256:07eb1c9f4c48fd032afe3716a4dddf6a4aeec8b5c65f2186c4a1cf43669984b2`  
		Last Modified: Tue, 03 Dec 2024 02:37:22 GMT  
		Size: 2.2 MB (2153811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cae77cd667e98610fafbede61fa0549f1f7081093bc862415f79a99bdad45230`  
		Last Modified: Tue, 03 Dec 2024 02:37:22 GMT  
		Size: 9.6 KB (9617 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:93d4d9f3f7698e5602c7ca95b389cfeef912291071e97fdaea11b653a2d5d0ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77409578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120fd1e4d4341f725ba40f6fa2dad1ea7372c2b0a361e9af72bc61bab99895f9`
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
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b690615125ba0cd0b1a573b849dacbf901ea6bfb20594dd6bb37d8d6acab1d`  
		Last Modified: Sat, 16 Nov 2024 03:56:57 GMT  
		Size: 48.5 MB (48517153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:517cdcf8f332b3b3746d82f9ccded4c73fb9e70354492643d28cc9d585730b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2164647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee6f95e4deb2cb1eb15849530c814ceca30bdaf4928beffa2cedb42edaa3686`

```dockerfile
```

-	Layers:
	-	`sha256:68477bffc6c5c6c62bfc0f3fd9a11d02fce037daac0d45218c9058be51b53899`  
		Last Modified: Sat, 16 Nov 2024 03:56:56 GMT  
		Size: 2.2 MB (2154901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a21e04a019d029fc43693834c7bcba556fa3de4e44bb1af88ffe280aa3ccc5a5`  
		Last Modified: Sat, 16 Nov 2024 03:56:55 GMT  
		Size: 9.7 KB (9746 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:cd6ecdfb33ed5c18764a42beaed66469425aa00713c00b4ac3f28a5ef1361665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82149516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c890a7b1a0faf2e3f6163bdb4f0078d7cdab127716e26e6a0c0c8de6d787d77c`
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
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:991986948126e836a79c1084e3bee33549a43b83cabfe16234aef5b4b30d86f9`  
		Last Modified: Wed, 16 Oct 2024 12:48:24 GMT  
		Size: 34.4 MB (34388822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbfea4ee85f4ed051ee83d0a60bc2750faec98bbb98e8111815bc0dc5534214`  
		Last Modified: Sat, 16 Nov 2024 04:01:37 GMT  
		Size: 47.8 MB (47760694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6ff290f216ac1d6aaae80777c68fce095aa187dbc09c61f6492955b854c12b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2167357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583c009e10b2e8e5abd1aa2d70c0bcc60c393774c09bad64dcd8977b2285bd0a`

```dockerfile
```

-	Layers:
	-	`sha256:afbe902440588382e9a00dba9890271ec796e70d279a324276b29cc606f138b5`  
		Last Modified: Sat, 16 Nov 2024 04:01:35 GMT  
		Size: 2.2 MB (2157683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5b7076ef98066d16959735d788c890baf0db9e6b0b5d8906b803250eed7864f`  
		Last Modified: Sat, 16 Nov 2024 04:01:35 GMT  
		Size: 9.7 KB (9674 bytes)  
		MIME: application/vnd.in-toto+json
