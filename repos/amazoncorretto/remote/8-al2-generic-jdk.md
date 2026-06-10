## `amazoncorretto:8-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:8c6b4f817dc07630f43286235e138f1551be06bc969737ea23305e8cdac17000
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:303d6d309297956b1d2380881e013fdaca40c36a55fd3fec426ba8fea5249a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139056446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3cc787f85ce32082d7a5e49eccdf2994dbc65e04a5f9d69c1692c7f302b271b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:26 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:10:20 GMT
ARG version=1.8.0_492.b09-2
# Tue, 09 Jun 2026 21:10:20 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 09 Jun 2026 21:10:20 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:10:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bf15654d32f2aceaed25c8e6fe45e5ad1cffefed578eb90f9bfe011cb9cf20`  
		Last Modified: Tue, 09 Jun 2026 21:10:35 GMT  
		Size: 76.1 MB (76114496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9c6e96d9e4a39f1ffb8a50ec824e089922b69c7ea8d54a463cab95ac8c54db00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66362f2ce26486bedf81c08a1ed4c0d5680bebc89fd4aa35c993532f4edfd2ec`

```dockerfile
```

-	Layers:
	-	`sha256:e8acbc403c4856e76f1867f3168c13127f085fe2778b4bedd4283781cd6c3d7b`  
		Last Modified: Tue, 09 Jun 2026 21:10:33 GMT  
		Size: 5.4 MB (5377455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae298e587722379bb95646ac695d5799461e33fa3eb6d56ee68cf5521b7943f`  
		Last Modified: Tue, 09 Jun 2026 21:10:33 GMT  
		Size: 11.5 KB (11527 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:184756873149191e3c9cfc6f779073c3d12ec8092edb804acbd0a0f1cd1b9535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124738699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b8a350daffbf6de90b5fdcc5f098d7f4f013d52ffa37ac3e6b11094c99fee5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:22 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:22 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:10:13 GMT
ARG version=1.8.0_492.b09-2
# Tue, 09 Jun 2026 21:10:13 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 09 Jun 2026 21:10:13 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:10:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2306dfd68bf489e4f593bbbc4e6fb78de86bc797383a3302342a651eb104b94c`  
		Last Modified: Tue, 09 Jun 2026 21:10:28 GMT  
		Size: 59.9 MB (59947990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bb635496f12248f6c6b0485c8d30c8f9484eacb206aaad8cf9272cf49d207d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6dbbdcacc2c7512750712769e12fd0e904d8194a1c568fcaa4d23f742592760`

```dockerfile
```

-	Layers:
	-	`sha256:f48237f0cd9486d961c3a0ae80686bf4ac8314215dcf98a55b1f99f4e81c1be8`  
		Last Modified: Tue, 09 Jun 2026 21:10:27 GMT  
		Size: 5.4 MB (5355954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bf68b67195c55d640c32e3d8d7ec0d9c6a26c93bbfb5444bda13eeb61ce72ad`  
		Last Modified: Tue, 09 Jun 2026 21:10:26 GMT  
		Size: 11.7 KB (11691 bytes)  
		MIME: application/vnd.in-toto+json
