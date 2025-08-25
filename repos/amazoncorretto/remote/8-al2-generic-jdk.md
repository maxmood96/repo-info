## `amazoncorretto:8-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:3dddca84fbdf1b5f38a6dddb91129d98e7d361bd8f0e4eacac8b3d0c362858be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:38e9d47ff37adc650de66bf3cf51e20dd775db240488d9e0618a829209561ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138631386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ab7faa8ba7bcc0aecb7b697c0fb712b81df2aaec09dc5d3728a03fdb80cfee`
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
	-	`sha256:f21a9c156d2ab29af4b5e451610a197ca56345598aa7ad950a22561b52bd146d`  
		Last Modified: Fri, 22 Aug 2025 17:34:29 GMT  
		Size: 63.0 MB (62978125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2d47bee61bc01341abad4e3405dc5a3670b4d03bee66f04d55eefa301f8e08`  
		Last Modified: Mon, 25 Aug 2025 20:18:29 GMT  
		Size: 75.7 MB (75653261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c4100a6cb4aa373d2ea7289de7a02eea1c75a283a3d1926996f870b82f7adb32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5386501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35386ad3c1940dd28c3eb1918328b4d73a10eb2d7be3429721aea017091ebbe`

```dockerfile
```

-	Layers:
	-	`sha256:c53ca431b746824390e9c3b228ac7990bd06385abc5bec0c5d1eae0fcc5ba74b`  
		Last Modified: Mon, 25 Aug 2025 21:49:54 GMT  
		Size: 5.4 MB (5374931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2639a5e380db4f3963fa858cc9e7316c80eb991f884d10f7f753823225a7fe64`  
		Last Modified: Mon, 25 Aug 2025 21:49:55 GMT  
		Size: 11.6 KB (11570 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-generic-jdk` - linux; arm64 variant v8

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

### `amazoncorretto:8-al2-generic-jdk` - unknown; unknown

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
