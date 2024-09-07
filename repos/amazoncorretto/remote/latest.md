## `amazoncorretto:latest`

```console
$ docker pull amazoncorretto@sha256:ca2d8fc1637cce74d4f298e05ca2f9018ec0c849f09857819190cd361db564d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:latest` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:902ac740ad87dc9c354de9b8c302695dcdbdb30816ad8e3649481fd23872a3e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138279617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97297debf1bbfe72bf6cea7e986c3184e5394f444b716a6d408eec54bda8f59`
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
	-	`sha256:7f8efc14a219454ff8f309d236d31a55327a6ff05dda42df51689619d9a34fdc`  
		Last Modified: Fri, 06 Sep 2024 18:59:36 GMT  
		Size: 62.7 MB (62695547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acd6f160fefd8d375edf6f1fb1df3872323b95d4ab484acb4428295c5977fd0`  
		Last Modified: Sat, 07 Sep 2024 01:05:46 GMT  
		Size: 75.6 MB (75584070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:latest` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c743260d8ba9e0180ec56d905cc5d22938f93491fb3427830b8c9798bee49755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5381226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa7cc24bff7c7d1814ff6b41b087136f654e898113313062193d6b7d1e647a2`

```dockerfile
```

-	Layers:
	-	`sha256:1f8296bb8b911472dd89315d02d5e898f907ad9ee1b01b57f9ee08a5e348a0d9`  
		Last Modified: Sat, 07 Sep 2024 01:05:45 GMT  
		Size: 5.4 MB (5369690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3e38e60025aacd0de5ecc165c88ac850b8cd1788cd0f1ae64850dde81fa7152`  
		Last Modified: Sat, 07 Sep 2024 01:05:45 GMT  
		Size: 11.5 KB (11536 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:latest` - linux; arm64 variant v8

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

### `amazoncorretto:latest` - unknown; unknown

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
