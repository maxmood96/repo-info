## `amazoncorretto:21-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:a7dfa8e261dc533623e107d33b233a6ba6a339ddd1c748facad0330d6d49415f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b8cfa0945f6076a0d194fa777609ab82edc735773440216ec081954e1ab74610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228702875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e149cc2c501b9fdf02df00f2c01e8a32a71a5e113cbffb7ecf21459eeb7a76`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:09:40 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:09:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:15:40 GMT
ARG version=21.0.11.10-1
# Tue, 16 Jun 2026 01:15:40 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jun 2026 01:15:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:15:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d80d3835ce8936ec0ede6caeb9410c7e15fc302623348ec599f325dbd3e201d`  
		Last Modified: Tue, 16 Jun 2026 01:16:03 GMT  
		Size: 165.8 MB (165760925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a81e6f0545d9f859ef2bc1362fcea1e98bbd2d39c312079d2b4267a858074ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5547732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd969a872e04699b7c535f9b8e22c8098d195ddab16120495eac1bbf4579c858`

```dockerfile
```

-	Layers:
	-	`sha256:6098edaef71cc970dafb5bb232f1010976a9ab5a6abb3816203372d48a84055f`  
		Last Modified: Tue, 16 Jun 2026 01:15:59 GMT  
		Size: 5.5 MB (5536520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bb3d95450bca12cf1940f0384852cb045cc58d773f14daceedc19251006f18f`  
		Last Modified: Tue, 16 Jun 2026 01:15:59 GMT  
		Size: 11.2 KB (11212 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:79b0a6a3fbd1fb13c5b3a8ebb44cdd297d8a0f289d5ec34f71d5227ea59d224c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228693732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b0ccffd571af2dd8400962cca0cc0f363cef8fd0f16255125f7f8eeffe9fd0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:10:52 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:10:52 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:16:46 GMT
ARG version=21.0.11.10-1
# Tue, 16 Jun 2026 01:16:46 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jun 2026 01:16:46 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:16:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f13b08c076b48cc17be56fff3c38de928e98b889c01b68dd638e8eca94dc6e`  
		Last Modified: Tue, 16 Jun 2026 01:17:09 GMT  
		Size: 163.9 MB (163903023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:048d49d73ebb36d47882fa4d7f1f38f3babe76dbde2c451ea029a18c8c67dd53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1484eae9e31318ef3ce19dbe71f60817c4f482ea19d21cd7a80f822f1ce924d`

```dockerfile
```

-	Layers:
	-	`sha256:61a59c20476ca3161c8af5ae4a2b6c35d368e6d45b85fc55b333b564a0ea23c8`  
		Last Modified: Tue, 16 Jun 2026 01:17:05 GMT  
		Size: 5.5 MB (5535209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b38c1b5e25a802a52d772de0f5b0a2869fa87dfc624b03c60dd443a7f8a144f`  
		Last Modified: Tue, 16 Jun 2026 01:17:04 GMT  
		Size: 11.4 KB (11365 bytes)  
		MIME: application/vnd.in-toto+json
