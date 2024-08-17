## `sapmachine:22-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:068e5569257450f6e4df7002c391cfa9876186850db43b327b9d5e88ff34a842
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-ubuntu-20.04` - linux; amd64

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

### `sapmachine:22-ubuntu-20.04` - unknown; unknown

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

### `sapmachine:22-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:33dd810cc647620bb511135a653037ede46ede31b5b4742be5089c49cef50586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236729681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b4f7b986b8b4c9164506e4072072b2d52c61030538032a2d37ccf0b2e7b7456`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ccd35673ab3662ac880d4ec0f077fa0b4e5364ffc198fb116efe4f11702e00`  
		Last Modified: Sat, 17 Aug 2024 04:12:03 GMT  
		Size: 210.8 MB (210755464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eb4b45028caa11b5fd5e96f48ad040753c26095ebc0923b010434f52d937859a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ef2cd9cbafa3bab52d511dfce0849ea9f016bd66b3fa1034ca1a3e6b047fa7`

```dockerfile
```

-	Layers:
	-	`sha256:75604043331ad19aae8c04beaef14a9a37bba8420716b5c5b43df7f69e761ba6`  
		Last Modified: Sat, 17 Aug 2024 04:11:59 GMT  
		Size: 2.4 MB (2367509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:097d08ebdb85c7bc1dcb7612183d1d5a53fead7c4e513c577994a9bbe2789f27`  
		Last Modified: Sat, 17 Aug 2024 04:11:58 GMT  
		Size: 11.6 KB (11556 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1182ae9b1afbb00f8b420b50e191260dc0a6dee021a13b263e53f3401e548edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245556398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b4370b0369068de178d5ae1cd4bceeef173e12ca7f6ecd9063262f93a0920b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3163518b71f785e08c4dab8350fde4139b51dd71af32b22000f18b173a82d5a8`  
		Last Modified: Sat, 17 Aug 2024 02:39:41 GMT  
		Size: 213.5 MB (213479258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e73d0b6ade52aea3e5046afeedaa4e43c66dc15d7596adc7b834af9399e850bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485e081753b3c76328399812f26bab14e56635c9dd800aebb25952d5b39a0f0f`

```dockerfile
```

-	Layers:
	-	`sha256:66a34abe769e0b5066f8384d007c4d0ff18b8dd5fcbaaccea71fafc416653ec5`  
		Last Modified: Sat, 17 Aug 2024 02:39:36 GMT  
		Size: 2.4 MB (2369653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e529cfbac912e55d24617a61068badfd3a19b8e076998fd9d5bb026b572fd777`  
		Last Modified: Sat, 17 Aug 2024 02:39:35 GMT  
		Size: 11.2 KB (11245 bytes)  
		MIME: application/vnd.in-toto+json
