## `sapmachine:lts-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:dc0d5a30eec10570bb2bef3f39fb73bb8bd49f8137909cd0ee70df7eae2ebe35
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
$ docker pull sapmachine@sha256:ea3c58d0f6d295c696c7ff4ef8bd306daeb0f07d030a94f6d956e086161826fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243646651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e007bd37ef56870891cb165ba98ba04d0e421645943335d17e2ca22275ec7e5c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Thu, 29 May 2025 06:11:31 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7246b3b254f3ac4f9df92f31e6f089196db2464ea0b91a0e3fa118ac6b437dc5`  
		Last Modified: Tue, 03 Jun 2025 04:17:46 GMT  
		Size: 213.9 MB (213931314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:102223788ca610b512e2e9e1c4a84b80895f1328f5455450183ac5c754342cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2266405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec16fb7195bf0fcbe1db55526a9edbe1420f325fe8a5d0daa22fcdeec168fe8f`

```dockerfile
```

-	Layers:
	-	`sha256:5a4c051fa7ebd235c09b95c94a1061ea6d3137de5e474a643e344e15edb5f093`  
		Last Modified: Tue, 03 Jun 2025 04:17:43 GMT  
		Size: 2.3 MB (2255753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:debe9f6e3abc00b9791214879da07c8e22feabba178b3d71b4f33341b36bd41e`  
		Last Modified: Tue, 03 Jun 2025 04:17:43 GMT  
		Size: 10.7 KB (10652 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:714aa49f07b3e323a2e1a9e9192b982bcb69637a842fd40890d145bd6b30d253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241030825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11794acb358a2a2c3e3e91982fb2b8a9bef61f38fe08e88d2e01b1cf2a20a90f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a70af77cdd6169cc3b06e77e571bb6845a80468d07858d51395a99831612ba5`  
		Last Modified: Mon, 05 May 2025 18:32:04 GMT  
		Size: 212.2 MB (212183949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:21fd5c9e4cdc8f78c5ffa183985f279694b25094d0acfbae79120b56747d49ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2245844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e10e80b35b900f10ed9af0080a0aa375b9706ded2f9bf0f7125fcc25e6d71f`

```dockerfile
```

-	Layers:
	-	`sha256:ad7347ef61094efeaae37a7ba09a22156823880308138be11b2a3a8f778cce50`  
		Last Modified: Mon, 05 May 2025 18:31:59 GMT  
		Size: 2.2 MB (2235028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0680dcd1c7715ff11778eeb51267657c68a4858c4c37057cb20ffb902771e8e5`  
		Last Modified: Mon, 05 May 2025 18:31:59 GMT  
		Size: 10.8 KB (10816 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5f39f58cb1915878ea51ae6074e9f4eb6dc5439cbc503c59a2a37f34ae12fa01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.5 MB (249490789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787ef919652dccae23a44a0d8ecacd164b91f1fb079ef4a2c6908f5a852c787c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Mon, 28 Apr 2025 10:54:08 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6ff2cf7edb5502415919fc57f1c74772d9979de015c611cf4a8163c2a507e5`  
		Last Modified: Mon, 05 May 2025 18:24:22 GMT  
		Size: 215.1 MB (215149951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1d0249f9d4ce069836263d49316c7ad3bcd743afc35e4ce9bb7b8845d0feda85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2247195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a35cbf6a0ce8aa0566f2a4fdf93c5997abf566c5b2c58e4a2707f3b4c8d856`

```dockerfile
```

-	Layers:
	-	`sha256:6fa6251783f964876a72f60b5aa5470d760e42543c12eb3ea40ce597cb2bf56a`  
		Last Modified: Mon, 05 May 2025 18:24:17 GMT  
		Size: 2.2 MB (2236469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78ac7549d9abaf332c6d3a00d573de9ce684c8d59962ba25677159973fb9ae5d`  
		Last Modified: Mon, 05 May 2025 18:24:16 GMT  
		Size: 10.7 KB (10726 bytes)  
		MIME: application/vnd.in-toto+json
