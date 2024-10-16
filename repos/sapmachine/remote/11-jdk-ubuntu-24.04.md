## `sapmachine:11-jdk-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:b6010bb5f900f00544710aa9889e6f3890c2f5826f9d54b733734cbdcd333505
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:c9aa5296d1bcd0aa86fb9cecf75f5fa1f7e70f0a138c4d13c37b30dc1e1cd3fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230871258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d477b28e415507fc5f84363159e0df1ad2bc34bf5e56619381253d8aac604ac0`
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
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
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
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42d944e6f6dea49f0f8d663009b615187e23a81ad7a50e2dcbb48afd4e2ea5b`  
		Last Modified: Wed, 16 Oct 2024 16:18:38 GMT  
		Size: 201.1 MB (201120895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:499bd25434d0b971f6316af01b464fc7f189e559407a29c7e2fa2cbefdbde8fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2477485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0d6117defb006314c28c373c2ba568aeafbcfa8dff28e23bac1c1040ab9639`

```dockerfile
```

-	Layers:
	-	`sha256:5259fd3731b811aba8c7d54f9dc4bbf72aa86bbdaf9a7c2a0ad4b24dba1ae09c`  
		Last Modified: Wed, 16 Oct 2024 16:18:35 GMT  
		Size: 2.5 MB (2466307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a03e0500c0d7e5fb1cf750782e5c8c6df7fb14a86d99ef92de46be9f6d0afacb`  
		Last Modified: Wed, 16 Oct 2024 16:18:35 GMT  
		Size: 11.2 KB (11178 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-ubuntu-24.04` - linux; arm64 variant v8

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

### `sapmachine:11-jdk-ubuntu-24.04` - unknown; unknown

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

### `sapmachine:11-jdk-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e20cc4b0b59aba3740ee0cab5c670ecb8ee2ac8073bd9271c2490ca4e61d2e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.3 MB (222282629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5d3952cb11766838ecd0f74e081bf5c1b1b0370ba06357e1dee8dd6c2cdf9a`
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
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
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
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2311b9c7ed18ae94577e7cb3b57ef542993fdce5c4f27b0812049354f5c1d3a`  
		Last Modified: Wed, 16 Oct 2024 07:06:24 GMT  
		Size: 187.9 MB (187893660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:aed687761c640c3944572d49372355be5e2e6247f128f4e1bbe0a8a0f01354a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2478982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bd38b91827d40ac9f3003b4099aa9a84b2f5aaac72c8b819b704b4d79c4ec8`

```dockerfile
```

-	Layers:
	-	`sha256:13357fdf0b707dbf0440dbcf231e5ebce9edf719e33d48906b7b5353f35143be`  
		Last Modified: Wed, 16 Oct 2024 07:06:20 GMT  
		Size: 2.5 MB (2467718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b2fa816b659e4d1cc12843ad1997df636cc7d84752262f4b6d193cf20fcc2c6`  
		Last Modified: Wed, 16 Oct 2024 07:06:19 GMT  
		Size: 11.3 KB (11264 bytes)  
		MIME: application/vnd.in-toto+json
