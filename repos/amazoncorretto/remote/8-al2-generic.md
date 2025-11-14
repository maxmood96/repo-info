## `amazoncorretto:8-al2-generic`

```console
$ docker pull amazoncorretto@sha256:827098f53a84c41a64f82e41ed69b4c335d3ac9167832bfcc3498f5ea72d5406
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:745a05d69e6eb6464346cc4a07e7669dcc8d7761c9fee145128ea51d6ad9bf23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138973701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2133fcfb6b547a55ab29ed5e46d1dff94697489fe060f778176126fb5aa50ea8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:59 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:59 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:14:05 GMT
ARG version=1.8.0_472.b08-1
# Fri, 14 Nov 2025 02:14:05 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 14 Nov 2025 02:14:05 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:14:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4f778b828927a548aac19be726dfcfecc006ab044b72c43bffff784fd5318e`  
		Last Modified: Fri, 14 Nov 2025 02:15:12 GMT  
		Size: 76.0 MB (76043129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0039f9929026fe81a0bcb7eb335c6432ac7fdd367a2578a38f895913a23eadf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c146b92e8b349d7432c0c8335bf4aaa316ebdbd62383aafbfa13c039e855d180`

```dockerfile
```

-	Layers:
	-	`sha256:7344f40f3ba84c2392fa5593c302ceff2c110458c14255ff0145ce9f67ec268e`  
		Last Modified: Fri, 14 Nov 2025 04:51:27 GMT  
		Size: 5.4 MB (5377358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed81111a16d0aa4c19870bb11d46a05ac44586a8c1d4b6489b70be09f84593f`  
		Last Modified: Fri, 14 Nov 2025 04:51:29 GMT  
		Size: 11.5 KB (11527 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0a327d03d07617cc3488d64bc54e733fcdc9ac1071529ebc9d4b932b7c3bfb88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124911882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d5200be3fbbe041292dd8aaab4258e57d4bba8e829655dce90eccaeb7b905f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:55 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:55 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:14:10 GMT
ARG version=1.8.0_472.b08-1
# Fri, 14 Nov 2025 02:14:10 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 14 Nov 2025 02:14:10 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:14:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c3f5dbd2a8b15f4cf535cdf778733a42929423d33a86e69f9714169993ae82`  
		Last Modified: Fri, 14 Nov 2025 02:15:15 GMT  
		Size: 60.1 MB (60119081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:11bd258c813fcc940845483a4ee3f2b75d8f5eddbfed7ac18565730d921181be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52fc69e0dcea812458bda08edeb514658be1c4fd93921ba68f3148606ca815a5`

```dockerfile
```

-	Layers:
	-	`sha256:169c8821b34eef0f67c294fcfce3a2ee9d322a2547880e5c0f0f40414142c391`  
		Last Modified: Fri, 14 Nov 2025 04:51:35 GMT  
		Size: 5.4 MB (5355857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9921852c727dcafe4628795acfbc45d8370d12601c9bc7f8681f6bda4b95df87`  
		Last Modified: Fri, 14 Nov 2025 04:51:35 GMT  
		Size: 11.7 KB (11691 bytes)  
		MIME: application/vnd.in-toto+json
