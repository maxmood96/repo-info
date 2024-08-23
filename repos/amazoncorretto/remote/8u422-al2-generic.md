## `amazoncorretto:8u422-al2-generic`

```console
$ docker pull amazoncorretto@sha256:52b1b0a7eeaec471252598b6c0ed723b17895465817411261b9567e4c9efb60c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-al2-generic` - linux; amd64

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

### `amazoncorretto:8u422-al2-generic` - unknown; unknown

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

### `amazoncorretto:8u422-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6f10cca4e12027f080829f719be7f6ccab695fa360af8417991342a4c17ca52c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124243621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25353e718660756fbbc881147e442b8a42f4fc6b4eb24804867bfca9f6a425f8`
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
	-	`sha256:90f49a0942af5d23537faf4773696e5a1ede92273c5b8379a6acc52111436bb8`  
		Last Modified: Tue, 20 Aug 2024 21:34:48 GMT  
		Size: 64.6 MB (64587135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51194aa775abd535d6ba8363f73e8c4765cc77216b018ac1ca6567c21b859467`  
		Last Modified: Fri, 23 Aug 2024 02:16:06 GMT  
		Size: 59.7 MB (59656486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:47a5f45b9dbd812049abfec5f94f7c3969bfc30ee08bd95e57383fbd8dc284f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bad7d563f7cc3d6b07e647867bbd439509f142bebaa371e25ced8c227d27e989`

```dockerfile
```

-	Layers:
	-	`sha256:1ec393a54c6c9653f17074d7efb51aa46690c0db2cfe317f2364387f1ef11ff1`  
		Last Modified: Fri, 23 Aug 2024 02:16:04 GMT  
		Size: 5.3 MB (5348237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2959961f4e85d7edd30bcabdf2385d535ae8072a9c03f9ccf240c04e8e9a11c3`  
		Last Modified: Fri, 23 Aug 2024 02:16:04 GMT  
		Size: 12.0 KB (11981 bytes)  
		MIME: application/vnd.in-toto+json
