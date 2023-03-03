## `amazoncorretto:19-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:0f5f3ccad683d3ad81dfffc875c5ef6e421a879ac1ba5093ac943ddd9c7c6c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:19-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ad9c96c62af9f3b00d1a94ce2f7c1401daa47b6e4fb4f4312ce600fa42a6fef8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221805808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bc81e7f78c23e7b4beb22f7ddb0d350dee16bbc37b9a044d9567e4ab6dddf6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Mar 2023 22:19:50 GMT
COPY dir:d2afcd884fd8e8edf2c9d3cff550c5573438d40a5b14c0bcde9ea94f2fad31f9 in / 
# Thu, 02 Mar 2023 22:19:51 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 23:19:53 GMT
ARG version=19.0.2.7-1
# Thu, 02 Mar 2023 23:20:17 GMT
# ARGS: version=19.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-19-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-19-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 02 Mar 2023 23:20:18 GMT
ENV LANG=C.UTF-8
# Thu, 02 Mar 2023 23:20:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-19-amazon-corretto
```

-	Layers:
	-	`sha256:65e7c8d35fc567b9f18bb2fe2de2c278d644adafea6fc7487a3a40d8693ef6dc`  
		Last Modified: Tue, 28 Feb 2023 20:08:25 GMT  
		Size: 62.4 MB (62389508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4af6cd22cac4688b02c27e43e2c2a0c3dd64ef66d6d27dfdc7505dc311aab82`  
		Last Modified: Thu, 02 Mar 2023 23:24:19 GMT  
		Size: 159.4 MB (159416300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:19-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:327d2a11f2bfdbe2c4cfad28dc75aec74354a1e9c1e840bfd9d59d287c217b9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221850168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92f22208de2b0793ab1b40da4d42a65ab02288560f56017c5ec4e56893c11b0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Mar 2023 22:39:28 GMT
COPY dir:82034448b19235d709c5681caa8414343fb6e1711c03e26721c451fa22d139eb in / 
# Thu, 02 Mar 2023 22:39:28 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 23:49:34 GMT
ARG version=19.0.2.7-1
# Thu, 02 Mar 2023 23:49:54 GMT
# ARGS: version=19.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-19-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-19-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 02 Mar 2023 23:49:55 GMT
ENV LANG=C.UTF-8
# Thu, 02 Mar 2023 23:49:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-19-amazon-corretto
```

-	Layers:
	-	`sha256:ff7a305ba0c9eeef6825ac8bbba292756a82e85d36e370fc6294d9b7cf402a6b`  
		Last Modified: Wed, 01 Mar 2023 07:58:02 GMT  
		Size: 64.0 MB (63999614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c25d901578c5ac2dd375e24a4a21e0623a9507c21c7475f83759d8122a1f69`  
		Last Modified: Thu, 02 Mar 2023 23:52:12 GMT  
		Size: 157.9 MB (157850554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
