## `amazoncorretto:17-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:bad4f17bfbfb7e1c4859f4f8de880519c3ca60174a827fceaa0e1d583b490441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f1407e43169b50da5e1d1279f3ec06e466290a03e8f847299dc85395f5412a5b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.6 MB (213565113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc059d0340e767de3d0b0956d5450cd35a321764d0fa9c85cd564ab87a8af9cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Oct 2021 22:19:45 GMT
ADD file:7aef897e53c30ca977c42dd7692208abbd381b7d2e7e07a91d929f3f0ac4ea5c in / 
# Thu, 21 Oct 2021 22:19:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Oct 2021 23:29:20 GMT
ARG version=17.0.0.35-1
# Thu, 21 Oct 2021 23:29:42 GMT
# ARGS: version=17.0.0.35-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Oct 2021 23:29:43 GMT
ENV LANG=C.UTF-8
# Thu, 21 Oct 2021 23:29:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:5263c4cb36ce7acd05658a221ec502b376a281d7a6075ad09beb23ac02a7668c`  
		Last Modified: Wed, 20 Oct 2021 18:03:24 GMT  
		Size: 62.0 MB (61976108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94a4ce83cf1e0c99f9d2c484933a8fe32145d269ae18ec0672d58c17a95cd5a`  
		Last Modified: Thu, 21 Oct 2021 23:33:14 GMT  
		Size: 151.6 MB (151589005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f26316e2564d93c4627fd6f36bd3efa5730c8bd51d9c6476e10492895865625c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213742880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d629a5baaa8744e2de59a633c1d3ee4ce93d60588b9fb67aa1c73d30b61faa7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Oct 2021 21:39:54 GMT
ADD file:d9148106dadecc4050f37ebf22ea9e7e56102619349368d1ce40d36f5e2fadd1 in / 
# Thu, 21 Oct 2021 21:39:55 GMT
CMD ["/bin/bash"]
# Fri, 22 Oct 2021 02:03:05 GMT
ARG version=17.0.0.35-1
# Fri, 22 Oct 2021 02:03:25 GMT
# ARGS: version=17.0.0.35-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 22 Oct 2021 02:03:25 GMT
ENV LANG=C.UTF-8
# Fri, 22 Oct 2021 02:03:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:e20b44047a77430ceb5678bf23278ca2841835a1b18a72adaace3d3a11c56031`  
		Last Modified: Thu, 21 Oct 2021 21:40:44 GMT  
		Size: 63.6 MB (63606878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea730173577e5dbc5a1b417334dcc54fcae44c0cbaa5209b220d27f3435f1f5`  
		Last Modified: Fri, 22 Oct 2021 02:06:07 GMT  
		Size: 150.1 MB (150136002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
