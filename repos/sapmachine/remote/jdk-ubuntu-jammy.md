## `sapmachine:jdk-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:3145fc1a0c1c4e6e36ce681e6c417b1391dbd176a3b20b40fcea98ddb8ed5382
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-ubuntu-jammy` - linux; amd64

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

### `sapmachine:jdk-ubuntu-jammy` - unknown; unknown

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

### `sapmachine:jdk-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:10db71a9a5a67f6471b6c03c0035164fca1416d6a38b11395a067ab1bea32ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.7 MB (238701983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4117234ef812507b2d6c7f151df1056890bf13f3663683fa947e065646e797c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b6e6ee7fcb2d0a2950121a1a2ef6bad72b0e94f9a78df69a6ad51431ff53a3`  
		Last Modified: Tue, 02 Jul 2024 23:54:58 GMT  
		Size: 211.3 MB (211341958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f787c9b7859addf68496872bba20654c15a5655636a221e9f232a5728fc8db49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2456266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47d525d9e983ab0ba66b3891354230daf5b5898d72b5e76187c18ea3444331f`

```dockerfile
```

-	Layers:
	-	`sha256:cb22090f0e3412ade3a2415c09c30898fb0188c071f134ad8f383c9c9b7fd971`  
		Last Modified: Tue, 02 Jul 2024 23:54:54 GMT  
		Size: 2.4 MB (2444692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8014998dc662f18ba78bf88af76495c8dde06c9e178556e1717624517d88280`  
		Last Modified: Tue, 02 Jul 2024 23:54:54 GMT  
		Size: 11.6 KB (11574 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:71ac490e642a3bfd33688b6777501bfd7a08d5d651d248e744c67d650e6ec8e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248938058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b0080e716896a8b70be778778bdac40d9fd9445427b99c2f7700472c535be1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e09c20b64d8f903a9dd215c9cfccbcb1d99501ba25b63564fedd9605d5025b5`  
		Last Modified: Tue, 02 Jul 2024 21:19:36 GMT  
		Size: 214.5 MB (214476977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3e3ef8e613b657f4117c5091891a61ff100b63c2a42331bef069684ee02c3d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1f6c248823f68346cf6809d8431f970b76703bb681ee3a47459c992b530611`

```dockerfile
```

-	Layers:
	-	`sha256:8074261dc9c2d05804cbe7eddfa38c2e6e3ecbecabbc9f1df53bede8ae784e5b`  
		Last Modified: Tue, 02 Jul 2024 21:19:31 GMT  
		Size: 2.4 MB (2447006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d4f97d8d05ddf68682f7cb9ae0f6ba6def83dc8116ecac8a7aa95f5747897ec`  
		Last Modified: Tue, 02 Jul 2024 21:19:30 GMT  
		Size: 11.3 KB (11263 bytes)  
		MIME: application/vnd.in-toto+json
