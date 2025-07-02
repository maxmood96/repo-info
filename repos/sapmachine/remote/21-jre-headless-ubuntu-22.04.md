## `sapmachine:21-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:ca9ad25d5f26028d66b600689b0bdd33c89e16ecd2eb086aee0530fb7202057d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:a2e5b0336460565801230541d1dbdeb487772942191a22d3d8e90be8cd0ebe97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (88048591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b570d112dcdd0210b90572a8a79ca9d276b16b522508214d4c98f2863717b2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef7ae22bbab8ed7fa09aa6bf98c84de16c5ce81ec3a84222611aa4a2462e905`  
		Last Modified: Wed, 02 Jul 2025 09:27:49 GMT  
		Size: 58.5 MB (58512905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8b7408b0c5fb3d22c341de8a438e85705ba9a4f99b9d5fe4b6c59be04a700b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49e35b10548a19210eaf3c1c75b3172a3d4b2e6b3c40d93abc0ef17770e9b1b`

```dockerfile
```

-	Layers:
	-	`sha256:51b051dd5eab30e41deb7e7bdc8ce2292d9f011d41be4e32e6b4e6a37c06d71c`  
		Last Modified: Wed, 02 Jul 2025 06:07:59 GMT  
		Size: 2.3 MB (2294797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94bf444ad8e2c8943d961c9e88fc72cd0aff71665060dcb921eeab3ebf7d2a6b`  
		Last Modified: Wed, 02 Jul 2025 06:08:00 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:50cfc0f12cf10c5ac87c843d85c49a83421e4d3ad90f280c128493fdafac4316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85015585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:879cd3aeda068fbe4d3b0caee5d12d77cb29bfa92763630403b3169af57d63f5`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829bfeb5d5c65f4dbde17a54b70e0c2ba8d391c7ba5d7b7352b3590bc6ff83be`  
		Last Modified: Wed, 02 Jul 2025 06:44:06 GMT  
		Size: 57.7 MB (57656313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e73addbce65ed1a332aa7a48b4900b5a834861f792202a620830074b5e8fde92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6577470cb11dad45d56c291ad6f60120ace874678bdb639414702709f31985`

```dockerfile
```

-	Layers:
	-	`sha256:2a070b6875d83bf56b2e615b96d7b90b1d537f96a1dfc7e3356cff7d5fcebf07`  
		Last Modified: Wed, 02 Jul 2025 09:06:53 GMT  
		Size: 2.3 MB (2294493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57cfdff19707adf0a30de4d2dc894ac98135bd2e81e69ad1595b313c1d363581`  
		Last Modified: Wed, 02 Jul 2025 09:06:53 GMT  
		Size: 9.8 KB (9754 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:41ba376a92e5a3545fba1d6591be7eeab479f1ce2706efaa00ceae64079fbf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94353537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ac3dc79e0d082d58ce4fd7fd1288b24d4e2a113b1a199d39c9242c13117d2d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db06309b0f2974b8e3b7ba4bb536e50542c976d9d9d76ddb1ce95e38f4284ef1`  
		Last Modified: Wed, 02 Jul 2025 04:57:03 GMT  
		Size: 59.9 MB (59910916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9c46d11f0f96fa7bfd892f3e4e039ffd886553504c87411202aedc4eb519e699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dad678d0a2ca67d46ee092ae15c0208d595a7e794613b14749dae41c4525100`

```dockerfile
```

-	Layers:
	-	`sha256:b74367805050a1acac96c057d50166b6e4354f8a73875cca5540565071639906`  
		Last Modified: Wed, 02 Jul 2025 06:08:08 GMT  
		Size: 2.3 MB (2298850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57d4fc719612e4b631dcc20da3a73c429db5e5b1199ffad313e558dba49c1179`  
		Last Modified: Wed, 02 Jul 2025 06:08:09 GMT  
		Size: 9.7 KB (9683 bytes)  
		MIME: application/vnd.in-toto+json
