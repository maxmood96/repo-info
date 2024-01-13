## `amazoncorretto:8-al2-generic`

```console
$ docker pull amazoncorretto@sha256:0484bde7f5ae7b7a0092219cc43c1a0c83928142719104c472b07218f3e80275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3c693b221c10ed7f1367960afc37b913db0d6c93266826d8d7ef41ac139da09f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138260004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e1a80cf4df61fd83b2fa41366c4955c668ca1ca7830fbc969b043636763aa5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jan 2024 21:45:52 GMT
COPY dir:b97e45ed3c8a3f1b9f45748b11869cc647c58d36ef808547c8bfc5893d6bcdef in / 
# Fri, 12 Jan 2024 21:45:53 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 22:14:35 GMT
ARG version=1.8.0_392.b08-1
# Fri, 12 Jan 2024 22:14:57 GMT
# ARGS: version=1.8.0_392.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 12 Jan 2024 22:14:57 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 22:14:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:1243323cbbce9384c54ac7f8354a552ac222dc3ce5d0ece482a667a33fce339c`  
		Last Modified: Thu, 11 Jan 2024 06:58:33 GMT  
		Size: 62.7 MB (62661001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6cabfc44baf04764162d5ccf437d05c5ed37327513a9a4edc6cbaeade6d739`  
		Last Modified: Fri, 12 Jan 2024 22:27:45 GMT  
		Size: 75.6 MB (75599003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7ec0867152fb0e011f6056a22eaf88542940b6b2629272f1757828f2d9b95f99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124072064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad353c95f8807cc4c3cdf42aff6f68aa2a3ffa5fcb762c0a8cd5de64d59e4e8d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jan 2024 21:49:23 GMT
COPY dir:eb2de4474e28d9fde9bbe1ffb630978f47dae30856e760ca73ebb5d0cb75efd7 in / 
# Fri, 12 Jan 2024 21:49:24 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 22:29:30 GMT
ARG version=1.8.0_392.b08-1
# Fri, 12 Jan 2024 22:29:46 GMT
# ARGS: version=1.8.0_392.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 12 Jan 2024 22:29:46 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 22:29:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:9620bfd6832ce2ca50093b819c4f62fd86c4b96a997fd5da88afa856b28cb1a0`  
		Last Modified: Fri, 12 Jan 2024 19:03:15 GMT  
		Size: 64.5 MB (64462448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50909be413c3460ab9a71b817b9f8d6bb20f2335ec1c36a06e21ce537e413ce8`  
		Last Modified: Fri, 12 Jan 2024 22:39:05 GMT  
		Size: 59.6 MB (59609616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
