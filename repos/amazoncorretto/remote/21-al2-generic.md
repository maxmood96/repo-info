## `amazoncorretto:21-al2-generic`

```console
$ docker pull amazoncorretto@sha256:cbae4fac2af2df50b411c532f5a7af9ce56f00768298854a24c76057c6817106
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:645638815f86d9e95e6dff63bdb61cea8552cfa20a30475086a330f9e3620376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228507155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae0299745d7204c4129572e978b377ef4a66c08ab9bcb26dc2fa3343b99e474`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:14:13 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:14:13 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:31:49 GMT
ARG version=21.0.10.7-1
# Tue, 10 Feb 2026 18:31:49 GMT
# ARGS: version=21.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 10 Feb 2026 18:31:49 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:31:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:f5abe3fbfd395e17e5203e7213ac7dbf150f56cd98e8268563339f7d27569870`  
		Last Modified: Tue, 10 Feb 2026 14:46:03 GMT  
		Size: 63.0 MB (62958957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3745b42022da445724f2547e61ae0b2dc6b897418dde7d9377a2fb3f5b48d3`  
		Last Modified: Tue, 10 Feb 2026 18:32:09 GMT  
		Size: 165.5 MB (165548198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8288eefb0844b0b5860d97bc913bd14af504ac73c93f902d31b9e143b050fd34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9589d67a5b50190680bb27cd9f3570892fd14e46c7393247e33065887410561b`

```dockerfile
```

-	Layers:
	-	`sha256:519bd3217ca01a4ce1d338d523fee6dadec11975948d0e5fa4dd8f0718e57818`  
		Last Modified: Tue, 10 Feb 2026 18:32:06 GMT  
		Size: 5.5 MB (5535607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5a912fe5ea6a87433b81903bf9ec7ab4b669558446829d45db7133ea3ff09b4`  
		Last Modified: Tue, 10 Feb 2026 18:32:06 GMT  
		Size: 11.2 KB (11211 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1de69983143c9d2a6334b10c3e4e484499180a79c2c2b5ebf1a634a55054582c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228410219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eefd1c79252de4b7ad74c539db5363e2d34fca5ae56721bb38f0b10896af0c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:14:03 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:14:03 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:31:44 GMT
ARG version=21.0.10.7-1
# Tue, 10 Feb 2026 18:31:44 GMT
# ARGS: version=21.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 10 Feb 2026 18:31:44 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:31:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:7b625f12eaf5f52ff71ffa6d83678b0481194ed88dfaa20ee4b8481abb9ba247`  
		Last Modified: Tue, 10 Feb 2026 18:14:19 GMT  
		Size: 64.8 MB (64799476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e50ffd073f08c33ad517c912c06075cc5cb34829d2b2b85c9cfa28d50726889`  
		Last Modified: Tue, 10 Feb 2026 18:32:06 GMT  
		Size: 163.6 MB (163610743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:07e385c4cda4b1d63696bebfdc80035338d63203181c4588205aeca58afbe5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5545660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17d3f65813e30ef1328880ae9d2a3af36ad2878339e67c6e09696eac35730d9a`

```dockerfile
```

-	Layers:
	-	`sha256:2cd67e4e31ad48418de4450f63ee2394c3b5cc4ef1834baf3739bfac1baab6b3`  
		Last Modified: Tue, 10 Feb 2026 18:32:03 GMT  
		Size: 5.5 MB (5534296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04ff12bb9f698ca7729c7948133d6dc520487777e313fead62c68371d7c362b2`  
		Last Modified: Tue, 10 Feb 2026 18:32:03 GMT  
		Size: 11.4 KB (11364 bytes)  
		MIME: application/vnd.in-toto+json
