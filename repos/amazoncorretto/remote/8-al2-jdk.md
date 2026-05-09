## `amazoncorretto:8-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:d8db83b7deeec6c9ffddf88a69d7b2d0c193f95a005a37c52f46cc0bbfc13020
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7f425fe25556662499102af6e74e739b38a5117d82a645102f035516c464e76c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138922509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f3c668b584e1bcf7d7e041b817d250ea78cbe746ca205f83be453988da297a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:56:20 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:56:20 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:13:56 GMT
ARG version=1.8.0_492.b09-2
# Sat, 09 May 2026 00:13:56 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 09 May 2026 00:13:56 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:13:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:3f708fc5705625846e206621966842bfead7ee5b8e4fc20aab0c77c563600126`  
		Last Modified: Wed, 06 May 2026 07:46:46 GMT  
		Size: 62.9 MB (62859738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d333b73720cbf1bc6d25075d1b7ccf60589403c0926be278750990ffe0b2cef3`  
		Last Modified: Sat, 09 May 2026 00:14:11 GMT  
		Size: 76.1 MB (76062771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3727947c0612c6253e98c8a084bfa9ead422f0dceabd0908d690a231597c6e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c2e6c8e2dba6bab3adc5e2a26e44120930a253f75b4fc8c0a05bcb79ebb2bd8`

```dockerfile
```

-	Layers:
	-	`sha256:e72cdbcbfdec6d82be2ae746879746a66335e814b6603bbd40d8076ed0a8a3ae`  
		Last Modified: Sat, 09 May 2026 00:14:09 GMT  
		Size: 5.4 MB (5377455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb20d9c680047ff82cccc02161ff61af4951c43f143d151bddf55ba164554d85`  
		Last Modified: Sat, 09 May 2026 00:14:08 GMT  
		Size: 11.5 KB (11527 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:955e19061b1956b9672d8e2271c49c49ceab95488fba71505d726c134fbf7c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124746019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bbd87a3d212f65543bb6f2a480c684fa5adeca59cf09e1607eab16ab678d383`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:48:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:14 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:14:10 GMT
ARG version=1.8.0_492.b09-2
# Sat, 09 May 2026 00:14:10 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 09 May 2026 00:14:10 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:14:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:835dd3779a793c24eeba54a176badcbf0ecf82042603b5459dd57e14ad679d47`  
		Last Modified: Wed, 06 May 2026 07:46:52 GMT  
		Size: 64.8 MB (64808915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf5c56505d3f9c19a2701f7fba6216724339730abbdc29d2c3874b88ef40bc9`  
		Last Modified: Sat, 09 May 2026 00:14:26 GMT  
		Size: 59.9 MB (59937104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f3242e9d382cec021f117168364d4869999d07def93e0d87170603b6f66424a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ece390b3ea22c048419cf66d38577365e5461624a8dbf8c48cfae864028565`

```dockerfile
```

-	Layers:
	-	`sha256:07c5ff8cc4c3a28fc70da32f6065395113605db7068a8788bf57900e4bad5bb6`  
		Last Modified: Sat, 09 May 2026 00:14:24 GMT  
		Size: 5.4 MB (5355954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a3053e70612271d9974e3c77a8241e5b229b72a9c48addae10641668209db11`  
		Last Modified: Sat, 09 May 2026 00:14:24 GMT  
		Size: 11.7 KB (11691 bytes)  
		MIME: application/vnd.in-toto+json
