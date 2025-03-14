## `amazoncorretto:21-al2-generic`

```console
$ docker pull amazoncorretto@sha256:5a05e062d9ee9617087088a889cb08e86fb5be9332ed2a50f961782477edf2a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cb13a99ac04f95b123043ebb186ef6aaeb84aa53e6fb31d15acb480c53276ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227591660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0d761a5d449f44163c7283c11dfec5398bb4823bebde7ac31ecc0c9940c96c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:f3dc83dc2e4e000fd189efee126db80e38a079b47b8e5229a794a0a6148bfec6`  
		Last Modified: Sat, 08 Mar 2025 04:13:59 GMT  
		Size: 62.8 MB (62772838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d780df9adcbd4f85fae763ecd2a7c4d99ab147a0e44e15e0f45784ba50fa4a`  
		Last Modified: Thu, 13 Mar 2025 22:53:06 GMT  
		Size: 164.8 MB (164818822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:be7b68c4922bf1e82116d6e010b88d65eb5ab73677d3cff4720a6acdca467679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5528248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0124ce79a89abfcd7bb6785de52f4a1c6528aa52f6a82e2b192ede192d57d77a`

```dockerfile
```

-	Layers:
	-	`sha256:e365a78ce822e240619cc17fc3b0beccf9c43c0a47759b56b91ae79cd947e751`  
		Last Modified: Thu, 13 Mar 2025 22:53:04 GMT  
		Size: 5.5 MB (5517001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c6d50c20b4fda821b54b64d1293d61c65264f63dc2c27b33161b3ad523008e8`  
		Last Modified: Thu, 13 Mar 2025 22:53:04 GMT  
		Size: 11.2 KB (11247 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7edc7f3ac14dda279516553e64cc83e1266273844635d3e888803f10de4e8024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227331908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd983d70c9d30139322d10f2bc01393a5c146b406a9f461a9a35db5aaef7a62`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:5270c35d4d9446d8a0ab2f41ab0020c11889bd8617236093cc9c87563d120b9e`  
		Last Modified: Wed, 26 Feb 2025 15:57:39 GMT  
		Size: 64.5 MB (64521208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9033b51658d3a3d4c550c89424db4382b2da4dfd6525286c8e303377d9c05bce`  
		Last Modified: Thu, 27 Feb 2025 21:21:38 GMT  
		Size: 162.8 MB (162810700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3ffbc751421b0758de5d3d908a78a063df04306aeca5ac3bfc2957106897a34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5527090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25e847f1ea7c6af60c33701f86f9c1884e2efe7580516c8727cbe6370fefd9d`

```dockerfile
```

-	Layers:
	-	`sha256:95ed4a3799914bf0057376585b6333477fc05e27714ec637932bec47c89d9a3b`  
		Last Modified: Thu, 27 Feb 2025 21:21:34 GMT  
		Size: 5.5 MB (5515690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6baa0a0e60d4b24fea4ee38ea173a66a6b50044ba3744040db9ada4a97e4f9e3`  
		Last Modified: Thu, 27 Feb 2025 21:21:34 GMT  
		Size: 11.4 KB (11400 bytes)  
		MIME: application/vnd.in-toto+json
