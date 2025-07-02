## `sapmachine:17-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:58a79e3bfdfd2e61d1e6726d59860bf753194f538653a5affcce5be0c3644c59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:9a6991143c4802b74c20d018b776bf1879c800c6a4f41785cebc66429c778fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83358684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61951792c32751619e8d97fcdcd965db6acb7193a642f68e48dcf812430cb2af`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81d56a7e66ad49c6890aff89e7f14d8b78689d798048e26a00968fccf216195`  
		Last Modified: Wed, 02 Jul 2025 03:12:47 GMT  
		Size: 53.8 MB (53822998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b7fdd95095e6c2033f9a5ceb1447e8d72a59bf59a1acb791836bd71f9a3c0193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2552444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ca7bdf2a1da7e3c142d428fdde93d767ab7f24e51063512114a286179ff60f`

```dockerfile
```

-	Layers:
	-	`sha256:609fa4d6f511b384c4b1e97614df477750ba6a6e253fe4f901cae88e6472b636`  
		Last Modified: Wed, 02 Jul 2025 06:06:20 GMT  
		Size: 2.5 MB (2543623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c500d1e2b50835e6998da418391d6b73ab02f7749d7ca3fca9f5c6b88da13609`  
		Last Modified: Wed, 02 Jul 2025 06:06:21 GMT  
		Size: 8.8 KB (8821 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:05695e92e16e5a80caf62d0051fd751ed0b7e4905d36399f58660ef42d0c92bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80578551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4f05424b08cfe61076188e887fb8e5523e649dcafb553c543fd93f92fc72e9`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55778c086181fdeed369fa05b00d4a0aa4934a70c0623d0eefb25a94cb11218`  
		Last Modified: Wed, 02 Jul 2025 06:49:44 GMT  
		Size: 53.2 MB (53219279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:51df23128a8861f49c285ffd5a9fbf653a280516b4431f0ce36e105c9bdf146e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2552230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5790e1c24508f405c6a2b1ac3a12397c2f0f9103a7311af8901981d07098232`

```dockerfile
```

-	Layers:
	-	`sha256:527540dd38e40e18ae4c04ca4c28b7f2632a6cfb03cf0e7707d524207c4a218a`  
		Last Modified: Wed, 02 Jul 2025 09:05:26 GMT  
		Size: 2.5 MB (2543305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e16ea0526082c91850ed518ed31df3e93cc4ae2900be87a103671828b2e48b13`  
		Last Modified: Wed, 02 Jul 2025 09:05:27 GMT  
		Size: 8.9 KB (8925 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:19b9cf694498093504e9bb8f88ca3b58a4810eaf3920ace57cb9261b816c5705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89772144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f67e850a34946bb48c94152e53e25413628d0f3e38ca75e70b331b8d01b6f4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6edc29ef71aa2ddcbb05c248cba0dc88d353c8689e469f5a6938af2fc890353`  
		Last Modified: Wed, 02 Jul 2025 05:06:20 GMT  
		Size: 55.3 MB (55329523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:29dfa0b27d596b3bfd3726ade3839c437d8651fb9b9006cd185fedb5857b8acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2556619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ef0397012f980aba7a80cafbd0e6a6b714cb2ad89e2091ebfa3d3b1ccc73bd`

```dockerfile
```

-	Layers:
	-	`sha256:c0e7de243e4ef5a3caaf6533d62e215ed8fba7bc0b689f51fdd5bd45274ef88f`  
		Last Modified: Wed, 02 Jul 2025 06:06:30 GMT  
		Size: 2.5 MB (2547754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cb64fbb4751937ef25881bc92f2456377b4e79453d9a323585cc4f4c4ff6a20`  
		Last Modified: Wed, 02 Jul 2025 06:06:31 GMT  
		Size: 8.9 KB (8865 bytes)  
		MIME: application/vnd.in-toto+json
