## `sapmachine:21-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:6ae6654a1d531d818697120759cb8f45bfb934f44452646b7569f62c891def0c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:e8991f93306cae05ec5c281c5a0f479c0603b81d14bdac4e0b243fe9d8d58f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88166505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e130e0bb6c3e3a0652c7b226dacc51e2dea86ce6804bed46e4fb322f95d8e536`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:38:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:38:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 13 Nov 2025 23:38:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23df7f5ff00c99cab3800f7b102edb2e3eb681c375ca356b896186b85881ac30`  
		Last Modified: Thu, 13 Nov 2025 23:39:22 GMT  
		Size: 58.6 MB (58629707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:af413e0d87a9ed72c28e67dfa771b10058c6f2edb100f463e203f34bff0a0012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9ba9c05b6017fc8bf9973316d939f0dcb4ed1988fcc492ddf24ffd6c278655`

```dockerfile
```

-	Layers:
	-	`sha256:e432c1942a8eae264f8337aa432e4a96a3408044b5e7a766c2032c86e987d99b`  
		Last Modified: Fri, 14 Nov 2025 01:10:33 GMT  
		Size: 2.3 MB (2294109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:875695a4c87adbdf5c337d1b1dfac59481fe4d5f1862043a691c161b9c2b0bbe`  
		Last Modified: Fri, 14 Nov 2025 01:10:34 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2e49030a64ddfd1637e5391400a0ef7b5617789aa0b57464bfa1e8e77134390e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85155985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25e6ccd1365706cced252693fe7e6a237c6d1200afe9b008a54faaeafdbf5c5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:38:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:38:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 13 Nov 2025 23:38:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3be747c25e8708056c38bbbe6ba45b83f6e49712febe774362da5c06cf4d95`  
		Last Modified: Thu, 13 Nov 2025 23:38:40 GMT  
		Size: 57.8 MB (57772108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ba1298f43c241967ef96fdc55aad931254b96aa15886ab61c7355c22f6b86418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9076e98b4dc830f4633c8f5a4fc45b27230c9276caca37fb1457b2772bae11d`

```dockerfile
```

-	Layers:
	-	`sha256:564c14396cc1153f9ae20d5cadfe23ddf20d5c40a5134f4a299da6bc32b03945`  
		Last Modified: Fri, 14 Nov 2025 01:10:38 GMT  
		Size: 2.3 MB (2293781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9af2313964fe4b6d2ab838b204476780e3cbbe10951e36d964a3ee9bb97ff4b`  
		Last Modified: Fri, 14 Nov 2025 01:10:38 GMT  
		Size: 9.0 KB (8983 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ced455ae8ad1c140e03f24137c549aa92e9b5b570b3a95d98c7c525db949c923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94019371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4d2a2814e9e8e5133d7db7ffaeb7fa0a26f485862c55cb4df6cf6fbdc9d82c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 07:06:37 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:06:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:06:42 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 01 Oct 2025 07:06:43 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5cbd366ff386192f0a2da5f5e6eca6e6f50d5c9e52029d908f56876ee0749f`  
		Last Modified: Wed, 22 Oct 2025 12:01:39 GMT  
		Size: 59.6 MB (59572582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d6de4f4f8471df3dcc4859eddd70ef49a6c55a058a09709dc913aee5db612777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832af92f2220300a76a0b6a2f4dbc50d3ccdfdf7641c8c2148218393bc962c54`

```dockerfile
```

-	Layers:
	-	`sha256:f80fd3ec5bfe6c86a68803f63fad6199f466721af13c77439d77d6364edcf1e7`  
		Last Modified: Wed, 22 Oct 2025 15:08:14 GMT  
		Size: 2.3 MB (2292134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c87d858c0b4d56ce1aaccca833e92a1dc095f99914f6c3a658b885bb306a1c81`  
		Last Modified: Wed, 22 Oct 2025 15:08:15 GMT  
		Size: 9.0 KB (8967 bytes)  
		MIME: application/vnd.in-toto+json
