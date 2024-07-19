## `sapmachine:22-jdk-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:41cafa4b813416c07e056001098ec292411ff969252556d3f59f76d4c2a7b881
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jdk-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:fd458fc046a898650d07c265dd77efed4741ad169c8a5fc0c3729fb230180771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240285867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75c30d7538648c4bb1f288a21ee0814b0c03a23c5c73e386a874db7b36dfb23`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dd43881ef17d31b4a2e07937fdd914975edddf3a0aba044740e09445b25905`  
		Last Modified: Fri, 19 Jul 2024 17:59:38 GMT  
		Size: 212.8 MB (212774098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e15fd1545c58b632390342fa658714cd053911cb5998e108385374c77b88cd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba628c59e0142f70c40681021b2965dd7abe714a0b3f78ae619e8d357cd8dea`

```dockerfile
```

-	Layers:
	-	`sha256:559b56df0086ebb2da77702b44c2c8d52b15da4013460010c3f6e68d8e718c44`  
		Last Modified: Fri, 19 Jul 2024 17:59:33 GMT  
		Size: 2.4 MB (2368408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f4c167e09f29076e67fef7421dd7706a8e5e315f6b1d94c2f7bc76f36589374`  
		Last Modified: Fri, 19 Jul 2024 17:59:33 GMT  
		Size: 11.2 KB (11158 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8e811404a6cdbeec47d97d48be4c06e6bc017adf9636dcd16f516af5c44ceee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236897491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927663a7f25f1373af10d71e42c84d463d30edf44c5d251d6b822355290dda2d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d4d5b088bd314225bd4f4ce0df3ac3c1c3fb4cdd8aad51fe82e960dfa8736d`  
		Last Modified: Tue, 25 Jun 2024 23:58:48 GMT  
		Size: 210.9 MB (210923274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d1460962264d1ae618e2249af97f5b3f010c812e80087e38b53177b49f4b4025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2351861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3acce6ff9cb6538e95643a0c8e13ce11facdafe36264f6a273116c72b1cbb4b7`

```dockerfile
```

-	Layers:
	-	`sha256:b16b4f84a4b26822504effe8f9601ee8701fccae5cb65ed5aa243c3e95e98cfe`  
		Last Modified: Tue, 25 Jun 2024 23:58:43 GMT  
		Size: 2.3 MB (2340287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0896c66d529655e7f38e014a4ca665f7a7c80c93841a0e733dcb10b546a1ce2`  
		Last Modified: Tue, 25 Jun 2024 23:58:42 GMT  
		Size: 11.6 KB (11574 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7c13afc38a5c5450f51115a2f82b65a072a35a24e89b6766e62c6fb760961bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.7 MB (245715678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e055c5e7f430a4cabe23b2b0811e0ed5822212512dee45ca393c6356716335be`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bf6d4a9d4ff6f2c90b3b65d2e2f59890fb90a09f2119cf29c18e08d6469450`  
		Last Modified: Wed, 26 Jun 2024 00:20:07 GMT  
		Size: 213.6 MB (213638538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cb4a7da81e409417e78bf0ecce85d9cd28bbdf5cd0260a5e8b378e3aae788108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2353694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f5a34b7e4b7a2277f2adc465f82ee8331167a6ff45c0b475bca8daca4b26fb`

```dockerfile
```

-	Layers:
	-	`sha256:8ca209e38880db9a411cda4de12055852f379e5cd9d0cfd5cf340ccbcdfff7fb`  
		Last Modified: Wed, 26 Jun 2024 00:20:02 GMT  
		Size: 2.3 MB (2342431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4c7f6c8cfe08d8bde6ba2156f944e7187fb81fb50b491540c11a4cc57e673f2`  
		Last Modified: Wed, 26 Jun 2024 00:20:01 GMT  
		Size: 11.3 KB (11263 bytes)  
		MIME: application/vnd.in-toto+json
