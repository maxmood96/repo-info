## `amazoncorretto:11-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:776e786d0b2b7e7b07f3ff1a7f5800468dae80def8ebd78026bd5be3ea4c223d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8cc41a2016b30820e484d1d1b686ce8fadf563978ec57d12f238fbd34483de66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.3 MB (211263729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c015e89f910d8a6ada02b2e464d7b77e3ad6e554d1dc4657d31eae99f210520e`
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
	-	`sha256:c93eb42fc1cb8cbc6518e0c84a8b5166a23b8e065c2ea156492279ccf234ec25`  
		Last Modified: Fri, 13 Jun 2025 16:58:44 GMT  
		Size: 63.0 MB (62962939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94257a018d3e9f5772f6e6292800ef2aed5b403abb6991c7db7841d955fc182c`  
		Last Modified: Fri, 13 Jun 2025 17:15:26 GMT  
		Size: 148.3 MB (148300790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d3cd658e113d5c29f7af0d60f4014f9d5183e29b35aa7b9729e9559df137cc7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5551033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed1f26cf3f6b65f98d5e2c26f2f48ca9836d660553a3ad1e48bc9ca2ea759ed`

```dockerfile
```

-	Layers:
	-	`sha256:8239489daa6b07f4491e02530c73dd2273a95c43f79e86409c506d24c07b9e6f`  
		Last Modified: Fri, 13 Jun 2025 18:47:18 GMT  
		Size: 5.5 MB (5539778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a68fb01adb66985cd03bb40a05c300e3f542ee881fb49e86b9267072c5d264cb`  
		Last Modified: Fri, 13 Jun 2025 18:47:19 GMT  
		Size: 11.3 KB (11255 bytes)  
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
