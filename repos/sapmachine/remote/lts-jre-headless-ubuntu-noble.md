## `sapmachine:lts-jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:432be8858b5b8c617f618fea2a228ddba5f4eb64c152ada2818c075736e862eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:4b06b079e58c617ed5433316cd3e4bb8113c0be5401257251efe629f83c5993e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97506382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e1b6c4f6f7834d2185a7566149731cfb5bd4494af384b41f4aedbf99a82a2f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc244670a19828abd2fe5012ee1c8a3e4842093a67681374431201f82962414b`  
		Last Modified: Wed, 17 Sep 2025 17:34:57 GMT  
		Size: 67.8 MB (67782932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:04339a3c1730ed6136ea247aa7efd466f01a6f1504d98f7e1eae1264d18e0538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa697eda2d3b0a83b5a48d55950194873618f8f89d6ea9fbe736606fa8e910aa`

```dockerfile
```

-	Layers:
	-	`sha256:b36d3a2d5b52645b6b37456734921ecb53c6423bfcb239b001d860d1982b120e`  
		Last Modified: Wed, 17 Sep 2025 21:11:45 GMT  
		Size: 2.3 MB (2280858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd7ef1ca608c6f651b15b935e7a8bec1f426797a0c58587a5bfa9d3c6ebc65df`  
		Last Modified: Wed, 17 Sep 2025 21:11:46 GMT  
		Size: 11.2 KB (11239 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:97089c5266230e6adade08d27ac5830aa91a00a8713981bc2f8fd426e9cf2059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95626557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df61374d3d828ea356c536a064e064a46ceef53d2b84c416c879eda9e769bf23`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbaaa1de5d20402b3276e2cf33facc7de7e6e05679c84de954343e88f1fb46a`  
		Last Modified: Wed, 17 Sep 2025 17:37:01 GMT  
		Size: 66.8 MB (66765240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e9de89f9c95d97dd91999ec785f6c7e4d53aed2892b8f30f62c7cce61e568d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a8482ce4c2dfd79216ece3f26c7f42ec52f2f43ebef9a3641e7b8169db70ac`

```dockerfile
```

-	Layers:
	-	`sha256:9707d3c143a12035b39ef2e335fb54d6a318bfe08f6d71d6e7dab1c9d857821d`  
		Last Modified: Wed, 17 Sep 2025 21:11:50 GMT  
		Size: 2.3 MB (2281398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f2c7da609a7dcf782b550873414af03de6300e3a2bd4d05b419bdeb88123a29`  
		Last Modified: Wed, 17 Sep 2025 21:11:51 GMT  
		Size: 11.4 KB (11425 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:09587e763a3fd3b38694ad2aec62ad3f55af555d6a6ad0397cc59141e61f8dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102834200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71172e83cdcfe5d387720b46269d325568fea5b25a7543888f99c20aa3fca1b9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:44:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:44:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:44:36 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Wed, 10 Sep 2025 05:44:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e2f71866f49ebbe3b3e806af4bf78e06d0e2d16b7267d8fc90d3675ebae245`  
		Last Modified: Wed, 17 Sep 2025 17:42:44 GMT  
		Size: 68.5 MB (68531073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:edac01a014615ced2e2417a98dd76610927a241dee5f2f0523d98fb793bfe1d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2289571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b486c58e27912bab23cfe201b465be7611436c42c3339f0613113255cdac2513`

```dockerfile
```

-	Layers:
	-	`sha256:c88e86f78b63396d2cdb257f84788b32979a3499d5a1bcec1129599aae34de0f`  
		Last Modified: Wed, 17 Sep 2025 21:11:54 GMT  
		Size: 2.3 MB (2278246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d017fe7ad171ac96826514c3e991a23d23937eb53b54aaeb82983b50ca006641`  
		Last Modified: Wed, 17 Sep 2025 21:11:55 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json
