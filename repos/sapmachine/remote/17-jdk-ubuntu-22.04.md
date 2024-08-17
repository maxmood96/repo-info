## `sapmachine:17-jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:e94200f8592be8e8c20fe523c28c0bfe54b6288c9c1738b832f3af032edca2de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:85e28b634360adffdb4db14990736a642dc22a91b0a02d33c3bcff9700f86e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229585885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d913978e83ffe39f3d71a1dd24b052401ed7e0df0e19e4f113c0ab2fee6991f6`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd67323e43a3b07f99cb66c5d9c780b874214bd022db16076e8b70b343a87e1`  
		Last Modified: Fri, 19 Jul 2024 18:00:46 GMT  
		Size: 200.1 MB (200051830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cd3ce5e629644707248105439fee3a3e1b5082af204d0a60dbe6f5214cdf353f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2481100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30da6affb3f60d2e30329e04f6c529049cb065c6700984d6cd3b000123be795e`

```dockerfile
```

-	Layers:
	-	`sha256:746e57e60d9f12a8fa187957223da71dc26ca15960b3e36dbd2590735c0fe1fd`  
		Last Modified: Fri, 19 Jul 2024 18:00:42 GMT  
		Size: 2.5 MB (2471217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab6a71808061110e57ea6195e0c4700c6970fcf66a87a2e0aa3001880509921b`  
		Last Modified: Fri, 19 Jul 2024 18:00:42 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:56f554c1640f1faf16426f6d46738cacdf91b2356acf2bbc180ed8a104bfbb5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (225999600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1493209208a21216134535bf15061dfa750e98c3818f2401b6375ce20ccf13c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14bc73cbf6d1597a3ac502ff1f4ba2350c93950661a1d3dccf8308f6976c2a9`  
		Last Modified: Sat, 17 Aug 2024 04:34:01 GMT  
		Size: 198.6 MB (198640917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1dab482ea2984b76caca7a29616c18759f818e24cd2ee3144f4d01d802568f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2481178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ae4a4f6e805da78a7cc0a95c1f1fff7f311b9cd747a78afc0bb28290f8db7f`

```dockerfile
```

-	Layers:
	-	`sha256:b8dbb678048230dd5ac0e94d5ad903effd0952f07ab5eee5ecb486a2670adbe6`  
		Last Modified: Sat, 17 Aug 2024 04:33:57 GMT  
		Size: 2.5 MB (2470945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f55a6bb9e30eaae90fdb714f0541aac8900eea9609c24ddbd0feace725b481`  
		Last Modified: Sat, 17 Aug 2024 04:33:57 GMT  
		Size: 10.2 KB (10233 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b19f69ac00e0a918ac975dcdc0aa6de8ebae695bd59de615a8bd427be7722b46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235588860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb981c602a994ef49e417fa07753103340b8be406a194d3d2e619281036c31f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ea8be783bf6b329c06ef1ae934c2aab67be18617de1c81af48832c098c37aa`  
		Last Modified: Sat, 17 Aug 2024 03:14:49 GMT  
		Size: 201.1 MB (201124682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a30f3d75b7713cc6d77a41555d3b461334242233190c09ed0c2c45501503fce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2483216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb2979fde55c63419a4515550a9bd5a2c736464090ffde754d4cf79d1dbbb72`

```dockerfile
```

-	Layers:
	-	`sha256:7ee2a575c0571384bac63e1b95939eadb701ab92b881a01d8d666c10a2a89bd8`  
		Last Modified: Sat, 17 Aug 2024 03:14:44 GMT  
		Size: 2.5 MB (2473271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd8c659929af7b4cfb4f9ac793a297663e1109ef9dc6f0c3415ee87a3e00b151`  
		Last Modified: Sat, 17 Aug 2024 03:14:44 GMT  
		Size: 9.9 KB (9945 bytes)  
		MIME: application/vnd.in-toto+json
