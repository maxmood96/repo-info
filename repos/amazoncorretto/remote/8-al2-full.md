## `amazoncorretto:8-al2-full`

```console
$ docker pull amazoncorretto@sha256:2a0ae6c368e72418dd840fca49b02d7497b4a081ad0821d9f10d443dc90810aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:42db43a00ea7892b6452f6d73c98ddd30920ae7b1c6e4f571c917aa33e474da3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137459976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98fb27a1fff308cb6da6a0f441103d53a2e92b167f7e91cea63663fca2bb3a70`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Dec 2021 23:20:03 GMT
ADD file:4eca58da351122eac20ffd87e3af2c0313089cb81650bdd4c2ef95a556fb842a in / 
# Thu, 02 Dec 2021 23:20:04 GMT
CMD ["/bin/bash"]
# Fri, 03 Dec 2021 21:51:33 GMT
ARG version=1.8.0_312.b07-1
# Fri, 03 Dec 2021 21:51:54 GMT
# ARGS: version=1.8.0_312.b07-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 03 Dec 2021 21:51:55 GMT
ENV LANG=C.UTF-8
# Fri, 03 Dec 2021 21:51:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:8b8a142162d22658bdf0283afcd00a9dd216c6637943ffe5f2ba53c4e3da0bd9`  
		Last Modified: Thu, 02 Dec 2021 06:01:08 GMT  
		Size: 62.1 MB (62090346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe3b43bb0490ccea1d6ee1f0bd653842c7ffb4612702102b80f43f87b2aae5f`  
		Last Modified: Fri, 03 Dec 2021 21:54:57 GMT  
		Size: 75.4 MB (75369630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8a38c10e7224df35b0d79154bc2466bbd4f3938f12370fdd2ebe789d3e2339e8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123114020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce88a3163392738e0a2548988c0119b4ee5aa622832dcf181f7f37a45b801e00`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Dec 2021 21:25:17 GMT
ADD file:1f2ecfca149ab81a0527241077c1b366afd95b6b7a1dd91bddfd6c40988ba994 in / 
# Thu, 02 Dec 2021 21:25:18 GMT
CMD ["/bin/bash"]
# Fri, 03 Dec 2021 16:53:43 GMT
ARG version=1.8.0_312.b07-1
# Fri, 03 Dec 2021 16:53:57 GMT
# ARGS: version=1.8.0_312.b07-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 03 Dec 2021 16:53:57 GMT
ENV LANG=C.UTF-8
# Fri, 03 Dec 2021 16:53:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:74f9a6be36f3bc3bf6041c40376d548e3a8b720a0455674b19e9174a9e567078`  
		Last Modified: Thu, 02 Dec 2021 21:26:12 GMT  
		Size: 63.7 MB (63692547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e380661d8c49f1ce048c939ec67322f868aa0690533ec1facd5c8f752cddef9`  
		Last Modified: Fri, 03 Dec 2021 16:55:32 GMT  
		Size: 59.4 MB (59421473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
