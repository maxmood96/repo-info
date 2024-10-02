## `sapmachine:23-jre-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:00980f7d67e25bd34fbc97bb1563b9957fe27a4e0c99605957b338ce87d9e714
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-jre-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:f87635bce1b73bf8447faeee62ea01a59acad474316e7522053cbc9a158a76d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86427379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72be06588320152cfaa88f6f4c8b323475f4c33b2a98637f55729776173edc8e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1bf1fba39dadc6157a6e4d08656c8c23fa08b4c97452d518f0e9b27d2e5976`  
		Last Modified: Wed, 02 Oct 2024 01:59:50 GMT  
		Size: 58.9 MB (58916327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a48d06eff5001f33cec562bd4a5038fca81fbcdedeebaca6ded3da4a97447e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2291312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eeb4f0905a056ae29ca1bab24525aff7a982c33c8aade8a8b21806b9e9ebedd`

```dockerfile
```

-	Layers:
	-	`sha256:2831794715e2211e326edfe26c682220ab9ae7417ecab267c499293ff7525613`  
		Last Modified: Wed, 02 Oct 2024 01:59:49 GMT  
		Size: 2.3 MB (2282785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd789940d7ea2a4159d7fb89322ef613947424578a88f2b0f9b14cece7135ae5`  
		Last Modified: Wed, 02 Oct 2024 01:59:49 GMT  
		Size: 8.5 KB (8527 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:36212afb7fe279d50feb6b895b17fb8384902165ece21e6e7cffb50f5b3183c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83921922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88140c93b0d5dbd53e4dcc3080e9772215e146fea1909ae6c647ce16b9c428de`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696c4ab6d11a6cebde5411e4e4238a5a01489c38620239d15cb2ed40984c3467`  
		Last Modified: Wed, 02 Oct 2024 03:47:47 GMT  
		Size: 57.9 MB (57948330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:309e157af4d2f3a01e11d81a21de5c34db556165ffabbf5aa6b9834b5b0e90ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2290415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6157cf6720c054ae69e0fb83d4b4982bd5ba973a99cb35464b851835124a1c`

```dockerfile
```

-	Layers:
	-	`sha256:b76661d03b685942f614ad0acd0fe21f405d5f922efc37de78384f83b13b8932`  
		Last Modified: Wed, 02 Oct 2024 03:47:45 GMT  
		Size: 2.3 MB (2281790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd443cfbc7c3abe63f57cd9762abd6aee9b7b571e68a5576566de70c90f636de`  
		Last Modified: Wed, 02 Oct 2024 03:47:45 GMT  
		Size: 8.6 KB (8625 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3a6fff4a8d5ad44ed99064dd9885e9e49ec691d46c1d01ffe80543aa6582e713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92011534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2184dc7b104d744ba8744d3da4866690377e8f5fc9e1e673836aae3998bb9b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:24 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:28 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Wed, 18 Sep 2024 04:19:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cafd57629abc05d597016161b87b83b544a17d39d1016cfb289a60295fc7d492`  
		Last Modified: Wed, 18 Sep 2024 05:32:58 GMT  
		Size: 32.1 MB (32076334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c015faff47c1aa4991497a1d1cdf8f112eb66f82224945dc10a782226ff778b8`  
		Last Modified: Wed, 02 Oct 2024 02:54:48 GMT  
		Size: 59.9 MB (59935200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:239fd703e0b950561ba220d4b68cfc1e0d6cdb4342c9d74cd5842cf1935c464d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0cf5f760d19b8b6c5f9936305ed6c9a9e6eb3de28ba560166b6af0983d5f949`

```dockerfile
```

-	Layers:
	-	`sha256:3a3e8b5e1ed915e70d9260ada095d9e46adab50bf600cbad9cb51bef474cf3bc`  
		Last Modified: Wed, 02 Oct 2024 02:54:46 GMT  
		Size: 2.3 MB (2285919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05ecfbff6c999efb33a62aee9119dccac2106d77f5a883b04cf36da9b0b5e9a`  
		Last Modified: Wed, 02 Oct 2024 02:54:46 GMT  
		Size: 8.6 KB (8565 bytes)  
		MIME: application/vnd.in-toto+json
