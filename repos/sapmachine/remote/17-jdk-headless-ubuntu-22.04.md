## `sapmachine:17-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:6f24a3ffd5aabcf3a5002cf0995bbe0c453dc510961e8f88eda04f8adf518c55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; amd64

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

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

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

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0c77cc9d84c09ae49bbb80a41574456e1181f759ad7e6a3ba4c4339ea55efb6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.6 MB (224647879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f8edb845a6701f5598ae17753efce0ab3f5411b3b685f53119540940cf1bdd`
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
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
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
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5caa984f45fe434b0e2af23116584083474e5fd452c719511819480d2013c3`  
		Last Modified: Wed, 26 Jun 2024 00:20:06 GMT  
		Size: 197.3 MB (197286097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:734f04bd23e8b1611f833452ec68033ba563ea7f1207a00a80f8bcbc48b74f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe53c0b953f19c5c60998607371dc1d861f01d5c93b912c63bb7faafe548087`

```dockerfile
```

-	Layers:
	-	`sha256:b602fe30234506d74d1cd7626f4dd29069b927628fd4e5a10d461ed1bd5319cc`  
		Last Modified: Wed, 26 Jun 2024 00:19:56 GMT  
		Size: 2.2 MB (2200200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83916579e5414afc4c8cdc71317680b3f865d44c9719809f80876509348614cb`  
		Last Modified: Wed, 26 Jun 2024 00:19:56 GMT  
		Size: 9.0 KB (8998 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:931ea7733ba5fb2f9a79b1a17f57ebb5c3ba37cb5748d10e51dd9508f911192e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (234038585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:191a56260ad487bd037c44e5aa8069b0cef1f470e805a830711f48b4494a2563`
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
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
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
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd77f13beaf21d264b7f3eca912540d7c13ddaaceca9d280e275074621f72667`  
		Last Modified: Wed, 26 Jun 2024 00:55:40 GMT  
		Size: 199.6 MB (199577892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:662f2d608a38b7f92c63a17b37db6a879d995e8c2cd0025be061bc34fb92f3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641968335737a5269f76fa3007cadbc0cf8636885076b67a74065dd82226dfbb`

```dockerfile
```

-	Layers:
	-	`sha256:b0b20b79d24c70dd05f215aefaffc14a3fd4ef104d202a26507fb0fd04515664`  
		Last Modified: Wed, 26 Jun 2024 00:55:35 GMT  
		Size: 2.2 MB (2202490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e30fc526d4349f4863884318ebda5af5b24f7ec6328a379060c1415424a492e`  
		Last Modified: Wed, 26 Jun 2024 00:55:34 GMT  
		Size: 8.7 KB (8735 bytes)  
		MIME: application/vnd.in-toto+json
