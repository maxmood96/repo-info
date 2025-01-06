## `sapmachine:lts-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:6c7ffdf1c0a4bb8808ff978048f95f87342867ffba69ca4811f0e7b4c6eb24d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:8e6da10680cc3116af0171aa8a6a88efc2fcea9c0f38e5e9dbf87c7d4bb278f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244107165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e370b9fff377324ab5307b0f89c2809229516976408255439b93eac85a961ce2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b26318a4cddb1494f040e60726fc397169b601e651e29ee1e5148e1b911b5b2`  
		Last Modified: Wed, 16 Oct 2024 18:58:57 GMT  
		Size: 214.6 MB (214571477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9affb08a77c5d86bc07233f34f0291866eaebd0b79f587a1f9b9df87d4944cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2492287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70e28f992352ed5c55b83f978342b67cfd622813cdfef7a3020f3703981a614`

```dockerfile
```

-	Layers:
	-	`sha256:89e59607e33a7682e29a3fe4697c792f2e9786eb5601c4eecb7f5c8d58b27ee4`  
		Last Modified: Wed, 16 Oct 2024 18:58:54 GMT  
		Size: 2.5 MB (2481058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9429aba27737beeb66a3aaeb92613003112d7cb4cd56b3fa198434e38f0ec204`  
		Size: 11.2 KB (11229 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:4ca86689193a31e77c16a7ad81b5cf4917584b5c1da7f2b2127690178e1aa604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240069572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feafc71906d0105a964f1ae8f765e160acc88417645d4ec426ca8eae07b22daf`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60124f91ec39d0275f9f7c82e3f9d17885c37c14e42e44d4450f787a774ec30c`  
		Last Modified: Wed, 16 Oct 2024 19:17:51 GMT  
		Size: 212.7 MB (212711243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c0e32a8f74fcb4ee95d0216daf693d421c232fa48c16044ab399cb1d97fef763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2492257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6588fe49200645c904440f78c4a5474cc50c1e8877016648b1bb4a6c3402f98a`

```dockerfile
```

-	Layers:
	-	`sha256:7ad6896fefcc66adf17f7c4269d5ccd6fa6ef946f0ddd6b97a5c7b51fc4aa951`  
		Last Modified: Wed, 16 Oct 2024 19:17:46 GMT  
		Size: 2.5 MB (2480834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da976f7a0e28bdf539b7f87bc9f31939bedbea8907a7ee2c649df76c71392fb4`  
		Size: 11.4 KB (11423 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:17d8b39130e14618137dc2b4571c522279e0c91c9d1e5755e10d3468a6e77813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250325916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6852b3a7127e39c59125f77a9a2eeb6e093d3c96f429f2706416097d8c062026`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406bc5f97c0e4e0e3fa5828f308a50d86e5718107e1f8942e26a8069f4032aef`  
		Last Modified: Wed, 16 Oct 2024 19:32:52 GMT  
		Size: 215.9 MB (215877674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3f94c0efb76ee0547ebc867b7ccd1b4ebafefef60cbbaba580e56e66216726af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54537fd0135abb9a9362afbc6035ac1710208b3a0641ebce8323ae5de8a6dccc`

```dockerfile
```

-	Layers:
	-	`sha256:2cfc316f8e0cac34bdc1752eedc66cacfa94c12dbde999b68515c76590628668`  
		Last Modified: Wed, 16 Oct 2024 19:32:47 GMT  
		Size: 2.5 MB (2483136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b92ec81446c43c6d4ab4395ac02aa08ff651ecbbfd85c959cdda436a0485b073`  
		Last Modified: Wed, 16 Oct 2024 19:32:47 GMT  
		Size: 11.3 KB (11315 bytes)  
		MIME: application/vnd.in-toto+json
