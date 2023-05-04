## `amazoncorretto:20-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:16ac1bbacff745a8691b47003db27f741b018f30066939cbeafa3324ca731e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:20-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8fbf7e779b50d75cab6b60b6b51f87e56cfe1a1d226656cb8741f2af2168d305
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223284322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2f4900eb4b5003e59c4d9dabb390f51fa3d46be1650a35213cbd6b1eb1923d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 04 May 2023 19:20:10 GMT
COPY dir:e8a4b2d0bb4f52911c2b1115b27842bc606a63bd56c8563ded4e6b898fe187d1 in / 
# Thu, 04 May 2023 19:20:10 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 19:42:11 GMT
ARG version=20.0.1.9-1
# Thu, 04 May 2023 19:42:34 GMT
# ARGS: version=20.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 04 May 2023 19:42:34 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 19:42:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
```

-	Layers:
	-	`sha256:7cbd40bc2978b9c91c4cf0a5064302062d07242909f83ad9d8d7e2a2d379cf03`  
		Last Modified: Tue, 25 Apr 2023 00:08:27 GMT  
		Size: 62.5 MB (62512332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f759079f01a2b6c5bb35d99a13862abb3d5341784e524a82aa32150b8e02973`  
		Last Modified: Thu, 04 May 2023 19:48:02 GMT  
		Size: 160.8 MB (160771990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:20-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e085f8bf2492d8ec7446f396a7c7bbe431d5a28b12da4fd465de34fefe8a8845
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222924652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a87a7cf27b391c76dd78259caed2bb0568902567acef508742a75bc2f40dfe5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Mar 2023 18:40:10 GMT
COPY dir:1d0df99dbb2a961dca382ec30c27f40e06635a9186a0715c0d2a629262a04288 in / 
# Tue, 28 Mar 2023 18:40:10 GMT
CMD ["/bin/bash"]
# Thu, 20 Apr 2023 17:44:42 GMT
ARG version=20.0.1.9-1
# Thu, 20 Apr 2023 17:45:01 GMT
# ARGS: version=20.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 20 Apr 2023 17:45:03 GMT
ENV LANG=C.UTF-8
# Thu, 20 Apr 2023 17:45:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
```

-	Layers:
	-	`sha256:949542da27c3c0ab979766d37f455344960f838d9f661b9db50bec634ca7149e`  
		Last Modified: Thu, 23 Mar 2023 21:25:53 GMT  
		Size: 64.1 MB (64126936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326861e0858fb720e441d99b1013c16ce38babcfb00fc569a730c114d214cf75`  
		Last Modified: Thu, 20 Apr 2023 17:56:16 GMT  
		Size: 158.8 MB (158797716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
