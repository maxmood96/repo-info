## `amazoncorretto:11-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:7d33560f828cb41695c3cd6a41844d4b9df919c34e0038a57c0bfb95d9cfd7a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:99a47b672a913c2c9a6c147e361e386f987ddcadd2bd99bf9b9807f6f80d14c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.3 MB (211322915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60660d6a58b59021a011d0e6c671b530241bc9f4c62b82f995bd4b12304340d8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=11.0.28.6-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:0c31e84362b17be00ccd03302ca56ddbf8561b17d46e8c82bc87c21d389e7731`  
		Last Modified: Mon, 08 Sep 2025 20:24:26 GMT  
		Size: 63.0 MB (62983288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8bea982d1e249b81683a47e2e85a574261090e0aaee8205b1f4f927391f09f`  
		Last Modified: Fri, 12 Sep 2025 02:10:01 GMT  
		Size: 148.3 MB (148339627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:557698c468b28ea1e3364713fb6b0a92b9f14c6ae4d0bbab83617c887f7bde53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5551033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc21b80eb531e1ecfefa73b7535888f10b07bfeb3ee19c897fc5e0d086992f0`

```dockerfile
```

-	Layers:
	-	`sha256:bab760463e3344da7fb808757719f1b6b931cae5a42faeb65f4aa22ddce95784`  
		Last Modified: Fri, 12 Sep 2025 03:47:18 GMT  
		Size: 5.5 MB (5539778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9a02dcca385180ea2e52d6d797e41955a3027025504fdadb3ee37ab81a5940d`  
		Last Modified: Fri, 12 Sep 2025 03:47:19 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8ad6c3e374538ac4874c5cd615f11d275bd5fe4031924935a4bb49dd545a9992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210165428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941947f915928e9476c4e090b622b786dc546003d8a7527170eb0235e3a0503a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=11.0.28.6-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:44fb931604a5509dd2f5cbf8d1604d64dd0f56962f61bf6cd3f092bce2e7687a`  
		Last Modified: Wed, 10 Sep 2025 17:52:55 GMT  
		Size: 64.8 MB (64791723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ec5a7667301b2aeb05129beae7ce8e7390d997ce62b515bcac2e7e699e6ce`  
		Last Modified: Fri, 12 Sep 2025 02:13:05 GMT  
		Size: 145.4 MB (145373705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7eb7edee76c0d55e78073aa8391b581346985b805d437a8823d6eb8faaffa56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5550679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cd4e3c3e6377060ddd2aeed6d97889753528896fa739337345109811f90958`

```dockerfile
```

-	Layers:
	-	`sha256:45c0ffb30aa8565a416858061e5d9f806f960880477208253244850cead233ad`  
		Last Modified: Fri, 12 Sep 2025 03:47:26 GMT  
		Size: 5.5 MB (5539272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:521ee4872649d611d116ee964e33920f3136e2a9d5318665dcc04de5c5203e5b`  
		Last Modified: Fri, 12 Sep 2025 03:47:26 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.in-toto+json
