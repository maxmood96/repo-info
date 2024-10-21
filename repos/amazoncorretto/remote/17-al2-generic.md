## `amazoncorretto:17-al2-generic`

```console
$ docker pull amazoncorretto@sha256:d6056109a005060e08b802d3ae2ec5c72552f2cf4466e7b221032c524bf0237a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f609c7eaad159b1c466f662a94d52dd783c286c16861901d48437c32f98a4d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.3 MB (214294513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8ec21f749c5f8f13de9b6b387a211ef00e14c8d1858de57652820e11335f7c`
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
	-	`sha256:32c87c6464b59c63781462d4129c84f2806c57bdb75e94414a62f13a51d7b113`  
		Last Modified: Thu, 17 Oct 2024 08:34:33 GMT  
		Size: 62.7 MB (62679539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66244e4b15839e8eabcae9bb42a203318664f4779635534564952783b057030b`  
		Last Modified: Mon, 21 Oct 2024 18:57:01 GMT  
		Size: 151.6 MB (151614974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7475b8a128339b4e2a4d94ce8c7851c9db157d37aa5f6cf32e4fca9950f2a35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5539034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda3dfa3b7a35d0d830237f2db78192e7dd55bf28075f867c7ed5344bc066e89`

```dockerfile
```

-	Layers:
	-	`sha256:9020da00ee847e66fdd3717f431b08774fa2a03fdc3203c2ecf3692df62acc8e`  
		Last Modified: Mon, 21 Oct 2024 18:56:59 GMT  
		Size: 5.5 MB (5527779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0068177c2af586cba13a9c9760f679a1c3a6913206c057256c265d734f1d9c45`  
		Last Modified: Mon, 21 Oct 2024 18:56:59 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d612a73485c52b0d0a25e92be1b64b7648a126b4eae4d9be10d4efdd4b3f7824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214825816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e200b9de7c447566821d763161104c2563906f467edbda428510bcf7ac467368`
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
	-	`sha256:c05d42ff0b796ff4b1055b91676cb7e4b68389f23472cfdf987fa036f88561a9`  
		Last Modified: Thu, 17 Oct 2024 14:51:33 GMT  
		Size: 64.6 MB (64587089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651b0d2256b215b37f265efa060f7500e983c3d10f7b2dc68ea4119590267fe8`  
		Last Modified: Mon, 21 Oct 2024 19:20:16 GMT  
		Size: 150.2 MB (150238727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4a635631a840f617544fe0a1fd42cc0033e0180eea3aaf6f07e2d2e279067779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5537874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ac5e398239658482e26443062c26f23b2e1901ac1a1e0b2ec1125807d881be`

```dockerfile
```

-	Layers:
	-	`sha256:9ffa01543c17e10234ac57fd1c19c7f10752d1b60d048454a96fa5b91094cbc6`  
		Last Modified: Mon, 21 Oct 2024 19:20:13 GMT  
		Size: 5.5 MB (5526466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57fce7598d834ef80702eee050e97502f5403cda2bb110311b62bda51f9e9c54`  
		Last Modified: Mon, 21 Oct 2024 19:20:13 GMT  
		Size: 11.4 KB (11408 bytes)  
		MIME: application/vnd.in-toto+json
