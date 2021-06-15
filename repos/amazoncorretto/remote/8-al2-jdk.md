## `amazoncorretto:8-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:e633693a03f576923a12203d3fa91628626450cebeab710f9ff48d1bd98a76f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:34062aeeb7827aff5fec2ceff9cfc8684ddcdaa7bf99106c029ff88544461f7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137240949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab161ed37a2582ae003ac0c25c10cd44c988b0b93ba14f4431585e632795226`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:21:29 GMT
ADD file:7facd6480673cc20118310fb00de5f2fb1f31f41220c1f01c018c356b050e1da in / 
# Mon, 14 Jun 2021 22:21:30 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:38:22 GMT
ARG version=1.8.0_292.b10-1
# Mon, 14 Jun 2021 22:38:43 GMT
# ARGS: version=1.8.0_292.b10-1
RUN set -eux     && if [[ `arch` == 'aarch64' ]]; then version=1.8.0_292.b10-2; fi     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:38:43 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:38:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:da5a05f6fddb3b2b567304a69bdcf94cf158162626ff7340ffb02dcca421527d`  
		Last Modified: Mon, 14 Jun 2021 22:22:24 GMT  
		Size: 61.9 MB (61949057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e193093e22cf1a77fdcc1c527def33d1086e31d65ca054cbfb9d77d24deb473`  
		Last Modified: Mon, 14 Jun 2021 22:40:33 GMT  
		Size: 75.3 MB (75291892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:aba72985c215ae94d41cea675151b287e37a693ceb54c29203585b17708b0c5b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122839461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd7c95671cf56a308295921e3f825a9736c134059ee3abf470b08d8def96d50`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Jun 2021 22:39:28 GMT
ADD file:1e5a044f2dd0ca1b0b24b1a4df777782b2b0f5655cf99fbe5951b957da5ccfd5 in / 
# Mon, 14 Jun 2021 22:39:29 GMT
CMD ["/bin/bash"]
# Mon, 14 Jun 2021 22:56:28 GMT
ARG version=1.8.0_292.b10-1
# Mon, 14 Jun 2021 22:56:47 GMT
# ARGS: version=1.8.0_292.b10-1
RUN set -eux     && if [[ `arch` == 'aarch64' ]]; then version=1.8.0_292.b10-2; fi     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 14 Jun 2021 22:56:47 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 22:56:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f1cac48392624bb90cc2bd89c4956c0ac28470e25dadd636b84d4149cfea987b`  
		Last Modified: Mon, 14 Jun 2021 22:40:21 GMT  
		Size: 63.4 MB (63448527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9093114e80fa08ebd40a61b8d81f6c5747109872aa78c8b047b7fbd170f894`  
		Last Modified: Mon, 14 Jun 2021 22:58:38 GMT  
		Size: 59.4 MB (59390934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
