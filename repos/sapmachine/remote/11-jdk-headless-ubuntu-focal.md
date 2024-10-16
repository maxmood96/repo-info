## `sapmachine:11-jdk-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:1657a97ae79d1bda8f7e8bf35b2f05f9cd3c17fb6dfdb8653c04c68aa5cea2d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:2a4fc2ef11859b0bd823ed127ee74ca4cc649c504f5ebf1a30ad95e159dc57c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226580420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e1b6ff166197a81ab149895ccc43432406c6d48b79c07ebd4b5b2b84d3b441`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad0ec57edb611060e90c023695e2446e0ad4d41497ebc0ff095d5e66d87085b`  
		Last Modified: Wed, 16 Oct 2024 16:18:43 GMT  
		Size: 199.1 MB (199069360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:65bb847530bf96ea65fdcc1490abab42ee2e4a808c01cd306f36e4d751b9bcd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2152058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd16bf66a6daed6371e789d51ea588fbdc444a59792a513afb74b53a7b1b6426`

```dockerfile
```

-	Layers:
	-	`sha256:16340e00d9c8e56d76fce93e97beafa7a71a921c86067d3bf14b18676bd853f2`  
		Last Modified: Wed, 16 Oct 2024 16:18:40 GMT  
		Size: 2.1 MB (2143341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad6d8af730b94fd3d242eedee632248ba3aadd7afb6c6bf1d700db747f5684cb`  
		Last Modified: Wed, 16 Oct 2024 16:18:40 GMT  
		Size: 8.7 KB (8717 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a3ab0e651e42391cc28d2f550695306fa9bef73827844104918da8dccb02d3a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.6 MB (223557062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ceba3bf4b47487ac6a9038ee7cc70cb02c7c9007b12987e2368a7c25ce65bfa`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc5a766b8fb9712fdd5eeb7438db30b66dce4422c9fe17f273d8fed8c94c0cd`  
		Last Modified: Wed, 16 Oct 2024 04:52:45 GMT  
		Size: 197.6 MB (197583234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:70464e6ef8f82c1a3cc1676159f5cbb6c5ddf1447caefb7dbec059b9aaeb7ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2152411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4bb16b8eb1e629a6a4ecfa1d77ddaf39f9e704a696396f1558bc3c440b89824`

```dockerfile
```

-	Layers:
	-	`sha256:e03c1e1e94d134cfd96fcd9f2b36764fa7f706dc7f88f2aeb07fe1f93f0f731f`  
		Last Modified: Wed, 16 Oct 2024 04:52:41 GMT  
		Size: 2.1 MB (2143596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b07971ea8bdefe5da1f47196036e8b152c4768d89509198936fb9814a8da31c0`  
		Last Modified: Wed, 16 Oct 2024 04:52:40 GMT  
		Size: 8.8 KB (8815 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d1622228bedb19c6a1072018e5d8d75504ab7a03b81f273535ddc0f720909b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217267151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58e5eb3607fc46504935c1d4155ec6e8e708a5ad3db6e3f041d000c6c683d50`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac775ff49569aeadb3e2001a23772776870253281ae91cd179946967d09490d`  
		Last Modified: Wed, 16 Oct 2024 06:17:40 GMT  
		Size: 185.2 MB (185190645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6740dae83e9c14df890cae7107ac884f0ed40c30109f5677a4673cf947577300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2153223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a61f981befa51180ebdd6c377a27449e247529350cea64cba13bdac5b8859b`

```dockerfile
```

-	Layers:
	-	`sha256:cd427b2f23600b4e9e9801396c0f3fa8e1f4948dfd4bf9f18e6dfc0ad1bcb83c`  
		Last Modified: Wed, 16 Oct 2024 06:17:35 GMT  
		Size: 2.1 MB (2144469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9676d7f83db7eedd0a8845d993f996064f41594ceb3c6d558feea61e93e39f32`  
		Last Modified: Wed, 16 Oct 2024 06:17:34 GMT  
		Size: 8.8 KB (8754 bytes)  
		MIME: application/vnd.in-toto+json
