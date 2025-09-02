## `sapmachine:jre-ubuntu`

```console
$ docker pull sapmachine@sha256:4608455cdfc299aa11d9aadab76896f98767e9491ebf514d964c6ff0679f7cdf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:b4578b9909ba3c15263ab972748e94356e3570796175229223bd38aabe19d041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97815257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc61e76d8b9f4384492919f8dae71a013641eb473b47053c3970717896df85b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc618ca8fdddc4c06ad7eb85b9b39742f4050588c83f4cfa325b13e6d7259a0`  
		Last Modified: Tue, 02 Sep 2025 00:26:49 GMT  
		Size: 68.1 MB (68092193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1b9c458a7032f905a2e94e1e88a7a065cff6d243633e6e4efee9e2c944176ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1063ca29a431afac7eccef190f8457489e92e60a8c35cc3a98ba9cfe02bd7140`

```dockerfile
```

-	Layers:
	-	`sha256:417beababce248d8a6f80036e5144d66cbdf72d8cdd3c84446e067c341631527`  
		Last Modified: Tue, 02 Sep 2025 03:09:35 GMT  
		Size: 2.5 MB (2526946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d9b82a23661bea1cabf82f5636898a48c9bc21111fd4a821ecd1da4d43b3e06`  
		Last Modified: Tue, 02 Sep 2025 03:09:36 GMT  
		Size: 11.3 KB (11346 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:31b9dc939b0ecc0e20dd163d01bf7a946aca2a6892186825152915e3eb755919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95994254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ffa950a8f63a9bf304a7a30275f0d31aeb49b4d52b134024267a5a3459b1e9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d545ab2e17ca906a8755577701c99448d01bc0df95e6d6a61b6fa5e66bf6d043`  
		Last Modified: Tue, 12 Aug 2025 21:14:04 GMT  
		Size: 67.1 MB (67133877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:adb515dd959e45dad4ff5dedf0853aee5d76d30ea588e4d0093eddeb5816fbda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2539053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b609ae1472b465c388f7723979d62fe0a6a25fd3f229798001d5d39fa9706616`

```dockerfile
```

-	Layers:
	-	`sha256:77920c88463580e9877eb93f39869e971b68c03dfed7d122d41c8dab68c16736`  
		Last Modified: Wed, 13 Aug 2025 00:09:26 GMT  
		Size: 2.5 MB (2527507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2e73e08a4b36b183d4362be678cc9f108f60a92d0be65a09a339ffc3e5fc052`  
		Last Modified: Wed, 13 Aug 2025 00:09:27 GMT  
		Size: 11.5 KB (11546 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ef54ff73549bd8b9e9467d0b095fd300bbcf5a7300b6e6021ff047c294827b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103345257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9975a6f859ee6c64e9db80c056028ec29418b501b48e485ba707715f80fb5bd0`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b7419fd6949351336992fb391cee8c968b75aa9b8f5f141cbcfa4f06bdfef3`  
		Last Modified: Tue, 02 Sep 2025 01:52:17 GMT  
		Size: 69.0 MB (69015724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d2c18b04e52930c2dab69f88dc03e83c5a7189906230b6245d3c0e58affe2087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2535859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a9334aba735ce05600842f8170799e7136e348d6c5af2f475c7c6622fef6a0`

```dockerfile
```

-	Layers:
	-	`sha256:0ef9423dd391885e554c8bd051c283524571ed2612342c2cdf8a3bff0f875798`  
		Last Modified: Tue, 02 Sep 2025 03:09:43 GMT  
		Size: 2.5 MB (2524421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd09f886dcc37b1d4be4378986a949a061d680624f996f62b9ea8905dc614039`  
		Last Modified: Tue, 02 Sep 2025 03:09:44 GMT  
		Size: 11.4 KB (11438 bytes)  
		MIME: application/vnd.in-toto+json
