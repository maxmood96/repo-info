## `amazoncorretto:latest`

```console
$ docker pull amazoncorretto@sha256:0c2c4df35e83b836e6f71faf01eae3ec98c2e7cba77e7a65345aed031595710c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:latest` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:25ce9aab0b30bcd17c6a2914cf42a01dbadb7727b83e4f7ae7682d638e52649a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138601771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996ed03191292d18bca533ab5ee5912a19916c962808810623ac6606fc185bb9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=1.8.0_452.b09-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=1.8.0_452.b09-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:c93eb42fc1cb8cbc6518e0c84a8b5166a23b8e065c2ea156492279ccf234ec25`  
		Last Modified: Fri, 13 Jun 2025 16:58:44 GMT  
		Size: 63.0 MB (62962939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edc54ec3599c16e4dfd631a20803c28205c24242d1f4d429c503804de3f368a`  
		Last Modified: Fri, 13 Jun 2025 17:03:30 GMT  
		Size: 75.6 MB (75638832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:latest` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:211c1a7a008720d16b292239099f76446f946cd5915ad2b8f564bdaa6b93d214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5386501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8bcb1f58182708f55f3262076ce427592bcfa93a8f16fb936a1b726b77bb79`

```dockerfile
```

-	Layers:
	-	`sha256:8e7ee75994fd017d7ac26794f50d41095140e973f78598a3b456409acb25fc4e`  
		Last Modified: Fri, 13 Jun 2025 18:49:42 GMT  
		Size: 5.4 MB (5374931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2c290f9086ca4b43e7b4f75a1c708a6f964aa8c02da34d2de48f2bedf2adaff`  
		Last Modified: Fri, 13 Jun 2025 18:49:43 GMT  
		Size: 11.6 KB (11570 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:latest` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0ad3d1f8268e80a21f53aca5c517ddf66dabe2a50cceeff031d12237cad3b359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124452002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ddd59726f6320099a17f6620b791f5c877e0cf76a590c9afcd62f4c0381ac8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=1.8.0_452.b09-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=1.8.0_452.b09-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:a3a141bfe5627b562a870ad931fe1cdc50d3dbf733a0568d089499010c9116cb`  
		Last Modified: Fri, 13 Jun 2025 17:05:27 GMT  
		Size: 64.8 MB (64790746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c0e8db55ba0608b29f8036dc93a60576d958743c6ff8f30379b8deece0f310`  
		Last Modified: Fri, 13 Jun 2025 19:50:44 GMT  
		Size: 59.7 MB (59661256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:latest` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:df9a4a147b2e79de189f91d9adc466c6031d3d927cad7f73b633f4532f898e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5365164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e87754027379e2531fffb6a62e7e36671def75d0346f20589a2167a6b0495c0`

```dockerfile
```

-	Layers:
	-	`sha256:e069448182947fd2aabbb0cac34831d1521ca0dc4e411a89c30b18c969c72f6d`  
		Last Modified: Fri, 13 Jun 2025 21:49:39 GMT  
		Size: 5.4 MB (5353430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42b79a65327b72c6a2f42a8f0a77094f345736ead680fa4ea962229ee53439c0`  
		Last Modified: Fri, 13 Jun 2025 21:49:40 GMT  
		Size: 11.7 KB (11734 bytes)  
		MIME: application/vnd.in-toto+json
