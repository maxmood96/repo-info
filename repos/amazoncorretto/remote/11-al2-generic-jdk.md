## `amazoncorretto:11-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:031567b1c054c660c1ec4308cc728b36a839f7295814aa395a484e5fb9cdbded
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:201f4fb41c5631668b753bab7b2e95ec6f54f66c25b30b21e88dea1c45a20eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (211045833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcb17228f9531bb9b6d04754fb8c90cd350439c78b87cf135adaae6a203b8f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:553ed992015a76bd7bd2b975b84fb4bb8d9fd1cc5d7f3cc5814806bd014114d7`  
		Last Modified: Thu, 15 May 2025 19:23:52 GMT  
		Size: 62.8 MB (62759985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62793b2fe15dae7110cfd55e7c36b23a9fd314dbdcaf98a285581e7daf363b95`  
		Last Modified: Mon, 19 May 2025 23:46:06 GMT  
		Size: 148.3 MB (148285848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cf52622c6efee8aa961c94a705c4e1537097f7ac098d900beae1e21b059f8cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea7bf2fbf751d9aa33dc389af288b903d76e56543fdf96f62c7f5293ecfa3b2`

```dockerfile
```

-	Layers:
	-	`sha256:e67aa02072bf64e9ff33c58387d6461df111951acab37c0580b0f4147290c91c`  
		Last Modified: Tue, 20 May 2025 00:47:19 GMT  
		Size: 5.5 MB (5535344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3528f584590e029007a811334d2773b3918744095a70bd308c35d14379def722`  
		Last Modified: Tue, 20 May 2025 00:47:20 GMT  
		Size: 11.3 KB (11254 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:539a237a305220035922978f848e7a13e0876c4180086d01221f3cbc684453b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209939486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992e765fbbd5baf3aad492ce2779fb6bb25f5e9daaa31a31d080e4bbf72deb89`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:1b914e688cac327114c45b9a58220765af260230389654eb4d8798d0a7d9676d`  
		Last Modified: Thu, 15 May 2025 19:24:15 GMT  
		Size: 64.6 MB (64607481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ddd43d51b59faf9892b662b9559a05952fef1b309459f4966cfbf2cf4bc329`  
		Last Modified: Tue, 20 May 2025 00:59:13 GMT  
		Size: 145.3 MB (145332005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:29e0a2e1d10568bd126eab5967262e98fc14020523119dcadaddff66b5b4b53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce729cff923fe555b8ad2c9a5acfaf725623be669c741a84f022eb243a3f0683`

```dockerfile
```

-	Layers:
	-	`sha256:81a43930b5342de205d0ae925f5461fa29e15a5579ddb4f243485a7b1179d4e2`  
		Last Modified: Tue, 20 May 2025 00:47:24 GMT  
		Size: 5.5 MB (5534838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25ba3cb19ffee40102e2da60d5ab52ff9103e827d74623c0941a416596c9df62`  
		Last Modified: Tue, 20 May 2025 00:47:24 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.in-toto+json
