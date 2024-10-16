## `sapmachine:jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:07fdee8d035062c148380bb51d04f93538c15ed2c98d4bfe833534db68a617cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:760650938763d4cc7da02adff62c26c283f01c293311faf73848dcf0f0631294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 MB (251106030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b83ec92a798c70650025b95a12394fb56930365ef671e6fed56038b47c61d9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d663240e9978d6eb37997cbadeb57c41a5c1910ab0b24faf7996c9a9003119`  
		Last Modified: Wed, 16 Oct 2024 18:58:38 GMT  
		Size: 221.4 MB (221355667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:95e3c7d719a62a055fbe6d21a74fbd0356c5ab279ec1c3070083d5b3b9923aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2232238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3710c877d03da97dfebdcf48347463fefc5a22948b3a14eebf8ced8b8368f1`

```dockerfile
```

-	Layers:
	-	`sha256:23b07c892f8062e426d37a24f8bcba8c0d409f701a91fc5eaf3601ee18d3f6a1`  
		Last Modified: Wed, 16 Oct 2024 18:58:35 GMT  
		Size: 2.2 MB (2221826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cd3a1fc1299d48b48a290c5c50fc4aa8e10f28ed82aed6a7a63c66789df189c`  
		Last Modified: Wed, 16 Oct 2024 18:58:35 GMT  
		Size: 10.4 KB (10412 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:72cad52a04236a400d99859fc6385a9f6ca7bf6201edd705387f53db191ae0fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.2 MB (248208623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66dc5a05c2c3d9dd25eca14dfdde665b04307fa653645d21d142b63fb582d7a2`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8a419dd8bbfcdfe5c894d5c65b469d198d3f368b2c74c87d7df122aeae3038`  
		Last Modified: Wed, 16 Oct 2024 19:00:08 GMT  
		Size: 219.3 MB (219322778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a5aa4bbd6971dd1f2fa3ad643aa213e5d05a72ed16f60c6386b0de2db75c39c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2232283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d887f7e9dbbe21d9fba007ce151d30d4c6f50f56f0c8cfeceeeb6d24d11787b8`

```dockerfile
```

-	Layers:
	-	`sha256:cb59b5ca3b2f1ef7c24fd3aff6fbe4b5e519befdc7f383f8209e0d9fc683ce37`  
		Last Modified: Wed, 16 Oct 2024 19:00:03 GMT  
		Size: 2.2 MB (2221713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28a351e3012ca46ab93d0df7ad3bb011d186ea1b53ff3cc6c4ec0b2c4d63485c`  
		Last Modified: Wed, 16 Oct 2024 19:00:03 GMT  
		Size: 10.6 KB (10570 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d30f5f5db695cb15afaa0fddfde1cd7d8056acddccc47228f0401b72d4482f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256695151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ac10267d7a5d6becfbb37c2926592bf466261663ca9bb023daf6a3d8930007`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:51:17 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:51:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:51:21 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Fri, 11 Oct 2024 03:51:21 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb008524381d65c04865f5de0edfe2a1725308e044dc1fee8a49914187cefbbd`  
		Last Modified: Wed, 16 Oct 2024 19:01:28 GMT  
		Size: 222.3 MB (222306182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c7ed18c46893d1360985d4f05cf7ae3a2b4c4d84a5e845b476cd715c7fb0e88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2233642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde8d2eca0fdb53c5fd6824838f54c6f465fc1e44ed553278f5cb6ec171d9f5b`

```dockerfile
```

-	Layers:
	-	`sha256:b83d9b2c2e6d6db90e1bdcca860e31552667aaa1f51e36181a65fe83e64c4003`  
		Last Modified: Wed, 16 Oct 2024 19:01:22 GMT  
		Size: 2.2 MB (2223162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d01f2c49f5d99452dd2ce017c7e389a17ef5a96484abb46141e30b58f6c2ae7a`  
		Last Modified: Wed, 16 Oct 2024 19:01:22 GMT  
		Size: 10.5 KB (10480 bytes)  
		MIME: application/vnd.in-toto+json
