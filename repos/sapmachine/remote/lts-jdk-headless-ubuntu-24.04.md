## `sapmachine:lts-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:416d4254ce8aec9e49245953be5f897656712f019d98ee597ef809c10f2cb301
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:031e6a6a49fa9ba309d77a0598e2193ea1d553a3a5083340bb649a385e763907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244153990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e84e22284e9b1d6109efd1ca548b3491f5bb7d84ac3b1180bf26bde05a2a8d9`
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
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
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
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a21f80e7891b051700206d8d6a7e0513fc24290e90568264ff678499da02a64`  
		Last Modified: Sat, 12 Oct 2024 00:01:39 GMT  
		Size: 214.4 MB (214403533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5c2f072c6a038d5dc630e9c2a87431e16b32afffae1a51256099b5ee34b70251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2224342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d064df970f1baf49423e2d99a0c1fbba408960741db8dc2b1533e6fede2b441c`

```dockerfile
```

-	Layers:
	-	`sha256:8378a9daff3da0823078a195338dc622f99013eb4595bbeecf51e7a136e82b65`  
		Last Modified: Sat, 12 Oct 2024 00:01:34 GMT  
		Size: 2.2 MB (2213906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bab452b27aaebac699a9428bc51193384f3deedb2fb6d3ff7f6504a3584a7ef3`  
		Last Modified: Sat, 12 Oct 2024 00:01:33 GMT  
		Size: 10.4 KB (10436 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d83818b13d5db067f7812e3b0896587edd936db03abdf816b9bd6f45ceeeab02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241388789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d8e4e807c608f7962c106fe00a1da4fb655a99597a62e47028dfd9ecac1d63`
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
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
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
	-	`sha256:0741829382faee1dada646b49acf3f4349f0c757e16139b7bb1874c6339d996e`  
		Last Modified: Thu, 10 Oct 2024 08:59:51 GMT  
		Size: 28.9 MB (28885616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3d8d643ddec79fdf63b7f4560b56f4ef822827667c1d092f40306006c4dbfd`  
		Last Modified: Sat, 12 Oct 2024 02:23:43 GMT  
		Size: 212.5 MB (212503173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:80c045ff3de72327002d2b65b9484da4ea3493666836f0a776dce95f566bd81f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2225017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b272ef2c91cf99d9d99a11206a3fbe5349d2f2fa06f4144034f32b58813b956`

```dockerfile
```

-	Layers:
	-	`sha256:54b4f4effefde809301a09408df85597f9538efa9cb7af9c8da7671c63fe123c`  
		Last Modified: Sat, 12 Oct 2024 02:23:38 GMT  
		Size: 2.2 MB (2214424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f53a748ee88498b11fbbc033c53c95cb1077848b56f81f1b9568d674b48935e`  
		Last Modified: Sat, 12 Oct 2024 02:23:38 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-24.04` - linux; ppc64le

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

### `sapmachine:lts-jdk-headless-ubuntu-24.04` - unknown; unknown

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
