## `amazoncorretto:8-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:4fa1e1606b129d1aa8e3430d2981a5d8d7bc221ea2104edf7d89cf4bf0cc3454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:59ab0e29c7a293b47e3e9c03e1c44df7a789950e198f7f3de98b4cee666b3ab8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137325816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bae6056b8dd3cff7e76b5b2602257fcde360d42ed6a8abcf56d4df470e931b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Oct 2021 22:19:45 GMT
ADD file:7aef897e53c30ca977c42dd7692208abbd381b7d2e7e07a91d929f3f0ac4ea5c in / 
# Thu, 21 Oct 2021 22:19:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Oct 2021 23:27:29 GMT
ARG version=1.8.0_312.b07-1
# Thu, 21 Oct 2021 23:27:52 GMT
# ARGS: version=1.8.0_312.b07-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Oct 2021 23:27:53 GMT
ENV LANG=C.UTF-8
# Thu, 21 Oct 2021 23:27:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:5263c4cb36ce7acd05658a221ec502b376a281d7a6075ad09beb23ac02a7668c`  
		Last Modified: Wed, 20 Oct 2021 18:03:24 GMT  
		Size: 62.0 MB (61976108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac86beca6e639f46bebdda9736b71ea89cebec1525062d5799d75b0f8c16832f`  
		Last Modified: Thu, 21 Oct 2021 23:31:21 GMT  
		Size: 75.3 MB (75349708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8a29d95ee341cf640b12796b53e40b7cf8bac71bfff188d10877be09bbeaaf1b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123020607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d706cfbc4650d9c82b64bb03a8f6c1cee043da645a9f1f7d924dac375fb1306`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Oct 2021 21:39:54 GMT
ADD file:d9148106dadecc4050f37ebf22ea9e7e56102619349368d1ce40d36f5e2fadd1 in / 
# Thu, 21 Oct 2021 21:39:55 GMT
CMD ["/bin/bash"]
# Fri, 22 Oct 2021 02:01:52 GMT
ARG version=1.8.0_312.b07-1
# Fri, 22 Oct 2021 02:02:06 GMT
# ARGS: version=1.8.0_312.b07-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 22 Oct 2021 02:02:06 GMT
ENV LANG=C.UTF-8
# Fri, 22 Oct 2021 02:02:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:e20b44047a77430ceb5678bf23278ca2841835a1b18a72adaace3d3a11c56031`  
		Last Modified: Thu, 21 Oct 2021 21:40:44 GMT  
		Size: 63.6 MB (63606878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2e72ff0622db143d0731cf2b734b5329bbf5df22f1349f84bccd7548919acc`  
		Last Modified: Fri, 22 Oct 2021 02:04:21 GMT  
		Size: 59.4 MB (59413729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
