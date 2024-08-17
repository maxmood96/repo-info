## `sapmachine:11-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:4d2bde9d6a679c498bf4001fdf262705caf55c797e074f09d513b358a926d80b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:2c2cb6811d00de8992ea435a353f98bd403bcf2a1b80ad922ee71537bb993b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78848267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8600db1c5301bde45d86cbe411d1a41104d49ff187e5e08cc11be4180ba66c9f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f1da786d5b84e980a6637b00e97a0eb74c2f482431d7bfd447a011adbde418`  
		Last Modified: Fri, 19 Jul 2024 18:00:10 GMT  
		Size: 49.1 MB (49143114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a4a0c128188f760413f55667c43cc57e463de73db9c458ca23211b209596c043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb3c58a5d62d97dffa1fc9a70b42e58b5d8597b8ada35c49ba9eb026cd0cc6a`

```dockerfile
```

-	Layers:
	-	`sha256:afb5e2aefbad7d8c9caf0f41f8d32b3c973299f682eb7d515d91d5d09234e5d0`  
		Last Modified: Fri, 19 Jul 2024 18:00:09 GMT  
		Size: 2.1 MB (2136172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69159d1463fc9a1eef9a07148eff086856ec5d6ab5d3be9f1471f88a355ba8a4`  
		Last Modified: Fri, 19 Jul 2024 18:00:09 GMT  
		Size: 9.4 KB (9364 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:4990fef7f73444ae2adc80a1b7c59eb5b7d839e1d45928c6174e1c7400ec5a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77324912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd636724c8caaeb8e1b2418bec26d81f240520084d7c3a2e6f5edd5349ea188`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2040a69b8843c5908910868a5f00703ff83b48c46adf1e3a4f765e3005403b57`  
		Last Modified: Sat, 17 Aug 2024 04:44:21 GMT  
		Size: 48.5 MB (48481226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f72c155d05d54eb6e623799118dea16d461836f3a2b9325d863783da120f1aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2146969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f82d9c2e0ec099bef4b4b795bde5c324ac1be364fcc01d0916d8525c5e21374`

```dockerfile
```

-	Layers:
	-	`sha256:dd57435ca8b9c9d3a0251708c3775606794f464a20ff6cd762606aa0bf26b879`  
		Last Modified: Sat, 17 Aug 2024 04:44:20 GMT  
		Size: 2.1 MB (2137282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8481b7c4822e85d1a929af5408d5928513772c2bef9a699700151c1e60de64c2`  
		Last Modified: Sat, 17 Aug 2024 04:44:20 GMT  
		Size: 9.7 KB (9687 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d0a8270d3cf0350c2f738b761dd53b70dc79f6e04ae6e057fda9e4d865e33b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.2 MB (82234024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a08c548b71f956f230f68a1293a97af2e89a1e39317f7814057cf9f276e421`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f16ff2741334b0be5d9f311961a37c8bd0feb2974974ec52a327bbae3866e29`  
		Last Modified: Thu, 01 Aug 2024 15:42:28 GMT  
		Size: 34.5 MB (34507572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66cf4a9792b48a17ec48b8f92e2cd2eeccd607fa7c628413055fe3eeab4bc37`  
		Last Modified: Sat, 17 Aug 2024 03:31:58 GMT  
		Size: 47.7 MB (47726452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:29b94e7fe5bbf54446966f83113dc18d769d1639fdf799162d566f8133cf97fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2149478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:519ad4a68fc2c9b9d785551d224983728a0bd9b27c8a421ea5a43bb528aed204`

```dockerfile
```

-	Layers:
	-	`sha256:09d3b520418dcb9bc3ae0c7ea220f1ca93c1142d1e8fb6a7ded855aaad0dc9fd`  
		Last Modified: Sat, 17 Aug 2024 03:31:57 GMT  
		Size: 2.1 MB (2140064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eec8b5b7c20b1946b56205f35ab23656c753e85772f235dc35b665d9e272f56c`  
		Last Modified: Sat, 17 Aug 2024 03:31:56 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json
