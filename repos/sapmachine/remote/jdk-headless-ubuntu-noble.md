## `sapmachine:jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:c83e4922f8fb209df174471ee32f268dd5b9d32d00b47b386974095b589e7f65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:a314ed928574338df6d3a1971b7f826b3d9244fe28b65a8600e200ee699524cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.8 MB (250750704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7703bd616e0bb5df4d8a7faa128ca35f7efed2d365d1a6c1109ac5073394283`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c95017bd0d70cba0a24dbab87a037ec84a2bf24c99da596cdf98a427b8e3199`  
		Last Modified: Sat, 12 Oct 2024 00:01:24 GMT  
		Size: 221.0 MB (221000247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e042b57a53d4b3617f21799ca20cb2adc461e3d71f183985919b03046e254dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2224087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32599cd2b7bc8c96e2b712e9dd774732ff00f413e34cf0237958842153547d1b`

```dockerfile
```

-	Layers:
	-	`sha256:6e9d3cab2726aad190b0ffa4df411dc7cdbd3e7cf0c89c87330b548bfd713293`  
		Last Modified: Sat, 12 Oct 2024 00:01:21 GMT  
		Size: 2.2 MB (2214745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc3c0135b52bd1e5b40fd3c8e17ac9b67ca2b921d793cd4edaa3d6a120ddf7d5`  
		Last Modified: Sat, 12 Oct 2024 00:01:21 GMT  
		Size: 9.3 KB (9342 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0156bb96d379c46f7d2f50f3403bb50191dc6ae5154d9e8c820310766657c449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 MB (247859956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:505bf2054fc24990fa1a475e53bede3f5c2141cd4f08cb3cb4cac04a4ade36dd`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97843d298df57976b1cb5f4a3e1acf2baa50b486d4abe610bedfe0be3af857b8`  
		Last Modified: Wed, 16 Oct 2024 04:19:54 GMT  
		Size: 219.0 MB (218974111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fed4db5e1e5712e7fcae6053540b906c94e334e805a05f26cf6b0c918e2c0ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2224060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f065ca61fce50968db52e90d73c5529bbbc50ea86f770028bea611213c5ac36`

```dockerfile
```

-	Layers:
	-	`sha256:f608aad1087137bb1c660aa617cc52f13ddf71f2d363a46d16e52b42acaf7ae4`  
		Last Modified: Wed, 16 Oct 2024 04:19:49 GMT  
		Size: 2.2 MB (2214596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23b87fbc6d350f664abffc90249851d197b1839bd3d33bd14ff1c749e4ad22b8`  
		Last Modified: Wed, 16 Oct 2024 04:19:49 GMT  
		Size: 9.5 KB (9464 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:2525f73acdff48123a8b41c4cd40cb0d32dbdda9ef15d38e4f758aff5d46f93a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.3 MB (256295751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af9ed9716e2c27e5696b3aa540039d871fe74f4a0e1e94b36f2b632e8f45c97`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0002d1c0c85815b9d2b92868f718993e4880def750a651123f0bf9f85e275b5`  
		Last Modified: Wed, 16 Oct 2024 02:35:18 GMT  
		Size: 221.9 MB (221906782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b591a2a57aa5d2d0248704d34b24c8126eeb9ba6c3eb7051ef091b4ed68484b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2225455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a3259b6f340e5e724b820b1c121f73d041d2377b375d74244d499849438167`

```dockerfile
```

-	Layers:
	-	`sha256:93547547939b4a9d5d78a5ccc55b21341c5585fb9a2a2c7ac2381ab4d0bd558e`  
		Last Modified: Wed, 16 Oct 2024 02:35:12 GMT  
		Size: 2.2 MB (2216063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6fb900b3c4686b263b4553514487b1e432848ae6073cd43f3f6bc2a82cfe4f0`  
		Last Modified: Wed, 16 Oct 2024 02:35:12 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.in-toto+json
