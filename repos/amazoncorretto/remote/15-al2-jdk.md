## `amazoncorretto:15-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:d83dd6b4c2b2228432ae23b90741365db9dc932510b2b7011b61565abf61eda1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:15-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b64c71b04e648643faf267133ebbc410a2fef9363c00a398e69b67037a634e63
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217646704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:853b88ab45328d9e2a24d8f20135375ca4cbc7c7e4a4854bba4d7b25c4690dd1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 Jan 2021 22:19:43 GMT
ADD file:bcd0b903093ee2c81a54e8bdc50176f4038662ab936aa0d94af08458d508aef6 in / 
# Wed, 27 Jan 2021 22:19:43 GMT
CMD ["/bin/bash"]
# Wed, 27 Jan 2021 22:38:50 GMT
ARG version=15.0.2.7-1
# Wed, 27 Jan 2021 22:39:12 GMT
# ARGS: version=15.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 27 Jan 2021 22:39:12 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jan 2021 22:39:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:62350c28fdb7b7cbd0e199dd893555ed129ed85da482d882b1eeb574988ea7d6`  
		Last Modified: Wed, 27 Jan 2021 22:21:18 GMT  
		Size: 62.0 MB (61996576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cdee73068a7e3af58dfb2f91a67a5c54288bf2c2b61a8bdef797fef8137cc46`  
		Last Modified: Wed, 27 Jan 2021 22:40:49 GMT  
		Size: 155.7 MB (155650128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:15-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9d9e4c227a5ed666e210f76a61e1d0bb253a275ffc0642ab6d6a4d5520b6c7cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 MB (219249623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24135c6374bfd68fff6741e45337a4706acfc6529c17f8346d5ca9c03cebff65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 Jan 2021 23:09:56 GMT
ADD file:7f69686262e0e0e5415d42ac0371f7d0df0330bc4f0556e5d4b73dd78ceb1197 in / 
# Wed, 27 Jan 2021 23:10:02 GMT
CMD ["/bin/bash"]
# Wed, 27 Jan 2021 23:49:30 GMT
ARG version=15.0.2.7-1
# Wed, 27 Jan 2021 23:50:00 GMT
# ARGS: version=15.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 27 Jan 2021 23:50:02 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jan 2021 23:50:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:c6741bcf27a42820ff66e35cc842cec9a845e9e9dba4ff7bd465fc6161442a86`  
		Last Modified: Wed, 27 Jan 2021 23:11:10 GMT  
		Size: 63.7 MB (63704713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b68666620335f38cf95ebec188e1b987827b8bac236561b2eda344ccef1ecd47`  
		Last Modified: Wed, 27 Jan 2021 23:52:01 GMT  
		Size: 155.5 MB (155544910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
