## `amazoncorretto:8-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:4a17b8a1daf66fbd192e46f077755846d5d91396a197a093d81cffb396e31a77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8f47b66806e84270995b2168613229623f975fdd05df7d19876ad00c24896ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138993491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3f795ef13f74c60e1dc302938964c356f4818ec853b629fc40770170873ed6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:30 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:30 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:11:03 GMT
ARG version=1.8.0_472.b08-1
# Thu, 11 Dec 2025 22:11:03 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 11 Dec 2025 22:11:03 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:11:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:364e8e668f0e62a54627e7d364c5d2a3a16f70f1c962628fd84b9ef8fb667d21`  
		Last Modified: Thu, 11 Dec 2025 05:04:46 GMT  
		Size: 62.9 MB (62940975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaad92ac026238a6e69c37e117eefc6fc2056917f9cf02d4682ae935499d87c4`  
		Last Modified: Thu, 11 Dec 2025 22:11:49 GMT  
		Size: 76.1 MB (76052516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3b86e81c6cdfe55fc7a108754921ec77a514ee3a1ec13b7ac60ade85a92eb3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6efc5d0a3ede7d3d52ba79b991bad0b996909fcade7d57fd950907e3bafc7d67`

```dockerfile
```

-	Layers:
	-	`sha256:b3eba61f06648aa1770756da132c64026f5b7f8de1d29cedb56da37d84e586ec`  
		Last Modified: Thu, 11 Dec 2025 22:51:25 GMT  
		Size: 5.4 MB (5377358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e559398990fd94301874ef7e41c4b22a73cb344363cd73398deb1f6652b2a679`  
		Last Modified: Thu, 11 Dec 2025 22:51:26 GMT  
		Size: 11.5 KB (11527 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:edcebef84ac723ce265d2947fcd7dbc2702a813b06a928804169da3f90117ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124913808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a55c694daccc71dda90ece7caa75423301ef1d3bdde20a817cb8351e42bb70e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:28 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:28 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:11:01 GMT
ARG version=1.8.0_472.b08-1
# Thu, 11 Dec 2025 22:11:01 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 11 Dec 2025 22:11:01 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:11:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fab5386d951251971cce18e051d0e0dc64bd28b832a63821f749d70b9003817`  
		Last Modified: Thu, 11 Dec 2025 22:11:51 GMT  
		Size: 60.1 MB (60118053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:837c856cccb3a2b48a894694e72f231e5943c90cc4298c34ad4c1ebcdb00aa79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607c848e1589430005fd4f476597d7038fbd6ce66821bf7881f2868365da064f`

```dockerfile
```

-	Layers:
	-	`sha256:84f63731ad2f8c9f81200856e4ac2393ddab946c00683d411504d51f0a548a50`  
		Last Modified: Thu, 11 Dec 2025 22:51:38 GMT  
		Size: 5.4 MB (5355857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7373cf9820189275c33e0fb95a7f7f6247490a0bc6397ff9067571df440d0590`  
		Last Modified: Thu, 11 Dec 2025 22:51:39 GMT  
		Size: 11.7 KB (11691 bytes)  
		MIME: application/vnd.in-toto+json
