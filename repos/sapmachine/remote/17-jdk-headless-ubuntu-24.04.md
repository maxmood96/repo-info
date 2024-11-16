## `sapmachine:17-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:eb24b0a99431626bdd9861a2c5af6d50004b3158a809bfa812966f8f6061d624
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:011b733ae6e406ea762876753671fdc016ffaab8b978cef54216c199eedbb937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228767439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94af195ab856769fdd17f908f4b38a02e07b71227d40157c8cb3537e774f5b3d`
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
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955156bc6fa8f5bc6c8cbb60e4a8fcfa5a3ac497b06649b5b3014474507e7b0a`  
		Last Modified: Sat, 16 Nov 2024 02:57:25 GMT  
		Size: 199.0 MB (199015655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:59cd282f408a9bcb176313b5c2abf53a6167ace6916ead1b2889dbb148e1d889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2240394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fd4ab1538cbbf583f97379438cf62c538b8c0a845776999777788fe5a63c1c`

```dockerfile
```

-	Layers:
	-	`sha256:02d2c565ab0b4689967ea720054baaac22876dc52b308527dc20acdca9ecb3d8`  
		Last Modified: Sat, 16 Nov 2024 02:57:19 GMT  
		Size: 2.2 MB (2230776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d7f996ca0955d3184542a101b6e92e6579c09740cd40084c7eb03e9277e748a`  
		Last Modified: Sat, 16 Nov 2024 02:57:19 GMT  
		Size: 9.6 KB (9618 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d4906d61296d2e04bcfaf0f4b419afe8831e593cef958519631583950b56389e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226623630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f49734cb2aecfcfeb2a69a2acc8fb25c8b1b4d501da433fefd43f463df1deea`
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
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1354e0baefba444abe0a2b7f52018c57857bf812f121ebf39a555a0f84c30088`  
		Last Modified: Sat, 16 Nov 2024 03:52:05 GMT  
		Size: 197.7 MB (197731205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:26db2cddffadb2199580f2d66549eb1153985f1786689779908fc44dacb10a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2241005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9420c7e9d1bc131b6fec6197fc485f92d4aa72ec491ff1bb0bdfa19e63a503ca`

```dockerfile
```

-	Layers:
	-	`sha256:5f19184097a4a97466cfddafb0b7122ee56431a649f0f4737f39a8cb946cd846`  
		Last Modified: Sat, 16 Nov 2024 03:52:01 GMT  
		Size: 2.2 MB (2231258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5537815de57baa669e32c7c9119079f62f5335aab76e4702d26d4a0350518c77`  
		Last Modified: Sat, 16 Nov 2024 03:52:01 GMT  
		Size: 9.7 KB (9747 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a7d9bee8cc1f5a29bbf8a25071e0993d9f9a402dcc26efd9127616d27f7a7d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.4 MB (234423820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c9e7f3333b7901fb439734d0763a7383cd68c7fc19465c7bc8d666a415f8dc`
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
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:991986948126e836a79c1084e3bee33549a43b83cabfe16234aef5b4b30d86f9`  
		Last Modified: Wed, 16 Oct 2024 12:48:24 GMT  
		Size: 34.4 MB (34388822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557d4e29ce8b053a425964873124ea9449e01c345e2aef3193db62e364a10974`  
		Last Modified: Sat, 16 Nov 2024 03:53:24 GMT  
		Size: 200.0 MB (200034998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3dad9f051317ac1f9aecd42db02ba941bf0291b6d24c3d1ed006926fe5a81ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2242388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f511d0317dcd03d8f826f7508c41f8f45d0fd83ce38548a6c18d4f0af2c480e9`

```dockerfile
```

-	Layers:
	-	`sha256:78c0bdbb23537db8bf24435be8466b28d41405c1b19e514c07a9ece84351c0a3`  
		Last Modified: Sat, 16 Nov 2024 03:53:20 GMT  
		Size: 2.2 MB (2232713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8739f0e3cf633a1d804d7813dd9256eab5e6d040ae3eb627f93ba0db20da285e`  
		Last Modified: Sat, 16 Nov 2024 03:53:19 GMT  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.in-toto+json
