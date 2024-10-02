## `sapmachine:21-jre-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:dadaff5b59c8dbb67d4600616e5babd27063d9f9bb2414c0aa809c1940acff9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:da50abe0ede9764139542a97c43e1cfffa91047d97f6150b2d0cefc068e26a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85797756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad1b8bc7f9efd94a6bf60a55c5fce70b664d4e25f9f095923ed4647a11da47e`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:fb8ea28a66bf45a370149362e79d57d7b67b04f1be24eed3a547d75ec8f2dda0`  
		Last Modified: Wed, 02 Oct 2024 01:59:50 GMT  
		Size: 58.3 MB (58286704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bbbe0e50f0a487023e2c2b693fba44f237637554b8ef57c759714f5910c0b907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aad9ac8922d672faea50ef633705fd83097bfbc6a6a1eb6f390105fce0c77cc`

```dockerfile
```

-	Layers:
	-	`sha256:ba17f6db4a797227cfffcb449e98b0b2373c6c85aa9ad1394ca3adf616debbae`  
		Last Modified: Wed, 02 Oct 2024 01:59:49 GMT  
		Size: 2.0 MB (2044966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c385f2ff7f73728c0d67374d5202dd018508913ac2da6ae2a2d1bc7f42d5db6c`  
		Last Modified: Wed, 02 Oct 2024 01:59:49 GMT  
		Size: 9.4 KB (9378 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:b29460367919d27312c9bed498befacbe5661c5b92d731c6a6e1f9c9c34121a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83355674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcf2ab06410284e0c1f434f2c3a464f5beb5815ee72ab1f761dfe47aa0f4b54`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:1c19c52659939618dce2ccbce4762bf948ceea0b0510ca585d610bc43e28aad5`  
		Last Modified: Wed, 02 Oct 2024 03:56:20 GMT  
		Size: 57.4 MB (57382082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7e297c842339e6a25e44974e6746b0653794095093e29106844f82c73a0e997a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373d7f25a3c8a43c4d32e946f648ea89baa15a7a639710e580a87426de60318a`

```dockerfile
```

-	Layers:
	-	`sha256:49b48bc6675a3a081121163167db049072023a2a99e2c75e6fc4b2d6ecca1859`  
		Last Modified: Wed, 02 Oct 2024 03:56:18 GMT  
		Size: 2.0 MB (2044617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e64915da0b63c398abdd5fb90b08aa044b33164eccdafc9dd74258c61bdc2f7`  
		Last Modified: Wed, 02 Oct 2024 03:56:18 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4bffa937fdfce5cbca7e31f97a27ac080c070325f6b25d7679d1fa39dd23ad5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91385158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6eb68a354454b8bd2d25d418a1556670c83ce120866b0633de7dba8942664c`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:6b5600fc15a5f4076d341a5f73d083afd2f38d128dee22a761d9714ec9351251`  
		Last Modified: Wed, 02 Oct 2024 03:08:38 GMT  
		Size: 59.3 MB (59308824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d37ddca7899432dd9178c623ff6f8c9b8e14446015c2ea1540882383f8a41b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2058108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2d65892227662817ea1cb494f1c7045ad8746fdd36f7189266c42381373e4e`

```dockerfile
```

-	Layers:
	-	`sha256:7daa15a74742e2eb9ec06d71785706ecff05313066568bb0803ff5b6a6c93e9e`  
		Last Modified: Wed, 02 Oct 2024 03:08:36 GMT  
		Size: 2.0 MB (2048680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7734500397ee03d4e164336e502076d6cd1da4dbf9a06b99c03cd80f4c77b5d`  
		Last Modified: Wed, 02 Oct 2024 03:08:36 GMT  
		Size: 9.4 KB (9428 bytes)  
		MIME: application/vnd.in-toto+json
