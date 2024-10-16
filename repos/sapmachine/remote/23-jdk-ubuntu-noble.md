## `sapmachine:23-jdk-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:cbfcdcacf8a0723d4b9bd64a0ecae1e4c2d6437e729e843e24cdb7523593835f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-jdk-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:6e3633aa976b630277c2ba2e7dd26d206ee65da49927ada49ddaff7861d84944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251937085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24656c25554f38712f264bf62422f2e2fe6a75fa44c447e0156c94947deaa4cc`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376e6d6f243e7286ce6a14ab744c5db3495e661989cc849c94544198b7ed6bcd`  
		Last Modified: Sat, 12 Oct 2024 00:01:22 GMT  
		Size: 222.2 MB (222186628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b95059d5291c9908210e2582d80728f79e5d676520e4a34e008c6c5c22680be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513bd6077544f001a595933ef93f226fbd99cf5c639801022d9db27a16c293af`

```dockerfile
```

-	Layers:
	-	`sha256:d6401e573861416d56bf20f6e77241aef07aab984cd27d7e6c152ffc23d900be`  
		Last Modified: Sat, 12 Oct 2024 00:01:18 GMT  
		Size: 2.5 MB (2452728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2218201242302e74d03a794a2d638f31398b126e4f9f3b8996bf86df3e2f3722`  
		Last Modified: Sat, 12 Oct 2024 00:01:18 GMT  
		Size: 11.1 KB (11083 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jdk-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c43f7f8b5a110ca0e4277a1ac088ec293036a834c4c271123beaa423d063e58a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249056331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291a0b0cc1d213b4a91155676292f7d1ff5f3e58fc0b6dbb05748e5c3717811a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0741829382faee1dada646b49acf3f4349f0c757e16139b7bb1874c6339d996e`  
		Last Modified: Thu, 10 Oct 2024 08:59:51 GMT  
		Size: 28.9 MB (28885616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2e713c76f8fa2975ba978d30c71f91f45e3f0596777fa049397c4d79982752`  
		Last Modified: Sat, 12 Oct 2024 02:19:07 GMT  
		Size: 220.2 MB (220170715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3cd34130aba4e63e985192b53315157a45e0cba23bd8e31a21661af876573183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faeef75a2b265d16e6d0246b71e68953052c9e7cd4824989b5bb74bda8e9cb76`

```dockerfile
```

-	Layers:
	-	`sha256:0f266c82c48cc9c48194072b21b7cd32aa54c52d0cc849bdbbc5165060115159`  
		Last Modified: Sat, 12 Oct 2024 02:19:02 GMT  
		Size: 2.5 MB (2452660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7023d4ee8cf5a98e556d40dac5818be68a1333ac2e6d8d0f0a47be8ee9ddd99`  
		Last Modified: Sat, 12 Oct 2024 02:19:02 GMT  
		Size: 11.3 KB (11277 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jdk-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:41711d11cd755d90a26d39215691c8c5d127c9a0e8e42054984aefaec4e3c411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257676622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b39fe2c6df46c5b4f5258594b1fa069601fe27431e22a26f9e74aace8d5197`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b978b0803fa06100b7e4e20e42311cfd06abf25c0cfeddd89b728b389f7c75d8`  
		Last Modified: Wed, 16 Oct 2024 02:33:47 GMT  
		Size: 223.3 MB (223287653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6fb9c72a8e3535e3b60d19b024b004460857e7d77e6b096d35eab4127cd9c642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b70cd3dbf5825e251049f06f85cbed830f8175ca9002eaf94792b6a62db3415`

```dockerfile
```

-	Layers:
	-	`sha256:de365a8171cf9dac78784d9b00ff58d33e0468146a0c15677d85d97cd3c33e69`  
		Last Modified: Wed, 16 Oct 2024 02:33:41 GMT  
		Size: 2.5 MB (2454145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6806c8872177de8bc8fbff0c7a5617c53868aaad689f0e3cfbe523b7b1f7759c`  
		Last Modified: Wed, 16 Oct 2024 02:33:41 GMT  
		Size: 11.2 KB (11169 bytes)  
		MIME: application/vnd.in-toto+json
