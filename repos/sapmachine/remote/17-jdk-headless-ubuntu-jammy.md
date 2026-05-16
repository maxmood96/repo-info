## `sapmachine:17-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:f0d71e65d6223f1b4f0132a9064c3d322720b25650c5d14c7e39d21e7be512b3
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
$ docker pull sapmachine@sha256:ca62871dded3843a3dae24fe3ac5e1fcaacb36ddd96eb2f3489ae0fa44169473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230149469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3dcfe32ceaab22464ba529a091d5a179e9f5d5b1ea26d86a65186a8c777a209`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:22:14 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.19 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:22:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 15 May 2026 21:22:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a0ef24daef951dfea1749d325ce6b6d1d0dd227d45383d3f64552beff8ec54`  
		Last Modified: Fri, 15 May 2026 21:22:35 GMT  
		Size: 200.4 MB (200412785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:37956d30d8fe2d582db910c0ad83afec3d021e2d77de815099739d32f66d3e26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15682054ee43a7146bee6a8fac654c619e95dd482a9b4f9cedf371f2bf0bdba3`

```dockerfile
```

-	Layers:
	-	`sha256:01d0e2c83908bf1607fd6c0a7d569899763ca75001a163d16637c2666efce135`  
		Last Modified: Fri, 15 May 2026 21:22:30 GMT  
		Size: 2.4 MB (2379052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da98ef80056b5a4e8784c256d3c0cd38b6e50ecd721c7c5ab9fcd6be7064fb9e`  
		Last Modified: Fri, 15 May 2026 21:22:30 GMT  
		Size: 8.9 KB (8890 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:235b2f1782012031e04b21ef7e0cbad658d89878a73219c4d187637bb250af21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226721366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88485b6e299ca690465c1b090b9ee87d153e550b358939963a90d026e7d34f5a`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:22:21 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.19 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:22:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 15 May 2026 21:22:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11dff86e5575676bf27c19e43e463ab02aa73dc4f2eb02acd8cfe2cac50620b`  
		Last Modified: Fri, 15 May 2026 21:22:43 GMT  
		Size: 199.1 MB (199114743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:31b0e516807e4015d1fa5cec10af712364c0bcdbdc942926384146e1d4fa5632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28263b83b0ad44c9031bbae82f2c83f150676fbbe39f4d321f32624e0a0b2585`

```dockerfile
```

-	Layers:
	-	`sha256:9ee75bc01352fd8aea379d0500465e9a12d6a472452e2089fdc820475aea0d33`  
		Last Modified: Fri, 15 May 2026 21:22:39 GMT  
		Size: 2.4 MB (2378724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef6c3d4c057e133f6c24e46d13acf7bf37163a7a4cf1d00ea9d9eee7c845232a`  
		Last Modified: Fri, 15 May 2026 21:22:39 GMT  
		Size: 9.0 KB (8994 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7d77ec6ae0cc7db5eaeb5acb9e52c61198e9c83a8e9cb2e9b4e26461f2e7615f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235705403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f51eae476ff8b74629a949ab2e007ec0c78753aad33d7f31e2f29aa894a666`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 09 May 2026 04:51:05 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:11 GMT
ADD file:bd6823713e9d7c2f4ea7ca1d6d549e2bed56e8ce1fc6f98e14f6eb3a3371ebfa in / 
# Sat, 09 May 2026 04:51:12 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:43:21 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.19 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:43:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 15 May 2026 21:43:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6970bf2b5ef1698cb51975b1a652f6511f8fd9f88ae7b247e3ee32591d975e63`  
		Last Modified: Sat, 09 May 2026 05:25:11 GMT  
		Size: 34.6 MB (34646720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6b972f04cd60563868530ddf1141d5a64a0b7d8e3156c2b8aa3bfb35bba21f`  
		Last Modified: Fri, 15 May 2026 21:44:06 GMT  
		Size: 201.1 MB (201058683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:221408d8d9869cb80c7e770c55a7dcb9ffd653fdeb8e7aa07151b4a92c2c8063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e7c77bf45ca09a515388d6d4c38a70a8ad2046a52a749e0834dd310c605aeb`

```dockerfile
```

-	Layers:
	-	`sha256:e51eb3d1824f05570c2899f76b1bd96c1258249a0aad5e942c39de084552d277`  
		Last Modified: Fri, 15 May 2026 21:44:02 GMT  
		Size: 2.4 MB (2376548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dca3743eaa2c7568c9b8c300129ed652c08f130c85277dfc3ad8446bdb3ff19`  
		Last Modified: Fri, 15 May 2026 21:44:01 GMT  
		Size: 8.9 KB (8934 bytes)  
		MIME: application/vnd.in-toto+json
