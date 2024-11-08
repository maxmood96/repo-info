## `amazoncorretto:17-al2-generic`

```console
$ docker pull amazoncorretto@sha256:beaee0dc71ec17ed95042f596effe49814bd5568381416404fc8c509200651ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8ef19811a904b36c3689006f7e58472f3635bfed4627320c4dea71f58a340f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.3 MB (214296080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87fd77f5c089f7bd4828ddc04f8e1a0634c6fb22501923a4b5f0424c005d25f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:8430d4c5a00587f0a8dc4c62f82455c123b54b9016d43897ee77c496c018a8bd`  
		Last Modified: Wed, 06 Nov 2024 20:48:04 GMT  
		Size: 62.7 MB (62681042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a083e9f2b116d1ae278ce847a47374ba222e670cee57c7a4767ad77fe66fbd`  
		Last Modified: Thu, 07 Nov 2024 21:47:53 GMT  
		Size: 151.6 MB (151615038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:88798ddcf3476b53b90b763fc83ac9fb2226fd52e19f66ee6334ec306c027290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5539035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840fad09329b3a49e0183eeaa42e00204df859108fd654a29bb328bda3523dff`

```dockerfile
```

-	Layers:
	-	`sha256:f5c8d13bc54bc93b2bf6769c13e15247b39599708ae288ede9fdd99a8b432e25`  
		Last Modified: Thu, 07 Nov 2024 21:47:51 GMT  
		Size: 5.5 MB (5527779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3144dad1677d0c127a204cecb5a828e0dfc5316ced76c3018383acbf09b2fffa`  
		Last Modified: Thu, 07 Nov 2024 21:47:51 GMT  
		Size: 11.3 KB (11256 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:03b0c52959df6edc85951614c1ec09cab2200899e4d64703f6cf49992b49e22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214833700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38851fdf58081276d7938116dea2ec6905a30a6941f37a692f7b4f3da7cd047`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0a62aca1c7d7ec3e0e098bf23685d8f0fcd19e33577a91dafc6dd30bef06deca`  
		Last Modified: Wed, 06 Nov 2024 20:48:17 GMT  
		Size: 64.6 MB (64588571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621032f3b5245522000736763c029c662256847f8f302dc80960bc4ee553d9ff`  
		Last Modified: Thu, 07 Nov 2024 21:56:37 GMT  
		Size: 150.2 MB (150245129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a55a31a1580402674c9f3fba2a4c58827f09887065a3ebf3c61d3f8242394168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5537874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5ebf589466ab1747cb4b74b54b20f547458284a40fb9df3376ddcf8898a363`

```dockerfile
```

-	Layers:
	-	`sha256:53e77dbf1ac0fb7135ada89e108d1ac88948fd342065673df360b9f91d7e60da`  
		Last Modified: Thu, 07 Nov 2024 21:56:34 GMT  
		Size: 5.5 MB (5526466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caa6325bcc59ebfcdace3d0a989f524c64ebb893a2bd77f1109f1580d6ead2eb`  
		Last Modified: Thu, 07 Nov 2024 21:56:33 GMT  
		Size: 11.4 KB (11408 bytes)  
		MIME: application/vnd.in-toto+json
