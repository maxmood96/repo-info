## `amazoncorretto:11-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:f91651c22f05fb7241ec1e19983b6dfc33ce816a22df7a1987d408fc294e12a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c9699f7d36d6f5fda6775348f35784d48586447d5d4b0aac78ec4cab1676d0df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.1 MB (210115913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a111b8e09e6a4b4a729c118a9dbd682cb5930d9d21bc8594391747a3ddaa43`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Dec 2022 01:19:49 GMT
ADD file:a69ca7a5499bcd9d6e4317fdbd7256e93be44364bb746f5da10b4268c090bda0 in / 
# Fri, 16 Dec 2022 01:19:50 GMT
CMD ["/bin/bash"]
# Wed, 18 Jan 2023 20:23:49 GMT
ARG version=11.0.18.10-1
# Wed, 18 Jan 2023 20:24:14 GMT
# ARGS: version=11.0.18.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 18 Jan 2023 20:24:15 GMT
ENV LANG=C.UTF-8
# Wed, 18 Jan 2023 20:24:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:5b4a36b5b78f93a5f470cf722b313bb32cddb0f8e0fa0db348059b5c0881b04f`  
		Last Modified: Thu, 15 Dec 2022 23:08:20 GMT  
		Size: 62.3 MB (62328625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f55f2021815a051cafaba1ebe12a8234c8d17320223fc81d0409df4084c28fd`  
		Last Modified: Wed, 18 Jan 2023 20:35:12 GMT  
		Size: 147.8 MB (147787288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5dae2f381781da83f728bf4795460eeeb033e26185969fb4b0aacb8cfbd85c18
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208920389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6b56df4279b64474ed003c0929851eedb68da07e06fb3fa39c0eaced6f43b4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Dec 2022 00:41:05 GMT
ADD file:26a6bf75c84c408d289e5569f13b1c65206966f875cdfc53ded0670cb85e35bf in / 
# Fri, 16 Dec 2022 00:41:07 GMT
CMD ["/bin/bash"]
# Wed, 18 Jan 2023 20:39:58 GMT
ARG version=11.0.18.10-1
# Wed, 18 Jan 2023 20:40:16 GMT
# ARGS: version=11.0.18.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 18 Jan 2023 20:40:17 GMT
ENV LANG=C.UTF-8
# Wed, 18 Jan 2023 20:40:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:6cbfee25f0741b3d3f4d2474d904a200cd8404a01aa17813bf3fc3d4ebb551a4`  
		Last Modified: Thu, 15 Dec 2022 23:08:20 GMT  
		Size: 64.0 MB (63964214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec844dce5e3e166143eef9f0213107e39132eeb0a192b134af1c48df884cbd2`  
		Last Modified: Wed, 18 Jan 2023 20:44:28 GMT  
		Size: 145.0 MB (144956175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
