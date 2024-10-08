## `amazoncorretto:11-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:85345d94fd90028060faad682837803cc89fb43018688ecf377ce2c6ecfb766d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:aa6eebe1e88a13f7b0181fd79b9ffb477e5993ace046f700deff6a31341fef7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.8 MB (210836627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f624c42988b88fcbf3c26f94724d1bf3a54ffc2830d0d2454b156f30527f89a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=11.0.24.8-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f956a2176a592b2f85941102c85f1a745c5e74f263c66fc5212bf9eb619f28e1`  
		Last Modified: Thu, 03 Oct 2024 13:25:55 GMT  
		Size: 62.7 MB (62678156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97123ff2751023dde3b084c2145bcad8da2875ed6c6d786e3fa23327d3850537`  
		Last Modified: Mon, 07 Oct 2024 23:59:57 GMT  
		Size: 148.2 MB (148158471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:11d5b405d96ea899a2df0528b591369b02ac296d749beacf32a965ccefbdd454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f621cba9aff5282dfde15313f4a9a452a867d89a759e4309b5f1b59b6837e725`

```dockerfile
```

-	Layers:
	-	`sha256:f8de29281c5614c5d46384a42e68a0224174376a39db70b285a0439c6eb44a17`  
		Last Modified: Mon, 07 Oct 2024 23:59:55 GMT  
		Size: 5.5 MB (5535102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5e052b639bc7c284bacf364f37f698bd1585ed309e7da9f4cbd47fd1cb62ab8`  
		Last Modified: Mon, 07 Oct 2024 23:59:55 GMT  
		Size: 11.2 KB (11226 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:033a662bcb0cb61178856ae5d9fc9ebaa868167c716b25ed3ac88f9e87802eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209837146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1cdb0ca702bd2a7285a0473094d072529d4deb284f589e03bf6ed9669bc331`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 17:24:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 17:24:23 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=11.0.24.8-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:0f8111d5d1a15a517300f742a82fff488242d02ac685b3d2f019de97e880b603`  
		Last Modified: Thu, 19 Sep 2024 19:09:03 GMT  
		Size: 64.6 MB (64586547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b13a87f534870fa84dae6903173a18a87eed88600e81d4c1486e37022e68bcd`  
		Last Modified: Tue, 24 Sep 2024 02:29:53 GMT  
		Size: 145.3 MB (145250599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7906cca96238f55d47f5a08762204fe77b4840fddd1d7caa9b9ce29d0c507cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b10333768b5278b9b4117afe9293871b0fc9b990ee383ce2d7fa3b5b81f6ff`

```dockerfile
```

-	Layers:
	-	`sha256:181ad60f3e8a1bfe07704dbbb957b6e3881958504b666b3a145f90ec17624670`  
		Last Modified: Tue, 24 Sep 2024 02:29:48 GMT  
		Size: 5.5 MB (5534582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd95e8b9c0b8e5eee20dbcae167829cbfb3f5010baf56e8507f202f01515bd6d`  
		Last Modified: Tue, 24 Sep 2024 02:29:48 GMT  
		Size: 11.7 KB (11653 bytes)  
		MIME: application/vnd.in-toto+json
