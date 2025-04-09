## `sapmachine:ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:365b1c8d7335c0003b47c6a0b5b968d1bdcc751f7edce00cb6575f6320d89dd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:d14b60c9849eab1030a9dc6ce41a95c7bc0867123d5c1b08dbfe20fffd3778af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262111536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47139728e4400fe65095f90684c34b7e38ac0e42761d1d373654f1b07c9f98d0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3437ed35f5c8d446cef703f6d9da0457dbfb86de2d1c0bf4dddc4f47150e8a1d`  
		Last Modified: Wed, 09 Apr 2025 01:20:35 GMT  
		Size: 232.4 MB (232393884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8ea0931b0413f8b516861d89954e36461b477b9991e4730c5b86f28453e99c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2474204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84b410ab656dc59be41d698a829ecc347b564a25deb4ad64be4b6bb2fd39d5c`

```dockerfile
```

-	Layers:
	-	`sha256:435e3e8b04cc77313e3724358919e098afcc0c0cc48b0859615a532301b76164`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 2.5 MB (2462905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b701ef4041a5668065401afd8f458b30d9b9089a6c92f90677ebc29c23a345a`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 11.3 KB (11299 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ba3f28f117dab887c19dcc2fbd491453b8bf5a78368555df28b4e1cb74148b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261450526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33f2431c2e82fdc3c122b32604acaa001e91fefa037687ab1998ed1e680e224`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11c53936a49f11dab09db667c9f6380067a86be449f9ece0bfd550a497645a5`  
		Last Modified: Wed, 19 Mar 2025 20:33:03 GMT  
		Size: 232.6 MB (232556928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:161c3e80499d7f4810297575161d98f5d4ee6bc929c7f4837fe81fc7348bb563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2477150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53dafccadc2274374c4eb618315203f12026f14fdb0d34bae3c12dc9dcb046bc`

```dockerfile
```

-	Layers:
	-	`sha256:f3922ea2aafee2e27b5a93887cc781832a71baa2013fabc6e2429a661d2adeba`  
		Last Modified: Wed, 19 Mar 2025 20:32:58 GMT  
		Size: 2.5 MB (2465651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a7334f1d276c0522945cde43156eadddd7361ac38c6b543408bf2202d6b6f9`  
		Last Modified: Wed, 19 Mar 2025 20:32:58 GMT  
		Size: 11.5 KB (11499 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9114fbeb4f6c3b602d7c34dd7473330d10d5f4a7062374bcaf7b2a1db8ecaa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.1 MB (268072893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add97a53dcba9389f98ea0b3388deebc6054604dcb06a5450bbba9aa6711cac5`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99dbed487d09d89c96ca9a6f11775281f704f98f496f1ecd9800b0596428fb45`  
		Last Modified: Wed, 09 Apr 2025 06:32:47 GMT  
		Size: 233.7 MB (233732026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7f5ee978899c9bf1dda7a9736ba38c0d7e763c9c48f3d57299eb81496d03934d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2475716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:265d55f0218085bb0807bd6c3fcaed6fd2b30591883236f2923ba2c65265f8a9`

```dockerfile
```

-	Layers:
	-	`sha256:7f9ad74d76d0a72d307413ae9de74b6d0a2b50c46e7efd8ca7eac55c3d17c8f6`  
		Last Modified: Wed, 09 Apr 2025 06:32:41 GMT  
		Size: 2.5 MB (2464328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:181445abacc6429a7d0461e43e8650835e9808600f1241d5ee4969a2f11985d4`  
		Last Modified: Wed, 09 Apr 2025 06:32:40 GMT  
		Size: 11.4 KB (11388 bytes)  
		MIME: application/vnd.in-toto+json
