## `amazoncorretto:17-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:363a288394fea55d08fdb55c4bbc2a36cf3de2ccfc7753774a404af03659db34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7dad09d4a0ae7bb993728d4f61a9e128e03fb9b1dddf34b3b8a2eca8c3e70692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214926805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588f956a2e5784aade095b7ef04fa76592e9f3635957eefd61b82dc988be74b6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:78d6b943ec35657899afc44f3f9b766ee923d9028028da721b7d4e7bc35e184f`  
		Last Modified: Tue, 23 Jul 2024 13:50:25 GMT  
		Size: 62.7 MB (62679166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16d1356ff865ed2ae4a8317d0fc95d8da710d367d04ec8a934e449d8ff736a1`  
		Last Modified: Thu, 25 Jul 2024 21:02:15 GMT  
		Size: 152.2 MB (152247639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:89910eb62d56f5fb7d142499ee2bc2ed3b0afc6ad97f328a5a8cf8fec106ce05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef9687d9af85339ed1e153f4ccfb51f8e01dca9792c0c73c30cb83d86343f61`

```dockerfile
```

-	Layers:
	-	`sha256:5cd84c8842b122bce4a1680e30fab57be7b36246aa6a8f043518f826aea85dec`  
		Last Modified: Thu, 25 Jul 2024 21:02:12 GMT  
		Size: 5.5 MB (5526938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26a7d06af902b9998d9671ee415af8ea111b4eb627701696dbfd4f64283347f2`  
		Last Modified: Thu, 25 Jul 2024 21:02:12 GMT  
		Size: 11.2 KB (11218 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:20453aadfa817aff708e96dd22f84b883f34f8bd7db112c9570a1179fa9a8e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215437570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9367599159146d8dda76baaad1ba415082b3fbbe1ec7e592fa5a646cc06cb9c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:7ae84cee97a8a17573116f568e78a8d7c8415a733e0ccb92185dd2e22634f9c6`  
		Last Modified: Tue, 23 Jul 2024 13:50:38 GMT  
		Size: 64.6 MB (64572700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f08078bcd6ff02413b92cd814007d7a725cbdd0f413bb3010cb3ee4a81ea9bf`  
		Last Modified: Fri, 26 Jul 2024 01:55:19 GMT  
		Size: 150.9 MB (150864870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0bc84b3ad5fc6b5d6b2d045ea54db0a8aaa4acfd7e41f22afc9f51cd647f86b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5537278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d46bb9cfff48e356df09b07399cc706236f3c488ae47823c995616f52163ed`

```dockerfile
```

-	Layers:
	-	`sha256:678032d8ec57a23312bc6b657ac4ba820d12697adf0e1141b8880464612646f5`  
		Last Modified: Fri, 26 Jul 2024 01:55:16 GMT  
		Size: 5.5 MB (5525625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2a340cc93b0c9921ffe00d4474b81949e28a295f14f90c39568d4e36f8afcfb`  
		Last Modified: Fri, 26 Jul 2024 01:55:15 GMT  
		Size: 11.7 KB (11653 bytes)  
		MIME: application/vnd.in-toto+json
