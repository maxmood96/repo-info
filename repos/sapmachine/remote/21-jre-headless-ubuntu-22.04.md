## `sapmachine:21-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:f9d385fc71731cbf6be5733c3e941093e02b74503ec13fcd6e4574b24e6e0979
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:10d1ec6f37d1d3318dd0ede66935673e0500744ec13243b4b2b2f53cd3cb214e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (87977405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78df735c0756900e38131125a044466664e49d2f28fba623ab1f4ead55050612`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa85bcf0fd8a8f98b1b1ce1f0c98f2c9abcd93b43e5f3a66a1595a5a1042bfc`  
		Last Modified: Wed, 16 Oct 2024 18:58:38 GMT  
		Size: 58.4 MB (58441717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9c4f3b94e85d73d39f8884a423ef9c8743e7b3eb833806acec3dda6c897f7fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2162942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e435c843ac93d2eaca521326a06e38a1fa967ce5d61a4ea6b5f6f9801def35e4`

```dockerfile
```

-	Layers:
	-	`sha256:be676d8b00fd88c3175d9acae3ca7222eecf0be5c70ace392cebadc4dc029cf9`  
		Last Modified: Wed, 16 Oct 2024 18:58:37 GMT  
		Size: 2.2 MB (2153531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a16be14ccad8e8d23a7e8280b16fc21e248e67d9e01730d747c406d8c54e69ee`  
		Last Modified: Wed, 16 Oct 2024 18:58:37 GMT  
		Size: 9.4 KB (9411 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8876eedc9a654d1130cffd96b7ebc3f6101edb00f7ede90fa02b0375573a3c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.9 MB (84912510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e755d90c32ddbb697a77daaa296c5ca99755b0e4708f2331c6700a57ca6265`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 08 Jan 2025 03:54:57 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66c6fd2a9f67eaa8eacb2ff2674cab3390fa0702f4c1288c7ee03d5d503e247`  
		Last Modified: Wed, 16 Oct 2024 19:21:07 GMT  
		Size: 57.6 MB (57554181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e84b6559566dc6f02c22988302ebfafd1b7ca74543ff81b04922bd157147ab08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2162758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7932c3908cff5cbc02f340c9e97bc0df98e4970a4e465aca315891eee99a9fac`

```dockerfile
```

-	Layers:
	-	`sha256:6d05173a4aec64477abd86f07a5a7c60eed4916271fb2344956f59f7a03c01ca`  
		Last Modified: Wed, 16 Oct 2024 19:21:05 GMT  
		Size: 2.2 MB (2153225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24144f403deef98ad13bda30c63ba849a2fb0e9810a6e47da185f0d03d5556f6`  
		Last Modified: Wed, 16 Oct 2024 19:21:05 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:213f864485fcb9f5037787903bad4aee2a28d013a37396a65800570353beb8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94292406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1263f80bf268451d63126bf11fe9b92b506b66ec8f4894ccff4ea15659b68ea`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b31f6201dff281c19e6e2c63234fe8dd0478f1109d0cd9943a42d100ec284b`  
		Last Modified: Wed, 16 Oct 2024 19:38:57 GMT  
		Size: 59.8 MB (59844164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f1899942e12c4c0641d43eb77dfd8f2b1898a701c0cba1cccc7b340b31dceba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2166912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d51f8b7978d3c77d6ef9e0743661b5295332dcaf21bd69c0e75aa098305995`

```dockerfile
```

-	Layers:
	-	`sha256:1f904d747af264dca457dc96f319bff9d6575812ef0aacfabf5e5683b48b98bd`  
		Last Modified: Wed, 16 Oct 2024 19:38:56 GMT  
		Size: 2.2 MB (2157452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da720ebd96354a2ff02bed6f4241e73f7b546b9003a95d317886db487e4b38a`  
		Last Modified: Wed, 16 Oct 2024 19:38:55 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.in-toto+json
