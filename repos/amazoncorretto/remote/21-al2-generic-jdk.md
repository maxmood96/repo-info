## `amazoncorretto:21-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:ad00d1e1bdf6cb857cf021b8b86a406656be47f627306d1eb14d202c384556c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2ab8a7c47c0ab8a70fa3663b2880aaa3af9c672a0eb23b0cfc3574aee8d2a57a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228416660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7dd07912d8c9b60ca273e0ef4fe7a55cf384e147295be2c3195942534268b59`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:45 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:25 GMT
ARG version=21.0.9.10-1
# Fri, 31 Oct 2025 00:12:25 GMT
# ARGS: version=21.0.9.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 31 Oct 2025 00:12:25 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:2e3ea9592aad33f5f11ca8c65604905de30de68b0c38dfad7dee51b605c2a2c5`  
		Last Modified: Thu, 30 Oct 2025 03:52:34 GMT  
		Size: 62.9 MB (62934068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b8bf1a2d41e5961e041978e350f514e0b16151864da2fa18fedc6f348e6f0f`  
		Last Modified: Fri, 31 Oct 2025 01:11:23 GMT  
		Size: 165.5 MB (165482592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:45efbbd39880d4673c16bdf1ad40f8b2dd5482989f76d4e882d44bd356176fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b906eb88eb848ed290f008b88aeb155dbf99f1b1e23715c1228e2f4f8e6298`

```dockerfile
```

-	Layers:
	-	`sha256:0bdc93130b78f628f8b2e77ee262b9c06e8b4f709ca1486b06060011aa3cd85e`  
		Last Modified: Fri, 31 Oct 2025 02:16:14 GMT  
		Size: 5.5 MB (5535595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26358deb73ea75768d69917144380483704a52fa8b9984985896321c6a85b805`  
		Last Modified: Fri, 31 Oct 2025 02:16:15 GMT  
		Size: 11.2 KB (11206 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c582727847b3ff71ff68ab90b31e721f5ca1e4f88e4562724c933954484991ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228380863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f4f1bfa84e3f215d3b180e69b605a7f7afbdd7f40a550abe108626e778e557`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:47 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:47 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:49 GMT
ARG version=21.0.9.10-1
# Fri, 31 Oct 2025 00:12:49 GMT
# ARGS: version=21.0.9.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 31 Oct 2025 00:12:49 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:2875a69d1768080ef2331610c2aea8f8cfff54b5df360eb9feb01240a7526ff5`  
		Last Modified: Thu, 30 Oct 2025 23:15:16 GMT  
		Size: 64.8 MB (64793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd1baf4e91e00d7b9956781f2599d36622339644d5c2a7ec70735ba3ae40162`  
		Last Modified: Fri, 31 Oct 2025 01:13:02 GMT  
		Size: 163.6 MB (163587405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c38690057a0f316854022b0515c274d0a2ce72c5ff9fd7b09d5afa449db7fe8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5545642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb422a046bae094b1b75dd2e292f9764e9cc272f82afcece5237a1bfb39ae18d`

```dockerfile
```

-	Layers:
	-	`sha256:0ade4b6ee07edfc08d05300569652153a787c6f09c49d3b9f9fb82700f3d7681`  
		Last Modified: Fri, 31 Oct 2025 02:16:09 GMT  
		Size: 5.5 MB (5534284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad86952dca33d47a39c706c540492b89ced6981ef151d134b9c8351cf915b63a`  
		Last Modified: Fri, 31 Oct 2025 02:16:10 GMT  
		Size: 11.4 KB (11358 bytes)  
		MIME: application/vnd.in-toto+json
