## `amazoncorretto:19-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:ec346fa782608946b65816d1429e17488f4c9296cbb42c5119eaa0e60df6aaf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:19-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1fafdadbe002d50f34aef28c40b5f9d48e243d9fc8b4151eae2dc97dea2dd872
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221791762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2898c5b2a3dc87787462b6319c91add31896842edfc50f13ffb9d8a3aba9f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Feb 2023 21:20:09 GMT
ADD file:29cd40b7c56d98385ece53bcbadfefd25bc70ccf0326777986ef6a5720bdfe83 in / 
# Thu, 16 Feb 2023 21:20:10 GMT
CMD ["/bin/bash"]
# Thu, 16 Feb 2023 21:41:10 GMT
ARG version=19.0.2.7-1
# Thu, 16 Feb 2023 21:41:34 GMT
# ARGS: version=19.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-19-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-19-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 16 Feb 2023 21:41:35 GMT
ENV LANG=C.UTF-8
# Thu, 16 Feb 2023 21:41:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-19-amazon-corretto
```

-	Layers:
	-	`sha256:d78505e615251c4f4af6eaa9507b67917d263d23551dcc5a1eed3c012d32a54d`  
		Last Modified: Wed, 15 Feb 2023 00:09:42 GMT  
		Size: 62.4 MB (62386320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ba0ac365005fede813f9be71bd31927c6294f54f94d6a50b019275601b6be8`  
		Last Modified: Thu, 16 Feb 2023 21:45:36 GMT  
		Size: 159.4 MB (159405442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:19-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a864c1fc7fe8e4efd8d1a9ceb1bc0294039c22beef77ed3ccf4bca359458e3ff
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221852147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a7ab9fbe7c2dc08ec298af547a6fba4318f4640561497aedbac1a19aafb2d8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Feb 2023 20:39:31 GMT
ADD file:17574026c2754afa903450c59a6d8f7d0905209b174cbe9c13252a61d5a6f916 in / 
# Thu, 16 Feb 2023 20:39:31 GMT
CMD ["/bin/bash"]
# Thu, 16 Feb 2023 21:06:49 GMT
ARG version=19.0.2.7-1
# Thu, 16 Feb 2023 21:07:08 GMT
# ARGS: version=19.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-19-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-19-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 16 Feb 2023 21:07:10 GMT
ENV LANG=C.UTF-8
# Thu, 16 Feb 2023 21:07:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-19-amazon-corretto
```

-	Layers:
	-	`sha256:71343c2791199c6e2c19c308cff6493497a02f57e225c11405e1934dc7428b3c`  
		Last Modified: Wed, 15 Feb 2023 03:16:17 GMT  
		Size: 64.0 MB (64003805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5f48e6fc41e6b7a87249fddddc322ba82eb6b526998e2369a74e0a5fe13935`  
		Last Modified: Thu, 16 Feb 2023 21:09:21 GMT  
		Size: 157.8 MB (157848342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
