## `sapmachine:lts-jre-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:f397ba3b3f5b2a9253c0942b8be4be8b022239e54e9373dd5cbf7154bb01de4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:ddb0801f885d45d628dd773e0444b3b1c8099bf0d60f520a39854d5a83f5377a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86998479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557108e928d10b36a1661ff9b60e212f727e5029862a0e73c005da3cec5203d7`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab10113d8e206191b3ca0d3463e562fe075d14a2efb982f309fd2249012b6266`  
		Last Modified: Sat, 17 Aug 2024 02:06:00 GMT  
		Size: 59.5 MB (59486710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8d22b8e8604be97d4bfa1106c01933a7c5258517cd14a542f6c02e9288347552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2291430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2581e13c88bf2dbf53d181d50edd56607befe24aa25cf67974769852d2df523f`

```dockerfile
```

-	Layers:
	-	`sha256:6c330e1ef911263a52e49d53f2f113b113e492bb64a491b18b049af2fc8f205b`  
		Last Modified: Sat, 17 Aug 2024 02:05:58 GMT  
		Size: 2.3 MB (2282204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056489b51adc0de04a5ebc0c27d53674c3e9f3c72ef17e2ccade1f3265fc624d`  
		Last Modified: Sat, 17 Aug 2024 02:05:58 GMT  
		Size: 9.2 KB (9226 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:44c200d56b7c8a1659c21721c9c563ee4535bf82d3347c7b173083c4249be61d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84555129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea282cede218225def3a884d38d52344d11dc65349a66529a8690e493f9904b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01633b8380a536a3c60163a443b985c18e2b9fcb7e8ddc164387a8e42e128b4e`  
		Last Modified: Sat, 17 Aug 2024 04:27:41 GMT  
		Size: 58.6 MB (58580912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:99fde141b90e7b855f8de80494256256631f42c797573aa3ccba8e11ecbbd88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2291414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd55a21a63582a195aafb91769931e242979548977be6c2f18e513adcc5af099`

```dockerfile
```

-	Layers:
	-	`sha256:720ab6657c200d99e3a9ad080af3499cb648cfe437718478a06f1c8954aaa5ce`  
		Last Modified: Sat, 17 Aug 2024 04:27:39 GMT  
		Size: 2.3 MB (2281864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec8902d9aa78d378bcb9c25048ab88f5ea6e083312b5081c4dd8f2bc06413801`  
		Last Modified: Sat, 17 Aug 2024 04:27:39 GMT  
		Size: 9.6 KB (9550 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5ad6c07dd6cceb1b3979f4bc633acce5b38ccdf0dce53029b819ec3aba3e0907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92748405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a03e476b93160ddd4381a2ee125c28535a44f3ca98f8d6634883cb277e03fc`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6041fd481c7cda40076e5f3cb540405d8bb9a86d9bd7de489a991f6934ba0b5`  
		Last Modified: Sat, 17 Aug 2024 03:05:06 GMT  
		Size: 60.7 MB (60671265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cdee4359e34cb506cf33a71ba23276fe6fd85b3420f2988d59150f7dd1d92573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b85595ce5a9c8ee9126ce7cf22346ead3da785623af5dfb585ed4c077e5c46`

```dockerfile
```

-	Layers:
	-	`sha256:1e8cc68811e01ff9566f08d9270159086549993dd70f2ec5c5ec7caa2f431ee7`  
		Last Modified: Sat, 17 Aug 2024 03:05:04 GMT  
		Size: 2.3 MB (2285981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24971da9edc3e728596cba02d995d6bd4a4e0c01657edf2ddd27393a8794e3d9`  
		Last Modified: Sat, 17 Aug 2024 03:05:03 GMT  
		Size: 9.3 KB (9276 bytes)  
		MIME: application/vnd.in-toto+json
