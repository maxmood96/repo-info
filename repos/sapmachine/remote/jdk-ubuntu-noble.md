## `sapmachine:jdk-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:5aa0c9f2b30328fb0ac5dd5efa26deb8c08cb382ffcb9ef3c1fb06194486178f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-ubuntu-noble` - linux; amd64

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

### `sapmachine:jdk-ubuntu-noble` - unknown; unknown

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

### `sapmachine:jdk-ubuntu-noble` - linux; arm64 variant v8

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

### `sapmachine:jdk-ubuntu-noble` - unknown; unknown

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

### `sapmachine:jdk-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9c2c335328d12c4003a5d211dc8ac54e6499879c695f17fb8e4dda2193838223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270744617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b12d73d4c24e139667745ea5a679befb59efb753e74a7b654ffdbe9588e2c6`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc072e12332c0a15a48df463ab8a66387f98a818ea4476acc9b836b98ab4aeae`  
		Last Modified: Wed, 19 Mar 2025 20:34:01 GMT  
		Size: 236.4 MB (236354793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0f6c9c265fae11343b082b44ae61af30f74cd1a1a2c746e382d8b87de04c522f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2477904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ab2ac9f553fdb6d018695a640649073cc82b7ed13ceb49b36da5139ae50862`

```dockerfile
```

-	Layers:
	-	`sha256:befa1f8a996a076830abf094b8479f1b7fdbf0caabf46de6485002190d805129`  
		Last Modified: Wed, 19 Mar 2025 20:33:53 GMT  
		Size: 2.5 MB (2466513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce8727040141704a9f06f17e5580ac243fd9517bf1593d263b8771a76ff255a9`  
		Last Modified: Wed, 19 Mar 2025 20:33:52 GMT  
		Size: 11.4 KB (11391 bytes)  
		MIME: application/vnd.in-toto+json
