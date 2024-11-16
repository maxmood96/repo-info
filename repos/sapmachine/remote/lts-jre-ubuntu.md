## `sapmachine:lts-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:68545541dcc02bf2d936b7ded65eda548fee9cfb9c607f04014a4196693969dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:06697e012477be7607de6c7e38efa19ec81913f57783fc656f3974bf251d8e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89796284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a50fbf31ae643adb76bdaa07fab62cf30037da8c9faaa54ad8a98de91f431b5`
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
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ad209cc3111c2658583a1a1e025ff8e7d576c80d122a338cf2fe84074ebe52`  
		Last Modified: Sat, 16 Nov 2024 02:57:16 GMT  
		Size: 60.0 MB (60044500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fffbebee1df464d0a7a8f0d42106eac80c6a5a71d737f854e2b5514c7e06c0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2397793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124d0d1a119b8f83c088eccb44a885b584c38bfb241704d596a8f4d628c682fe`

```dockerfile
```

-	Layers:
	-	`sha256:e678f5703ad7ff371b2c0db2e545cc6eb95daa7cf78ac6c864efcaabf66dff31`  
		Last Modified: Sat, 16 Nov 2024 02:57:15 GMT  
		Size: 2.4 MB (2387344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aad3fc500217df7703f8a6d1526cfada9ee6b258c3ef039440f4ddebcc27b42`  
		Last Modified: Sat, 16 Nov 2024 02:57:14 GMT  
		Size: 10.4 KB (10449 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a4be52976f4c1dcc736c88835804aa13bbf3d2520b307f57dc002ff54ffe6eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88100209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfe287779cd4e28aad6fbfba1d4a853c12ff142dd15daa9b4e68a667fa8912a`
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
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcdb617b8d6ba000e94f2e44012af31fc533a8b86491a98ba45307da468b3e3`  
		Last Modified: Sat, 16 Nov 2024 03:49:11 GMT  
		Size: 59.2 MB (59207784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5e9640b674bfc435a1b59f380b7b36d1500aba75ce2e699826f045b1336ad3de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fafedd4c14fda54a247848046e72443ef31c226858775153eb4a587ff367c24`

```dockerfile
```

-	Layers:
	-	`sha256:644ec5337372513e6db327c3d9a5813c8fa8f8e41d5ff53f8b17cbc9fd7647f9`  
		Last Modified: Sat, 16 Nov 2024 03:49:09 GMT  
		Size: 2.4 MB (2387871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a7652e55c13ac6682ca3516a7dbe666aa704233e2998effd4f434ec6af21a26`  
		Last Modified: Sat, 16 Nov 2024 03:49:08 GMT  
		Size: 10.6 KB (10613 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4822e4b50830d645440521b5b49f3c1fa016b24e75ae907977e6e96f2e493c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96139953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3977c3567a5bd8e6ec4d2fba90e0ee64b975a56bf9ef0edbee1abe21dbc14611`
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
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:991986948126e836a79c1084e3bee33549a43b83cabfe16234aef5b4b30d86f9`  
		Last Modified: Wed, 16 Oct 2024 12:48:24 GMT  
		Size: 34.4 MB (34388822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc20dacd0ad6b43c911e8c03255013fdfd8d4998943d19f4feeaddc4c45bc4c`  
		Last Modified: Sat, 16 Nov 2024 03:48:48 GMT  
		Size: 61.8 MB (61751131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c75fc584a6b209e53fc883efa6ba4daf68b461b106796c69ab5ebabc375243d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad88e5f4ecb67a613e2bb1ded3f0fffcb09264e273861a8b7818ebf073549492`

```dockerfile
```

-	Layers:
	-	`sha256:cde9b74a3ea7cba1ddbf1045d4f39c92fb2387e99bc8bb68f58d8a831778b454`  
		Last Modified: Sat, 16 Nov 2024 03:48:46 GMT  
		Size: 2.4 MB (2391311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff84763600a3bf1e4a00588368087bd0c44d78abd025a4afb4498e1d0f8410a6`  
		Last Modified: Sat, 16 Nov 2024 03:48:46 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json
