## `sapmachine:17-jdk-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:2b16e200047e3f43b4b44919911f56c22d1b94bdf58b142c69e40f8383439d97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:0f5abe7f04c2b8fba9e34690cd854b90dec8da006fe5d38bf48fa6026e13bc07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 MB (225900018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21235c435527a021aa582f6673fbefe9e2c090fb2dced533d4ce747fd4bf0193`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ea158b6dbb39c255910d7c410ecd8fdf8ca6c1534ca50bd6adfad0c69cab89`  
		Last Modified: Fri, 19 Jul 2024 18:00:33 GMT  
		Size: 198.4 MB (198388249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d0ef345fa5e3729666a1a739bb3eb2358587c42a2a261cd317d1e937c46784a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe02e32269258822db058b6d7a6bb57aa51cab3854bfe2c72dc307d5a9a1aafd`

```dockerfile
```

-	Layers:
	-	`sha256:7f5f630477c07a8fac626565e6259ceba60aa8e63fb25ea38b6f82f26253772e`  
		Last Modified: Fri, 19 Jul 2024 18:00:30 GMT  
		Size: 2.1 MB (2125393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37c5f9310fb8de30a288678dd4b3b9029a4298dad72bdcf51a5c9aae803d3403`  
		Last Modified: Fri, 19 Jul 2024 18:00:29 GMT  
		Size: 8.7 KB (8679 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:53e0ddea0049517b910153b9c5459e75ac8420573b3d62af59e0037e06711402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222859718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9486c6928b5fd49456991bb5065e4ff0301943114ccacede7ba7e91255580bb9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2175b459e448d04c513de8fbea1e041ef26f38228076cec92d6c79efede069fb`  
		Last Modified: Wed, 26 Jun 2024 00:24:07 GMT  
		Size: 196.9 MB (196885501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a24a65b6f120d1705edb7294176dd03dc1598aea948e718e35e1feb86ed306c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2109167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903e08ccb0bf823def93f4ef047c4745216f64f1c0ee684a14518beeebd4a19e`

```dockerfile
```

-	Layers:
	-	`sha256:2a9dba45a6d6499a89e2d1a0965d14fadc4baab6df8484c340255d10e38b0966`  
		Last Modified: Wed, 26 Jun 2024 00:24:02 GMT  
		Size: 2.1 MB (2100169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab68ac63af61c5e8f7a950c3e62efae8cff22a3b46cdfa3248aee24853ba5e19`  
		Last Modified: Wed, 26 Jun 2024 00:24:02 GMT  
		Size: 9.0 KB (8998 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:880c75fc2f24c5e20a06dbf83aa4dfb4be7167363b749a55c28a388805d6c309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230854172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498a02699108c53f906e9a393f0bf834c18abf66c50226f7e7a631fb59058f71`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e9d84297ba2446e6e945d3e07e8e0b28d7e35c7e80b2a663f96e1eba9c4ead`  
		Last Modified: Wed, 26 Jun 2024 01:02:28 GMT  
		Size: 198.8 MB (198777032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9194352282e550d9af9f3ead480df34dd1fd92f587c6eea3a91837cd7ccdcaa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2111030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0615b60fbfcd78f2c327e82d20ede852e26be2ff4fbee1a87cf95d252a30ca87`

```dockerfile
```

-	Layers:
	-	`sha256:232bc4f8000f4b6865307fe196c86a8c562cf418443d4ab3c531602c882a1659`  
		Last Modified: Wed, 26 Jun 2024 01:02:23 GMT  
		Size: 2.1 MB (2102295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66b97868d6763a0fcac4c827d0daded676f5a6843aea022caa1a6ba7017e8c40`  
		Last Modified: Wed, 26 Jun 2024 01:02:22 GMT  
		Size: 8.7 KB (8735 bytes)  
		MIME: application/vnd.in-toto+json
