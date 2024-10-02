## `sapmachine:lts-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:8d1b9d409f8c914acefd261719094a64301629a9e6e892966be0846e32997997
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:a2c3a9a290298ad8b4a2997145f06e9f24ecfc750eb98419f81a98ebc9326546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88893105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae90f62ac2298693cd69a810f70d924682793b58a0b028253476cca787a744b7`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b51ddbd79d2038ce239e91f286373eb93cc51fe4b9e6fa85cd3160b5a0167b`  
		Last Modified: Wed, 02 Oct 2024 01:59:49 GMT  
		Size: 59.1 MB (59143245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f355f5562dec2f142dbf99c5415162ba4b0c4ea06a2827b89b67bafcc7e9d98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2140015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9aa514f41810fcd1299747fcc2a2ab87790606416c4c4a545bf748f3a6ccb3d`

```dockerfile
```

-	Layers:
	-	`sha256:43bc5730953bf0135ae89d8fe81fbce6546858e4064af345beb58b911e964616`  
		Last Modified: Wed, 02 Oct 2024 01:59:48 GMT  
		Size: 2.1 MB (2129614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0a5ae8e2dc0bb3aede06ff567950d2877c79641e25d766243c4846c1a5ed27d`  
		Last Modified: Wed, 02 Oct 2024 01:59:48 GMT  
		Size: 10.4 KB (10401 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3950a62885badf82d898e1f04b651c34346855b727eb786ff710278f8e43013a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87128919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a024102ae34828ebe70e0e91d13b213e864c426179dd6c87c90242e0ab84da8`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968c8b2d99ccc9be44cea0ef7ee509bce5bd75b229d6e553925c63cd169ab6ec`  
		Last Modified: Wed, 02 Oct 2024 03:52:12 GMT  
		Size: 58.2 MB (58243489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6afe3ac526367f767c032d11777f10bfcdacf33392c7b629a58af829eeb9655d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2140692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83938f45feeeda892b887adeec2e4e4a150bc576c9e45f4eac5288774c6aa8b2`

```dockerfile
```

-	Layers:
	-	`sha256:10b579249e54aff7754ce8973adc5517e31080b770c83de9fa7250081c15e5d8`  
		Last Modified: Wed, 02 Oct 2024 03:52:11 GMT  
		Size: 2.1 MB (2130132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:745b80bccd59578a36ace22c8782a206df3938d0c01b1b22844735d109e4c323`  
		Last Modified: Wed, 02 Oct 2024 03:52:10 GMT  
		Size: 10.6 KB (10560 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e891cb53009ef6a08746f0818b00b6c9e3f4579a78dac76a84ee727fc15e6a98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95021337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae55b3b981947b3d7f0c68df93944edfe8451c745bc1d6f548d2549f5068ae1`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:02d903566b998a9262d33a607ddfd51e0fd03d28f420fe11f8a2d4fed1eefb53`  
		Last Modified: Mon, 16 Sep 2024 07:36:44 GMT  
		Size: 34.4 MB (34392021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d5db09b965aa7957d9f067bdb2b1599faedab805a8503720d5fe733ef0fb58`  
		Last Modified: Wed, 02 Oct 2024 03:01:39 GMT  
		Size: 60.6 MB (60629316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2d24d6d2c9fb3ca3a9099838fcdc7fbd1a78e664ba16b46914423e6acaecc476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86750d3a4decd2eb0323d59287d0184efef7262bfce2ebcee976c416f3a53ba7`

```dockerfile
```

-	Layers:
	-	`sha256:3621d53900bc6aa3ba355e36b7502330e52389ee7631c3fe3afb1ca5274f256e`  
		Last Modified: Wed, 02 Oct 2024 03:01:37 GMT  
		Size: 2.1 MB (2133518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ade46a66faf15ca786050116f4124f1ce6cc5930724ad16af11e936ca383225`  
		Last Modified: Wed, 02 Oct 2024 03:01:36 GMT  
		Size: 10.5 KB (10470 bytes)  
		MIME: application/vnd.in-toto+json
