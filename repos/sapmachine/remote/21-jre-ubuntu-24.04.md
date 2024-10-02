## `sapmachine:21-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:d64b8168675ae126cc87e539dc406ca7f12f658bfb518bda7050c8027f7d8887
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:5607fc4f212072557bf23ee8f414328c251d4e170a273bb44674e7ede620b436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90078781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30daf0401361bf41ae3c5017f27bab8cf8dd30bd6c22b041af79d2c79efc737`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
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
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5c5036b6e7d0e38895ed8fa557f76b8872b571712d092e6bec31428a446824`  
		Last Modified: Wed, 02 Oct 2024 01:59:58 GMT  
		Size: 60.3 MB (60328921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a745b6e6c5a322b0f8f9fdb0199c6e684d2216168f1c6e51c69b762496d2827c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2375856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127b784e6bb930752ebf89a8f28cdb759798d31ec3277205be6138c374a9e873`

```dockerfile
```

-	Layers:
	-	`sha256:be7c52b07f57edd0d2fecb8502396ec92a4a346e36ac3fe49de150a085abd33c`  
		Last Modified: Wed, 02 Oct 2024 01:59:57 GMT  
		Size: 2.4 MB (2365655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a1f51195e21fbeb4af73c836fe04b190ac6084de3ba5b1a28e466dc5d69d7ce`  
		Last Modified: Wed, 02 Oct 2024 01:59:56 GMT  
		Size: 10.2 KB (10201 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ecc509cccb8888ce4ec0e85cda532b8bee8753ca8b8cdd7a1ce4d2022760900a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88323632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02b79d5d114c89396f5a27079d87b04490e91f28d4e558287c3dc2b9bc96550`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
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
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d94077355a21a6aed7229b3a4f17b15ad75c697e32456d1532e05bd334789c9`  
		Last Modified: Wed, 02 Oct 2024 03:51:28 GMT  
		Size: 59.4 MB (59438202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0fa22012449ba949583ec477515015fbd1c28546e65b1dfe7979b9d8fe307c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8fca0f9585485527230b93809a10578020c92e0a33d198e68d051c2d3f5c11d`

```dockerfile
```

-	Layers:
	-	`sha256:397f6da62456441695ea28cd903b283a8578672d53d67ffabc5723be63680a4f`  
		Last Modified: Wed, 02 Oct 2024 03:51:27 GMT  
		Size: 2.4 MB (2366182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a254b6759cafa990302d752a6c559e164fa184a3c4f66a6f67f269b2927f187c`  
		Last Modified: Wed, 02 Oct 2024 03:51:27 GMT  
		Size: 10.4 KB (10358 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f5748e9fdab2f89667ba6d510b4ee4cff9a07d0b82c24c9bfd38a6db72884459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96406280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f19772dfd1146a555d4911a478320cab647e0968bc6a5dab24e1281e94cfe4b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
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
	-	`sha256:02d903566b998a9262d33a607ddfd51e0fd03d28f420fe11f8a2d4fed1eefb53`  
		Last Modified: Mon, 16 Sep 2024 07:36:44 GMT  
		Size: 34.4 MB (34392021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e00b0926ac843aa23ac19cda0a9fc1b2205fc246016560ed4f28ccc167ddf99`  
		Last Modified: Wed, 02 Oct 2024 03:00:32 GMT  
		Size: 62.0 MB (62014259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:47bf01966967524c52204eaad658cc43b0f121d3ed47973c4779a9a7413f5f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5114344e000bc4921a383038a8869d02767fec1655a585e2137fdfa369aec95d`

```dockerfile
```

-	Layers:
	-	`sha256:6e1d02a1c813bed7986a4e1cc95679bc4c0c1a02624e10254964dd11ca95e0c8`  
		Last Modified: Wed, 02 Oct 2024 03:00:30 GMT  
		Size: 2.4 MB (2369622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bad0253bdab53c34848e28e1a4ab2b5bf5b79e892622ac236895d20d32ef2c4`  
		Last Modified: Wed, 02 Oct 2024 03:00:30 GMT  
		Size: 10.3 KB (10269 bytes)  
		MIME: application/vnd.in-toto+json
