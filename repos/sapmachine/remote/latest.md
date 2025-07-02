## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:a6565751b9f9844f9b27929060983a4d9829f73ed3b307dfb431fc1d1132bac2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:f5294f94c240981b73861f7181c9c2bc8a8c1af3e28d63fe4f92a3f0f618ee4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262145387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f66801ddce3cc42de27e7d0f48b4139422ae8153d0fa27915a29efc498f96be`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efac1039d1e2555cc9f0d9d9247db11581ba7624d284fe94446a2a8f5243270`  
		Last Modified: Wed, 02 Jul 2025 05:12:49 GMT  
		Size: 232.4 MB (232427021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:latest` - unknown; unknown

```console
$ docker pull sapmachine@sha256:662d771ef7b6d1ba34d53f4cb3867af22800f3d28717984e9543848e9e798e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2609354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714835dacd7853be24fc1a4eab2bc7653feb12afa5f8b0b5ab156bf9083397d5`

```dockerfile
```

-	Layers:
	-	`sha256:01675690dc0e4e0da28961358e9294c1e39c1ba8c11cf4a5cd33ca3d3af9b9f6`  
		Last Modified: Wed, 02 Jul 2025 06:09:12 GMT  
		Size: 2.6 MB (2596069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf81fc3611f485629e909cd5740231a8a1ea9ef3aef29065eef93cb6be802242`  
		Last Modified: Wed, 02 Jul 2025 06:09:13 GMT  
		Size: 13.3 KB (13285 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:latest` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9d8da46b6f0a36f8eaf74c5d3d2ce0e82f21d5f1ad46e47c6e1c6bb280a2562d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259212316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73520ab42db68440cc31efeccecd8718ba2c72f13b3a596115123e169756cec8`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774d3a6234a70719b14242ec6746abbc91d4d06f6f1036f09ac21cb7abf06b51`  
		Last Modified: Tue, 03 Jun 2025 16:47:36 GMT  
		Size: 230.4 MB (230360417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:latest` - unknown; unknown

```console
$ docker pull sapmachine@sha256:80e530fc415f5647f14249dd2ea6bb7aa0d30cfbe63a3886028aa50384bac1a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9abc99f60eb66617d0de7fc5d2ce38e7250a3b68d28544e544937ab71b9ffac8`

```dockerfile
```

-	Layers:
	-	`sha256:791b3f5a1282abe6b6cb27af21f0746932e251bd4ec33a9edf9e54bdaea2fbee`  
		Last Modified: Mon, 09 Jun 2025 22:07:40 GMT  
		Size: 2.5 MB (2489744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f051c01d8d0c77a92008ef146e910b28fdb90169bbaf0b9569f1d551ab9db76a`  
		Last Modified: Mon, 09 Jun 2025 22:07:39 GMT  
		Size: 13.6 KB (13557 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:latest` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:db0e3b37a27c70017e27cf125a8effd3b5250ff9bcb28b8c6dc91f1713be5e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.1 MB (268079561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be27933a9bbfd6cc5c8c43440253017808516dc94e978dd5a833acf7eaecae02`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0ee2ad4851a2865bf2427f712dc71191e5619527646a7b6b65f7a76ecb4289`  
		Last Modified: Wed, 02 Jul 2025 04:36:20 GMT  
		Size: 233.8 MB (233758055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:latest` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1dcfd1a2bd25aaa659a1fe1fd85637a45ee99607ab16cac50adf36f27f72c3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2611075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79638b4a059c0b6216f08218ebdfc9b8530b5e05eae619d36cf6c907621e876`

```dockerfile
```

-	Layers:
	-	`sha256:33c2bed13d376ecd03573b1935bb594235f3f2c4f4ff9849b1d67ea128f4c8d6`  
		Last Modified: Wed, 02 Jul 2025 06:09:23 GMT  
		Size: 2.6 MB (2597662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b612f418203c7043ca8f0dd0156274062a81a1c03110eec748eb82b1b9205cca`  
		Last Modified: Wed, 02 Jul 2025 06:09:23 GMT  
		Size: 13.4 KB (13413 bytes)  
		MIME: application/vnd.in-toto+json
