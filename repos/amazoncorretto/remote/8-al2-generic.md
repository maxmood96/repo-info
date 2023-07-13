## `amazoncorretto:8-al2-generic`

```console
$ docker pull amazoncorretto@sha256:ee5f5e320ce46609edd516a7878eb285abe7be2aa0e138ee387cd6d1fb3bd922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:be93801ed518e85576feb97ca04f717daf9cd9c99778625ac04a37f6fbd2936f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (138046713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60dc2910eed2cac3279993ee8373826a60397761c17de729169cb9bc861bc88b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Jul 2023 01:20:13 GMT
COPY dir:be29c71398840090bec7021ae8f2d354451564507602cf38257ad90a915b1838 in / 
# Thu, 13 Jul 2023 01:20:13 GMT
CMD ["/bin/bash"]
# Thu, 13 Jul 2023 01:37:04 GMT
ARG version=1.8.0_372.b07-1
# Thu, 13 Jul 2023 01:37:26 GMT
# ARGS: version=1.8.0_372.b07-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 13 Jul 2023 01:37:27 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jul 2023 01:37:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:e90aa42bc48ff728ab10fd485b42144e863dfd8689dd6ea94c78ac0357ec5101`  
		Last Modified: Fri, 30 Jun 2023 00:09:38 GMT  
		Size: 62.5 MB (62485766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af55887f9844f60718e431d2119c9d34d8e37fb63f3273a0e40626a231d03b0b`  
		Last Modified: Thu, 13 Jul 2023 01:48:42 GMT  
		Size: 75.6 MB (75560947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:00c05d1e0f15bd53ba6a842f5b47c6229362ed04f05e6165e9ca08865ec8a7e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123716384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd3317f7b7be62c61ebf3a3676c029b6b70263a50047a1384a190c5fa3b12c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Jul 2023 00:40:00 GMT
COPY dir:a284fdf4a484ebc9131c665fc151094ec73265d07d353476272944e301722064 in / 
# Thu, 13 Jul 2023 00:40:01 GMT
CMD ["/bin/bash"]
# Thu, 13 Jul 2023 01:04:13 GMT
ARG version=1.8.0_372.b07-1
# Thu, 13 Jul 2023 01:04:29 GMT
# ARGS: version=1.8.0_372.b07-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 13 Jul 2023 01:04:30 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jul 2023 01:04:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:20c8bca6ae5daad56b485a4b6f1f395a51727d69eb6a7566c53b00a366e46576`  
		Last Modified: Fri, 30 Jun 2023 17:38:06 GMT  
		Size: 64.1 MB (64128925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a9b1cb871f779ca6f5ef505173e5f822ff23abe34f85226a69534953940227`  
		Last Modified: Thu, 13 Jul 2023 01:12:50 GMT  
		Size: 59.6 MB (59587459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
