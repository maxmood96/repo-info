## `sapmachine:17-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:7296641c29d40c0beb78ef9d5ee47007890c22c51feefd6a1b4dc0b77a2fe637
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:bea4090de3d3197d82241289654adb70ac1148589ad0107ceb733728810ae567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228416699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:848c50cb74e3b8a1d0ad78d5ade4f2a7a30670539cb4d0610ff933534b9faad8`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19a42b609536e1c7a7bcf84d3a7ecb2c6b07bf3c77447c51d21f9d0f3538965`  
		Last Modified: Tue, 02 Sep 2025 19:43:19 GMT  
		Size: 198.9 MB (198879764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b2f6a1e1a6b2ce763b2dff60926379c31a035952d5b19096bf6b1bfbee1279ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3cc4e8d35ea683cea72c861b04a1f272b8e14943c4d230ee0a229afd3a9b87`

```dockerfile
```

-	Layers:
	-	`sha256:74e397c9e721281c261f28633e9e1a60d58e0962969aa9a9e289fb872f87d98d`  
		Last Modified: Tue, 02 Sep 2025 03:05:34 GMT  
		Size: 2.4 MB (2375767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b1e08737e92a7a0208461aa5b8072c8130f9303d7b88bb889ae7c7de0277c3a`  
		Last Modified: Tue, 02 Sep 2025 03:05:35 GMT  
		Size: 8.9 KB (8933 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:addaab5c4e670769f08ace1315bf0b9302fc931cc275f84e6b1a192edb15cd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.9 MB (224933943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07fdc8736c9f4666b8a169ecbe3eb5e5cda7aed8f9cd616b67a73c81a43013e0`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17688dac51eec53568800665c73543a95f2f9d4c23c9f0c09b6ccf2d488edfcb`  
		Last Modified: Thu, 02 Oct 2025 01:35:37 GMT  
		Size: 197.6 MB (197550836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:de62d4d27ae88f2d78f2d68e8d38b4846fbb482c666919096449108a9ff12858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228caa85c8a83e1aeb632ca33676e19cdc1fdbaf9154412f58854eb9c05afbba`

```dockerfile
```

-	Layers:
	-	`sha256:9cea14b0d6418af11924961617126f59954e4c82bc58b2689552af1f286c2dfa`  
		Last Modified: Thu, 02 Oct 2025 03:04:52 GMT  
		Size: 2.4 MB (2375439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b63c9b8562be9de9a82e3c5f025065e9d764c5ef25ae670e6cb1ef6dc5a7dc4c`  
		Last Modified: Thu, 02 Oct 2025 03:04:52 GMT  
		Size: 9.0 KB (9037 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:312e398a1740abc95036ebacf55b3f88d5b8ed4958908e340971151abaa8eeed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233821962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8f6c23c0752f8edec59849c3ac2066e4423be24f11a2bb1c416372883710be`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dad747e4a12a6d6704bf3072222540ed67631423511fdc4380f0d6eac5ec19`  
		Last Modified: Thu, 02 Oct 2025 04:51:08 GMT  
		Size: 199.4 MB (199375173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fc5ef0c4df2fd30f3ce2974ec83254d95147a28cf9d02eba2aa229df0575fb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcd2535f5997670f4a97b0cc55d6e302cb0fb06768212c48b3afaab00b34daa`

```dockerfile
```

-	Layers:
	-	`sha256:8cee16de4003663d305033447974e5037022e451ce8abce647f1f9b94fa8b8aa`  
		Last Modified: Thu, 02 Oct 2025 06:04:58 GMT  
		Size: 2.4 MB (2371846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdd7cbdadf6429b1d6de15624e0b8cfa1d68a4921317e9e9148bef075ab63b68`  
		Last Modified: Thu, 02 Oct 2025 06:04:59 GMT  
		Size: 9.0 KB (8977 bytes)  
		MIME: application/vnd.in-toto+json
