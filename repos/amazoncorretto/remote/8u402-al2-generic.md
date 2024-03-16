## `amazoncorretto:8u402-al2-generic`

```console
$ docker pull amazoncorretto@sha256:087e2bffb73304ef707b58981801388ff58a003114ccee467dc6069071f02551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8u402-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ae412cf01acf30ceb90897b03b1b00d0f1e833a63e701085392b383212e391ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138180165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce664a4813e4d3b22a23c1bd572b251ac13d99e599ea0dd6bfef893f9b596acb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 16 Mar 2024 07:59:14 GMT
COPY dir:40a794c5e13cc08a029a91ecc5d045abb1bd5b12f20c10640fe8595ecfefa662 in / 
# Sat, 16 Mar 2024 07:59:14 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 13:31:05 GMT
ARG version=1.8.0_402.b08-1
# Sat, 16 Mar 2024 13:31:27 GMT
# ARGS: version=1.8.0_402.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 16 Mar 2024 13:31:27 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 13:31:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:fbbe555f6365629780fee590c2a87f84df704cf88725f26d12c40efd06a20308`  
		Last Modified: Mon, 11 Mar 2024 23:51:11 GMT  
		Size: 62.7 MB (62650553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8fb3e842b158f995b64b7e9c9b16fd7309e3efe721677a541055d89e9df989`  
		Last Modified: Sat, 16 Mar 2024 13:44:23 GMT  
		Size: 75.5 MB (75529612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8u402-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:840f539efcbb1d361ce06203cf4eb484e4bf78a0dfb26d2cbfd05a42a820c8be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124216753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47f9d0565ea0b7409747b679e280892781ee0d1c07733f0118be20bfdb1f439`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 16 Mar 2024 00:06:05 GMT
COPY dir:60a98a70510e647cb179bdf64e415936867e1b536f6e2209b88df6cf5ebf8753 in / 
# Sat, 16 Mar 2024 00:06:06 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 03:37:04 GMT
ARG version=1.8.0_402.b08-1
# Sat, 16 Mar 2024 03:37:21 GMT
# ARGS: version=1.8.0_402.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 16 Mar 2024 03:37:21 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 03:37:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:1210c2cda2cd148732bb93623044ab07d9ead686e335afc95ffa891e3032d56b`  
		Last Modified: Mon, 11 Mar 2024 22:40:31 GMT  
		Size: 64.6 MB (64576374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c4a5dc6036ac4e91c355d4d9d4d4f8f8414c13fe717274aa46b86813710d10`  
		Last Modified: Sat, 16 Mar 2024 03:49:55 GMT  
		Size: 59.6 MB (59640379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
