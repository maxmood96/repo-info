## `amazoncorretto:21-al2-full`

```console
$ docker pull amazoncorretto@sha256:a442b4beb07a8f4b20f66263bf620187d2e48a6ec882ce4d6a1ed63135c281d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:466e333b54bbf25bb190757b49bdf2141627d5baaa09115ecf73e6c201ba9736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227470695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac8ba5e9ff3b9758423348ae41998cdb8604f0c6eabb2ad45cb3fee22fd8ea5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:32c87c6464b59c63781462d4129c84f2806c57bdb75e94414a62f13a51d7b113`  
		Last Modified: Thu, 17 Oct 2024 08:34:33 GMT  
		Size: 62.7 MB (62679539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37908904c56cc5c3c9c4ef002a3127d26705ba6a3dca54ba848eb8a34d149934`  
		Last Modified: Mon, 21 Oct 2024 18:57:10 GMT  
		Size: 164.8 MB (164791156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:262d33b274a139309edbc74565c49f4609dd17c825ee7d477b989b36be92ed79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10868256c1aacbeaf507f452a4fd9d5ec5288d203b47e344e5ef6d9872372003`

```dockerfile
```

-	Layers:
	-	`sha256:4bddc50f0100511abfc33eca379d7fd8d1bf60221dc736d5f4611808d5a9c7dd`  
		Last Modified: Mon, 21 Oct 2024 18:57:08 GMT  
		Size: 5.5 MB (5527670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cb12804f6174299615d42c06b194d81638365c93b381f2ce35659aab0016082`  
		Last Modified: Mon, 21 Oct 2024 18:57:08 GMT  
		Size: 11.2 KB (11248 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8da82163c6310a727435cdd3fb956a4e4e22faeeed2a951db93ffa71777f9ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227425760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d32592b2d139deb985bc5f5e934b437796c800aa5800ca2f9bd8d4eeb71d36`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:c05d42ff0b796ff4b1055b91676cb7e4b68389f23472cfdf987fa036f88561a9`  
		Last Modified: Thu, 17 Oct 2024 14:51:33 GMT  
		Size: 64.6 MB (64587089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8275ee7e98e99b52993535510f2c91a30443129766cea22ea712e5c68223171`  
		Last Modified: Mon, 21 Oct 2024 19:24:24 GMT  
		Size: 162.8 MB (162838671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:98c40ab4a73288afeea4eb588bc19971d1dbb86e9dabd96ba9e68ae4047e5f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5537758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070eb850b2384b03832eeebe46aac29b9bbb5215c4c4e7bcf67bd80908a20a21`

```dockerfile
```

-	Layers:
	-	`sha256:91eebc4ff52ad9ee1e1f2b9d199ec89794d93aff583fb3fb54d14954f45108b5`  
		Last Modified: Mon, 21 Oct 2024 19:24:21 GMT  
		Size: 5.5 MB (5526357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e3cadd6964f3400d98ee7b37ce911dd197c28958dfe3ca362fe10d1e88389aa`  
		Last Modified: Mon, 21 Oct 2024 19:24:20 GMT  
		Size: 11.4 KB (11401 bytes)  
		MIME: application/vnd.in-toto+json
