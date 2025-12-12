## `amazoncorretto:11-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:48e0967cffa6d6fd863c722ba86e4f2aae4cd3d39a56a098f8504d6a49b2a357
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:41cd15d2bf3b6229e57221c2dce54e0f0ee339bf991b7c86fa07b2c9c8ec4673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (210992276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2540f44a62a826caf3c336ab486c865f46ea6d5e8a8fb85243ed0da1319583c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:30 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:30 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:11:16 GMT
ARG version=11.0.29.7-1
# Thu, 11 Dec 2025 22:11:16 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 11 Dec 2025 22:11:16 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:11:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:364e8e668f0e62a54627e7d364c5d2a3a16f70f1c962628fd84b9ef8fb667d21`  
		Last Modified: Thu, 11 Dec 2025 05:04:46 GMT  
		Size: 62.9 MB (62940975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8810818f7605218d14faba2899daa8d60dfe8037b7990f38c5097686d92d84`  
		Last Modified: Thu, 11 Dec 2025 22:12:01 GMT  
		Size: 148.1 MB (148051301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9fc7f81e887a8672f10a2344d8b78b58bdefba83f6d4df69e3cc31a594d825c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b69de0dbb03b154e4a2f23d24d8da29602d4c5ebec0cbe137da0d304afac59`

```dockerfile
```

-	Layers:
	-	`sha256:016f030ee2ef3e08040ea671f8fff53d3e50b1a6d893bae446249added261358`  
		Last Modified: Thu, 11 Dec 2025 22:47:19 GMT  
		Size: 5.5 MB (5543009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c77ba6a6bac230ee38a963eb75129860d8bcc4626414ff9840242ede05faba6`  
		Last Modified: Thu, 11 Dec 2025 22:47:19 GMT  
		Size: 11.2 KB (11212 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1d9165152b5eaca5c93ea024697317638ad332b7ade6caa0f563f2776abe5b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209940299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea43cfd4f9eeb973a5d0e04ee32dc972ce56aa863d6aaf7d32ca8fb88c6cbbf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:28 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:28 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:11:24 GMT
ARG version=11.0.29.7-1
# Thu, 11 Dec 2025 22:11:24 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 11 Dec 2025 22:11:24 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:11:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c137c3709cb6578b5ff011e0fe71f764cfaa69a84b9a9702891d15a17d0b2124`  
		Last Modified: Thu, 11 Dec 2025 22:18:43 GMT  
		Size: 145.1 MB (145144544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4eb5bd205dea425adeb4fa5bcf5b5fb20b0811df3e17efb608dafd8db5d90231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5553867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35cb222a870a6b7a24a518b8a93821b33ceb0cbb5d33e2f0ac9b639e76f8dae`

```dockerfile
```

-	Layers:
	-	`sha256:ed3f78a4a323c15b87e212f61d42eb157f1b564635144d39ea4097ab7c7f30ea`  
		Last Modified: Thu, 11 Dec 2025 22:47:25 GMT  
		Size: 5.5 MB (5542503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d62e72bcbf6214621f7ffb871e40d5e590d1f60a77332dc14a6e070586c9d241`  
		Last Modified: Thu, 11 Dec 2025 22:47:26 GMT  
		Size: 11.4 KB (11364 bytes)  
		MIME: application/vnd.in-toto+json
