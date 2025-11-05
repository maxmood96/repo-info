## `amazoncorretto:21-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:5694c60bb3a784e25866e20608f13b0450986a37888ed82a463378a03e93eca3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:11aac5344270fc112e7a46ded5064260da8709f4bd8dd81f59d7cbecc52665bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228420039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a188df204f2bc4af05ece24df9143970b8f9cd4c02e86556716a1556b253e6f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:45 GMT
CMD ["/bin/bash"]
# Wed, 05 Nov 2025 01:06:08 GMT
ARG version=21.0.9.11-1
# Wed, 05 Nov 2025 01:06:08 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 05 Nov 2025 01:06:08 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:06:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:2e3ea9592aad33f5f11ca8c65604905de30de68b0c38dfad7dee51b605c2a2c5`  
		Last Modified: Thu, 30 Oct 2025 03:52:34 GMT  
		Size: 62.9 MB (62934068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bb82af62a77255279f1c497851a6fe8f80f84cef1425a841bf7348ca44f3fa`  
		Last Modified: Wed, 05 Nov 2025 02:35:06 GMT  
		Size: 165.5 MB (165485971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:480d8cf7e0c089c8f010b3a67fa7067b176ba4709f241f92dc9fee7cff5f6015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7c44643d7dd78065ce5b2e24b3b51ed4e5caf96baa8caafbb67f5306ce8ed4`

```dockerfile
```

-	Layers:
	-	`sha256:b0222ae487e96f4a668670cd26daa6c2cfea811bf47b308f2cd36910f6c918af`  
		Last Modified: Wed, 05 Nov 2025 04:47:53 GMT  
		Size: 5.5 MB (5535595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edb3c7ab2dd36ea60d619b44f30c5ec7c83fe0dc55562658a7559c6c7aa564df`  
		Last Modified: Wed, 05 Nov 2025 04:47:54 GMT  
		Size: 11.2 KB (11206 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fb0dbbf8eba69167e4882e04cfd6b89d634c264fc3f9f321a628c8615ba3983c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228376399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f3b53818684e75fb757eac1d9e466c7109692fe507b83f5436f2a1a1e2e897`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:47 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:47 GMT
CMD ["/bin/bash"]
# Tue, 04 Nov 2025 23:12:18 GMT
ARG version=21.0.9.11-1
# Tue, 04 Nov 2025 23:12:18 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 04 Nov 2025 23:12:18 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:12:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:2875a69d1768080ef2331610c2aea8f8cfff54b5df360eb9feb01240a7526ff5`  
		Last Modified: Thu, 30 Oct 2025 23:15:16 GMT  
		Size: 64.8 MB (64793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ad0d1fcc61302619a93c14ea37d679d5cc2a8f138552caa19924202526997b`  
		Last Modified: Tue, 04 Nov 2025 23:26:04 GMT  
		Size: 163.6 MB (163582941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4956392fc36c8d42d555654622c0f68176675f9e47e6dbca44a9de7339264d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5545641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bfe47dd784b751d3233f796ce2cd0a6991ca0d7a6df3d1baea8effdd5bf4111`

```dockerfile
```

-	Layers:
	-	`sha256:e149125170ded5568a08dc65a01d627e4c73dfd4a2ab1386fcc4e5557eaf18e8`  
		Last Modified: Wed, 05 Nov 2025 00:17:33 GMT  
		Size: 5.5 MB (5534284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60ba333048120a25cf8d127b18308f5e8c260e5b957cd7bb9bedaaee870d69ff`  
		Last Modified: Wed, 05 Nov 2025 00:17:33 GMT  
		Size: 11.4 KB (11357 bytes)  
		MIME: application/vnd.in-toto+json
