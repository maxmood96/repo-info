## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:4aaff4a4ad503dec56375d2127cd442ddde8b9b80295503216202cc7324a9fed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:b69edc823624d5994a171a23d7f3ca424344d7b5c05b01bb58dbf23f3e3ed2e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.1 MB (355079476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd336f46781bc581795412175468db23185c3f736633a211d5ababc09c97286`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 24 Apr 2026 00:03:09 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:03:09 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:07:40 GMT
ARG version=1.8.0_492.b09-1
# Fri, 24 Apr 2026 00:07:40 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Apr 2026 00:07:40 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:07:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 24 Apr 2026 01:14:53 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 24 Apr 2026 01:15:03 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 24 Apr 2026 01:15:03 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 24 Apr 2026 01:15:03 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 24 Apr 2026 01:15:03 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 24 Apr 2026 01:15:03 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 24 Apr 2026 01:15:03 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 24 Apr 2026 01:15:03 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 24 Apr 2026 01:15:03 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 24 Apr 2026 01:15:03 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 24 Apr 2026 01:15:03 GMT
ARG USER_HOME_DIR=/root
# Fri, 24 Apr 2026 01:15:03 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 24 Apr 2026 01:15:03 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 24 Apr 2026 01:15:03 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e31bc602eae80620b93a07bcadec78ad83d112fa08abc35008da53ebf7ca3693`  
		Last Modified: Wed, 15 Apr 2026 10:04:45 GMT  
		Size: 63.0 MB (62952183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531adab3b047702ba6f5ca72b2356d3ef807ec1a89ef6c694bb3b982cfec2c42`  
		Last Modified: Fri, 24 Apr 2026 00:07:56 GMT  
		Size: 76.1 MB (76139049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f9037d2b5529fdbb6efebe120c1e095c963b21328b01af065307aba8dc83e9`  
		Last Modified: Fri, 24 Apr 2026 01:15:30 GMT  
		Size: 176.6 MB (176600690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac525b2f5091958996215520abaeda2513af201db0d6e396fcd9a76a60a53e2`  
		Last Modified: Fri, 24 Apr 2026 01:15:27 GMT  
		Size: 30.1 MB (30074323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b2ac641a5bdae673b1c2dcad5f588c84c000aba81ac05bff7fa6e43323a5fe`  
		Last Modified: Fri, 24 Apr 2026 01:15:26 GMT  
		Size: 9.3 MB (9312218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48beb42b2be9aba349274458626376e33bffd43d8f062fb0a544f6d647ad848d`  
		Last Modified: Fri, 24 Apr 2026 01:15:26 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf4628aafffe0838d3ed0a79ca289612d8ae697784e8552bc2cd33c2ea738dc`  
		Last Modified: Fri, 24 Apr 2026 01:15:27 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:923218fbb894ac3d6a3aa816864170c8643e358c94928bee2e02c56dea03a52d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6789888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca02893270cc4fa45d0fb5d2596ffa96ce05362395fe83343d636d47984cf81`

```dockerfile
```

-	Layers:
	-	`sha256:9f89539e5e096a2740176dcac6bc85cefd137ed3f8df30b4031ca1b254c0a0cf`  
		Last Modified: Fri, 24 Apr 2026 01:15:26 GMT  
		Size: 6.8 MB (6773702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5df23a19996376d26e42a36aabb36f0110af0c29a379a848782dca85f50d39b0`  
		Last Modified: Fri, 24 Apr 2026 01:15:25 GMT  
		Size: 16.2 KB (16186 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d1498a966a7def6053fafc926d4e5653bbe91a3621888f3f2e7d38e22c2835d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.4 MB (317372575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cc7e154d572967c841598e679cc7868569cffe136c0242ca984bdcb332582a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:35 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:35 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:07:17 GMT
ARG version=1.8.0_492.b09-1
# Fri, 24 Apr 2026 00:07:17 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Apr 2026 00:07:17 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:07:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 24 Apr 2026 01:14:46 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 24 Apr 2026 01:14:53 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 24 Apr 2026 01:14:53 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 24 Apr 2026 01:14:53 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 24 Apr 2026 01:14:53 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 24 Apr 2026 01:14:53 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 24 Apr 2026 01:14:53 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 24 Apr 2026 01:14:53 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 24 Apr 2026 01:14:53 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 24 Apr 2026 01:14:53 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 24 Apr 2026 01:14:53 GMT
ARG USER_HOME_DIR=/root
# Fri, 24 Apr 2026 01:14:53 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 24 Apr 2026 01:14:53 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 24 Apr 2026 01:14:53 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0089d862b3b6e84c40891727df0dc5639dc509aa2f4dc6079056a5a3f8b526e1`  
		Last Modified: Wed, 15 Apr 2026 10:04:56 GMT  
		Size: 64.8 MB (64798783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3474265d81c23af61defdf241fb98bb0d0f2c53e1cf76dc78cc7bc4c49255290`  
		Last Modified: Fri, 24 Apr 2026 00:07:32 GMT  
		Size: 60.0 MB (59958797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b894e34dbbfde80840f4d700a7bf0b6abec9c51a14026bc6f7d74bcdc7953d25`  
		Last Modified: Fri, 24 Apr 2026 01:15:20 GMT  
		Size: 152.1 MB (152105614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfd50307433d08717900ad57b09aec1a7b41c28d1da3e6ce97c990c063f75e9`  
		Last Modified: Fri, 24 Apr 2026 01:15:17 GMT  
		Size: 31.2 MB (31196120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7400dc08e2d0667608c796f5c58ddc27f0698e2f834462e7784975599c6c4b0e`  
		Last Modified: Fri, 24 Apr 2026 01:15:16 GMT  
		Size: 9.3 MB (9312250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edde22f27b08f2d20e7288bfd39ffbb90f1b827287ec1f7cc5679c12a84685f6`  
		Last Modified: Fri, 24 Apr 2026 01:15:16 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9422976bae2e96ad38ef084dd74d885e9bbc4df576be2ffc4b6c83bdaadf455`  
		Last Modified: Fri, 24 Apr 2026 01:15:17 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:ca5a3ecc2c3329c07757e96b585e5b4a1c01950dc6104cd3c8308c9ea69c6719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6767232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7d829b2ceae1c1bd152ab279f68feb30a5fa9863cb8b57605dceb22007f5ca`

```dockerfile
```

-	Layers:
	-	`sha256:b9b13b80e9b0bd39e29e3d10f97f31d9f1e284920bbec06883965a7107b8ac7b`  
		Last Modified: Fri, 24 Apr 2026 01:15:16 GMT  
		Size: 6.8 MB (6750899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d27324da880dc3018b0772538d9c256d3960de82b1e2ed985a4ad4052a8f1af6`  
		Last Modified: Fri, 24 Apr 2026 01:15:16 GMT  
		Size: 16.3 KB (16333 bytes)  
		MIME: application/vnd.in-toto+json
