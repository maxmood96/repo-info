## `sapmachine:21-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:1e45a8ed850fede502b237f8df7f38f98da2347503ed52342ebb9e3a0e020373
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:52de579db5edc11d5a7de46e25a0d5be8370edef8ebfeae5dea5dac19d09cacf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90079930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3594be76fba1ef3aff829c9464f05cfb619d48a3817ab2119a5fc5bd84c3f88f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8123ea1eddacc7757389bf608a2242693cac06fba4bea8f67bffb6cf5ff1c27c`  
		Last Modified: Wed, 16 Oct 2024 16:17:44 GMT  
		Size: 60.3 MB (60329567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e84f499833d36ac5a8e46c26f19226e2c028a157ed17796053c3df4285f56156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6d54f965546a505ecf0bdd4479894f729f49c4dbe5cb4626cecd4ad04f2066`

```dockerfile
```

-	Layers:
	-	`sha256:e7063fefad9c58dcdad66049d836f2a04a1be50a5e7a5af47ce4b23e8bcf7658`  
		Last Modified: Wed, 16 Oct 2024 16:17:43 GMT  
		Size: 2.4 MB (2366294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3343f8b08a81e92d5e94d9733c68f685128cdfe33a09226d2efe98f1a34789c3`  
		Last Modified: Wed, 16 Oct 2024 16:17:43 GMT  
		Size: 10.2 KB (10234 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6f03fd6a633dde3821a1fb8ba0d40904c0db189f5c405c8588b4c886ae1f89a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88324449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523d538333c7e5bd280d86eae9d0a317c4132b68e10e4845a358021961800c9c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1892d8ca9bf385bd37d1ae76187b83aa28986549f9bf5949d192d93e3e51b06e`  
		Last Modified: Wed, 16 Oct 2024 04:31:06 GMT  
		Size: 59.4 MB (59438604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:177906e30a2a41d062250b5c3ebf8dcc4ce328707ba838aca45c7bf11092342c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06665d1ecdff5dc0f4ffd51ecf9ced6a355939777bcf1779c2f0468533ba9d71`

```dockerfile
```

-	Layers:
	-	`sha256:3c7a23ccf4424539dde23f547d76c218bd779e6f1ac03c18bdc19644b09730ff`  
		Last Modified: Wed, 16 Oct 2024 04:31:04 GMT  
		Size: 2.4 MB (2366821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5020491ddaf9ce2b7d9f84d25dddf25ff12cc3d269adfe2dc1ec90fd8b71ada9`  
		Last Modified: Wed, 16 Oct 2024 04:31:04 GMT  
		Size: 10.4 KB (10392 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:bd5334fd4ea9c911cc36393c1e73ae053763e8786e8f8b0b9162750014022491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96403592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0bf110124e072ea67077cc51568af06a06c5cf3c72b8fa9a38f6fca63557d44`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97916f71f27e537c2ed49135a45fedbb69b953fb55074d9182cd44faacb727b4`  
		Last Modified: Wed, 16 Oct 2024 02:48:09 GMT  
		Size: 62.0 MB (62014623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:68d285c1db2eab4b9cd8f1dcb5611469d797e1d11fff50ce2bce7ac4a517346c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae0d438fdbcac33a14a20039f09730cf26737c6cfaf78add7da28d6e48d4933`

```dockerfile
```

-	Layers:
	-	`sha256:703c34df91fa275a234c1a0a912c63fcf15371539773b7813179e58251226174`  
		Last Modified: Wed, 16 Oct 2024 02:48:07 GMT  
		Size: 2.4 MB (2370261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfba3addf8b5b05813cdd561533769e4b20f3201180b984ca4b44698d253d490`  
		Last Modified: Wed, 16 Oct 2024 02:48:07 GMT  
		Size: 10.3 KB (10302 bytes)  
		MIME: application/vnd.in-toto+json
