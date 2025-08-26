## `amazoncorretto:11-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:0f84594a75e2b883e28a779bb29736fbfbb07fdf262d8dcd06944c221edcc54d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:631e2f8db16cac55acfecdd76d5fcef29d38844bb23c9c72761431658ff472e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.3 MB (211314837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63dcd00e0aa850e21f2a3c884e44675483dc8612a426ef9a7f715477f49910d`
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
	-	`sha256:f21a9c156d2ab29af4b5e451610a197ca56345598aa7ad950a22561b52bd146d`  
		Last Modified: Fri, 22 Aug 2025 17:34:29 GMT  
		Size: 63.0 MB (62978125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e392f411b02e2eab074a9b83d03cff1a29b558ba7abe1b4b224b81cf9461a623`  
		Last Modified: Mon, 25 Aug 2025 20:55:14 GMT  
		Size: 148.3 MB (148336712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:137e4c6d8947e0d68b315d0468696b99fae7cb671000360da39c1f1136c847d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5551033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493cedc30457be28f0f1c6a1fa84d0551e4b8fd38979dc4a5860fcfe23ba623b`

```dockerfile
```

-	Layers:
	-	`sha256:0e1f616c30a4a32902ef8d57e49345624b46f4da9a723181d291eac220b27c66`  
		Last Modified: Mon, 25 Aug 2025 21:47:19 GMT  
		Size: 5.5 MB (5539778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9612e41b888fb64686d5c83b16d06c95098c5b69406a8f9b2e7cc116706d4aa3`  
		Last Modified: Mon, 25 Aug 2025 21:47:20 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:299a7ddafac7b0ec24da9da2cd642a2fbebaa7cb0657e7ba83d42062e202b59b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210180840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377b38c87a1e0a8cd428deee89ebf56b4ed78b5d74aa460c1ebc30eaa333d1e8`
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
	-	`sha256:a3bec375112fa06818025bf7b6ee4b903edf4e301e27d2464f104b8aabf964f3`  
		Last Modified: Fri, 22 Aug 2025 17:35:51 GMT  
		Size: 64.8 MB (64801350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb7192c32fa4304183daaf2bd2088b988a2ac245d547f64ba6babe344f5546a`  
		Last Modified: Tue, 26 Aug 2025 00:49:07 GMT  
		Size: 145.4 MB (145379490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a6b6143b46edfd98acefbeed2bcecd411abd0c9d44ac44792652e77c1326c5fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5550679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17446e02cf65d0d1d36f0c12e36dba48af6e2c9b322c3befc5b613e59a1b877f`

```dockerfile
```

-	Layers:
	-	`sha256:6a2e8ea9286fb9761e31afa19b1d9a30b0729580bc693b60f67738b53f0f5d79`  
		Last Modified: Tue, 26 Aug 2025 00:47:21 GMT  
		Size: 5.5 MB (5539272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e564c5e3f36f323f0807185a9f79994154e3c11d6034fa05b58f6fe69ec6539`  
		Last Modified: Tue, 26 Aug 2025 00:47:22 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.in-toto+json
