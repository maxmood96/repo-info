## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:3809438e180ccfd901c7c74af796609328b1d81fe23945a0604153e5b47f17f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:d84fd4a249d2be4f4a2b05284ad1e3b4c67ef1085070b9dd1b22a8460c619dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.9 MB (449926486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8902e936fe42666b88b1bbb1b7ff236fd8de1adeb81f7cf22610ecabcad54d2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:59 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:59 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:14:32 GMT
ARG version=21.0.11.10-1
# Mon, 22 Jun 2026 18:14:32 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 22 Jun 2026 18:14:32 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:14:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 22 Jun 2026 18:26:22 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 22 Jun 2026 18:26:30 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 22 Jun 2026 18:26:30 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 22 Jun 2026 18:26:30 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 22 Jun 2026 18:26:30 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 22 Jun 2026 18:26:30 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 22 Jun 2026 18:26:30 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 22 Jun 2026 18:26:30 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 22 Jun 2026 18:26:30 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 22 Jun 2026 18:26:30 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 22 Jun 2026 18:26:30 GMT
ARG USER_HOME_DIR=/root
# Mon, 22 Jun 2026 18:26:30 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 22 Jun 2026 18:26:30 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 22 Jun 2026 18:26:30 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b5a31d0a32c9342b5b53f098c4d8ac4fadeb6cbc6b34b2e4424fd39eb880bf9a`  
		Last Modified: Sat, 13 Jun 2026 04:09:34 GMT  
		Size: 62.9 MB (62942019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92113e9c830991e7d2cd18b6ce514b1aa820517c514266197ea2d8073457c605`  
		Last Modified: Mon, 22 Jun 2026 18:14:54 GMT  
		Size: 165.8 MB (165761238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9323fbd13ac1d0464b9971a53b32bd346ba4ef780c37aa59e30d9633cb0ab859`  
		Last Modified: Mon, 22 Jun 2026 18:27:01 GMT  
		Size: 181.8 MB (181803767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d5c9fce787c4342503cd3fc13ec0f357469fa1593cad8b9db60ca2a0e208f5`  
		Last Modified: Mon, 22 Jun 2026 18:26:57 GMT  
		Size: 30.1 MB (30058477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9626f2b5f3a93a691a544465ea2f78ca9cd25ffdf344efbdcbe67ec62521852`  
		Last Modified: Mon, 22 Jun 2026 18:26:56 GMT  
		Size: 9.4 MB (9359974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3553b5aa1fd76b1928255312bdb5e5837876aa6b90c98a7ad3b769c2b9b371de`  
		Last Modified: Mon, 22 Jun 2026 18:26:55 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ad6cf8e3f3d10f6b58854c735b20ba36319514b96f9e3d8d500d1a5a358b46`  
		Last Modified: Mon, 22 Jun 2026 18:26:57 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:03a82b2a1a46657b5ab3fff970978ee450ff64c99e3468d67d1d2b35bebfd32b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6949286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188c48912244edc7d52621872d9a9d238ca80d527014374010176bfd88e9b267`

```dockerfile
```

-	Layers:
	-	`sha256:1b914a9eecf70834e437dedcd913cb150d89f7a1cfa8639deacb51081d32ed60`  
		Last Modified: Mon, 22 Jun 2026 18:26:55 GMT  
		Size: 6.9 MB (6933068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eb98b734ce4aed82a2315fef4deabd73a047c67d30c59574349dfebbf9d07a8`  
		Last Modified: Mon, 22 Jun 2026 18:26:55 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:05f10acfeffc1c3be7a3ba8dd743b34874530577e29f8e8ab8777a9e6f1f16fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.5 MB (426518758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945f8b0cffcf45775445aaaeacea66b7fd840203c73d6bff1e0e7e6a0080b5d0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 22 Jun 2026 18:00:28 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 18:00:28 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:14:53 GMT
ARG version=21.0.11.10-1
# Mon, 22 Jun 2026 18:14:53 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 22 Jun 2026 18:14:53 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:14:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 22 Jun 2026 18:34:20 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 22 Jun 2026 18:34:27 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 22 Jun 2026 18:34:27 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 22 Jun 2026 18:34:27 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 22 Jun 2026 18:34:27 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 22 Jun 2026 18:34:27 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 22 Jun 2026 18:34:27 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 22 Jun 2026 18:34:27 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 22 Jun 2026 18:34:27 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 22 Jun 2026 18:34:27 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 22 Jun 2026 18:34:27 GMT
ARG USER_HOME_DIR=/root
# Mon, 22 Jun 2026 18:34:27 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 22 Jun 2026 18:34:27 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 22 Jun 2026 18:34:27 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4b30ecc040ec91b7e580ef7f93f591eaf80422b110a473c44b4d0dbcb2301395`  
		Last Modified: Wed, 17 Jun 2026 13:06:48 GMT  
		Size: 64.8 MB (64794736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9ab00298aadd58a3bb8cae018cd5b3d4b05bdf586ebc30fe105caf4842da84`  
		Last Modified: Mon, 22 Jun 2026 18:15:16 GMT  
		Size: 163.9 MB (163862118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48830ebedd68157937e975ac4703577853bc363ca2f3fe6f181aac423816dee1`  
		Last Modified: Mon, 22 Jun 2026 18:34:55 GMT  
		Size: 157.3 MB (157304224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931e36e517be654304a9438d6933c2ae36e90e5ee221c663ca3ae6bf09aa8c54`  
		Last Modified: Mon, 22 Jun 2026 18:34:52 GMT  
		Size: 31.2 MB (31196702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be442336fbab60d311695a90f25e8c86f117d21b2c9bc76d6308c742ed089f89`  
		Last Modified: Mon, 22 Jun 2026 18:34:51 GMT  
		Size: 9.4 MB (9359968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f454b6624a067cdf1334f0d00806ee5a89a82e237d66f2068a8fb29ed6742362`  
		Last Modified: Mon, 22 Jun 2026 18:34:50 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81e9550a51cc80cadbd298358b7f9184cd6b0d31bf658ce2ff2c377fe26f445`  
		Last Modified: Mon, 22 Jun 2026 18:34:51 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:606817b03d9e1ce0fe65856717b2608440575b24fbd37e95c1582491ac55cadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6946833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d2b75d8b7f46c61b44e70f257b87c8fd2c6345cec4fcd3d2d6792a38adb364c`

```dockerfile
```

-	Layers:
	-	`sha256:1c67ffb6ce50348e33b8922d2e4f97fcf7c10949e3c7d312ba50cc51adbc0f6c`  
		Last Modified: Mon, 22 Jun 2026 18:34:50 GMT  
		Size: 6.9 MB (6930467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8d3b51e69301bcd11e93337dfacd42ef90673005c4d272448050f47c675d4b`  
		Last Modified: Mon, 22 Jun 2026 18:34:50 GMT  
		Size: 16.4 KB (16366 bytes)  
		MIME: application/vnd.in-toto+json
