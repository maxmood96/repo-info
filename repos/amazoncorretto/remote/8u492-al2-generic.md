## `amazoncorretto:8u492-al2-generic`

```console
$ docker pull amazoncorretto@sha256:2fa846e0506e1c86e56d586a1aeb609ccffb1e27fa825ac70e6c8c92a677875f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u492-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:48a725c40ce83fca2c9504b6635484dd8172bfc70bb77d6f7609d1523dacc66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139091232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522f9530e615a928d5d41681baefcc4d3f74e05052fbbe94f8d319f9675b070d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Apr 2026 00:03:09 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:03:09 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:07:40 GMT
ARG version=1.8.0_492.b09-1
# Fri, 24 Apr 2026 00:07:40 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Apr 2026 00:07:40 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:07:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:e31bc602eae80620b93a07bcadec78ad83d112fa08abc35008da53ebf7ca3693`  
		Last Modified: Wed, 15 Apr 2026 10:04:45 GMT  
		Size: 63.0 MB (62952183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531adab3b047702ba6f5ca72b2356d3ef807ec1a89ef6c694bb3b982cfec2c42`  
		Last Modified: Fri, 24 Apr 2026 00:07:56 GMT  
		Size: 76.1 MB (76139049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d0c1fb4fc3777c5d104db0815d72dee363c85d5eea4cd36a12f516c18b8649f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e08cbb89acada5e01638ab8137f8b35d8ccd499f8dedb5af36e433b8eff583`

```dockerfile
```

-	Layers:
	-	`sha256:516715f155c06be2dcff3cb60065bfbb38dc80e7a7d6ef4f9eb8fc3dd5b0e575`  
		Last Modified: Fri, 24 Apr 2026 00:07:54 GMT  
		Size: 5.4 MB (5377455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adfb2cde9703bcb87fd5cd1815fbabe33e8c4ce2ef543f005a7b75ca8793ee53`  
		Last Modified: Fri, 24 Apr 2026 00:07:54 GMT  
		Size: 11.5 KB (11526 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u492-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1d426085c70345e0e27f13b1e62d52056c8bf90ff2aa88c325e9acf55eeac832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124757580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b56823e034d01a161577ea7f8d78e7969e73730867ba54468d036cbd4d59840`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:35 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:35 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:07:17 GMT
ARG version=1.8.0_492.b09-1
# Fri, 24 Apr 2026 00:07:17 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Apr 2026 00:07:17 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:07:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:0089d862b3b6e84c40891727df0dc5639dc509aa2f4dc6079056a5a3f8b526e1`  
		Last Modified: Wed, 15 Apr 2026 10:04:56 GMT  
		Size: 64.8 MB (64798783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3474265d81c23af61defdf241fb98bb0d0f2c53e1cf76dc78cc7bc4c49255290`  
		Last Modified: Fri, 24 Apr 2026 00:07:32 GMT  
		Size: 60.0 MB (59958797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:36d215656f575ecc7a8dcd6fe175a63d7bc2e94c6fa7977c4115968d72fc4aa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07856f1e57c398143267e85aeaa6927d70aad4268f816dbea44d3e1e274c4e5`

```dockerfile
```

-	Layers:
	-	`sha256:2574d8de31972872287d8646dfef88b9660c85ee8b97553281256e0abf2ba7bc`  
		Last Modified: Fri, 24 Apr 2026 00:07:31 GMT  
		Size: 5.4 MB (5355954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39e6bd3cd26fa75ba59146917c51033ea8121dc201aca43b18f1eaa0f1ff2257`  
		Last Modified: Fri, 24 Apr 2026 00:07:30 GMT  
		Size: 11.7 KB (11690 bytes)  
		MIME: application/vnd.in-toto+json
