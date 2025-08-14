## `sapmachine:jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:90c227b5f95c31a00e5aa91e89e13a00b4461bf0391edfa187c8fd58fdd25286
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:5bfd85bedb27d15e8e579cf4849af2b783486e7d961764d3d9a72c634fba0849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (260998183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbfdb2f679847fa0d6eae8140d1d2cc61c6e715e382b17e2f4f157fb9cddaa9`
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
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1583a5ea1c5671460a3b9d48bfae7e546fa69d0ed6238aa3d1fc0aab52b06350`  
		Last Modified: Wed, 13 Aug 2025 12:06:23 GMT  
		Size: 231.3 MB (231274968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:17a5a52a8131502fe7dbf639caabbdfcd6ca883eaa89ee703459b991eddd4b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2359992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:763dfc4a268332ee9077f55378c41b728d297b1beece374571e06080c32aa125`

```dockerfile
```

-	Layers:
	-	`sha256:5e83985371e0693280ebf85f859b942fc26d314cfbc5d1c76199084557af62f2`  
		Last Modified: Tue, 12 Aug 2025 18:07:10 GMT  
		Size: 2.3 MB (2348391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00e84440f395f8f749c034f361af8d16021337dd4a262d2504a09838059406b7`  
		Last Modified: Tue, 12 Aug 2025 18:07:11 GMT  
		Size: 11.6 KB (11601 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2a9440778b373b2fa5be4214dd4721ddb254b6472f13f077bc45d2823f5aab8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258063524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0cb3538c3154dc1187db6f9dead896483d884a3cec3056b8e777544a926482`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:5840d6aaa6b7e0040f1d33e705304b7546563a6ae2f9f5ba712f6dfd4b36250e`  
		Last Modified: Tue, 12 Aug 2025 21:12:37 GMT  
		Size: 229.2 MB (229203147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:204d995e7b68ef58d56a08fb4623794454649a0bf35761e7f0798b5a2ac662d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2360745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e33027d0248fd803e91baf2aa90ced1263a4315f639fb8d1fb519531b96bea`

```dockerfile
```

-	Layers:
	-	`sha256:0b7eb99904ab83ffa558c6a19fe0cc00b40113c91e22bfe8ebb4750c9673c9f2`  
		Last Modified: Wed, 13 Aug 2025 00:08:57 GMT  
		Size: 2.3 MB (2348943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6502c680faafb741c93673cf96bb83c7c06fee86e908ba57f2bb50faae27eb4d`  
		Last Modified: Wed, 13 Aug 2025 00:08:58 GMT  
		Size: 11.8 KB (11802 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:bad9e20880be26a49ba16ed7850bd91b355ec439c66213d4b498cbcd811a19a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266276485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1efb3a1ebc6e1de6d070c9799a62e0b46f56ce3a6bada0d4e312fb68e43efbdc`
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
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409c6b3f1ee961c2d4ad6a39cdaeb388f76957c7f8574cf734eaeb0451ba082e`  
		Last Modified: Tue, 12 Aug 2025 22:23:54 GMT  
		Size: 231.9 MB (231946835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:64776e43d89b3d2fb90a9cdaeeb7928c0ed4b2e04fb1f8d9ce9ff39266661090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2355545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3630a85865346a8de8677f3f9bee78fb03ce5e4dfdb061091db7157e161cd438`

```dockerfile
```

-	Layers:
	-	`sha256:4f634874f63ae41d401ef173c0992ca0177ca40d3f8028f72e40560bb55c6b46`  
		Last Modified: Wed, 13 Aug 2025 00:09:02 GMT  
		Size: 2.3 MB (2343851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fde2b53bafd437c8c413a01228b0a7a2cbcc82d3a4dacdb735f5d15068bc453b`  
		Last Modified: Wed, 13 Aug 2025 00:09:03 GMT  
		Size: 11.7 KB (11694 bytes)  
		MIME: application/vnd.in-toto+json
