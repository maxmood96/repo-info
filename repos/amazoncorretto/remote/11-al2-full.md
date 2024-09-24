## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:f275d279c6ba9c23787aa90de9dcda1d79c8c74f56f2f39bf9c5a1f880e70ecf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c733122108b8c1c153e926188b44368b55a83f8719413fa0f492941aae87b0eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.8 MB (210840610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cedac30310a240bc1bb293c42ea44f70aa15352e1a7e099f9b3bc1b0d4cc29b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 17:24:19 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 17:24:19 GMT
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
	-	`sha256:69e49d0477d7418fa8148e4dd5ab6e7b541cf2bdf558ddd0198722553d8ecfb8`  
		Last Modified: Thu, 19 Sep 2024 19:08:50 GMT  
		Size: 62.7 MB (62678534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479f09e35e6e3627bcbcdd37ab192f0cc30f108878818892166a0c48c63e9ef5`  
		Last Modified: Tue, 24 Sep 2024 01:56:43 GMT  
		Size: 148.2 MB (148162076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:497ff65033ed8259540585805c2af3fb1bfcfaf68d7094d1d7a48814c8a6d1a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 KB (11002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98900d57614d0b5891183fb16bb6585b4db7effc8e4be06cae706a1d2244616f`

```dockerfile
```

-	Layers:
	-	`sha256:c561e24c443e1ac37cf8aff980e2b8cb4b60ab34cabdecc044d582be268e6761`  
		Last Modified: Tue, 24 Sep 2024 01:56:41 GMT  
		Size: 11.0 KB (11002 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

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

### `amazoncorretto:11-al2-full` - unknown; unknown

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
