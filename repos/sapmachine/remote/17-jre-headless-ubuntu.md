## `sapmachine:17-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:1ab830df135983c4d2b241b6c2a5688682783a04e0a167a46b5c22206c09d57c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:4b3d1190472cd18e4ce185eb318eca9404d806dbe9b9d2575ed94bddd68c3f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82608936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e3b6a34c0e59a4a20a9c58f15b3317c21a42a306138cb4704ce6152f0ac265`
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
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ec5443365884feef2e12ffdb8b72df371aebadd206cdf1ee2cef7b84591a40`  
		Last Modified: Fri, 19 Jul 2024 18:00:07 GMT  
		Size: 52.9 MB (52903783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:609c43d2370d18ae65d3066cd656463ce4113ac601ee3f7a0677c640c3f5b0b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b62332643458b9bdbf1ce1a517dad9b874290766695ccc8bad0b2b0d4c69a2b`

```dockerfile
```

-	Layers:
	-	`sha256:7530b3acaa8e67eeee22ed234b60b293ff400733d334d83267b321abfb84aaa1`  
		Last Modified: Fri, 19 Jul 2024 18:00:06 GMT  
		Size: 2.1 MB (2124106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:602fe895e275ef0d60ba85e0ca3da1d8a83fbc45211746b2783e86bc61132f4e`  
		Last Modified: Fri, 19 Jul 2024 18:00:06 GMT  
		Size: 9.4 KB (9364 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:4aa24be0f1dc4f1ef26d2280565d929964c3a3bc14b835921081470b18989bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81131237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e1f3e0dcefefecfc569fbdda77ec385e9390cbe7ca14fb7ea7ee4760d35975`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0dab6aeaf34190f16ef7be4d8c522fb0e098c79f902893a791a5faf6f00b81`  
		Last Modified: Sat, 20 Jul 2024 00:23:57 GMT  
		Size: 52.3 MB (52288194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bbd5d71880300fa51c096bb83d98210423288492f85c28223b3581d9934df3f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83e3f53d39e691fd27f391dbbd6db7ba12d87a117eb41ab4106ff9a490f69b0`

```dockerfile
```

-	Layers:
	-	`sha256:577e26124ce33317db8ab9fe07c39045304c535da0bb85a13d11195e2d4854be`  
		Last Modified: Sat, 20 Jul 2024 00:23:55 GMT  
		Size: 2.1 MB (2124588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70bb2605ea60a8a29d0bc91e9ce6194f1972c6b688c67514ad3540e01996e6c2`  
		Last Modified: Sat, 20 Jul 2024 00:23:55 GMT  
		Size: 9.7 KB (9689 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:046a10f4668dc87ae628fa09cbe65b11ede35f89dc0f1c4995e9e5bb6528485b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88837976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41be9d9319005db054dbd640555474ff669d0815364b580dc66e28b1d09d4101`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:24 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:28 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Fri, 07 Jun 2024 12:00:29 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c07f616c3272ca1b9d91b7ca3f8ca8878bec97b33f5c0ed0171e37444484c93`  
		Last Modified: Fri, 19 Jul 2024 23:35:34 GMT  
		Size: 54.3 MB (54331947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:308a6374e05a5f46f12290ad0b9903a851c387c54080bb98f5b914b33364c251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417e2895db089457bc169e9b64a5c906e68c6011529517cc9da4cfd085a6c725`

```dockerfile
```

-	Layers:
	-	`sha256:2a1539e90fc5c1ffde28765b070f3da98294312476edae606ecc39a71cbf2115`  
		Last Modified: Fri, 19 Jul 2024 23:35:33 GMT  
		Size: 2.1 MB (2127992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:904d00910668cb37e5ba7475a08d4c30197304d96bc8e80d846367edb492a8be`  
		Last Modified: Fri, 19 Jul 2024 23:35:32 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json
