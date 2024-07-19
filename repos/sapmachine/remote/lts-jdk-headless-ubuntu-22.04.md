## `sapmachine:lts-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:f04a1bcef9286aab39e914bc01f3599dd922df5bddadb4aa306e0baf7815caa1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:e20116aebb9b2a5b8442559ac7a934a0d216a04b1d214cf5ea81280c71cf1622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243531787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b3806dbff49735255bb39b0bf8aaf9a1858e27ef61c2beac92e273c6af975c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6792a2843e0aa78921d599854fbe2343959fcbeb6e4aff9be58cb5aea0e907`  
		Last Modified: Fri, 19 Jul 2024 18:00:28 GMT  
		Size: 214.0 MB (213997732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e15c3643219f403ba0a9d1796abdc3e378498647cae897f129b3251783d1ddc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2240542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a430c4ec4f67ef07f1f9c6c69061cec7dec94c2b1e68eb757acad74fd725a8c`

```dockerfile
```

-	Layers:
	-	`sha256:5ff32ed3040f096e10914a46e19a5db25297f39cdf1cbee536d5b043d75f49c1`  
		Last Modified: Fri, 19 Jul 2024 18:00:26 GMT  
		Size: 2.2 MB (2231168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1939968e734c0206b39b20c210e22563d8a356fe5f759bd294e7c3db6a83a7d`  
		Last Modified: Fri, 19 Jul 2024 18:00:26 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f912637e8c071dcda4f36ca8218230581703fbbd3b6f482853257794a50edb40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.3 MB (239264941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2cc329a2cf84003d9e512afadf85aa7244803148c565e0591d9ce9ab4bf4bd9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a05571d00e68d9f76afeecc5d7fbf31800c6b7e8652e36767bbbe5081531a87`  
		Last Modified: Wed, 03 Jul 2024 00:00:00 GMT  
		Size: 211.9 MB (211904916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f04ece5ee42800b169c9a07dfc961c7b3177142039dd2980240cc7517a7ef71f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2213786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796ce6536f8c1b6153cb36a6da6eb72f0ec42159d85314d8a841fadd51edaabd`

```dockerfile
```

-	Layers:
	-	`sha256:2c0fdae4731cbc9c32af9e06c327454d735f4073f22db49be451823d7d8e0551`  
		Last Modified: Tue, 02 Jul 2024 23:59:56 GMT  
		Size: 2.2 MB (2204069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b392c53ffed541d9b6f94852f6010197df163f3d496e8d39996bf257c5f8e100`  
		Last Modified: Tue, 02 Jul 2024 23:59:55 GMT  
		Size: 9.7 KB (9717 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:108ee996ade8e245223d2482d0267faf13ea49921afd6e87eed344be82e0cd1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.5 MB (249463265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e539344479cc309ec3258f880e3953b118ebf3640c1d04d8d9721adccec06ac1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1962d4435d08ba61c23622c4093f70f3e7e0697381f6c2a0245649aee417122`  
		Last Modified: Tue, 02 Jul 2024 21:27:15 GMT  
		Size: 215.0 MB (215002184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1469a6aea21fd98e81b83d078b1bd835fd5021a9d0da9dcf5f8000a515253096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2215789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b44fca1010676b219ee55608bff7ed6af76592c1d728927dc037841cfa365bc`

```dockerfile
```

-	Layers:
	-	`sha256:b4ce7ba64b477890d51660b85c3523a59dbba1ff3903b9792db222d8e146e609`  
		Last Modified: Tue, 02 Jul 2024 21:27:10 GMT  
		Size: 2.2 MB (2206347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e86c4cc76917cfca419baa9b24528036985fa937ebd8cfd3553018832b2a0039`  
		Last Modified: Tue, 02 Jul 2024 21:27:09 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.in-toto+json
