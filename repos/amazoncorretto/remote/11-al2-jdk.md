## `amazoncorretto:11-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:4f1b07958fc7c1ddfd19938dbd2de4a446e22e1d83ef422d353df0e464755e4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bcc81a7d8365260ccc377e2e3b7ca2dd3a7dd3dace92ed39198302940709899b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211148711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe339da6a262d9471b8d6e9e557f01f0132ccf78c41a6c976d92652fcf00378`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:21 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:21 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:33:04 GMT
ARG version=11.0.31.11-1
# Wed, 22 Apr 2026 21:33:04 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 22 Apr 2026 21:33:04 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:5a3a1a219789b0285ea1d6a41ad03e6fab76f369592968c458dbfffd408719dd`  
		Last Modified: Thu, 09 Apr 2026 08:25:08 GMT  
		Size: 63.0 MB (62955266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de281a9d7e202695fc9494277d90cff7fdc687a00a5c23a293228e58433941d7`  
		Last Modified: Wed, 22 Apr 2026 21:33:25 GMT  
		Size: 148.2 MB (148193445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4dba45512c65193f53dab02b9e8a7a8aad974d39887e1817efa44ce2f5b7aa7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a8e349dad76bbd767964df3d2b52ee28ff1d36ac3ab559ef26af783ac86cbf`

```dockerfile
```

-	Layers:
	-	`sha256:340b5c197f8b8044f6dba36bcc68d5cd915ed27c412cb7b396164f9d3ed3f8a5`  
		Last Modified: Wed, 22 Apr 2026 21:33:22 GMT  
		Size: 5.5 MB (5543110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfc974278e6ba7661a4370de275ae4ee8fe1616cc0fd36ca040ad2f93be88bcc`  
		Last Modified: Wed, 22 Apr 2026 21:33:21 GMT  
		Size: 11.2 KB (11213 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3004fc381f6ce2c0addf3a85f099673ef13e6df9f7d540ca4b97093998a25f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210170562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c0f98d49170cdfc9662920205ca6d9f684e5abefbac1aba5cbc07706502fe9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:35 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:35 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:33:17 GMT
ARG version=11.0.31.11-1
# Wed, 22 Apr 2026 21:33:17 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 22 Apr 2026 21:33:17 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f1f2697b3535de3cb27d338e724d6283baf064a258669349257ede7e5670fff3`  
		Last Modified: Thu, 09 Apr 2026 08:25:15 GMT  
		Size: 64.8 MB (64802975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b5ed46dcfa823b8750e3a141aa014614f8315f8e0ea57cbf0d90691c2ba855`  
		Last Modified: Wed, 22 Apr 2026 21:33:38 GMT  
		Size: 145.4 MB (145367587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2d1418ad2280028b1a732751e81b5caf17b1562b7a44e2ef18ba8a968db537d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5553969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e91e857e7146cd78da397db14403e64f04fd49805c48d21b6715377fd597b8`

```dockerfile
```

-	Layers:
	-	`sha256:13ceae918e07281a3442d6959368545dd64fccf37ad44aa442fb0990c11787f4`  
		Last Modified: Wed, 22 Apr 2026 21:33:35 GMT  
		Size: 5.5 MB (5542604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b805b2e6ac68dcecd8417c9e3b2a71613eb0f0899c17f374c5c1078ad39d66`  
		Last Modified: Wed, 22 Apr 2026 21:33:34 GMT  
		Size: 11.4 KB (11365 bytes)  
		MIME: application/vnd.in-toto+json
