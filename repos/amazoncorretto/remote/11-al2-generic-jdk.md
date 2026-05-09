## `amazoncorretto:11-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:fe4c59f70f7a4113d7f72cc734f670e7bca0eb3fe897c4dbdd9647a9fbff4eb8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8396bfc2564046cabb0d092b601dce22a59f365130059eab8da7fb27145fa3c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (210990830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520ad66fa03541337c56bf4fd13d964595ec3a8e9b3e64685dd4905b68744a09`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:56:20 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:56:20 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:17:53 GMT
ARG version=11.0.31.11-1
# Sat, 09 May 2026 00:17:53 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 09 May 2026 00:17:53 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:17:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:3f708fc5705625846e206621966842bfead7ee5b8e4fc20aab0c77c563600126`  
		Last Modified: Wed, 06 May 2026 07:46:46 GMT  
		Size: 62.9 MB (62859738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e464088dbd5f6653e4e0c07b5f2d527d722f3bf507fd9fbb34d5e1cde22539`  
		Last Modified: Sat, 09 May 2026 00:18:14 GMT  
		Size: 148.1 MB (148131092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:42a83e997a4bd85491a634b3a46a1a2131913ab6c654ae62767ab780f31b237e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e724142143e8b39028232502f692836872a89e9cc76549353733c65aaab3b468`

```dockerfile
```

-	Layers:
	-	`sha256:dded482c215c3fa4ac342d511ccbc2c17eb54c32767fa26f2e847215aa50ee87`  
		Last Modified: Sat, 09 May 2026 00:18:10 GMT  
		Size: 5.5 MB (5543110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:698037e44ad8bdf976dee47b2dc8687fb6a8aaea33493905c84bdf41bc15fcb2`  
		Last Modified: Sat, 09 May 2026 00:18:10 GMT  
		Size: 11.2 KB (11212 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3cd982609d8bc8bb9c792137b17329c78d706c0bcef99e19d0500542d4cc8970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210178439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b53f0848cdca76d92e44aa7c54cbe034bb78c18217f618ac907df70d5d2e3c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:48:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:14 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:15:11 GMT
ARG version=11.0.31.11-1
# Sat, 09 May 2026 00:15:11 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 09 May 2026 00:15:11 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:15:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:835dd3779a793c24eeba54a176badcbf0ecf82042603b5459dd57e14ad679d47`  
		Last Modified: Wed, 06 May 2026 07:46:52 GMT  
		Size: 64.8 MB (64808915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb0a5f3a3c9dc710ff191a89cf4a8c47f22b985f703039c16f8aa64c070c82c`  
		Last Modified: Sat, 09 May 2026 00:15:32 GMT  
		Size: 145.4 MB (145369524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2fa0677cce8f5284ad8b7060fd0d4614ede65cd5d06920f55e8f724d3d0e821f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5553969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2483e7627caeff6bf0872701bf04b239641eb590fc3058dd4e6588107e4d0d`

```dockerfile
```

-	Layers:
	-	`sha256:357024ceec4cbcb91ee5643d329357a40d25ecddb5930a48dbf4445bd282fb03`  
		Last Modified: Sat, 09 May 2026 00:15:28 GMT  
		Size: 5.5 MB (5542604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11662b3b37f745630cf7764e5def9af5fa17fb74d652e98ff9458924f26e6cab`  
		Last Modified: Sat, 09 May 2026 00:15:28 GMT  
		Size: 11.4 KB (11365 bytes)  
		MIME: application/vnd.in-toto+json
