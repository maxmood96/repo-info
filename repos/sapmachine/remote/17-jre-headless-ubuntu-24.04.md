## `sapmachine:17-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:fac0befc1f29439317a6f2442c4d74e465e5bb422127a68165db31c01e25d58b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:1e83af6959f4710a85362302675237afba1527c5a6761436d39c1c0429412382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82656760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5085431d47c791ddfaf1d7e31433d8c07de788426ad4b21f4a41eeb99d20d14c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5095edc48541d1face8fb6aa5517ae0a559102bfcbd96b2ef30d171a7bd1144`  
		Last Modified: Sat, 12 Oct 2024 00:01:06 GMT  
		Size: 52.9 MB (52906303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ef8da419a4f23c39b91603620a4b94ffe4e60e9b082db2c0c110ced0b6aee5a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9fc164f002d0003ee207500a997722a6f5bd9340a85409683ccc0452e81a84`

```dockerfile
```

-	Layers:
	-	`sha256:085a754c32183b8b47a1a240084f405c2bb42dd2d8018207df416bcb2d17dd0a`  
		Last Modified: Sat, 12 Oct 2024 00:01:04 GMT  
		Size: 2.1 MB (2127316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:135c5e614cb2a11c20a02d9c897e445238483f4026147cd1cd5907d0cbc2c56d`  
		Last Modified: Sat, 12 Oct 2024 00:01:04 GMT  
		Size: 9.4 KB (9402 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a1dd22abb34a0c5d20cbd9d0d7b693127b1ff3c25e83984131d659ccd21e8f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81174066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681285e919bf5f5a98f3866f15af36c529f8812f2f4f2f21fb2b9be5b29e14dd`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1101c98a4b728a53fa7308a80893780f98bef1a3a75d35461ad8ddd612c4cca`  
		Last Modified: Wed, 02 Oct 2024 03:59:41 GMT  
		Size: 52.3 MB (52288636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1715accdf5c4e6fe896bd8ecb95deda0a7613e41d3a2ca08585b9940c7f3206d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828b89f10c80e51a153355b70d4e99ab610bfafc39cb871ce97bfb558acf18a8`

```dockerfile
```

-	Layers:
	-	`sha256:d97cfbceb7ee146891ed232dcad091ff6b25e93193d8752b98117f908d03cc9c`  
		Last Modified: Wed, 02 Oct 2024 03:59:40 GMT  
		Size: 2.1 MB (2127159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ae361ce376080ce62696ff8df48c782fc680bcfd01ce9c4ba87f374b370c721`  
		Last Modified: Wed, 02 Oct 2024 03:59:39 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3032e7312f1ad86757a64901b074e588e92d38f4b55334624e407610e3098896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88718503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f9386763e0e5cb6b5cdc919bf9797c779810ce13b4582d82db7870e297e63a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:02d903566b998a9262d33a607ddfd51e0fd03d28f420fe11f8a2d4fed1eefb53`  
		Last Modified: Mon, 16 Sep 2024 07:36:44 GMT  
		Size: 34.4 MB (34392021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1569b4ed8a010e09a4b10ef660dcf1a36b4809763f7a6b964b6a7bd4590eea`  
		Last Modified: Wed, 02 Oct 2024 03:13:49 GMT  
		Size: 54.3 MB (54326482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:be42c2ca25e180ceb7f67ceb62a813f86e8eb3e6da132d644a4bd8fe4bd641b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f7cdbb7ba1bcc90aab2821d78d13c351dc08232db74645de77aaae06e346ef`

```dockerfile
```

-	Layers:
	-	`sha256:edc328fa344b234e80e2f0294c4d300f4c4d827edda1895b5aef9f6481e4f577`  
		Last Modified: Wed, 02 Oct 2024 03:13:48 GMT  
		Size: 2.1 MB (2130563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c58c22a73ebe9939f0d7ae590056defb8d9a7fdd81315db133394118598525b5`  
		Last Modified: Wed, 02 Oct 2024 03:13:47 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.in-toto+json
