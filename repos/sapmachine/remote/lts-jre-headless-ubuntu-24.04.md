## `sapmachine:lts-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:11a92d9c25cf77af750b142a99e7504dc6b30a44ee5bc8026a2dc7f67b2bd10a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:685c18170a2dfa588e26d522f06beec38c5fd7f1ee8934623b0f80d20bfad14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88647485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e96da3494974f4fdf3cbaf6ed2f05a50e52cee96dbe21feb3837f89cab24bb`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:157d7f00da4c06058c773d4bac8adf8c6bf4330b21e2898ce92343e4fa58a16a`  
		Last Modified: Wed, 02 Jul 2025 06:55:25 GMT  
		Size: 58.9 MB (58929119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:081c36d4f2688d8c25018843d4475338365177c8b5070a2b1925e8401e3539c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d869d15e375bdfec8f6df87674299aac9e1d147b7da6e9d26c7d779220ddeb`

```dockerfile
```

-	Layers:
	-	`sha256:67f9467d2f47a389955881db7c51c3a561822a63a48dedcd279e08d85446992b`  
		Last Modified: Wed, 02 Jul 2025 06:07:51 GMT  
		Size: 2.3 MB (2273184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb630e2262afa73aee4152e06b4cf01eec19850387d9881784aaa9233ce58314`  
		Last Modified: Wed, 02 Jul 2025 06:07:52 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2377058a1c82c3ca887189d0ad2f56e7f12f69cdf53b3656f9cc4481b3b41787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86968244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e702096391a31d56cb4c8f6005ba56ef81600d06ddfd50434cf8ecadef51923`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:39b33e9bf4f386ecdfebfc3db4a7dd1176d41cab2c99ebc5d0393a494e9c1494`  
		Last Modified: Sat, 07 Jun 2025 16:10:58 GMT  
		Size: 58.1 MB (58116345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a9959808b6c1cb4a2f5a61b529c05f4c14e8a5f66d4e7a11b0e5cdf5aa380804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2183566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb069b4b856a8f8554830dd18b1c8ebb45d19ccaa3a4e12dd00bbd9ea4c6672`

```dockerfile
```

-	Layers:
	-	`sha256:846801ccfa885b2401e26233f775b19681f1a404620b7bca2ffe366820c9f16b`  
		Last Modified: Tue, 24 Jun 2025 17:35:54 GMT  
		Size: 2.2 MB (2172751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:019e1f6b2dd4e45b21ab1276f36afc67420bc8c5c0d6c0d4767e83ea50251265`  
		Last Modified: Tue, 24 Jun 2025 17:35:53 GMT  
		Size: 10.8 KB (10815 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c4998035f3b15abc2fa2ee3a77a00569cb7ace9847df74fbfd680d2a68d44764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94738198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd791a241141fd3134388b2da807ecb127733150d6fad4aa5f0a71530894228`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:749f4951e794f690b54ce8d36c1157dfbd78f78c265c8f0293247e9ff46359ea`  
		Last Modified: Wed, 02 Jul 2025 04:51:13 GMT  
		Size: 60.4 MB (60416692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:95e9ed677b0937315fb28531c99d7ecfbd7f92c60af7fb5ef78110230927d1df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2287931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbecbe3ba662c84f2528b18c76c274d614503bece9ea05f58f29e4ea1dcee6e`

```dockerfile
```

-	Layers:
	-	`sha256:98a79a5d786ee35dea6b968f7beb6a7727772a31521b3b3c6d6758e3c84d9893`  
		Last Modified: Wed, 02 Jul 2025 06:08:01 GMT  
		Size: 2.3 MB (2277206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91dca2ef7679b0360c666b1a0c99fc2d47b04aad32966a1e6bc0bc32091777a0`  
		Last Modified: Wed, 02 Jul 2025 06:08:02 GMT  
		Size: 10.7 KB (10725 bytes)  
		MIME: application/vnd.in-toto+json
