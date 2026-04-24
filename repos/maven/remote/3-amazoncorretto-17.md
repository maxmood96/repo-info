## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:ee449dca251e2c1fee0e2467b05377db1dbe6792a0efbe48f58c3d3526a83ac4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:be5d050009789e3c0ac593343d427b81ac086306619fe8296a0f0633180c3678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.6 MB (431630696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6b78749b804c6c5448b335d7b36914190df70e9958882380d95556549c15ad`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 24 Apr 2026 00:03:09 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:03:09 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:11:35 GMT
ARG version=17.0.19.10-1
# Fri, 24 Apr 2026 00:11:35 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Apr 2026 00:11:35 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:11:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 24 Apr 2026 01:13:48 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 24 Apr 2026 01:13:56 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 24 Apr 2026 01:13:56 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 24 Apr 2026 01:13:56 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 24 Apr 2026 01:13:56 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 24 Apr 2026 01:13:56 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 24 Apr 2026 01:13:56 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 24 Apr 2026 01:13:56 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 24 Apr 2026 01:13:56 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 24 Apr 2026 01:13:56 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 24 Apr 2026 01:13:56 GMT
ARG USER_HOME_DIR=/root
# Fri, 24 Apr 2026 01:13:56 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 24 Apr 2026 01:13:56 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 24 Apr 2026 01:13:56 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e31bc602eae80620b93a07bcadec78ad83d112fa08abc35008da53ebf7ca3693`  
		Last Modified: Wed, 15 Apr 2026 10:04:45 GMT  
		Size: 63.0 MB (62952183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7564beac752dec0bb235968831bc5d422be39ca32258d704c3310f0b700ee4dd`  
		Last Modified: Fri, 24 Apr 2026 00:11:56 GMT  
		Size: 152.7 MB (152688400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94648c4acbf50da08818e3d3a4cd45090f6aebb2520e2224839a4dec58625558`  
		Last Modified: Fri, 24 Apr 2026 01:14:22 GMT  
		Size: 176.6 MB (176593893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87684994e222a44afe414b84da62dd1afdf0959f672336693e8cc4088969aeb0`  
		Last Modified: Fri, 24 Apr 2026 01:14:19 GMT  
		Size: 30.1 MB (30082991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8309438c7aefe007f0921fdadd08fdb97ac3a725eae041549e5d406192e58a`  
		Last Modified: Fri, 24 Apr 2026 01:14:18 GMT  
		Size: 9.3 MB (9312218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872cf255298bf0e2d023af67c379dc831a74a27a9b03e592a15cad72a2339676`  
		Last Modified: Fri, 24 Apr 2026 01:14:17 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70727e2a1cd091d957c2f40f6bc2f22ee918b684ca947b50105b03eb0387c9b`  
		Last Modified: Fri, 24 Apr 2026 01:14:18 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:209eb59be70398b18da11af16c8aeb0525e57e606c10d01ab7d83f557871e2b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6949358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043a0a407813c50686804d55a9e02226076dd38c0b256bfccc6699372956c029`

```dockerfile
```

-	Layers:
	-	`sha256:9a765db8a3e0290ce28e78eab4921be60e7836a84de1a1798f54097833533153`  
		Last Modified: Fri, 24 Apr 2026 01:14:17 GMT  
		Size: 6.9 MB (6933162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c7a720fc57ca39cdb46447f470c2a70129038dd4a2b2296bac8b42bf9893580`  
		Last Modified: Fri, 24 Apr 2026 01:14:17 GMT  
		Size: 16.2 KB (16196 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b6a78632bead79deb3a67bf58c9b357a4d33935db65707041a4cee2e856bffa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.7 MB (408726651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb049399d761ab16b14e358257f1fa1108b9d66c7419a263b4a805753cc7678`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:35 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:35 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:10:49 GMT
ARG version=17.0.19.10-1
# Fri, 24 Apr 2026 00:10:49 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Apr 2026 00:10:49 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:10:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 24 Apr 2026 01:13:54 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 24 Apr 2026 01:14:02 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 24 Apr 2026 01:14:02 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 24 Apr 2026 01:14:02 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 24 Apr 2026 01:14:02 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 24 Apr 2026 01:14:02 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 24 Apr 2026 01:14:02 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 24 Apr 2026 01:14:02 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 24 Apr 2026 01:14:02 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 24 Apr 2026 01:14:03 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 24 Apr 2026 01:14:03 GMT
ARG USER_HOME_DIR=/root
# Fri, 24 Apr 2026 01:14:03 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 24 Apr 2026 01:14:03 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 24 Apr 2026 01:14:03 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0089d862b3b6e84c40891727df0dc5639dc509aa2f4dc6079056a5a3f8b526e1`  
		Last Modified: Wed, 15 Apr 2026 10:04:56 GMT  
		Size: 64.8 MB (64798783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976d2f926c87c0b9d8781e94d0cdcc2bf692f1538c27d2ce584358e445f69559`  
		Last Modified: Fri, 24 Apr 2026 00:11:11 GMT  
		Size: 151.3 MB (151311695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cdfb322e7aa0331b193ff824fe42af358ea8a4e6506f7c4a1b9c5995a72367`  
		Last Modified: Fri, 24 Apr 2026 01:14:30 GMT  
		Size: 152.1 MB (152103697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730a77d5e2e91087f3eccd7bea50668ee3315762db26895e5f8174a02d094a25`  
		Last Modified: Fri, 24 Apr 2026 01:14:28 GMT  
		Size: 31.2 MB (31199211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89abb415ebe187516602aac531c4780f27e6b15d5ed0d055000c2321aa7b51c5`  
		Last Modified: Fri, 24 Apr 2026 01:14:27 GMT  
		Size: 9.3 MB (9312254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc785130cb3ade16140d9ac5c0a7d9092eba3e77f813d7468f04e9767bb8418`  
		Last Modified: Fri, 24 Apr 2026 01:14:26 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feaad5f9185652e4947311731a0c2880075ee498b119a86e949d898d37d4389f`  
		Last Modified: Fri, 24 Apr 2026 01:14:27 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:7e9f30a2af1140e2f5f5998b2e47276f4912b3b1dec3daa104f1113f94ad02ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6946905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4d5bd93aa960199ae87f45f2bcce3cb9ffb6c02eee211b248914a104bdb717`

```dockerfile
```

-	Layers:
	-	`sha256:ce8e216dea4a5f41d89d71004ccf384b8b72b2f319c69ee9c839fbe0341c72a8`  
		Last Modified: Fri, 24 Apr 2026 01:14:26 GMT  
		Size: 6.9 MB (6930561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44c9f46edcbe415a1d3ae3c02c363d447c0c3ae23f4c14b8d1ef46a9e0b50a5c`  
		Last Modified: Fri, 24 Apr 2026 01:14:26 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json
