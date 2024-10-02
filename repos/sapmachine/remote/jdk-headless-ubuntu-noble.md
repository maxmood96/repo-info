## `sapmachine:jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:3730a6b7d850f075238ce35eb2e1ea57567cc6f65b4a84e04f936b9fd3530f96
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
$ docker pull sapmachine@sha256:717785bc72570a8e87c42c0f7ebcee3a9796f0f54eb5776ce476b70ae1f02fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.7 MB (250749391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f46656e293dcda8d97c65a4cd15f291b588af380b4c3e78e11090861c814070`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:30 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:32 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Mon, 16 Sep 2024 06:23:33 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e370ca91f0432663bf9e17f29ed628a7cb1ca41d8554def47c90630f052297`  
		Last Modified: Wed, 02 Oct 2024 02:00:16 GMT  
		Size: 221.0 MB (220999531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8e13893a901e851237d4dca0f9fb7a0c2c0e5e6cef87327eabb619856f24d359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2223415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1931fb15784d3331a6b81ce7790597f04dd51e9e9d99931bbcb5f777f7bd724`

```dockerfile
```

-	Layers:
	-	`sha256:fc8f8e4106ad8359cf39ec3e13f7b44c8e50a76ce991d35a4cd43a9171594884`  
		Last Modified: Wed, 02 Oct 2024 02:00:11 GMT  
		Size: 2.2 MB (2214106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d340eb900327b202adaca876110e13c977cd7ff154c6a72e86879631c707d63`  
		Last Modified: Wed, 02 Oct 2024 02:00:10 GMT  
		Size: 9.3 KB (9309 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a2445037acd557c090100716a7cbf96f233c5c7de7c8060f19db724eec04ec50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 MB (247858884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff16ace72c83f76512bcad85d369ded193b4e984dd33536a65d7eb38d8c48e4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a880cb019fb966d9908b599fb8ff4083feea3120a77506f98b6fb632847467e`  
		Last Modified: Wed, 02 Oct 2024 03:42:57 GMT  
		Size: 219.0 MB (218973454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eec1f511eaa7a876665d03ae53a2f6e884bea55d9ed1b35d9549031c02b08804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2223387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a923e749591a1675a40c61281887fb8d556b8701a32565ac4a999dbcd1e57aeb`

```dockerfile
```

-	Layers:
	-	`sha256:dd30429bbd6d011eda28bc0e13a96e68a094f878de918a938fb161f640ba4733`  
		Last Modified: Wed, 02 Oct 2024 03:42:51 GMT  
		Size: 2.2 MB (2213957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c1e5fe41643780aa8090b82dae458dd0bf3b5707050e58fb8a48ba23a179b5`  
		Last Modified: Wed, 02 Oct 2024 03:42:51 GMT  
		Size: 9.4 KB (9430 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:895194f07247ba21cddc4fb2e8af15ef5bee9cb88f4294288ea2e4eba5ea602f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.3 MB (256298879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f33b3e5f584e08485582acd979c96e46895956ffc8a5cf62ec21f108d4550e4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Sep 2024 06:25:02 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:25:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:25:05 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Mon, 16 Sep 2024 06:25:05 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:02d903566b998a9262d33a607ddfd51e0fd03d28f420fe11f8a2d4fed1eefb53`  
		Last Modified: Mon, 16 Sep 2024 07:36:44 GMT  
		Size: 34.4 MB (34392021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89571d6a97b4b39369f436e091ba49ae35c2418794b42a958e1970aebc853f90`  
		Last Modified: Wed, 02 Oct 2024 02:47:19 GMT  
		Size: 221.9 MB (221906858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1e20f8419d20dd52a8e2efc43745dd588ac8734051866e6c9373d27013ed7fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2224783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6b7aa7f6637763469196c00e94de09049f36c5c437172eb04c7db129b1ac6c`

```dockerfile
```

-	Layers:
	-	`sha256:61b406b18d4ad628fe6c6702483e74ca6ed8e6d22e4efe442d903c9961ea0408`  
		Last Modified: Wed, 02 Oct 2024 02:47:14 GMT  
		Size: 2.2 MB (2215424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:285c8b04831110963562981b4e66bcc9f478fd86754c0296b4f7807748885b56`  
		Last Modified: Wed, 02 Oct 2024 02:47:13 GMT  
		Size: 9.4 KB (9359 bytes)  
		MIME: application/vnd.in-toto+json
