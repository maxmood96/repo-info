## `amazoncorretto:8-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:cbe869d571ded0a13632918d1f3927a062b2ca7decf4d5731ef57068a3616f11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bdf881868cdf3c883e8a1a650af2425b89d5cdbbe82284e99728dc80805eddc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138381440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3766eb8b093fb0692c19873abf073d007a126805624727ee999a0d3e61c2028`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=1.8.0_452.b09-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=1.8.0_452.b09-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:d95443c3dbb00d5bc2eae8f837647b2757c14518822de8c1758b9842856c04b8`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 62.8 MB (62759330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0227c5aae73547a934fb63815da96c62e365586acf65eb08d84d013b26d33531`  
		Last Modified: Thu, 08 May 2025 17:06:35 GMT  
		Size: 75.6 MB (75622110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:99d9ee9931bceb77ffe76eed05ebb6d7c483bcb5e98e40b7c1a545d50a4744fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5374253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38906ceb4732cd80affe59b8288222c30137a2ed74cccc1fc404a600e79da738`

```dockerfile
```

-	Layers:
	-	`sha256:635d980264e65eaf03e0b5bb6dfd11220e65ddfc5b6142c94009de1564b47ea3`  
		Last Modified: Fri, 09 May 2025 01:09:15 GMT  
		Size: 5.4 MB (5362684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe8bab0a65d34e5e392370ec5804b1584752fa4c3269fa0b7a62148ccb18d2a8`  
		Last Modified: Fri, 09 May 2025 01:09:17 GMT  
		Size: 11.6 KB (11569 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1d58304f61dfd63414f91a558772a9507cd7904d0b924f719a90217a8d7ffbee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124246771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aaf59ebf80e690fc9cffd984d6447a8abc1441d4677a1b1e497c5ca89c72d11`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=1.8.0_452.b09-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=1.8.0_452.b09-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:08a465b69ed13c6a3d1f2674c3766151b11bcb021ca0e952f6a01f81b18fb3e8`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 64.6 MB (64594727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6add68a003d938ac1161e2aaf2bbca1ba506b410b64f978bd984643fbbf73876`  
		Last Modified: Thu, 08 May 2025 18:20:34 GMT  
		Size: 59.7 MB (59652044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:abfe4af84ff1a96f7788175108fd822f4bb8d4cd864d383dd193ffa18cdf900e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5352916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b4c1b3dd82ec9649a16e0176d61d2473ccd98c77557989162680164ce143e9`

```dockerfile
```

-	Layers:
	-	`sha256:bc135f044c000f321793493f790048e1218f6e3bf6959b4a148e2155c5fe400d`  
		Last Modified: Fri, 09 May 2025 01:09:17 GMT  
		Size: 5.3 MB (5341183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24508aee4ea448b836cda24b9b498c6ac75d81398c3e09c68040862cfd61b0b3`  
		Last Modified: Fri, 09 May 2025 01:09:19 GMT  
		Size: 11.7 KB (11733 bytes)  
		MIME: application/vnd.in-toto+json
