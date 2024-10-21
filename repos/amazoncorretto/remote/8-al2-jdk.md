## `amazoncorretto:8-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:21fa3e77609a908d6e4299ec896cebc547b8c7fd6bd6754499e76251efd6a406
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8bc886b39f1b9faf67290ac4e022871736bac339375889eee1da44b952d086d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138259362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da248698e44158e98cb18d40dc27046b92221abf4871ced67e5b320aa40c7fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=1.8.0_432.b06-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:32c87c6464b59c63781462d4129c84f2806c57bdb75e94414a62f13a51d7b113`  
		Last Modified: Thu, 17 Oct 2024 08:34:33 GMT  
		Size: 62.7 MB (62679539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcde7c572465b0c2044d390c8c2af0e3814567c28a2fd6ce2525c3968db45fd`  
		Last Modified: Mon, 21 Oct 2024 18:56:44 GMT  
		Size: 75.6 MB (75579823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bc607ff4af1eea7bd4314b3b1697fdbd5c16dbb8dd1bcadd7cf69856e4a1f326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5381327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:330e172f155ea21ae376595d7f4ac0dd8969e1e755da91fceb9f495ace18d1b3`

```dockerfile
```

-	Layers:
	-	`sha256:05d1723d25f5174de88b9cc0e596ffa0c56d24d1db222ba6ab6d30916b7ff3e1`  
		Last Modified: Mon, 21 Oct 2024 18:56:44 GMT  
		Size: 5.4 MB (5369758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdd2d2384afdc322eab77ba52f45f28e17ab13153f3d0d781d22e9ff992e9c9c`  
		Last Modified: Mon, 21 Oct 2024 18:56:43 GMT  
		Size: 11.6 KB (11569 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:db3a2994c995b028ca9a7d4b73f5894bb2234ffa21e021d6787b32e82595c0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124255671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0fcb9d8060c48c8f78368dc2f4eabe8aa0698702b3d47f77e0632f3abfc2d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=1.8.0_432.b06-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:c05d42ff0b796ff4b1055b91676cb7e4b68389f23472cfdf987fa036f88561a9`  
		Last Modified: Thu, 17 Oct 2024 14:51:33 GMT  
		Size: 64.6 MB (64587089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4630336f3060e79bf64076b281308ad599aaaba9d1d9b474ae38126c908edf98`  
		Last Modified: Mon, 21 Oct 2024 19:13:59 GMT  
		Size: 59.7 MB (59668582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bceae760b1eefce5341aa69c8eb87e8728e16d50b32b97b3459b5fe470e3f3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c58e63058fa6dc9b40556608c579c281e38b7365d9241ce3e9391e81a0df943`

```dockerfile
```

-	Layers:
	-	`sha256:58f05f72025ef6c47233a16db5a747b217a511d675ab9e178f3130e40917292b`  
		Last Modified: Mon, 21 Oct 2024 19:13:58 GMT  
		Size: 5.3 MB (5348285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43e62c53c1965a24710f9e5e994229504784297c88f8b0d01ce57f03e59e60e0`  
		Last Modified: Mon, 21 Oct 2024 19:13:57 GMT  
		Size: 11.7 KB (11734 bytes)  
		MIME: application/vnd.in-toto+json
