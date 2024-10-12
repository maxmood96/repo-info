## `sapmachine:21-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:5f92e806c54d7f17a149acdb58010041c2e6fc3b866d218b0fe4d5261f1a2691
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu-24.04` - linux; amd64

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

### `sapmachine:21-jdk-headless-ubuntu-24.04` - unknown; unknown

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

### `sapmachine:21-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:32568d4cfe3e95c7281053887c87adeeb3ea5af88d7da6ad3f16af07dc945dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241388247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849fd769a4e2f295fef5e4ad6281ff09bc7cf668f9a183d1b081325f2d40b601`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:316c1983efdc3b35f0d98b98d79e53eb75b56cd6a3067c09ff9a8f87ddc3c6cf`  
		Last Modified: Wed, 02 Oct 2024 03:50:45 GMT  
		Size: 212.5 MB (212502817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8e262e927529cde1f960bf58daa1d2e03882cfa86bbf46826b7ae5c31206b45d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2224346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5ac04c0b8590f9c3bbecefefba9c24aae709e1a186ead72b8681b3c6483b01`

```dockerfile
```

-	Layers:
	-	`sha256:202ab4711a270df163c8684a4c1be6d8cc8c28a6e4ef8e243b364bb10ba7700f`  
		Last Modified: Wed, 02 Oct 2024 03:50:40 GMT  
		Size: 2.2 MB (2213785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f49b6e52c34d3407c380c9b1333105c5fcd5e2b4362f81b9e4e5ffa07e92ac90`  
		Last Modified: Wed, 02 Oct 2024 03:50:40 GMT  
		Size: 10.6 KB (10561 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b677cb1f33420323228ccb73fa150276af1f6b951c0cc226b588d836f5d28aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250059690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b7c95060e527b091a93e3166d505e01f8c320b4a7ec686bb75eb44dfb148d4`
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
ADD file:6ec0ebf9a019b7c00b0121b97e89fcad881460415f8dcb9bb94b1cc7f5d0a5bc in / 
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
	-	`sha256:0e110547234fd795b1c6d90b50b5df43ec509107fdf663124acb5e3861c38ef9`  
		Last Modified: Thu, 10 Oct 2024 09:00:03 GMT  
		Size: 34.4 MB (34389412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106b9fc86acfb39c006ef779e0ce055f54cb79574bdfb53b700893eefe3720c1`  
		Last Modified: Sat, 12 Oct 2024 00:31:26 GMT  
		Size: 215.7 MB (215670278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:22688e589e9158e0210c96f95d91a2f40d10ec0af91a76c4769acaa34cbb3150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2226365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84050931c8f610aafb46a13b31634cb99a5224e8d3d1f01689099dadab14b3f`

```dockerfile
```

-	Layers:
	-	`sha256:c1d2d66933bc3c9fef3c1370b56a6e4a2446edf147d3d07c775f8fba813edbc8`  
		Last Modified: Sat, 12 Oct 2024 00:31:20 GMT  
		Size: 2.2 MB (2215861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a340ab8a1992b85ba490f626187a0c9b55806ce074c0ae5bb347c1bbc2fcefa4`  
		Last Modified: Sat, 12 Oct 2024 00:31:20 GMT  
		Size: 10.5 KB (10504 bytes)  
		MIME: application/vnd.in-toto+json
