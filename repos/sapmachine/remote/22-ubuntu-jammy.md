## `sapmachine:22-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:d1363b0d4d4a9fb5ac8368e36a67bbd5b88de105cff7ade1e1d642fabc426278
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:cb72d52e6da5b85fdb8c59a2ef9d02ba159d6d30273c3a478f3f827939b95939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242763574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1591f825faba27799b9284f5240fdf07a789402928b5722fb26b445c0e510c0d`
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
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8895c1cd7d6b4056fb945937b74edab60d7ebc7f030e8e795b29462b3a103f92`  
		Last Modified: Fri, 19 Jul 2024 17:59:23 GMT  
		Size: 213.2 MB (213229519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8154a854ff56c8facadc3bd453d95033920f4e3d351403474ded98c22c0e343b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2486788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997207c8565ec49f7026b70eb4daac5290feb83ed6b6a4e049c8ec5d5d94c4bc`

```dockerfile
```

-	Layers:
	-	`sha256:e4c3a664f3654d8a2b41a018fa5ad323f225a811bf7de03dbf6fd3a2811599a7`  
		Last Modified: Fri, 19 Jul 2024 17:59:20 GMT  
		Size: 2.5 MB (2475629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fa7a5a37ee7e83c22d75f267623f37078125d01c412814b59ae5b11f9655097`  
		Last Modified: Fri, 19 Jul 2024 17:59:20 GMT  
		Size: 11.2 KB (11159 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:513cdb8b5fd5ce309fddae9ba35d76fa33032b49a13c42ad04729bccffea1b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.5 MB (238534131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00199ebb210e525ad8566dcced84e9fcf1201f605ad59df7a452f057a89a7873`
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
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d867ed73c365ccd042a25d14b82511ee119032187ce17c647728dfcd90b37211`  
		Last Modified: Sat, 20 Jul 2024 00:00:33 GMT  
		Size: 211.2 MB (211174106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e05a634513fa58935a6b56c4dcd7d175f8404572e3a34f69020f8252743e2416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2486330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c212fa6ee221a74f25f5af2f0e80b40d6d3e7e3caa9a1fbf0d974b9b4631a3cf`

```dockerfile
```

-	Layers:
	-	`sha256:ffada188ee66a29d26d357f9231278c73e4b4434a99814df47990bb3ae5f9f37`  
		Last Modified: Sat, 20 Jul 2024 00:00:28 GMT  
		Size: 2.5 MB (2474774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64a1a229cec0ebc86a4638ea07bda878ef79b1bd74d9c726eae6eca1ddf23b9e`  
		Last Modified: Sat, 20 Jul 2024 00:00:27 GMT  
		Size: 11.6 KB (11556 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:cc8c816cba7e82e62c492ad59542328f075ab0904bd458a472d38f9de831752f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.8 MB (248774397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712c26ae8341f2f3f92aed7546737f5dc47f712240441bfc8a0b26031704930d`
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
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3d6f814aa982ccadce6c026aafc83bcd519e87dbb0a4ec346c4421959b438c`  
		Last Modified: Fri, 19 Jul 2024 22:56:38 GMT  
		Size: 214.3 MB (214313316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:42e9eb0f2deda16158561c05bde41503b53b8ced9bd952fae38f974d672ae53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2488333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59c0093daa2e7e850a3259ac1318435226fd87a11fbad7a155e18d0e501a491`

```dockerfile
```

-	Layers:
	-	`sha256:f816e07d28f7dea8125577ba86b394916f4959a099e8635a896f365a81441234`  
		Last Modified: Fri, 19 Jul 2024 22:56:33 GMT  
		Size: 2.5 MB (2477088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:706ceb452602149263a4ed2fc5dad391943d4e861b19ded94a2a0987cc7ee479`  
		Last Modified: Fri, 19 Jul 2024 22:56:32 GMT  
		Size: 11.2 KB (11245 bytes)  
		MIME: application/vnd.in-toto+json
