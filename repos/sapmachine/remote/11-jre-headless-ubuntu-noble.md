## `sapmachine:11-jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:648344819e25b99118834f132eb671cc944254b27379e52d304d6d0803203b11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:7f9bf99b71dccd7591a891e36db1ba24ca583525634daba35be54e0d41883b49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78951094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbb59d488cd214201fcade9e44944817c66ad1468dc828dbe32e4ce62b381b2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:54 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:57 GMT
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
# Wed, 16 Oct 2024 09:25:57 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12030ae4e61f5613b4b95eb0cf2cdfdd5af3f398093e7a333b327b8ab5541395`  
		Last Modified: Sat, 16 Nov 2024 02:57:07 GMT  
		Size: 49.2 MB (49199310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9a82a01858dcf97bd622ebedc67ede7a3e1041befefc3f2dcd41101b36ba956f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2163409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6010f6f6e1776ac42337c33350294e3f15fdbfa2e2fa392ce2188612bc6a159`

```dockerfile
```

-	Layers:
	-	`sha256:a09d5662622f396b4fb35b7671187564e1c42d0183d135a978d0252253ce4e9b`  
		Last Modified: Sat, 16 Nov 2024 02:57:06 GMT  
		Size: 2.2 MB (2153791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac4d66bf4ffd9df3e5b2024167da7a79312252768a30d051a5050f3fdb589a89`  
		Last Modified: Sat, 16 Nov 2024 02:57:06 GMT  
		Size: 9.6 KB (9618 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-noble` - linux; arm64 variant v8

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

### `sapmachine:11-jre-headless-ubuntu-noble` - unknown; unknown

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

### `sapmachine:11-jre-headless-ubuntu-noble` - linux; ppc64le

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

### `sapmachine:11-jre-headless-ubuntu-noble` - unknown; unknown

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
