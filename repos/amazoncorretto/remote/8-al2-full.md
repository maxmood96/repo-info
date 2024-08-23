## `amazoncorretto:8-al2-full`

```console
$ docker pull amazoncorretto@sha256:d04cdc134a2c5b9d18406c2c5fdec266a2097ddb2b05a7f61e49be8b733e20de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:32ad42000166503d40340c3981b9639a0306579fa5e54c3aad59acc49b58a879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138207129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c594b122ef9a4101f46752da455a60addebb37464192f4607ad817c39b86dc05`
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
	-	`sha256:6eeabd86b075e80cf303c4a0348cf048d31ba6ae2d42b051bb230016153f8809`  
		Last Modified: Tue, 20 Aug 2024 21:34:48 GMT  
		Size: 62.7 MB (62659944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229dec7daf8721ff1984dc04adc130496f3d6b98671d467ae9fbde93cb0cfbdb`  
		Last Modified: Fri, 23 Aug 2024 01:50:14 GMT  
		Size: 75.5 MB (75547185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0b019c9b21448cbd81b6dbb0014ddfd7aac52152a163c370d501ac4166940166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5381226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3c7691103cd3008ee7586d47cf65b1614ce10ee98fe9104f8b3cbeae5f35fa`

```dockerfile
```

-	Layers:
	-	`sha256:f8485ce3be0920b7ca8bea71f5d2dc8881c7428538c75453178eaa58e3165879`  
		Last Modified: Fri, 23 Aug 2024 01:50:13 GMT  
		Size: 5.4 MB (5369690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ef90d0790e5b51f4d505744d17cacdd9c434512bdc0b957aa813caf2ef6628f`  
		Last Modified: Fri, 23 Aug 2024 01:50:13 GMT  
		Size: 11.5 KB (11536 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-full` - linux; arm64 variant v8

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

### `amazoncorretto:8-al2-full` - unknown; unknown

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
