## `amazoncorretto:21-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:0bee3cd54b789bb54b9f6bfbf2d89615e225e587e6eada2c7ca0a191d4689332
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9cb4c2bdcf109591faf0a18fcbe321952d3bb648550ab79892be2890017840f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228702901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec35124075e9196b8ccc6ecb8b1c4059653cdfc2a9126354a0e335e50a411ce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:26 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:12:10 GMT
ARG version=21.0.11.10-1
# Tue, 09 Jun 2026 21:12:10 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 09 Jun 2026 21:12:10 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:12:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5791d5c110764fa8f2390f8d17939212dd64a2ca31a8a6a258f98c77bb152e47`  
		Last Modified: Tue, 09 Jun 2026 21:12:31 GMT  
		Size: 165.8 MB (165760951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:84fcb41dc4e3e4c693593702d4c8ad531fdf77c5407ffda351e8b72dde750716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5547733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffc3f2f4e31a614e559fba34aebdbc8b202b9c8ea5fd1b29f4d25bfedf08ba1`

```dockerfile
```

-	Layers:
	-	`sha256:f964b722e0541d3a635cd4d917e229801367d6a3c04525f6472dadee0b173667`  
		Last Modified: Tue, 09 Jun 2026 21:12:28 GMT  
		Size: 5.5 MB (5536520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9042e7373435fafee4830f4ef9a9d990ae683f880054699f46892090f59fd54d`  
		Last Modified: Tue, 09 Jun 2026 21:12:28 GMT  
		Size: 11.2 KB (11213 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2588d53455d18965688bb3975359ffd4b8321209800d415eb5c484e1467a9b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228693886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5289900dd44447de0cdde38e6aaca9d82668896a57e0678b1afbf6bae552d76f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:22 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:22 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:12:06 GMT
ARG version=21.0.11.10-1
# Tue, 09 Jun 2026 21:12:06 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 09 Jun 2026 21:12:06 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:12:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6a6813817c138e164f43ad54138149265c955b2755ac22261df33bc302aaf6`  
		Last Modified: Tue, 09 Jun 2026 21:12:28 GMT  
		Size: 163.9 MB (163903177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ead44c565b5128bde62acb76e8b2b3ff0ea4b9f38f10270a78465ab87ef50899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c669313919aa8ee776b201cbc68eb48699b958e4b253f3376a6a42b024c47b`

```dockerfile
```

-	Layers:
	-	`sha256:8256ca63ad0e8a67ac8a4ec3b63b2f8b440d15c2e721ecaaea79a72f52ff11ca`  
		Last Modified: Tue, 09 Jun 2026 21:12:25 GMT  
		Size: 5.5 MB (5535209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d6a0b774e0c47c7c002c11c40cd82fb9f443518e9b5ec375fe00d73fcdd7ed0`  
		Last Modified: Tue, 09 Jun 2026 21:12:24 GMT  
		Size: 11.4 KB (11365 bytes)  
		MIME: application/vnd.in-toto+json
