## `sapmachine:21-jre-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:f0368d3a7751f1cee3c55884fcfdf1b8d4248666e62ccf16c5143867af73f62d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:4ae106c2181057ecdb8c59b2845e377c4a824ad68805284ca75533700fe0a26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 MB (86777011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270737b2f5643671956d1faa9e14fddf153d0ec26b24a9b76920ef820d05435b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e7e955ed826242e8a293f0ee75669320ab1d9f7c3318c085072f776629fca8`  
		Last Modified: Wed, 09 Apr 2025 01:21:31 GMT  
		Size: 59.3 MB (59266617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:673b824422091b2009f897bb892896d878c85e1bdfad67132f795111da7f42cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522093eab188cec6fb4a3694557f91c4998e4b965f8839d01795101d6847dc64`

```dockerfile
```

-	Layers:
	-	`sha256:57fee8ac6d009c0e951287dd4cd0c928c72209c9ec2d2b0265b9ac7260d18d63`  
		Last Modified: Wed, 09 Apr 2025 01:21:29 GMT  
		Size: 2.3 MB (2301221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:472cd35b7adb1e0d370f4ccc890069c5f9de00566cc9d976a3161379c762a95e`  
		Last Modified: Wed, 09 Apr 2025 01:21:29 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2938729ea6e8cf63676cb5329c0939a123fa01019c734deb8d010d942791099f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84422577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888f590c0295230c43b74a53351fd765be45c209d473ad52401f224698c44223`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92792b6596e64aadc637b09f2d9c658c83ad35d7286041d71b97f35120c571f2`  
		Last Modified: Wed, 09 Apr 2025 09:38:30 GMT  
		Size: 58.4 MB (58444916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:43bf5933fc59758d1bd385c9f15d3fa8d3ed77ba4cdcf794725d88f4408125f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba5d20831c13c627765b2682408279aaee316fdf10aa4703aa4e39d1ca8d21d`

```dockerfile
```

-	Layers:
	-	`sha256:c76b468b7768a5129f8eb28b5b4de566ba45190844bf79aae367d2670c1f06f6`  
		Last Modified: Wed, 09 Apr 2025 09:38:28 GMT  
		Size: 2.3 MB (2300883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90673bb02424e17babf982eed8f0f707b3472d06c087a79e86572277eb42f49c`  
		Last Modified: Wed, 09 Apr 2025 09:38:28 GMT  
		Size: 9.6 KB (9608 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0d381122b0b3d03f31091d74784cc6f76b2fec68f83792056e6b2e4dd440a481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92544521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd06f3a37577c81b7724095be973bcf89eb37851fd213a0ad87eae1ed214e49`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Tue, 08 Apr 2025 11:48:44 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41b16f37b2e483e6feb6ee84788edabd5afe8c7fcd8de1152c48c5b301aa908`  
		Last Modified: Wed, 09 Apr 2025 07:07:18 GMT  
		Size: 60.5 MB (60467575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:12d155a28f3d59b744bf0832842ebe427f0ccf16f26306442bd036a36216987c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b4500688f5269ef7d0bd7431afb45b666e19ac3ceb8474348aa3e935eb0a49`

```dockerfile
```

-	Layers:
	-	`sha256:4524ead280aae2daa268d992efbee8eb23821d136e4f8650219336c43f68ba5c`  
		Last Modified: Wed, 09 Apr 2025 07:07:16 GMT  
		Size: 2.3 MB (2305000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f375a70088f998c8c37394fbe8a0a4c406d40554a04d9b51b75654f03cecdaf`  
		Last Modified: Wed, 09 Apr 2025 07:07:15 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.in-toto+json
