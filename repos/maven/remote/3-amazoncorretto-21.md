## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:5b37fc0d5ecb552ec57dfa215e25a3bee9475f9cbf4eab2737e4fa9d9730df75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:33f16fe9d1ffc14a2e24b37bc56c858d07581d514c10028ba970a3e25365e3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.9 MB (447850332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66d37292c6df68f897bbfd00d6bd9abe2754997186096c37326ba08e6d1200b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 22 May 2026 20:12:28 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:28 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:12:11 GMT
ARG version=21.0.11.10-1
# Fri, 22 May 2026 21:12:11 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 22 May 2026 21:12:11 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:12:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 22 May 2026 22:09:06 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 22 May 2026 22:09:13 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 22 May 2026 22:09:13 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 22 May 2026 22:09:13 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 22 May 2026 22:09:13 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 22 May 2026 22:09:13 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 22 May 2026 22:09:13 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 22 May 2026 22:09:13 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 22 May 2026 22:09:13 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 22 May 2026 22:09:13 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 22 May 2026 22:09:13 GMT
ARG USER_HOME_DIR=/root
# Fri, 22 May 2026 22:09:13 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 22 May 2026 22:09:13 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 22 May 2026 22:09:13 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:45dd431b24e3561020a83f5e29dd2642d9ec2f2788c6826e5b1e9ee25ee38759`  
		Last Modified: Sat, 16 May 2026 04:14:19 GMT  
		Size: 63.0 MB (62951975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa9a0f866da5bf4cda881c339deb1430d89b88b30e6877b722611f7e7afccc4`  
		Last Modified: Fri, 22 May 2026 21:12:31 GMT  
		Size: 165.8 MB (165759980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3dc1053ca6bae139a055f1f3b68e25a2ed14a70eb9a69b0c1e1f0aabf1c6f8`  
		Last Modified: Fri, 22 May 2026 22:09:40 GMT  
		Size: 179.7 MB (179700260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160c390a1d502679af1da8df706cb096f2c051f55801b145d38d2cc48999a11d`  
		Last Modified: Fri, 22 May 2026 22:09:37 GMT  
		Size: 30.1 MB (30077142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37eb8871f15380f0ee3e166330ac2cb15dc54ad840de02aa8824d60ae9a52d47`  
		Last Modified: Fri, 22 May 2026 22:09:36 GMT  
		Size: 9.4 MB (9359966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49316f540e31d4599311e34ec97c53f7c3641f03a5d3980d4332e19924e2e533`  
		Last Modified: Fri, 22 May 2026 22:09:35 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5e67a3b29faa5bf2afa8771e3b925dd9d35e4b0b6e5572f939541ebc97df7f`  
		Last Modified: Fri, 22 May 2026 22:09:37 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:c56581d286a3b7d4657f42fc81dc7a78fcae2af033aa4cd8f2a245bdf75ba127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6949286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4fd03e9d5d2987c51cfd1d7351828552484c415e67fa31f70428edf629563e4`

```dockerfile
```

-	Layers:
	-	`sha256:41226d1ca92ddba44aafadc95e700ff563202e142542a05a127dc55b55214612`  
		Last Modified: Fri, 22 May 2026 22:09:36 GMT  
		Size: 6.9 MB (6933068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c1404414ffb18e52125a3b398f204cb686f67992369eed608be7a960d714ff5`  
		Last Modified: Fri, 22 May 2026 22:09:35 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:e98ef0cbb2f535fda659965d607a5f6ef640e5d795ee9088e82648fc9be0dc7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.5 MB (424522102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23f0108057cee2165a5b736c5e0f929a89ea84993ee0d6d03cdfd61eaa79352`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 22 May 2026 20:12:43 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:43 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:49 GMT
ARG version=21.0.11.10-1
# Fri, 22 May 2026 21:11:49 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 22 May 2026 21:11:49 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 22 May 2026 22:09:24 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 22 May 2026 22:09:31 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 22 May 2026 22:09:31 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 22 May 2026 22:09:31 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 22 May 2026 22:09:31 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 22 May 2026 22:09:31 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 22 May 2026 22:09:31 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 22 May 2026 22:09:31 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 22 May 2026 22:09:31 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 22 May 2026 22:09:32 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 22 May 2026 22:09:32 GMT
ARG USER_HOME_DIR=/root
# Fri, 22 May 2026 22:09:32 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 22 May 2026 22:09:32 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 22 May 2026 22:09:32 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9b55de233aca71116430038a4df795c9fbcd988648b5d3ff05692945d681a5dc`  
		Last Modified: Sat, 16 May 2026 15:07:44 GMT  
		Size: 64.8 MB (64790017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c97e9b0bf2ccbef6baaf54a1caddc245b53958888385774b48af9968db9a55`  
		Last Modified: Fri, 22 May 2026 21:12:12 GMT  
		Size: 163.9 MB (163902526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8697f2658193a3b07821a0d07d34b70c2738ab53bec9028750e1d9c3c6626b8c`  
		Last Modified: Fri, 22 May 2026 22:09:59 GMT  
		Size: 155.3 MB (155270069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4dcde55721214da3fd49a209b30da2738db34c4412c60f7a03d42d70fad49c7`  
		Last Modified: Fri, 22 May 2026 22:09:56 GMT  
		Size: 31.2 MB (31198507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ecde87132baea553aef1d4318495a73c52a510c401c2e4011860b3636a080e`  
		Last Modified: Fri, 22 May 2026 22:09:55 GMT  
		Size: 9.4 MB (9359974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426580e0a734eb9cc3ae5c0b25055435a934d2527de8cfd0629582311c641878`  
		Last Modified: Fri, 22 May 2026 22:09:54 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b323fcade104d1840ab28379a6d9ad8eedcbdbe1c33afe317943a9633d00f4a4`  
		Last Modified: Fri, 22 May 2026 22:09:55 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:cf141f503fd8804d216a819189e490e84fdf150791730c962b55bedb3847c8e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6946833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb85289b38cd9afc0e7f3e959e5c7431763f5020ca5fdd4bed92454f2e5863b2`

```dockerfile
```

-	Layers:
	-	`sha256:37abce6fe5327f477e842436cbcfd7aab36defe9c99db6c5d23594df822ed3ff`  
		Last Modified: Fri, 22 May 2026 22:09:54 GMT  
		Size: 6.9 MB (6930467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca1d0323da0b7f9f471017dd7f090e6c04e29c54ac9932cb18fadef209bb266f`  
		Last Modified: Fri, 22 May 2026 22:09:54 GMT  
		Size: 16.4 KB (16366 bytes)  
		MIME: application/vnd.in-toto+json
