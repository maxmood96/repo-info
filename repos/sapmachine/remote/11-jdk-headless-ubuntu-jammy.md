## `sapmachine:11-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:7f3c182662b880bff0e95484fa989fdbf740219497f2dc323f17c2a8028c4959
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:59b29e19bce5c7af4d8af03c97e713c763f72816c7cc84f0eb3e75f03cdc11f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228999250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca4ba9ee5b1714ae61a67da08cca4c687e36522b60ae4c82ce7a63b0389994c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a04dc5fe26b017dfc94fc18a4a8a2bcdcbc3f96ed09538caa1a81b992c4e48`  
		Last Modified: Tue, 02 Jul 2024 03:32:43 GMT  
		Size: 199.5 MB (199465195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2a0091dbef729e15d86ac0a3571c970ca74a171d546c0fe56586d70e469f41b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2229696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb45a858e426e794c42277e09fcac8c9423e1198bfa4afe70b4247c04399dce`

```dockerfile
```

-	Layers:
	-	`sha256:f2591e17e5d8d7b6c04c92b7a772bfa9e13ba87b330a5d539faca3d60ac0730b`  
		Last Modified: Tue, 02 Jul 2024 03:32:38 GMT  
		Size: 2.2 MB (2220999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51f23a582a1071de6188e7572167a9bec2cbe50a17464838ab0bb8ecfd4191c2`  
		Last Modified: Tue, 02 Jul 2024 03:32:38 GMT  
		Size: 8.7 KB (8697 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ad8fabd515e1e4e247adddcecba7cae1d9c2cfa320848ab940800e34626cfb57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.3 MB (225307961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca19d54ca6f5050c3ac5a7408640a002101b4b6843bd0e1ea65d30f58f19bd0a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae4f99c8601d6b3497a48d959988a64e5c1b84409cdbdc5ac5bb18cd3022cd2`  
		Last Modified: Wed, 26 Jun 2024 00:33:04 GMT  
		Size: 197.9 MB (197946179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:627737a50727beec459e6cafd5d685cbce7c8067265ec20d4810bc253ba04f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2230295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d7a31902cb6d02e46c6c57e38f9b0e190156faba5785a9efc055d4b0620063`

```dockerfile
```

-	Layers:
	-	`sha256:5733c98d35eb89d7ae9b03b3bef46423248cd2ee7339ba3a274374be1d48ebb6`  
		Last Modified: Wed, 26 Jun 2024 00:33:00 GMT  
		Size: 2.2 MB (2221297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:991979bd156e75954f53dfb77eee064d2b8b940d76762ebd87296fee1c41f882`  
		Last Modified: Wed, 26 Jun 2024 00:33:00 GMT  
		Size: 9.0 KB (8998 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:fe9429658520d8ac80381a2ea6268d6c7db32fb29ac59ba912913ba17363efc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 MB (220416281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42bef8a654c305f43aa7f435b7bde5e07328c53b25150ecf52a717c161a9a7ed`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4185260f5a85604ba58ea9ba6d2a0cf271737a154627900de12264dd5be581e1`  
		Last Modified: Wed, 26 Jun 2024 01:16:02 GMT  
		Size: 186.0 MB (185955588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fb78c8effd89c79ad5936105cf4c73d9a41e93280ff281d578a8f692f19e8bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2231069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a73ce2613e92db56617c54b0977ab81d8254b5225ae567dbf90883b93623a72`

```dockerfile
```

-	Layers:
	-	`sha256:37b710a755c1bd2aa43c8849068f419df7f9d479654286cd8deb9bb6de46fc3a`  
		Last Modified: Wed, 26 Jun 2024 01:15:57 GMT  
		Size: 2.2 MB (2222334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:602ee5f1bfcfa23e5b113a9e41b14cd275669f476afb171458ea85a2acb53f85`  
		Last Modified: Wed, 26 Jun 2024 01:15:57 GMT  
		Size: 8.7 KB (8735 bytes)  
		MIME: application/vnd.in-toto+json
