## `amazoncorretto:8u462-al2-generic`

```console
$ docker pull amazoncorretto@sha256:e1840fb04df4de838bbef22a3328ab5ff514a0ed681013a79fefb580756424b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u462-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b17c2a460b526febe0967d4eb0ab09025668d64edc4cfd10787e3600877e0413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138597970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996510ddf2ff2bb31c4fdb6af5a655f9d2a8decc731733121726b493aeb8b04a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=1.8.0_462.b08-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:dcefe03e9009da4739e237894f3fe49af6782d53d9e2202e46127bd568617855`  
		Last Modified: Sat, 09 Aug 2025 04:15:21 GMT  
		Size: 63.0 MB (62959372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39db7ac6ff7998d3ba3f82d40efc7b780dc838bdfe378bd477dd9e0a84b8dc14`  
		Last Modified: Wed, 13 Aug 2025 23:11:34 GMT  
		Size: 75.6 MB (75638598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:78fcdaf2bc6172240e9438a501f110f68f199387c3f3d2d4ba1af74a3a519595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5386501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28830d24cc991ac3c6bdda4adaae7ee98de5e3ee305e45c4146a5270e6f18bf8`

```dockerfile
```

-	Layers:
	-	`sha256:c49a197c6c3eeebf65a5ff056200075c6827b31bf16028141bd0439fcaad483a`  
		Last Modified: Thu, 14 Aug 2025 00:49:56 GMT  
		Size: 5.4 MB (5374931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f75c1b78afbc30edcf03878a1769558d0775a02bf1c65ad42df7d38108e0e5c9`  
		Last Modified: Thu, 14 Aug 2025 00:49:57 GMT  
		Size: 11.6 KB (11570 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u462-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:40cf1175d475085835e6dee6f93e42658883ef7be3505d9d026dcb9b38b365a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124458073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:496b6a8134c16150b8c3de16c118c5bbd1467a3ae412f5b9854566cb0159536e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=1.8.0_462.b08-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:2c5df7aef58ef9598380ed47447cb5a8a274be6648b1015fa328f378b9e2da76`  
		Last Modified: Wed, 13 Aug 2025 22:57:44 GMT  
		Size: 64.8 MB (64794364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d538537e0d73d255d35180edec69f83bcb5c0c727eeaaec07e80b9ad0116e1`  
		Last Modified: Thu, 14 Aug 2025 08:49:45 GMT  
		Size: 59.7 MB (59663709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9d9d3f0479e495ccb9d5a392b6ca42588bd40915d53f2620bffeedb09a86bba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5365163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132a6b4278ab34aa3d82506f56a85094a5963c0254ca8aaf59e94a8dbede9188`

```dockerfile
```

-	Layers:
	-	`sha256:9a21467d8edacf3a10b193a673c08b35babe9be9cd56ed62fbc3be3ac6d4a13b`  
		Last Modified: Thu, 14 Aug 2025 09:49:41 GMT  
		Size: 5.4 MB (5353430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2c5d685760f442f3f71567038d894f280bfd0160835e39e5979a83a79ba8244`  
		Last Modified: Thu, 14 Aug 2025 09:49:42 GMT  
		Size: 11.7 KB (11733 bytes)  
		MIME: application/vnd.in-toto+json
