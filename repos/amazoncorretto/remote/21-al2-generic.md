## `amazoncorretto:21-al2-generic`

```console
$ docker pull amazoncorretto@sha256:3664f91eacdcc0e5e804b9cd830ccbe57c1c2773c1e67096872d46901b45230f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7ae4dc65bd95fe871c029585d34363c5e00e646e9ea5cb780fd0ec974d34b8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228455636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295750348d8a6f430e4674cae7cc727cae7dac763b07cd2334ae2f61a4f640d1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:16 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:16 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:01 GMT
ARG version=21.0.9.11-1
# Thu, 15 Jan 2026 22:10:01 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 15 Jan 2026 22:10:01 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:10:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:89d3b5863331d6bb79d550bf0acce60aeac36e2c065470bf6d6f8d76c9cb6f4f`  
		Last Modified: Wed, 14 Jan 2026 13:13:55 GMT  
		Size: 62.9 MB (62940156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764343a8a8f79d8c00b1ec06bd8200f0f02fccf18829a21af3210a0530260cfb`  
		Last Modified: Thu, 15 Jan 2026 22:10:21 GMT  
		Size: 165.5 MB (165515480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b917cfc044ff89c6e6818ec01ac65c39e9a85f313f091fb8703ba631bc22c567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774213d0a94e0060b3d84eebe32409a55aa3560bff24837da56072e3e3ec1e68`

```dockerfile
```

-	Layers:
	-	`sha256:e1b0650aad5a54212a29faa43bbdb3a0489c22de7a0cfccff9e4133ccce35555`  
		Last Modified: Thu, 15 Jan 2026 22:10:18 GMT  
		Size: 5.5 MB (5535599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d79351049d609784139ffc0c3edc84e16c22ce0552c9b00db980ed0cdc20b4a`  
		Last Modified: Thu, 15 Jan 2026 22:50:38 GMT  
		Size: 11.2 KB (11206 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:82c395a2629a35fde448f5b98bb1f5c6169d353711e42ab6b3481c39f4340f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228335773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8436f12747935397be8c2b20afdc707cea9fdf1c0d2aa98caecc671b3c4356`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:03 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:03 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:09:28 GMT
ARG version=21.0.9.11-1
# Thu, 15 Jan 2026 22:09:28 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 15 Jan 2026 22:09:28 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:09:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:afb133ffe3cfc9458fcd28fa75abd002d894e187faa842d48d3c35c676633646`  
		Last Modified: Thu, 15 Jan 2026 07:47:55 GMT  
		Size: 64.8 MB (64770434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a500f859b9dda48b019ef3445c78f9ef24ca6838fb3acbf7d0421862e6bd73`  
		Last Modified: Thu, 15 Jan 2026 22:20:19 GMT  
		Size: 163.6 MB (163565339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:27ce172ca603b0aa57fd440ac9e68e35a96c3ec566d91474b962f6660fccb157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5545645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d0cd077f3de7b838359a593a4a0b1c82cdda1046b9f6c7ab145209e1b22fc8`

```dockerfile
```

-	Layers:
	-	`sha256:6e867f6d885e65ea334e33543c69cfa2eef7116c45ec0ee79247e6718e054a94`  
		Last Modified: Thu, 15 Jan 2026 22:50:44 GMT  
		Size: 5.5 MB (5534288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc468bf211db702ff88115c36310cc99ecd85562c11db11a1e4555564f79443e`  
		Last Modified: Thu, 15 Jan 2026 22:09:48 GMT  
		Size: 11.4 KB (11357 bytes)  
		MIME: application/vnd.in-toto+json
