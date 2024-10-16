## `sapmachine:11-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:29cc6bdef18b810db7f0cc91768229d5f9b16cf4bc7197477a941dca92f3d8fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:fe71df8acf9a806ff5dbe0bad2b852c2cfad497663e2aab2a2251df649081d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230871258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078af2bef7e8c07c9581794d6453901bd94ab5107015221bb8fc76903f5d3d35`
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
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75847505a3d01c7bb95f32dc71edc02a45590422a16c4874252a60cf650c73b1`  
		Last Modified: Sat, 12 Oct 2024 00:01:37 GMT  
		Size: 201.1 MB (201120801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1d90d14ef93945406b10fd9c625127f76975ce26d6d5b1cfa64b3cece2d2b80d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2477485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f32326bdce5cba8a5e4b2455d910b9db02d04611c85e53c40e67a631eb4fb6`

```dockerfile
```

-	Layers:
	-	`sha256:94eb0485380961bd89ed830ade1b3f0e8bd60c249ef2620cffb933b8a4ad51bc`  
		Last Modified: Sat, 12 Oct 2024 00:01:32 GMT  
		Size: 2.5 MB (2466307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fe40d3483899b3d79ae2260b46c18964c9e75d5b1a1502fd10130aec95f6ea0`  
		Last Modified: Sat, 12 Oct 2024 00:01:32 GMT  
		Size: 11.2 KB (11178 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9a292dea185c717d9cb027933c3b190abac160e4b5773dd33b27ffd73f47846d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228520007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c75bc94b1fce07ad994b9b0f71335dcf4084558e5797d45a8259ead10c118d0`
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
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4eb8ad8c70732ad23793f4277b7f062b333f7ccc181ecac11b8007d470c2ecf`  
		Last Modified: Wed, 16 Oct 2024 04:47:11 GMT  
		Size: 199.6 MB (199634162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:682040bcf17c538cf05c213032613442031f4f023d200bfc7485de3ecfc2c16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2478870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5013ddba2c32aaf4f9049a3411ccd060f27241d6247fd17209f3fa312a544dc`

```dockerfile
```

-	Layers:
	-	`sha256:8e26bb675835f9389e7ea5b71055f634611573574a4df21e75c8e50ad49b8d89`  
		Last Modified: Wed, 16 Oct 2024 04:47:06 GMT  
		Size: 2.5 MB (2467498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d76687c6c124ad1d60b50325f3752b296e059df237a137e03391312daba76531`  
		Last Modified: Wed, 16 Oct 2024 04:47:06 GMT  
		Size: 11.4 KB (11372 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d492d80f682b1fa9b3837c24974e064355e16eb0392d4662d902a5640d735c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.3 MB (222283220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a785c861606406cdeac3541b634835d71994f5a22486c333bc6d665fd03f09dc`
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
ADD file:6ec0ebf9a019b7c00b0121b97e89fcad881460415f8dcb9bb94b1cc7f5d0a5bc in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e110547234fd795b1c6d90b50b5df43ec509107fdf663124acb5e3861c38ef9`  
		Last Modified: Thu, 10 Oct 2024 09:00:03 GMT  
		Size: 34.4 MB (34389412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0041620149f5480c60b1aea9dad1cc26ff1637ec5a49ca13c1f15d7209cbf1`  
		Last Modified: Sat, 12 Oct 2024 03:41:21 GMT  
		Size: 187.9 MB (187893808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e233fc1889461cb3e52f429e186e6f84dd88e99e5fd4416eeeb8573f39302e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2478982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9249d95d06075ca0f1b10b60783044f532c3f1dbb7c0f89f0a6c207ecb7c99`

```dockerfile
```

-	Layers:
	-	`sha256:d68b4d04721913a6c143c5e7affa88fd2aa4003c97a61b37e8f3e276010b846b`  
		Last Modified: Sat, 12 Oct 2024 03:41:16 GMT  
		Size: 2.5 MB (2467718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cde3f3dcaf619c3de3626b3f3abd9e77883914906be7d497077be4faed8e60da`  
		Last Modified: Sat, 12 Oct 2024 03:41:16 GMT  
		Size: 11.3 KB (11264 bytes)  
		MIME: application/vnd.in-toto+json
