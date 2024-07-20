## `sapmachine:lts-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:560c62d5aa99cf9d46688d9bbfd90d88f2e5c346edbf0b8d8ffbd06a9d0b3193
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:96ba6aba1e1e8f00901a186ceb2ad644cc12009ffddece80540bc004ff38f0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88260512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae7ba07ba350c257542df91290905efe16fad04b400b0bba1f0e9401f3b4d5e`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:3fc8f2b7aaa93afcf11bbffd96f29777f75b7a582aa57ef4381edd0cfa3532b9`  
		Last Modified: Fri, 19 Jul 2024 18:00:13 GMT  
		Size: 58.7 MB (58726457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f03d9598f210457bb373661d03cdd79846f10f174443150a735b05a89cb3e8dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2156888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c073eb3a097c3f19b43d4e59725e56991feec6bc00fdd1c5f2c4947d44c85f`

```dockerfile
```

-	Layers:
	-	`sha256:022e68e1c7fbdb8801ccde8eeff93c06d1c728d7a5582a62682f462789dcc2e1`  
		Last Modified: Fri, 19 Jul 2024 18:00:12 GMT  
		Size: 2.1 MB (2147515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f486cfdc3ff221e279087fafe54d39c41e9628949042ed3b7777838953319e79`  
		Last Modified: Fri, 19 Jul 2024 18:00:12 GMT  
		Size: 9.4 KB (9373 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6bcc5e391b87709fd0ca5740fca6fa80e34c6b428f7d08e6447d018f97e0a2b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85138816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847477f143de3ffd1758cebf1b91a044159023f31798caf78f615aa4689410c4`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b73ac12e1273c9f7352a9c1966164209a3dbdc6330975cddd39c23d2c87da13`  
		Last Modified: Sat, 20 Jul 2024 00:16:06 GMT  
		Size: 57.8 MB (57778791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dbcc47e45250eaa5bbf7a89ef35e593d507ec3f13ed32a2980ca1be18dd16cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2156907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7f488aef80fa65d8217232b08ff6467c45132c9d0f981cb5eb759d31a96562`

```dockerfile
```

-	Layers:
	-	`sha256:3675d4df65f0494ff95c5c42c1583f698a710215ee480b2bd995ce1a50ae14b1`  
		Last Modified: Sat, 20 Jul 2024 00:16:05 GMT  
		Size: 2.1 MB (2147209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb6c8aa9d6ba05837e15827c31fc6e202da09184d8e1dddc14933924b639d4d9`  
		Last Modified: Sat, 20 Jul 2024 00:16:05 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d2928c705aeb119099ec3bbb2f9cf26049c7ab403fb86dd339cc4da8c84450fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94573483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3735b3e41ca28a8802eabd32221c06de03f1239d98b1e9ae7453c5c9f35266ab`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e376c623297f57da0cf0bd4330857f4539117a689610227d4206e8eb107873`  
		Last Modified: Fri, 19 Jul 2024 23:22:39 GMT  
		Size: 60.1 MB (60112402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7fddb8283c352b04fbf1e558274670fb45a43d56bed3c537f79e52a29ddaaed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2160859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2d3350a6cd289190777232aa9da55dafecf180f7dab14d12c4b61e3f63142b`

```dockerfile
```

-	Layers:
	-	`sha256:322f07162e88a950a650e0918c240ffaa3cdb60a838cbaa72f97807597ecb20e`  
		Last Modified: Fri, 19 Jul 2024 23:22:37 GMT  
		Size: 2.2 MB (2151436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:682560ba4c2d70cfbbe436748c9746ae8a918e5914b93a09b3e6652e9b410cef`  
		Last Modified: Fri, 19 Jul 2024 23:22:37 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.in-toto+json
