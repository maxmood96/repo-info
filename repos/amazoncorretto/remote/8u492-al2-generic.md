## `amazoncorretto:8u492-al2-generic`

```console
$ docker pull amazoncorretto@sha256:0e1e5eaa7270eb696d7e29596ead40bbdfb553fdf7c3d1f8e290caa606460e6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u492-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:af267850573bcb8602d8e2b091be887e8a5135c8079cc25e2e4a89e8f3afd660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138931857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575e197966980479eb994cdccda9823baf426f512f4a68006f9faeb1e229b75d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:39:12 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:39:12 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:10:49 GMT
ARG version=1.8.0_492.b09-1
# Mon, 04 May 2026 20:10:49 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 04 May 2026 20:10:49 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:10:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:1deb63baef8049d37b87192670264bba74a0207718cc43a1c66077f5bf81a3c8`  
		Last Modified: Sat, 02 May 2026 04:14:38 GMT  
		Size: 62.9 MB (62860009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c02de56533fff71bf18fbfad92f6106e8f409b7dd02965c624405e9ebf1699`  
		Last Modified: Mon, 04 May 2026 20:11:06 GMT  
		Size: 76.1 MB (76071848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ec0a1bd876b42e417a36a3143c508befdf13fb1be6295b4aaf22eddb6c76a78e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ac367fee0f53aa8fb95ddc5437e4e3dbf77d8a6983370262436a85fe8a715f`

```dockerfile
```

-	Layers:
	-	`sha256:23bd0b2b1e43c839444ae32c869b2d1c73dee1f31b2b81431b9a22ee0788daaa`  
		Last Modified: Mon, 04 May 2026 20:11:04 GMT  
		Size: 5.4 MB (5377455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:356be0ad03268017840acb0165247e18113fef1ec6d482137b8c96a87ae49b09`  
		Last Modified: Mon, 04 May 2026 20:11:04 GMT  
		Size: 11.5 KB (11527 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u492-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:379b555f09231a72d468b461abc7f57d17fc39c169f5420605ab71c954edb3ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124745704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872cee0b21618870e29c2647ea8f66b95e63e4fd582442edc09599ad819a5da4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:40:38 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:38 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:10:30 GMT
ARG version=1.8.0_492.b09-1
# Mon, 04 May 2026 20:10:30 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 04 May 2026 20:10:30 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:10:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:d78bec86efed585192790ef27ca98e5305604b02ec838239205e149e3aff726c`  
		Last Modified: Mon, 04 May 2026 10:12:23 GMT  
		Size: 64.8 MB (64795531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da2e05bee31f87c0f97d9a6b58641e0711b23eaad8853fe098cccf3966d6702`  
		Last Modified: Mon, 04 May 2026 20:10:45 GMT  
		Size: 60.0 MB (59950173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2f2bc137a5e44c486110801579f735f68853c94eb2609fb830aed4a79171e47a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d1496fe049ff57b9690865751a380f04631473bc64936c9c0b064e1a349906`

```dockerfile
```

-	Layers:
	-	`sha256:374f3bb2bc162294811b3edb10891512453844b4dc576a0070c6fef59e446cea`  
		Last Modified: Mon, 04 May 2026 20:10:43 GMT  
		Size: 5.4 MB (5355954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:004118c21dec23b611e2b434132e47c8e25246b52af39d8dd626275e4fc86008`  
		Last Modified: Mon, 04 May 2026 20:10:43 GMT  
		Size: 11.7 KB (11691 bytes)  
		MIME: application/vnd.in-toto+json
