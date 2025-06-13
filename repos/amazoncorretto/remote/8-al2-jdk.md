## `amazoncorretto:8-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:224f78dc3c8a93b26a9f5a91a63d1ee1474c60ef6f5f42ae813377caab11ee14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-jdk` - linux; amd64

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

### `amazoncorretto:8-al2-jdk` - unknown; unknown

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

### `amazoncorretto:8-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0bd897b1c2f093d14abc3f34a7b580b9abd7c9c266df76f58780bc35d6fa0d1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124277370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfeddbb002bf295d9665cf0b1681d78d89633e822841814f3878ed6e447a5f84`
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
	-	`sha256:1b914e688cac327114c45b9a58220765af260230389654eb4d8798d0a7d9676d`  
		Last Modified: Thu, 15 May 2025 19:24:15 GMT  
		Size: 64.6 MB (64607481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb3b2712e189e0631ebe7dd80180ee04b03d459ad71401283a9ad0ad1561536`  
		Last Modified: Tue, 20 May 2025 00:52:07 GMT  
		Size: 59.7 MB (59669889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:97e7bec504a219de1c9cdbfc1ef52f418a2e1b20d6ee62c88acd30c5085abb02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bea23600939ac67d1f2a7c3e661ca711b6ff0f6c4b99bda7396fdd2fabdfaa2`

```dockerfile
```

-	Layers:
	-	`sha256:269291439d561be64c94b75356d69e41c59c54089677903f244b5ccb741ecef7`  
		Last Modified: Tue, 20 May 2025 00:50:35 GMT  
		Size: 5.3 MB (5348996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba1f9d1f793ef6e4a665576713d1400af2a9b5e00769695d06a97228014ef6a5`  
		Last Modified: Tue, 20 May 2025 00:50:35 GMT  
		Size: 11.7 KB (11734 bytes)  
		MIME: application/vnd.in-toto+json
