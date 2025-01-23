## `amazoncorretto:8-al2-generic`

```console
$ docker pull amazoncorretto@sha256:811524364ec9be28977303d91def7bbcd8d14d7fec853c2bbac1480710f93645
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:93eb19ae0cb47c2c143abe2c1ab8a8dd9452898814458d52791da82b86cd09ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138198357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbe03af79e677cd58825124ca259ad4c6e510b92e1790d99e00dd4f08b38e57`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=1.8.0_432.b06-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:9fe0de22bd8b7f693a2d87aff899a83b863c2f1cc5f64f563c01e4537bcf04e8`  
		Last Modified: Fri, 10 Jan 2025 22:01:24 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41f411e0d334645f31261059c924866a66afcdef7098bc359491a78469d619f`  
		Last Modified: Sat, 11 Jan 2025 02:29:08 GMT  
		Size: 75.6 MB (75562527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2dfcc0e18869bd0274f52cfb6d69b2b26be2dc092a3a06c5b77d87d723cedd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90a5aa61a99692edff1a7f8b5bea460dd330ae00becd37008188470b449d7fb`

```dockerfile
```

-	Layers:
	-	`sha256:9a43307194e7d84c1dc2e7479ff97cd58253ccd5db18239c05c950c66d9f691e`  
		Last Modified: Sat, 11 Jan 2025 02:29:07 GMT  
		Size: 5.4 MB (5359564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78416cf9d605670ec874ff9ee09d5a7ba24dcf8486e447fabcf79bab0a223c1b`  
		Last Modified: Sat, 11 Jan 2025 02:29:07 GMT  
		Size: 11.6 KB (11570 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ce95b9903afa01eb591f8e20820c6025d13d16df3252a3eaf22a65f0d8ce1352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124261455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14e18af4e528ff530d538673012d299e24d62665881c033196a0b453b5c209c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2025 20:35:28 GMT
COPY /rootfs/ / # buildkit
# Fri, 10 Jan 2025 20:35:28 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=1.8.0_442.b06-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Fri, 10 Jan 2025 22:01:38 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a40fc02393a849ecb556016054b90c4bb62c50d5ac13a9617e59cc0d2b432b8`  
		Last Modified: Thu, 23 Jan 2025 18:28:55 GMT  
		Size: 59.7 MB (59671150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ad406d0d187950ae63878ffebe4735f387065216a606180c908314fa5944b4a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5349797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669c139484c6db7cd0a8069f01e583621cc26ca1d829cb4164afa711938b294f`

```dockerfile
```

-	Layers:
	-	`sha256:9627f50dbd597f8782925e839cdbe4c79ef459fd71ac606cd88b422490350803`  
		Last Modified: Thu, 23 Jan 2025 18:28:53 GMT  
		Size: 5.3 MB (5338063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d9cb9e8c8b8e87638c61a5ce0e9bdf1d1b35eb9122aa6e3654b220843ffea8`  
		Last Modified: Thu, 23 Jan 2025 18:28:52 GMT  
		Size: 11.7 KB (11734 bytes)  
		MIME: application/vnd.in-toto+json
