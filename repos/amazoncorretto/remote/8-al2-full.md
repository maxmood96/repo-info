## `amazoncorretto:8-al2-full`

```console
$ docker pull amazoncorretto@sha256:3ef40a7725225cd091f5520f29a155ee64228ee946cc60578fe760e7d00a2525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:07afdf315d8cb623bc86bfecad4ad0a136ce5c9696fa9b154c038aa521c62303
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137868426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5fe3f7eece9e24ea8c377ca51e5475e4415b4201af37cd86e585b0c2abe7f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Oct 2022 00:19:49 GMT
ADD file:33ce740675602f8911c110c617b08d74ebe9c26c82226b4815019d8c2d0a2263 in / 
# Fri, 21 Oct 2022 00:19:50 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 01:08:12 GMT
ARG version=1.8.0_352.b08-1
# Fri, 21 Oct 2022 01:08:33 GMT
# ARGS: version=1.8.0_352.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 21 Oct 2022 01:08:33 GMT
ENV LANG=C.UTF-8
# Fri, 21 Oct 2022 01:08:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:e3cfe889ce0a44ace07ec174bd2a7e9022e493956fba0069812a53f81a6040e2`  
		Last Modified: Wed, 19 Oct 2022 18:11:43 GMT  
		Size: 62.3 MB (62306642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16e5667014795f6356f1eca12b6db23f4d7b314fbbc976b833603bde6bcf1d4`  
		Last Modified: Fri, 21 Oct 2022 01:13:34 GMT  
		Size: 75.6 MB (75561784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b199d2cde87ca0a0e9b7d625ea56d3e8c56448b6e6576c580567271a022def34
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123513713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee11ea889de3c2c0e1416370b1c49a43d071e78ff94949b53aaf7cb8defec585`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Oct 2022 23:39:31 GMT
ADD file:45362bc0bb55d35f704a938eb431f8accb86d1bb8e52b78f3ef34eb141c3ed82 in / 
# Thu, 20 Oct 2022 23:39:32 GMT
CMD ["/bin/bash"]
# Wed, 26 Oct 2022 10:45:39 GMT
ARG version=1.8.0_352.b08-1
# Wed, 26 Oct 2022 10:45:56 GMT
# ARGS: version=1.8.0_352.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 26 Oct 2022 10:45:57 GMT
ENV LANG=C.UTF-8
# Wed, 26 Oct 2022 10:45:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:d900cba9f9f55565485a1181c89317c2718b6232095971d67af440a33db15594`  
		Last Modified: Wed, 19 Oct 2022 18:11:20 GMT  
		Size: 63.9 MB (63919869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0fce50e055487fffd4248a19eefeeb97d71de219bae42d71e2c4de48b703aa`  
		Last Modified: Wed, 26 Oct 2022 10:47:43 GMT  
		Size: 59.6 MB (59593844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
