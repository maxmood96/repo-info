## `sapmachine:21-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:5ce72dc8b3e031a22b628c12361a6b1bc45353a923e94f5506dd8f6f9ec8864f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:ae1aee9a151c3c4e4350b36bc4e87655a7eb7b01c5c14d7c8ee45e955b0a9aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244153957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f06647f01283f1d32bba7f8afe75a7bb0537d522575b0d8c480c09006d04d4`
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
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea79825c6c26ec452f663131ee54ba8d6d1d81d83c6afba88d6099a8e281e343`  
		Last Modified: Wed, 16 Oct 2024 16:18:04 GMT  
		Size: 214.4 MB (214403594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:deb838f61cb4cd73401703734b9db06d4abbfeb15d014cbfcfeb4a92fa1527c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2224342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01836c1449d329ef256aeea28f1a3fb99c0dd187e31b42ed864f45bcff0b6af3`

```dockerfile
```

-	Layers:
	-	`sha256:668dc0ec4fab67f1dbaf3497c2eaa3957f7235c81f780288088fd2200bb35299`  
		Last Modified: Wed, 16 Oct 2024 16:18:01 GMT  
		Size: 2.2 MB (2213906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0d417c73e83c791d2308a43fbf508f6537c55937fa83867ac8af81563ed4317`  
		Last Modified: Wed, 16 Oct 2024 16:18:00 GMT  
		Size: 10.4 KB (10436 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0de0f985db533c56607702fd99c30762f472c6268b479c09ba555e91cbd1c0e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241389027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00fc2411e82d23e989f67c4e94f5870109603cc4af0f8cd35d7d45b7210b651a`
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
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916bde35d18170650c3252e80a617f61fb31505cdaa6a69862fc3f871141416f`  
		Last Modified: Wed, 16 Oct 2024 04:30:13 GMT  
		Size: 212.5 MB (212503182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d80ae2a168e6181039cf3ba7c853f1ae56dbcc7a19996f930b388f557ea191d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2225018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b511ae2ce91e97d060ceb201130bf30bf49317967f2796663b389badfa26743c`

```dockerfile
```

-	Layers:
	-	`sha256:973c5c88017e8eaafee6e2e1ec193c54467a67080d8d40db67e9ee49da031135`  
		Last Modified: Wed, 16 Oct 2024 04:30:08 GMT  
		Size: 2.2 MB (2214424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2b1bca90a55c0b5cedf2894bf3a6bc3ffbd9ffeef6848203087da827551a080`  
		Last Modified: Wed, 16 Oct 2024 04:30:08 GMT  
		Size: 10.6 KB (10594 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:684806249ee537d05cbaeb5f5876bca26a41a1e032b46f8b28ffcb1a1d6909db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250058982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0326fd5eb771ef7fd0b0a5f305d81dc190d4255e929316ed9a3acf8e17b702cf`
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
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f219856635d97e2e6f3d2196bd129bb1a066dd977bcb7d3caca3bc968e87cd83`  
		Last Modified: Wed, 16 Oct 2024 02:46:57 GMT  
		Size: 215.7 MB (215670013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d5b68ba4c3f4708b060a7753f2152f2771a51ca9d5b31a37e7c24a3ac5c97ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2226365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b2f31c0ec3b5ae581025a60b097eca8724b3a36e6783802ea67418080e3894`

```dockerfile
```

-	Layers:
	-	`sha256:e6bfce2227c4544df6f1e4c69e35a2205cf0b0e673e4b1919b0fd550de332e11`  
		Last Modified: Wed, 16 Oct 2024 02:46:52 GMT  
		Size: 2.2 MB (2215861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c415790a59ee498b511b7e539d167b3e57f62d6e06fd5e7259b9cae33c26d7a8`  
		Last Modified: Wed, 16 Oct 2024 02:46:51 GMT  
		Size: 10.5 KB (10504 bytes)  
		MIME: application/vnd.in-toto+json
