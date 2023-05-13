## `maven:amazoncorretto`

```console
$ docker pull maven@sha256:e70bb8ce678fa02273ec47073dbba1a668722805e2c069ce25d6e8b7ca4eb9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:c810e7b58caf569bd6a37326b278d6dffd0359dd7b598924dc9057fb81ddb2a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.2 MB (370246083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba77f53f0fd21fbf5511de89b0eec7302274f6b3eabd9a547f712624dd51107`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 13 May 2023 00:19:34 GMT
COPY dir:7a824a76678fb4ef17879dcecd9fac65df3d1efbef31a3b874da9f49f49b6814 in / 
# Sat, 13 May 2023 00:19:34 GMT
CMD ["/bin/bash"]
# Sat, 13 May 2023 01:33:37 GMT
ARG version=11.0.19.7-1
# Sat, 13 May 2023 01:34:02 GMT
# ARGS: version=11.0.19.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 13 May 2023 01:34:03 GMT
ENV LANG=C.UTF-8
# Sat, 13 May 2023 01:34:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 13 May 2023 01:34:03 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Sat, 13 May 2023 01:34:03 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 13 May 2023 01:34:03 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 13 May 2023 01:34:03 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 13 May 2023 01:34:03 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 13 May 2023 01:34:03 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 13 May 2023 01:34:03 GMT
ARG MAVEN_VERSION=3.9.1
# Sat, 13 May 2023 01:34:03 GMT
ARG USER_HOME_DIR=/root
# Sat, 13 May 2023 01:34:03 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 13 May 2023 01:34:03 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 13 May 2023 01:34:03 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:bf72c394abb748707ec4590d5017f36ad47098c9b92adc1b04c3ea3ba0b395f6`  
		Last Modified: Fri, 12 May 2023 00:07:44 GMT  
		Size: 62.5 MB (62494714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20fca57aa3ff41998ba7cda3aea10ad664a82e3fde09396157d1b38c91a39590`  
		Last Modified: Sat, 13 May 2023 01:37:04 GMT  
		Size: 147.8 MB (147786886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876ea8e3d9a506b86332243468128aa595e37ef468d497fc1f4f746170c9aa2d`  
		Last Modified: Sat, 13 May 2023 03:56:23 GMT  
		Size: 150.9 MB (150856929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91dc14011142208f89ca054d39c3cffd80bf3a9dcccaef9b730fdb8a4a04535b`  
		Last Modified: Sat, 13 May 2023 03:56:11 GMT  
		Size: 9.1 MB (9106172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4105fa4c9d5e2a7ff65f392d23e2ed38aae3352c7dec356ef6b627f88c6ad9`  
		Last Modified: Sat, 13 May 2023 03:56:10 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91a5ec9d1c9952365dec6f918e283d72d25ab65f6d9f9161c899a2cb767fe81`  
		Last Modified: Sat, 13 May 2023 03:56:10 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69dfee9455dd7a3961ca5fd33bc838d8c896f2775546d7c2757b53f9d5da531`  
		Last Modified: Sat, 13 May 2023 03:56:10 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:4fa1af5545616111cb48afbdb4de5f42604450284dfc95ec51d6a7394f315cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334106637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0baa72afb182746c89e55e9766e8703cc7f4c5a87ce9e8085b2d25df7771e67d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 13 May 2023 00:39:27 GMT
COPY dir:71cecf11386ac326afd2beed7b45e00586f5b9ab017bb6ace5dec65e5aa62900 in / 
# Sat, 13 May 2023 00:39:27 GMT
CMD ["/bin/bash"]
# Sat, 13 May 2023 02:30:45 GMT
ARG version=11.0.19.7-1
# Sat, 13 May 2023 02:31:04 GMT
# ARGS: version=11.0.19.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 13 May 2023 02:31:05 GMT
ENV LANG=C.UTF-8
# Sat, 13 May 2023 02:31:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 13 May 2023 02:31:05 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Sat, 13 May 2023 02:31:05 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 13 May 2023 02:31:05 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 13 May 2023 02:31:05 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 13 May 2023 02:31:05 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 13 May 2023 02:31:05 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 13 May 2023 02:31:05 GMT
ARG MAVEN_VERSION=3.9.1
# Sat, 13 May 2023 02:31:05 GMT
ARG USER_HOME_DIR=/root
# Sat, 13 May 2023 02:31:05 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 13 May 2023 02:31:05 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 13 May 2023 02:31:05 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7ed20885ae48fa1760360e568c1aaba07f51cc6d418715514060ff0826a40c72`  
		Last Modified: Fri, 12 May 2023 19:28:02 GMT  
		Size: 64.1 MB (64134800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b4304cfeb9cd05da40eb403f2ab7b43356f3ffd9ce751e9b43e88435ad661a`  
		Last Modified: Sat, 13 May 2023 02:33:32 GMT  
		Size: 144.9 MB (144939618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab8373b66494b347cf6f89bc80f44b794b850c21b2131e393945bdb1c28e743`  
		Last Modified: Sat, 13 May 2023 04:26:44 GMT  
		Size: 115.9 MB (115924666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1695da556392e043e132c60d071754cba70c15242d2ce1dbcc8960188feb387a`  
		Last Modified: Sat, 13 May 2023 04:26:37 GMT  
		Size: 9.1 MB (9106167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e930c42f96f3a49dc6c075010a917e50ee9f4a63c7a3f7af8fadd23a08c43a`  
		Last Modified: Sat, 13 May 2023 04:26:36 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17ed6136f63e03f7c5b3041342047c3f9686bd698d04d626919cf462295f3d4`  
		Last Modified: Sat, 13 May 2023 04:26:36 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f289b6342a2aca3f223904c427dfef7392b000d2561b06495e8360b57a37008`  
		Last Modified: Sat, 13 May 2023 04:26:36 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
