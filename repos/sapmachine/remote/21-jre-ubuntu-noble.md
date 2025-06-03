## `sapmachine:21-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:43055d571f30f75a3fa3cd5d065cac2c57d55245392554ca973e1a72d0aecba1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:0d669a14d4706d66cfde34ec019803ff7e2f1ff7848825f26d19875ae4fb6f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89832117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3360f6800997628887098faff85701d27256bf0c5f64e52038467107d6800426`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Thu, 29 May 2025 06:11:31 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f08b6ac693aed410c68b66f113715bcc2f29b765aac454a39caa1a1d03344fe`  
		Last Modified: Tue, 03 Jun 2025 04:17:34 GMT  
		Size: 60.1 MB (60116780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:98dfb29979b1dca952185785e92ea06269cc1994d6a8589bae93ba7c952638a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ba510be9adde9d49f87c2ad6eb64bfda0f6447ce7190df56a46b700c8f0809`

```dockerfile
```

-	Layers:
	-	`sha256:750770981e66e7de2154157900d00b308556ddfb8fb4244afd13876a8723dfa6`  
		Last Modified: Tue, 03 Jun 2025 04:17:33 GMT  
		Size: 2.4 MB (2412030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4b02a40fb6d42ac9f0b6a35c6c8eec964bf2cb12e60c20044189d435bc0d242`  
		Last Modified: Tue, 03 Jun 2025 04:17:33 GMT  
		Size: 10.4 KB (10450 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ce04a215b34d17306ba620adb5f5954cdf5b912ce7a3cf4a9589853d593582a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88163718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0e19660aae1d54444f89c4c598cb92390853474ba7515267e571366e61b509`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Thu, 29 May 2025 06:11:37 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cfbb6e4cb3a9eb115711f1aad289e4c3e9e9d19d020ea1af234a3628358edd`  
		Last Modified: Tue, 03 Jun 2025 06:01:58 GMT  
		Size: 59.3 MB (59311819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1653e2aea41c44a4d25df5d62514b70e197213e49d6c88d0aa55ea556a13d65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2423172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e632409815ff78669fe4605c36143a464fdda4177e9d0e829b6fdeaa3e63f0c3`

```dockerfile
```

-	Layers:
	-	`sha256:390db35dfd651b9df7ce2c3d84f8fd5e16dc0912c800f7d5464cde3e7353a2d8`  
		Last Modified: Tue, 03 Jun 2025 06:01:56 GMT  
		Size: 2.4 MB (2412558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cef032ecc22319df3b841ef352dff5f20bc13cbfa2cd542ac52d0402bdc14b2f`  
		Last Modified: Tue, 03 Jun 2025 06:01:56 GMT  
		Size: 10.6 KB (10614 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8a59b78bd16b5a07d254914730d6c3270c5bb7fe2deb564564ce4dc261359dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96140207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2327b0a4477c02b883ac50927a0f4978ff91c4eab1044f91bcffed02983d25e7`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Thu, 29 May 2025 06:11:52 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3c15065d83ea63e3fc2b8d5ecd5d143327486e23416fae585c948f40ba22c8`  
		Last Modified: Tue, 03 Jun 2025 06:02:19 GMT  
		Size: 61.8 MB (61814997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c714802adb009c253cf1fb8c2bb84fcef8d747667693619f922ba0dd4c4c67d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2426657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a0f11e632112a7bf2edef95e9c98e88a9f3d919e2559e2b280cf5921c4e5a6`

```dockerfile
```

-	Layers:
	-	`sha256:ce0016c8ad7a4967df1b3366f5f6bf49954b0547c8823bb082ec21e6360d099d`  
		Last Modified: Tue, 03 Jun 2025 06:02:17 GMT  
		Size: 2.4 MB (2416133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed787037decbfc83f08763ddac1a8f5902799db19be9392656d5bc3187afde6c`  
		Last Modified: Tue, 03 Jun 2025 06:02:16 GMT  
		Size: 10.5 KB (10524 bytes)  
		MIME: application/vnd.in-toto+json
