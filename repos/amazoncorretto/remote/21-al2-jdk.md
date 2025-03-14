## `amazoncorretto:21-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:c0643148d077b3917bf6c085aaa1ac35ff1f202344ab8691cc0f5953f9b97f8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cb13a99ac04f95b123043ebb186ef6aaeb84aa53e6fb31d15acb480c53276ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227591660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0d761a5d449f44163c7283c11dfec5398bb4823bebde7ac31ecc0c9940c96c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:f3dc83dc2e4e000fd189efee126db80e38a079b47b8e5229a794a0a6148bfec6`  
		Last Modified: Sat, 08 Mar 2025 04:13:59 GMT  
		Size: 62.8 MB (62772838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d780df9adcbd4f85fae763ecd2a7c4d99ab147a0e44e15e0f45784ba50fa4a`  
		Last Modified: Thu, 13 Mar 2025 22:53:06 GMT  
		Size: 164.8 MB (164818822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:be7b68c4922bf1e82116d6e010b88d65eb5ab73677d3cff4720a6acdca467679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5528248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0124ce79a89abfcd7bb6785de52f4a1c6528aa52f6a82e2b192ede192d57d77a`

```dockerfile
```

-	Layers:
	-	`sha256:e365a78ce822e240619cc17fc3b0beccf9c43c0a47759b56b91ae79cd947e751`  
		Last Modified: Thu, 13 Mar 2025 22:53:04 GMT  
		Size: 5.5 MB (5517001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c6d50c20b4fda821b54b64d1293d61c65264f63dc2c27b33161b3ad523008e8`  
		Last Modified: Thu, 13 Mar 2025 22:53:04 GMT  
		Size: 11.2 KB (11247 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:344f322ab8e78b30ded0bba8306c2f83a785dd29b0a21a72f4d6180a2a63db17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227461375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050f7950dc345257574e7320d42fe56f49add50fe843e7ce6846f1cab970e395`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:37d03ccf62e80c78860df81fce0c2ae4e2349efe1a11714ff404080836c55d45`  
		Last Modified: Mon, 10 Mar 2025 14:33:01 GMT  
		Size: 64.6 MB (64576854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ba70ad9272af4f1da57809248cf192c75eaeddc71301ad6210dd3f5a0ab670`  
		Last Modified: Fri, 14 Mar 2025 00:18:23 GMT  
		Size: 162.9 MB (162884521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0059c1bf570cb49dd07b98a19a8abe944682bd15bfd39872b9c24c35e8567c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5527090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817d105c462524d332201540817c187dfeeda365e660a7b85878d25e7385476e`

```dockerfile
```

-	Layers:
	-	`sha256:10524f79332272592b735221b232d96545c2cf4d6a63adc455e1534935e45883`  
		Last Modified: Fri, 14 Mar 2025 00:18:19 GMT  
		Size: 5.5 MB (5515690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c245982e85fa3986986acd2b69b800d6fd1bf448766f747d8bcc6f2c5a8de62d`  
		Last Modified: Fri, 14 Mar 2025 00:18:19 GMT  
		Size: 11.4 KB (11400 bytes)  
		MIME: application/vnd.in-toto+json
