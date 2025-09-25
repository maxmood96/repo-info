## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:21e30815efd0f97411f30334bf9abdfaa8621dd4e1371d902707b3b4f532a3cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4354f45b21ca24649b2b245f12e43097636bf11d6860630315acafa225fb1dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211225820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb758981fa9818f1a2a7ba86d541b3b59a8a78fcafbd9f11134f4ab76f9f47f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=11.0.28.6-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:fcc68e74b985a5b6eee4c73b52bbf6b5465b7b43a029c51e8950289a9262b97b`  
		Last Modified: Fri, 19 Sep 2025 15:29:12 GMT  
		Size: 62.9 MB (62933841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f867df2562f4ab3700d662bb34c006adfbcd9774b94f2d4eea34e265d66cdafd`  
		Last Modified: Thu, 25 Sep 2025 03:16:01 GMT  
		Size: 148.3 MB (148291979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ab47b94d4ae3fb24cb28178054443a59a6f07c0b246da998a91230e63509324d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5551033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60a16666c55be8ab0ba15e2152d442df9dcc0d42386d7ea8fe98cc2e8b36b32`

```dockerfile
```

-	Layers:
	-	`sha256:0fdd46a90e9ffc2b1a6ae72f1b82065ee59ca6f9d25485785c60443dbf27f856`  
		Last Modified: Thu, 25 Sep 2025 03:47:19 GMT  
		Size: 5.5 MB (5539778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67537a4a0b572829944aabee932356b1ddccf0cde1cecc81208bae99c326e1d3`  
		Last Modified: Thu, 25 Sep 2025 03:47:20 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ceeec82a1964581c6c1b2a5daa7bbd2ae222d758ffe5bff9b2d6b8d814140f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210165438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5099b2252003e45902ea4013fd8e5d6f3a1946541e5806136cdbf76db06a9e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=11.0.28.6-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:43d39e1e5d32e8ac06f789363477524a09029961f1236d4dc3927f200c572bee`  
		Last Modified: Fri, 19 Sep 2025 23:24:58 GMT  
		Size: 64.8 MB (64793147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98223774ca3971d08cc0330a7721d384585058505d9b480be8e88899ad5219c4`  
		Last Modified: Wed, 24 Sep 2025 22:12:57 GMT  
		Size: 145.4 MB (145372291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bfe33ba12baa4633ea7a11dcb4e86e8e270a54844fac1604c9eda65116922eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5550679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d0b7629fdf3860c94f8c9b88a761a925b0282f2b8e5a6e7dcee2a088192a3d`

```dockerfile
```

-	Layers:
	-	`sha256:2ae6fa9d27c779f15b9880c84aa27604c8edac9aed9bc2d741190adba7621b56`  
		Last Modified: Thu, 25 Sep 2025 02:15:49 GMT  
		Size: 5.5 MB (5539272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ea4a67d7bb9da26daf2ad1abac65f68326482b5eab25ef15d4597876ee89894`  
		Last Modified: Thu, 25 Sep 2025 02:15:50 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.in-toto+json
