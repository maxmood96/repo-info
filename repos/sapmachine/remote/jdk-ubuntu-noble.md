## `sapmachine:jdk-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:118e753142336273ffa79d6d42eb9aac59aee5b0c2c884373fd1b9da755fd8f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-ubuntu-noble` - linux; amd64

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

### `sapmachine:jdk-ubuntu-noble` - unknown; unknown

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

### `sapmachine:jdk-ubuntu-noble` - linux; arm64 variant v8

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

### `sapmachine:jdk-ubuntu-noble` - unknown; unknown

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

### `sapmachine:jdk-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:86c74de1f71880f7eb5d9ceb832a96d2452ebc4a102856e8b7dde0326761a638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257677163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f032bfed998de043de9ff2fefca4f40f106cc533b3d821198c60104450ba74dc`
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
ADD file:6ec0ebf9a019b7c00b0121b97e89fcad881460415f8dcb9bb94b1cc7f5d0a5bc in / 
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
	-	`sha256:0e110547234fd795b1c6d90b50b5df43ec509107fdf663124acb5e3861c38ef9`  
		Last Modified: Thu, 10 Oct 2024 09:00:03 GMT  
		Size: 34.4 MB (34389412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9ee307c62630cdcb216d07a17988ae7241a0502516ebe3314ade11fbece96a`  
		Last Modified: Sat, 12 Oct 2024 00:24:17 GMT  
		Size: 223.3 MB (223287751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3b5be8eaf13f83f4bfd22d76f94ce2c79a192aae316cc1cce6a895a24659f767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6c5196578435fab2140d7f007ef4b65b0b49ea8c991b5384b463f7a8f94e5f`

```dockerfile
```

-	Layers:
	-	`sha256:611932e2a8c5a4b3793d4128ae41cbdfb75e5441a47fc8347e094371aabb4e5f`  
		Last Modified: Sat, 12 Oct 2024 00:24:12 GMT  
		Size: 2.5 MB (2454145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9be5a65dc22e6600fb9419cf6f1bed5bcf34a9300ef800e2dea81d346bf3159f`  
		Last Modified: Sat, 12 Oct 2024 00:24:11 GMT  
		Size: 11.2 KB (11169 bytes)  
		MIME: application/vnd.in-toto+json
