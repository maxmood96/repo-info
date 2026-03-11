## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:6f6a2603e1b0abb0c995cafbd888c04473e2d101da6f2c9b7bc023eccb4e6a0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:e940a7a7f10259a8b1bd02d80676c00d2445fb63377b45086fd0fb8249dce3fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.0 MB (354017721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8901b1770f144f2be21edff14f17ee71118dee227f8352aa93354add16def67b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 11 Mar 2026 18:22:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:22:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:31:58 GMT
ARG version=1.8.0_482.b08-1
# Wed, 11 Mar 2026 18:31:58 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 11 Mar 2026 18:31:58 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:31:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 11 Mar 2026 19:17:00 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 11 Mar 2026 19:17:08 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 11 Mar 2026 19:17:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 11 Mar 2026 19:17:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 11 Mar 2026 19:17:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 11 Mar 2026 19:17:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 11 Mar 2026 19:17:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 11 Mar 2026 19:17:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 11 Mar 2026 19:17:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 11 Mar 2026 19:17:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 11 Mar 2026 19:17:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 11 Mar 2026 19:17:08 GMT
ARG MAVEN_VERSION=3.9.13
# Wed, 11 Mar 2026 19:17:08 GMT
ARG USER_HOME_DIR=/root
# Wed, 11 Mar 2026 19:17:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 11 Mar 2026 19:17:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 11 Mar 2026 19:17:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:94fc983b0f2661f620fb3c97c279be6e7a6a21ff4a004bf4df15272612aed901`  
		Last Modified: Sat, 07 Mar 2026 04:10:35 GMT  
		Size: 63.0 MB (62956510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4d53067f2cc3fbfbaaff55c5e004564933e732b39179727b563000bbd60805`  
		Last Modified: Wed, 11 Mar 2026 18:32:14 GMT  
		Size: 76.1 MB (76123376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3c34cfe0f9fe52efcf43e67a1eb245a944d7098027dcec33674b972ef1c0c6`  
		Last Modified: Wed, 11 Mar 2026 19:17:32 GMT  
		Size: 175.2 MB (175163686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9a3163bcade03704297e32e31bc0b2b831193040bd4012153d664473221bde`  
		Last Modified: Wed, 11 Mar 2026 19:17:29 GMT  
		Size: 30.1 MB (30075581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dff60e5404a62a472ee4cf29b90150f36cfa48cb1b30fe613f7cf7d69f692b7`  
		Last Modified: Wed, 11 Mar 2026 19:17:28 GMT  
		Size: 9.7 MB (9697524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8449f9358a98dadf17d6e5838dce552c3bd4959a9a5f5e6a28c6f69a5527170a`  
		Last Modified: Wed, 11 Mar 2026 19:17:28 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540c88db05872971b67b7d936eb70c57be7262b346454d509f4fc22bd6725721`  
		Last Modified: Wed, 11 Mar 2026 19:17:29 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:2b7e55632336051992688404aa149477dcffdf65264d9a7b8d9fd08b0e8cc677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6798281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281d89372bf39ae38b87d2794a1cb87d227821cbc56a9b1ce691e0888d0dcde1`

```dockerfile
```

-	Layers:
	-	`sha256:cd05d472ed00c9a4292b1e3b28fff43b8175a09c40abb374b40827dea315917b`  
		Last Modified: Wed, 11 Mar 2026 19:17:28 GMT  
		Size: 6.8 MB (6780094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7fd2857a747cf2f2e835e69b0222974ec1d192d0bafc586299f80515af55a01`  
		Last Modified: Wed, 11 Mar 2026 19:17:28 GMT  
		Size: 18.2 KB (18187 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:333d49d6b0b5128a8a8dd36f79305cd8046a35b456406dcbad2a28fa48e25161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.4 MB (316396896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16288f511ac02da7de8bf841fd0ebd84095e6c409d962448a38ff136024b6b88`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:38 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:32:11 GMT
ARG version=1.8.0_482.b08-1
# Wed, 11 Mar 2026 18:32:11 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 11 Mar 2026 18:32:11 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:32:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 11 Mar 2026 19:17:17 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 11 Mar 2026 19:17:26 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 11 Mar 2026 19:17:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 11 Mar 2026 19:17:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 11 Mar 2026 19:17:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 11 Mar 2026 19:17:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 11 Mar 2026 19:17:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 11 Mar 2026 19:17:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 11 Mar 2026 19:17:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 11 Mar 2026 19:17:26 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 11 Mar 2026 19:17:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 11 Mar 2026 19:17:26 GMT
ARG MAVEN_VERSION=3.9.13
# Wed, 11 Mar 2026 19:17:26 GMT
ARG USER_HOME_DIR=/root
# Wed, 11 Mar 2026 19:17:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 11 Mar 2026 19:17:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 11 Mar 2026 19:17:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1331e22401e9e6f680f618ca7ac295b00616904425c0ac818294801fd11443e3`  
		Last Modified: Mon, 09 Mar 2026 09:10:03 GMT  
		Size: 64.8 MB (64803149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991b141cbb1d71a90eb891797bf83c37fa38a55434ccedfc7752216e35e69bfb`  
		Last Modified: Wed, 11 Mar 2026 18:32:28 GMT  
		Size: 59.9 MB (59923077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a7a963a8d1acd2b10de2af98516a8eaf64ef4d0f6af94699545de7b3c745b8`  
		Last Modified: Wed, 11 Mar 2026 19:17:52 GMT  
		Size: 150.8 MB (150762086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f503f0ccd221d9f2c60cd778cf2d8f859076cf4c6aea2bfd6f3f88b529b80782`  
		Last Modified: Wed, 11 Mar 2026 19:17:49 GMT  
		Size: 31.2 MB (31209980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0788518df8d289d1c6b12c87fd92ea1a889952c952a2a1d78950b8fb91884d`  
		Last Modified: Wed, 11 Mar 2026 19:17:49 GMT  
		Size: 9.7 MB (9697559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3cb7d3663c92e87883a1179df8bff125c0ceddfd9d59ffa20c33e16647a808`  
		Last Modified: Wed, 11 Mar 2026 19:17:48 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc8d3e825fb29869b1b1636f47e0d59673e703199c44f9811431a30e4a166f4`  
		Last Modified: Wed, 11 Mar 2026 19:17:50 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:5597189817a0d92e26f0b89b38aeb33c49e2faa45b89a88cbf7464aff6358721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6775626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f745eebb603d4e3119778d1331d9cd28630f38df53c707729d982a42dc94f05`

```dockerfile
```

-	Layers:
	-	`sha256:d4e8a2a89f9e5bab61ed8cfd954f5806ed12e45541f0d6c55ecba110f7e9d875`  
		Last Modified: Wed, 11 Mar 2026 19:17:49 GMT  
		Size: 6.8 MB (6757291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:194d93c14a1976792886a484b300cede6db7906d3d28d7b0eeff58bb38b6b5a2`  
		Last Modified: Wed, 11 Mar 2026 19:17:48 GMT  
		Size: 18.3 KB (18335 bytes)  
		MIME: application/vnd.in-toto+json
