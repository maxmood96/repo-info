## `amazoncorretto:8-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:c06220663543eb09ce8baa0ec1872f68a127bcec083154d713b44ad06818dcdc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dddbe7fec3670ec75732cdf900322077c92c204d13445b40602ad5460d619787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138247498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e615bf42e60bc00863c2d86238aa8a634442ee12f84c4e318eaa0f7a448714`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=1.8.0_422.b05-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:78d6b943ec35657899afc44f3f9b766ee923d9028028da721b7d4e7bc35e184f`  
		Last Modified: Tue, 23 Jul 2024 13:50:25 GMT  
		Size: 62.7 MB (62679166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba3e469516848c9e5827a5c193c9649717e5fc70dc9e65985a1ab4065891012`  
		Last Modified: Thu, 25 Jul 2024 21:01:03 GMT  
		Size: 75.6 MB (75568332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:65b5b7426aa04cd1b9ce9dcdf4d7a5983549fbb2bbde7750a8d70879780b38ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5381209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5e848492e671925cdd8604dff30f87e154a41c81becdc8157136958a69755b`

```dockerfile
```

-	Layers:
	-	`sha256:20abda2d400349ccfb3c4af15010bdeed77fea841f084088c5dbcf15b65810a8`  
		Last Modified: Thu, 25 Jul 2024 21:01:02 GMT  
		Size: 5.4 MB (5369674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa20c8a7c40e547f7d2319b39963dc91076222b084d177f3e28dd04cc58d566b`  
		Last Modified: Thu, 25 Jul 2024 21:01:02 GMT  
		Size: 11.5 KB (11535 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:56cccfeda8ab21be186a20bbd1d4ba08018ee418f58179acf650d80e84fdcc4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124228739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a546b79e7393ea2709e92b546a65e0290d4fecfcfe0e03373b0d5bd5264734e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=1.8.0_422.b05-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:7ae84cee97a8a17573116f568e78a8d7c8415a733e0ccb92185dd2e22634f9c6`  
		Last Modified: Tue, 23 Jul 2024 13:50:38 GMT  
		Size: 64.6 MB (64572700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1a293592675dedef36879a73d5ca3a5f38d1373c13888a09927e61b13d983c`  
		Last Modified: Fri, 26 Jul 2024 01:46:03 GMT  
		Size: 59.7 MB (59656039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8d64c7c06f89fc33a3da0fef460271a604cf78641727541e8e25235b85fb00d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4abd8b93cfa39a8c46b299bd6d7433f1c62359df3580a24dc35110a04d734f67`

```dockerfile
```

-	Layers:
	-	`sha256:b027f84d4569c74c936115459deb4648cd2e6d0647c84498d174c865e3edb979`  
		Last Modified: Fri, 26 Jul 2024 01:46:01 GMT  
		Size: 5.3 MB (5348221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7051fccb331d3138bc93d93b6d78b9f8129bbab12b27212ab93f02e86081991a`  
		Last Modified: Fri, 26 Jul 2024 01:46:01 GMT  
		Size: 12.0 KB (11981 bytes)  
		MIME: application/vnd.in-toto+json
