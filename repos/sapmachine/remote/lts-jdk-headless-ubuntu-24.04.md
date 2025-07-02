## `sapmachine:lts-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:f5842a21b1efc4a2388cd8d5b381940a569b58c032ba87c311ed91f9422089b0
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
		Last Modified: Wed, 02 Jul 2025 08:55:09 GMT  
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
$ docker pull sapmachine@sha256:7a0f12b05f74123d812852ec63b81762ba0b8210fa957b79f74b059860e67051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241037614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504c76c4b70b941ba7f70fc4e0e20a45eb6c18e582fe16d7f0d50921b487d5a9`
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
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
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
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ac0d9348d479f8fc68b6ff3a06a24eeeba6a61d6eb2437e11fb5e6e7ab0863`  
		Last Modified: Wed, 02 Jul 2025 06:39:19 GMT  
		Size: 212.2 MB (212181596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2bd8baf7a655db3bb23bbdba27b13c4a6c98f1ae31b0ae4d92cc11ec6c74fbde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2368039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f900470332c07e30c760b9c114dcf25c8e52b8dd9a7610bc1031a579e22bdfa`

```dockerfile
```

-	Layers:
	-	`sha256:f606242cd9ea1ac52dfc3159ff0265b81eebd980ac22685647bbb8d4ee794113`  
		Last Modified: Wed, 02 Jul 2025 09:06:26 GMT  
		Size: 2.4 MB (2357224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc39e5179c0c2019511c37b94dbcf0d3da4176d9807b266ad27e1a7eb8bb935d`  
		Last Modified: Wed, 02 Jul 2025 09:06:27 GMT  
		Size: 10.8 KB (10815 bytes)  
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
