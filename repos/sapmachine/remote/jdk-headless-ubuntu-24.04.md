## `sapmachine:jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:bfff72ddf0015eebceda380707ab496a96d90a4a721c885b812cf4794942d1ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:dc4b4ada8708d1e9522388d880c528fe3d6cbf40a2165f9df88963cb3ecc709c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (260974545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21d5de2e6d00595e97b9f452b518da49ce77ddc99f1bd5515962dcb0a89a1c5`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b5fb71752b8d3ea51eb621b7b218863f50b9de62c9b3b4692a4cb83bed693622`  
		Last Modified: Wed, 02 Jul 2025 07:21:48 GMT  
		Size: 231.3 MB (231256179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e68462b6f6496cdeaecc13135c37afa0e6c2baf09b71a4cdaebf84b5bfe3aa4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2358035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50190653233e8ff2cc7a08be8068c12c8834fd3cf1cefb0cc64dbb857347727`

```dockerfile
```

-	Layers:
	-	`sha256:68651857022b664d145fd28cbb9e8ef524c45a2c5a7a13867dbaccfb80defd1d`  
		Last Modified: Wed, 02 Jul 2025 06:09:20 GMT  
		Size: 2.3 MB (2347407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd86e38ec73af4615a77821474d869873f739b682a962bfe3d60fa89100e7e86`  
		Last Modified: Wed, 02 Jul 2025 06:09:21 GMT  
		Size: 10.6 KB (10628 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ed883763b1c0916969353b729eeca442b69292dcc3528f13e5bd8e0822abcf05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (258017790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2539f0368b5736beda24acb7610c2dd6e09763639c5df6f840048ff617be08`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:9f841730254c0144a4d324cb687d900a3137e4f6e06cee3ed80253ce07368d97`  
		Last Modified: Sat, 07 Jun 2025 16:55:13 GMT  
		Size: 229.2 MB (229165891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:db302eea61323276b0fd26c699e96c9ed0976993c34d6ea3d4b343868ecda54e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d46be0f24785c1df093c87071841f9b97ed36b9d8db33ecb58629a26ca07426`

```dockerfile
```

-	Layers:
	-	`sha256:5308a683700426c1bafd4bca16b9bf0d3e19686896a92b1dd018a9856e1a17ce`  
		Last Modified: Wed, 02 Jul 2025 06:09:25 GMT  
		Size: 2.2 MB (2246971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27bb83e00e81489ad1ef82b521d74dcc4c5af98b344143ed4380aa1ff69b4769`  
		Last Modified: Wed, 02 Jul 2025 06:09:26 GMT  
		Size: 10.8 KB (10792 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ab9ca0c2271693eff4f59347c7ac21c0a43169883f3df566a1df906aba3167d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266688562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e0aebe8c9c5d0ae78be83b34878fcda89bf5b1f00edec63db674fe33b91213`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:c4c012d1050ccce4f9a2d6050236e979b70c2eef0806607d934c93a21dc7c392`  
		Last Modified: Wed, 02 Jul 2025 04:37:46 GMT  
		Size: 232.4 MB (232367056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:750117144d8ee148d37a5804155f4d9a41a21369619f28e0ee13171fdc322963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2359567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae52d8dcffc7789418362cdf2dfb83febe833ad6aa21e1c416aafa1da2c3ed0`

```dockerfile
```

-	Layers:
	-	`sha256:491c94a323dfb39e555136c85bf1e1104c38bd097cdcc20db027289b52dbd977`  
		Last Modified: Wed, 02 Jul 2025 06:09:30 GMT  
		Size: 2.3 MB (2348865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3da3c02b1c5cea58e5e832142b2e045236d21c848a908a45152f64f0fb1082cf`  
		Last Modified: Wed, 02 Jul 2025 06:09:30 GMT  
		Size: 10.7 KB (10702 bytes)  
		MIME: application/vnd.in-toto+json
