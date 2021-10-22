## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:eac8bd7aafead38ec1e0be008814a23739cc7f94fce908326cf1a994c946a121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:768400671fc62342e08b2196d4e10c339016edde063d8b6d6739b0d43d6b9cc9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.7 MB (208746840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d771ee7508f49e3674f415bfafbc0d08976b9eb88d4579617a3e75db3620f3bd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Oct 2021 22:19:45 GMT
ADD file:7aef897e53c30ca977c42dd7692208abbd381b7d2e7e07a91d929f3f0ac4ea5c in / 
# Thu, 21 Oct 2021 22:19:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Oct 2021 23:28:10 GMT
ARG version=11.0.13.8-1
# Thu, 21 Oct 2021 23:28:33 GMT
# ARGS: version=11.0.13.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Oct 2021 23:28:34 GMT
ENV LANG=C.UTF-8
# Thu, 21 Oct 2021 23:28:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:5263c4cb36ce7acd05658a221ec502b376a281d7a6075ad09beb23ac02a7668c`  
		Last Modified: Wed, 20 Oct 2021 18:03:24 GMT  
		Size: 62.0 MB (61976108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9fa85bea77510327bc7908e11b491f6298bdc25fab855d9265928c2f0a9283`  
		Last Modified: Thu, 21 Oct 2021 23:32:02 GMT  
		Size: 146.8 MB (146770732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4da750ebb075e53d3bc6594d675df097918fb7e745a0b64a967d14cbfed43130
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.5 MB (207536407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382bf9989a84ee8b27cd6f523d54a681ec0d83467e10afe346f8f795680a5608`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Oct 2021 21:39:54 GMT
ADD file:d9148106dadecc4050f37ebf22ea9e7e56102619349368d1ce40d36f5e2fadd1 in / 
# Thu, 21 Oct 2021 21:39:55 GMT
CMD ["/bin/bash"]
# Fri, 22 Oct 2021 02:02:14 GMT
ARG version=11.0.13.8-1
# Fri, 22 Oct 2021 02:02:31 GMT
# ARGS: version=11.0.13.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 22 Oct 2021 02:02:31 GMT
ENV LANG=C.UTF-8
# Fri, 22 Oct 2021 02:02:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:e20b44047a77430ceb5678bf23278ca2841835a1b18a72adaace3d3a11c56031`  
		Last Modified: Thu, 21 Oct 2021 21:40:44 GMT  
		Size: 63.6 MB (63606878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1e16f0b5b1bca9c76f0e5b214a6125a30f4a670ac4de220530010565098437`  
		Last Modified: Fri, 22 Oct 2021 02:04:58 GMT  
		Size: 143.9 MB (143929529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
