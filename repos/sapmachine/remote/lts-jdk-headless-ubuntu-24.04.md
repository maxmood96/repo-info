## `sapmachine:lts-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:1c77cebfd7b312df7ec5b59bc99e039881b82925a80a2f14077cd59bf8fbd2fb
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
$ docker pull sapmachine@sha256:32668240a03d85ff9f0dd9f42ac78329e61b1d0fbd7d1d7bb03f1c9a9df1c0ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243646456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea0fac7133760a95529e818ec495a6bdfd4f0ee3cb28f4cab4c9dc0327d359c`
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
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
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
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4930444abd1473cdeac620ddc7db6babeeabcf83e790b7ffff4fec104d6c30d1`  
		Last Modified: Wed, 02 Jul 2025 03:12:52 GMT  
		Size: 213.9 MB (213928090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2d67460fd9b5670ffe30477cb3a21e5ef7ed89abcf0e326847e246bcbc0e58bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2367357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e6dc61bb19b87074948cd16ce41492c2a678174b6ae95a56a2e87f7373abac`

```dockerfile
```

-	Layers:
	-	`sha256:06e9ee41ca466d031141d99d6128184ac7deba67fa93f949b9e9afdd6fec38da`  
		Last Modified: Wed, 02 Jul 2025 06:07:23 GMT  
		Size: 2.4 MB (2356705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ba7fef85e2727dfb09d9b4d5b7f646b2ae86ca6ad45e4baf972d1d09fcd4316`  
		Last Modified: Wed, 02 Jul 2025 06:07:23 GMT  
		Size: 10.7 KB (10652 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:cf9019aa82932b512818fef2f29935de5605357ab8ad52b1aae57fb7409f7f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241036621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558ebd1352d8aaf4f8a268d95786fd70a9f398f3eaa4142031c21252c3d6a022`
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
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
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
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5e3bc27e3b8e44a231b4fd09b5ddc0f69ac162e2e94f3fbb9609955987d3e4`  
		Last Modified: Sat, 07 Jun 2025 16:19:29 GMT  
		Size: 212.2 MB (212184722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6d1115e3f810d67689e7bd365f277dbfb334d18392016cf30ab292e002a1ac85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2267088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247380f8bdf4ef58be651acd512f322d7cd7ca661e0aa11759660ec9be22059c`

```dockerfile
```

-	Layers:
	-	`sha256:425701167cc365d188dc3afec18f8fdd62a16a3f9fed77f40bf90c757580ac9a`  
		Last Modified: Tue, 24 Jun 2025 16:58:10 GMT  
		Size: 2.3 MB (2256272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64b00321e25339bb2182af5aed5aec5b488a71dce0b78127ef3a5feb6fdde0f8`  
		Last Modified: Tue, 24 Jun 2025 16:57:57 GMT  
		Size: 10.8 KB (10816 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:325b44b9db8f3f073e68b1cef2100f43e884b040dad5114c2fdd03a68bfc46d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.5 MB (249460297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6a0649aec6040d3a79a38d6ae6ed9d62b1cbdff2785de893b3787eebd1dd17`
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
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
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
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044b6b42ec136e7f567924ca5a2363385cb7de0e1b77b0573d59874ae0a979d9`  
		Last Modified: Wed, 02 Jul 2025 04:48:53 GMT  
		Size: 215.1 MB (215138791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2aefc3bc3c32bc5a8bcc30cad8070e8fd120acb8edc7a28c3c90a8d8d6032589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2369507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f430e4ca9021e53c6b9a3e55bb954c10d6e1439d8d56958aae8c43fc086a887f`

```dockerfile
```

-	Layers:
	-	`sha256:0e4e71c06d96bccb170e3519c03b4c8e4907a96027b85b39f742a5793e13405c`  
		Last Modified: Wed, 02 Jul 2025 06:07:33 GMT  
		Size: 2.4 MB (2358781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a780f3aa484c33a6bd073854466da1af372122c7f221c16b2273353e17639654`  
		Last Modified: Wed, 02 Jul 2025 06:07:34 GMT  
		Size: 10.7 KB (10726 bytes)  
		MIME: application/vnd.in-toto+json
