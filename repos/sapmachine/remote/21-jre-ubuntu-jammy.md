## `sapmachine:21-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:b7aa1cded0a3c10952acb82ee1b25cb2fe069526201580c6a857264dada4c7be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:eaef6147d2d22a91b9f00581f020918692f8c4887a3077c1af533cb9c679bc44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89473762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aaa5aaeafe9a9733ab44d587899ad52d936011a492e49d95cefee92cf697a7e`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:bd4e818870235d4fdc19ef88b66823f495e340951d8c1971c4d6820179bd7fd9`  
		Last Modified: Fri, 19 Jul 2024 18:00:21 GMT  
		Size: 59.9 MB (59939707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7daea58bcfec36d64cab4ae8931383c5fbccf06acdff0941b545284164a3b1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e081a8f6d988fecb9d893ac4c508716a96af86349fff61a4ee460b381960de`

```dockerfile
```

-	Layers:
	-	`sha256:43c1fe298a45273090e7f68a39ea7e5fb000227e4704d2649c8a7cb4d2b17eea`  
		Last Modified: Fri, 19 Jul 2024 18:00:19 GMT  
		Size: 2.4 MB (2389425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be24238fbb6776a7a0694fded9f07af00eed2a4f90747ffbb68db6becbb38a82`  
		Last Modified: Fri, 19 Jul 2024 18:00:19 GMT  
		Size: 9.2 KB (9226 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ea45a5dc2d5a621b42e62983d4b9b4ff4ff29f52a94a7138033725f74ba3067a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86287531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6f6eea40c10b47c2d29755fa1079ba0762727baaffe314afb0a4475ed5d58d`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:c88a496f6805bcb022a79a46ed6b66bfbb43fe308cb5337eccd3affd3b79983e`  
		Last Modified: Wed, 03 Jul 2024 00:00:45 GMT  
		Size: 58.9 MB (58927506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6d10bb63e4ea8039992c27b411fdbf2077738ec0a034399f7c84bec7a69b7041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2369250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d1036fb6297f1f7234b869841e1f91cd98a39eaec717e0a9d5cbea213ba40c`

```dockerfile
```

-	Layers:
	-	`sha256:8ded531ca0a2c9fb1b48f58afee45178ac842913f8bdf2d6ca3655d730b84c09`  
		Last Modified: Wed, 03 Jul 2024 00:00:44 GMT  
		Size: 2.4 MB (2359681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14166c850a8c3517851655d599ae098064ff9c370d9d068c172f6f57ca66c99f`  
		Last Modified: Wed, 03 Jul 2024 00:00:44 GMT  
		Size: 9.6 KB (9569 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ebbb18605c98f1cee8034215fda227609f94dca9c6fee9d8750e4e3ac76e0051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95894228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d28ebeaae8a6d924406166b606a35443dcbe8c5f94c1e027a3e44994044d16`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:e417c4b704d29c182e7a69b9b835595ecabb32fc4ac24a8fedc317f3fce92e22`  
		Last Modified: Tue, 02 Jul 2024 21:28:30 GMT  
		Size: 61.4 MB (61433147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ced66fa3285fa4a3bf91ee4293a0e36a362d29f0f64226e7c64cd5af6e7d18cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c797f63066459e6bc4d3bfba5f861e55ed85bd79020e475f0ab6a56806495e`

```dockerfile
```

-	Layers:
	-	`sha256:16f84be4aedb5727fa0fcf9a90d0631ce79b329c65de31b572c67c8b915fa3ba`  
		Last Modified: Tue, 02 Jul 2024 21:28:28 GMT  
		Size: 2.4 MB (2363968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7836f2711d87a09991d320301ff77e4dabe6c7b04530b1375c890d4cdf5cf6b7`  
		Last Modified: Tue, 02 Jul 2024 21:28:28 GMT  
		Size: 9.3 KB (9294 bytes)  
		MIME: application/vnd.in-toto+json
