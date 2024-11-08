## `amazoncorretto:8-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:4de90f5df08646cf0dbe5688265a07e65156f2200fd2cc8967b89e025b218299
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ec8112caf1525c4b93f1c73b4b089342027aaca11f6980be18bc0e154101bd96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138260951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76895861f12bf2dfe89d5bd93862009be3144a4e2f64db0db00399bb8c6329e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=1.8.0_432.b06-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:8430d4c5a00587f0a8dc4c62f82455c123b54b9016d43897ee77c496c018a8bd`  
		Last Modified: Wed, 06 Nov 2024 20:48:04 GMT  
		Size: 62.7 MB (62681042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c363a312c426933bd456625d195f6759f3d413b26273b42391a1def6e166026e`  
		Last Modified: Thu, 07 Nov 2024 21:47:42 GMT  
		Size: 75.6 MB (75579909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bd9a754c4269f7148fd286e426c5150f343ff93735e961c751855487f97739aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5381328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1ac33e9f7d6437fbe3c4dd4567460c5a87606095bb93c5830b6798d53dc585`

```dockerfile
```

-	Layers:
	-	`sha256:b101048eddfc05c9949c65fd2df9cb8833264d015fe844ceca63f9c2bf1325c9`  
		Last Modified: Thu, 07 Nov 2024 21:47:41 GMT  
		Size: 5.4 MB (5369758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:decbae59ae4f2ef17516efa2b86ba31ac5f62b5b93943a42cedb8219961893f2`  
		Last Modified: Thu, 07 Nov 2024 21:47:41 GMT  
		Size: 11.6 KB (11570 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:807663e478526b94374252991f8ae1f47a153327a4bd1eecc7edd647f0399a8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124262314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a5ef0a439147914b267d8172a95e85e8017a1ae77cea8c51e48ade176f2be2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=1.8.0_432.b06-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:0a62aca1c7d7ec3e0e098bf23685d8f0fcd19e33577a91dafc6dd30bef06deca`  
		Last Modified: Wed, 06 Nov 2024 20:48:17 GMT  
		Size: 64.6 MB (64588571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcfc1abc92ca5b6535ba64e45e51a67148ef5e82a5cf13f1fefa3eb27f0982c`  
		Last Modified: Thu, 07 Nov 2024 21:47:27 GMT  
		Size: 59.7 MB (59673743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a44ce9c39f25847d58e43ad7a7b9e75be178471c79e18ba330a3ac0c74e91a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e12d788412b619d4b354dbe8cb36cba934f89d22509e9c5646042cfb4834dff`

```dockerfile
```

-	Layers:
	-	`sha256:5f0cec65b36999fa4ea5d2e554fed36ddd1dd2f0f66c3f12c46e2841c0f8383a`  
		Last Modified: Thu, 07 Nov 2024 21:47:26 GMT  
		Size: 5.3 MB (5348285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9107da083e5085b79447c05802261ac3e8835abca13c2f597e453aff5b481dfa`  
		Last Modified: Thu, 07 Nov 2024 21:47:25 GMT  
		Size: 11.7 KB (11734 bytes)  
		MIME: application/vnd.in-toto+json
