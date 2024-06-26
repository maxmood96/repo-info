## `sapmachine:22-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:2c1c8a11412978f5b4cdf44acbd7265ef99a7c818c3cf3576e87242857b93a58
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:7a96983707f0a2b24977e4c43572edbce8363d86a2b43ede06dddfc80bf2dd8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87641558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca483f105ec999edefc89290810e5c2f94ec5bca175a1b703b9f07d6d37f1224`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2b3591223abe46113d563984c485fdb10fce45c153062b3dd86fbb1ad468cc`  
		Last Modified: Tue, 25 Jun 2024 22:58:41 GMT  
		Size: 58.1 MB (58107804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:130040b5393a7179d5d8a36bbd9d153c593ef14bdb2eadb659ead7493fb620d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2131346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b8219607f99d203c8eb8c70891274673178d17b84c0604dcb826a2aa5687a1`

```dockerfile
```

-	Layers:
	-	`sha256:445d6f1089d4da154c77cfedc2a584fcfd15fefa3f965aa35380bfc6edeec629`  
		Last Modified: Tue, 25 Jun 2024 22:58:40 GMT  
		Size: 2.1 MB (2121971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f99e0a0e9580b3b8521413227f9bed62d78def78431d9aa9d2acac0d9880c5d`  
		Last Modified: Tue, 25 Jun 2024 22:58:40 GMT  
		Size: 9.4 KB (9375 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:5001f7663398d62c9564f36ce121e67b8bb023b03f0df2d79c0e7c76d41f2083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84468829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef3d4a9ca86911cf9c67bbb1abe50e98cf2ae485b66612a54e991e56c2ff11e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0f00b9dfdafcad2ff1f25f282140541e614e32245f683a2e63fc564cdf8017`  
		Last Modified: Tue, 25 Jun 2024 23:57:18 GMT  
		Size: 57.1 MB (57107047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7fad24dd0611c0918e3e690b85ef9c20f9bedea9c588fe3b718ca9f6a14e0c58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf041a070755f2beaf45ba13d385b32767f5b02c6bc604d7884c8fa480b7557`

```dockerfile
```

-	Layers:
	-	`sha256:55856d8593ec14d63588c2e9a4aef681441f25c26efc85f908d4e9df9d8150d1`  
		Last Modified: Tue, 25 Jun 2024 23:57:17 GMT  
		Size: 2.1 MB (2121034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6b97f18348a3618808b9e1beeaa934e6fde4303ce3127994b7ca535505777a2`  
		Last Modified: Tue, 25 Jun 2024 23:57:16 GMT  
		Size: 9.7 KB (9700 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:37e999de1de98af7754fdc18da6b35a5ade9d76f2355adbc50aac81e12efa2a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93829387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789476d27634e550892ccb67d4d9cdc281b0ebd0b625be9422c9053dea40ecd8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17876b55122bf07f92cb39208f31feffdf35a6dd6d8a80bbb1b78013b7e2cb70`  
		Last Modified: Wed, 26 Jun 2024 00:17:46 GMT  
		Size: 59.4 MB (59368694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:97086b24e66b0c6f462d39bae1e3cc8e179bde132e620d78699cd527b545be2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:587c679706456306b9cae030f082363dd9e69b05c9ba6b9cd8bd0a732f61bff1`

```dockerfile
```

-	Layers:
	-	`sha256:91b4c15fc439ed72f901334e7468b96d4f5c34d3cdba2d4970d3aba68fe384b3`  
		Last Modified: Wed, 26 Jun 2024 00:17:44 GMT  
		Size: 2.1 MB (2125261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:168453b6a06e51ce7489827c5861e3bce8d05b9a1e6c9cd0940acd7fed794155`  
		Last Modified: Wed, 26 Jun 2024 00:17:44 GMT  
		Size: 9.4 KB (9425 bytes)  
		MIME: application/vnd.in-toto+json
