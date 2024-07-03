## `sapmachine:17-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:ca48bddc7c472a1c1179cd05a39375effd1f1e6057217d84729198132464f53a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:315a6367775b57ee8391cb200e5284adcde38b1e4003498644cb149ea628ee8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228230824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67d611ae8793bb90b44c283d7a8e3513df5aa9b83b2e965f9cd33a3d2b199703`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350232e0323d78bf4a0e69e166179c8a2b4f1b5f3578b6a83323a30fc96d3430`  
		Last Modified: Tue, 02 Jul 2024 03:32:14 GMT  
		Size: 198.7 MB (198696769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9ac9291d8c79c05ba54aa2647477e148a1c3684e8006915ec7d3c4d43a618d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbbf7dd6c4562fde3d5955e70e8406b2c882c86c4212932cb64b4e69b13a762e`

```dockerfile
```

-	Layers:
	-	`sha256:8c37d260856497e33cc8f6d49ed174736555067d961e77101bf0c88f0ab98e0b`  
		Last Modified: Tue, 02 Jul 2024 03:32:11 GMT  
		Size: 2.2 MB (2200530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ed5a531e5c52a5d7414effbaa35c5592111210acc09223e6c6ca025b9d22bf6`  
		Last Modified: Tue, 02 Jul 2024 03:32:11 GMT  
		Size: 8.7 KB (8697 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8a0255b5e5b61bc7c0b0ff9f7082a5295360c9d9400913af40ea5c8de3456057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.6 MB (224644587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e5c7bd6394a727864c5b44e8fe36a77bd1aefd9388bf82c6399dec5faa13294`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c8da520d6ede9ce171329dd8fa2c0ff77faecdfe7b45c3d06e2655307708a9`  
		Last Modified: Wed, 03 Jul 2024 00:03:40 GMT  
		Size: 197.3 MB (197284562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4e9cfcd00ccfebd19b48057032c54b75ab95a774385a175e3653e47752a07fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a322953c12840373a5d0b127a0b6613f91acad758dc990fce41461b47170db87`

```dockerfile
```

-	Layers:
	-	`sha256:3a1f637658ea1ce04bca5f5cc4abcae1d10e3059b44db23bdfb0d9e1741c0708`  
		Last Modified: Wed, 03 Jul 2024 00:03:36 GMT  
		Size: 2.2 MB (2200200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:686cc7d481402a7c14a663b48ce19720c228f8c1c5887a93be6ae312fe461ef2`  
		Last Modified: Wed, 03 Jul 2024 00:03:36 GMT  
		Size: 9.0 KB (8998 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0e4713cd9d8d89fa4e4a20b68e05c6b0bffbdd99e20ba9da55632bc2d7dd0d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (234039202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b8dc357acca1fc5ddb9c0b4e1227fd64a4fc93c066706ddc09271b27a9aee0`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b4181d4a55aff777ff36f62815dc42bc86eca246a5a8d091af70ae6f12887d`  
		Last Modified: Tue, 02 Jul 2024 21:33:14 GMT  
		Size: 199.6 MB (199578121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:199c0829a0b921f01d34924e05314bed7da7785df4c104b2121898b43d3b568e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e5375724b243ddcbf1a1ffb0bda5d2af1e1aa16f340da6684767c37c009b4f`

```dockerfile
```

-	Layers:
	-	`sha256:1e7c097c1be71d98d1d59bf46f5788ef14bbff960168347a7c095982328d0253`  
		Last Modified: Tue, 02 Jul 2024 21:33:09 GMT  
		Size: 2.2 MB (2202490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2de4f6ff7a1dc71b91b66b26b3263bbb4e3a818ecc3053e7322f3bbdc6e6d0f`  
		Last Modified: Tue, 02 Jul 2024 21:33:08 GMT  
		Size: 8.7 KB (8735 bytes)  
		MIME: application/vnd.in-toto+json
