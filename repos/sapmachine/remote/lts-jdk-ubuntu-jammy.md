## `sapmachine:lts-jdk-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:96179eb7c2f0983149cbe95b1312fb01e02150513a8bf7bb0be6db99823d3128
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:59508e6b8e281680019e99df8d5e41cb196632bb89bb1396810db1f79abb0bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.5 MB (251533482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc57a23370b0c1dfd1c859ce315f98da31c3826d216395a97c3ef161867b3de`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:03:46 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:03:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Apr 2026 23:03:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cc1745fdc80dc64c97b76c821a8fde78aad09c8fc214cfec9330b6e17ce83b`  
		Last Modified: Tue, 21 Apr 2026 23:04:08 GMT  
		Size: 221.8 MB (221796984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:61d985095ba329cfa5333bf964410fdad183758e84bf3521d0922dd5d4cee185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525e21e64a5d1c6e7d6fb5c981351025b140264a690ee6002d8b82750828472c`

```dockerfile
```

-	Layers:
	-	`sha256:53cbeb6745f56351d143797fac9a7cf090395834266c138e311204651504a578`  
		Last Modified: Tue, 21 Apr 2026 23:04:03 GMT  
		Size: 2.6 MB (2623518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b0b23703aded337368715b199b46d7ed67680a1e771f22b4765b77cdfa1a82f`  
		Last Modified: Tue, 21 Apr 2026 23:04:03 GMT  
		Size: 11.4 KB (11402 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:72e4d62577fdcc3b904746af73e22a52cae294d3d4ef82df72000276a5b5c173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247156446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9fc325db53a4db782be750966f2565e2d3d188b0e1746e83beda5406022e31`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:05:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:05:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Apr 2026 23:05:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524a8342de8f5ef987b6d4452653416ae8343fce975d0addc264a66fe1917665`  
		Last Modified: Tue, 21 Apr 2026 23:06:08 GMT  
		Size: 219.5 MB (219549903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c9f90008a04983323bfba5bc15ffe0b59a1b31ac1d1961b5d4c1e3c90d1039e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71254ae50b4d68a21a01aae78baaf8e7f50981dfca73ae5f6da537f592e53527`

```dockerfile
```

-	Layers:
	-	`sha256:4b74326d62e3448270cc41a8bb9dd8688d46eb2790ae3d0473f8c3a7340e9de4`  
		Last Modified: Tue, 21 Apr 2026 23:06:04 GMT  
		Size: 2.6 MB (2623293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79e8660bdcec5878a2a76057342e5e971887742cb0fc4d8d56cdb4eca83faf5`  
		Last Modified: Tue, 21 Apr 2026 23:06:03 GMT  
		Size: 11.6 KB (11602 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f5448e34b97ce890c16891732aab8416c707afe8e6aa64e37ea48b5907433e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.5 MB (256520584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67277a2ba6eb34cc718f150ffe24e035e2e3efcb74fca882d23c5eb4d461af5e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 23:29:25 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:29:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 23:29:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8bb913e458a68c2a42987dc7fbc8da25089821ca8ece9d56d9330e9d5b0294`  
		Last Modified: Wed, 15 Apr 2026 23:30:06 GMT  
		Size: 221.9 MB (221872186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5c0eaaa49ea05610747a5d4a9b3550d493a16b0e75f1c15e41ca29e90bc8edd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2631393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec44bdddda69f8e5f2ad5f1dd6117696eeff46a39cd21347031a12652821a55`

```dockerfile
```

-	Layers:
	-	`sha256:631d18977a7aa75fd2bef49a0e8a1999528d0849a837c7029924fb0caf10bde1`  
		Last Modified: Wed, 15 Apr 2026 23:30:01 GMT  
		Size: 2.6 MB (2619900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45b64e7514709ecf177f3efeb7f0fe63d84b16e7a2ea044dec02e4dc9df4046e`  
		Last Modified: Wed, 15 Apr 2026 23:30:01 GMT  
		Size: 11.5 KB (11493 bytes)  
		MIME: application/vnd.in-toto+json
