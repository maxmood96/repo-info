## `sapmachine:21-jdk-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:bc4e875b85e8f7a87434499530463e391e1bcf9a1cf1cb4f3b8bf8488227bf78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:c803b3876ad064e5684098b71502393cf0a100099953126ec0f66d4438f294ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242271479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f23aa824ff1e01b91c53abfb642c369e1e53e0097a1f6d4aaa49d9adc9d4930`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e0e9f776f071da53f560e48312aca1d67eaaa76f793326116b5826e63730be`  
		Last Modified: Wed, 02 Oct 2024 02:00:13 GMT  
		Size: 214.8 MB (214760427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d6be580ebb84f2497a56835b98c6cc2e98c3b4552a1d48a0791efcf1adf9f382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbb39cd465c935af86bb301dccb55c4ef3289fa27434eada47c694a06a3e8ea`

```dockerfile
```

-	Layers:
	-	`sha256:fc2360991856bb4502f6d0b1ecd6f5d3c12cef9d0132c197d654d9fb773f086a`  
		Last Modified: Wed, 02 Oct 2024 02:00:11 GMT  
		Size: 2.4 MB (2367834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43a178db2c925cbb6fa42f21aedbdec247ab2ed619f94a6460f70c7ba3836b58`  
		Last Modified: Wed, 02 Oct 2024 02:00:10 GMT  
		Size: 11.2 KB (11196 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ce1a39b23d00f9ec7626e48138a61d53027ef824e85b09e2f9d2c6d3bdbd43cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.8 MB (238812312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fefdf69fcd65fcaffb8cad7d5113b45161551a77b8c75d3a0e85619532ac0e2a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01aba429a214d289802eb8db111742e0a206e4d61112d94be225eb375d8997cd`  
		Last Modified: Wed, 02 Oct 2024 03:53:29 GMT  
		Size: 212.8 MB (212838720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7cea2e7b919e7eec68e2619475a61ea4b6cd18622e0fe9a8b5917805644bef4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2378956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cbf0031b453ed9b1270d041d0d92d4ad92122e63b77131f7946aed33b660fcc`

```dockerfile
```

-	Layers:
	-	`sha256:32c8ea410e1182b86158f4f1065af69e6da4b9ba9555a5b47f80c8ccb19db892`  
		Last Modified: Wed, 02 Oct 2024 03:53:21 GMT  
		Size: 2.4 MB (2367566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:738b99afe35a4a818b25832d690fa3060d85d3c4512390ba9917952942359304`  
		Last Modified: Wed, 02 Oct 2024 03:53:21 GMT  
		Size: 11.4 KB (11390 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8515c3265869e7346112183c46cd0004e1192b0338b638cab4591711b099c5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 MB (247779310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554774e1794baab47e2ed1606023e3768ae1bf0113ef99a70f98b5f5dd52b9ac`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cafd57629abc05d597016161b87b83b544a17d39d1016cfb289a60295fc7d492`  
		Last Modified: Wed, 18 Sep 2024 05:32:58 GMT  
		Size: 32.1 MB (32076334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d0c5f8a9bae161d750acf9e95d30facbaa92ed35f3274a775571a24f1f4fda`  
		Last Modified: Wed, 02 Oct 2024 03:04:08 GMT  
		Size: 215.7 MB (215702976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:120db8c89f7207b89fb01f45f9b9a7b5ae7b3829dfba0eda6a6aabaf3adf919a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ee1ff9dff4fb11040ad0f07da3460aff3d252a70993033f543fd73713ddd25`

```dockerfile
```

-	Layers:
	-	`sha256:b0e64ba9f2b7b82ce771c65ace0e98e4677522251f8a3623768d00de2135fcd9`  
		Last Modified: Wed, 02 Oct 2024 03:04:02 GMT  
		Size: 2.4 MB (2369698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5b0366530cf7420b382049a1eb455d2f8816d11251afb3f35c0eb975ccc4122`  
		Last Modified: Wed, 02 Oct 2024 03:04:02 GMT  
		Size: 11.3 KB (11282 bytes)  
		MIME: application/vnd.in-toto+json
