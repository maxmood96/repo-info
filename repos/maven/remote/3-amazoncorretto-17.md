## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:202d9532fc5519f7df02f4b9a6450af93a97a48276bf7975d25f9a10284d366b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:dfe27b89c9f729f342a9bf29fa4e912d53ee5adc6d87e3886487839e8d5b65c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.4 MB (374431906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8e7b39c2bdd19ecacdd4e5028826515410e7dafec953d4a11a91ee5db8001b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 13 May 2023 00:19:34 GMT
COPY dir:7a824a76678fb4ef17879dcecd9fac65df3d1efbef31a3b874da9f49f49b6814 in / 
# Sat, 13 May 2023 00:19:34 GMT
CMD ["/bin/bash"]
# Sat, 13 May 2023 01:34:17 GMT
ARG version=17.0.7.7-1
# Sat, 13 May 2023 01:34:42 GMT
# ARGS: version=17.0.7.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 13 May 2023 01:34:43 GMT
ENV LANG=C.UTF-8
# Sat, 13 May 2023 01:34:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sat, 13 May 2023 01:34:43 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Sat, 13 May 2023 01:34:43 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 13 May 2023 01:34:43 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 13 May 2023 01:34:43 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 13 May 2023 01:34:43 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 13 May 2023 01:34:43 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 13 May 2023 01:34:43 GMT
ARG MAVEN_VERSION=3.9.1
# Sat, 13 May 2023 01:34:43 GMT
ARG USER_HOME_DIR=/root
# Sat, 13 May 2023 01:34:43 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 13 May 2023 01:34:43 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 13 May 2023 01:34:43 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:bf72c394abb748707ec4590d5017f36ad47098c9b92adc1b04c3ea3ba0b395f6`  
		Last Modified: Fri, 12 May 2023 00:07:44 GMT  
		Size: 62.5 MB (62494714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edf64cf85c039184023bdfaa7e82e8a607c7f0a55286cce0c938431af0d83d3`  
		Last Modified: Sat, 13 May 2023 01:37:36 GMT  
		Size: 152.0 MB (151974038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49b4a3dc518fd66860f57ba814bc907251038be413abe9732e86057ec03d453`  
		Last Modified: Sat, 13 May 2023 03:56:54 GMT  
		Size: 150.9 MB (150855628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7729465f23aaeafd2cb2b38a39af222215ab7401d0186e7433e84e496932b2fc`  
		Last Modified: Sat, 13 May 2023 03:56:42 GMT  
		Size: 9.1 MB (9106142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e1b67dfcecd1aa19ca1d2a5ac5e06e078eceefe44156ac32711073d2f7eb1c`  
		Last Modified: Sat, 13 May 2023 03:56:42 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1dee3033ba6d7dd31f73c22a68ad78d83a886cf9aa1c5b67367ee481af6c6bb`  
		Last Modified: Sat, 13 May 2023 03:56:42 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7109d335b7f2fbaac401b9e17757c95fe2a071fc21e99c5cfa88d3896cf1bb`  
		Last Modified: Sat, 13 May 2023 03:56:42 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:055663bbec7ff57f54df1f105a0ede9757aa3f450a6c88c2730d54e82f234bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339627370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4cf3e4ca393f71714e3f90126595c63796c4485b4c775c5ef68c344507e00c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 13 May 2023 00:39:27 GMT
COPY dir:71cecf11386ac326afd2beed7b45e00586f5b9ab017bb6ace5dec65e5aa62900 in / 
# Sat, 13 May 2023 00:39:27 GMT
CMD ["/bin/bash"]
# Sat, 13 May 2023 02:31:16 GMT
ARG version=17.0.7.7-1
# Sat, 13 May 2023 02:31:36 GMT
# ARGS: version=17.0.7.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 13 May 2023 02:31:38 GMT
ENV LANG=C.UTF-8
# Sat, 13 May 2023 02:31:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sat, 13 May 2023 02:31:38 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Sat, 13 May 2023 02:31:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 13 May 2023 02:31:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 13 May 2023 02:31:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 13 May 2023 02:31:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 13 May 2023 02:31:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 13 May 2023 02:31:38 GMT
ARG MAVEN_VERSION=3.9.1
# Sat, 13 May 2023 02:31:38 GMT
ARG USER_HOME_DIR=/root
# Sat, 13 May 2023 02:31:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 13 May 2023 02:31:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 13 May 2023 02:31:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7ed20885ae48fa1760360e568c1aaba07f51cc6d418715514060ff0826a40c72`  
		Last Modified: Fri, 12 May 2023 19:28:02 GMT  
		Size: 64.1 MB (64134800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f531e2cf78efc9a3808075863cbac8998096d9d52e7683e55f2b9908762bd327`  
		Last Modified: Sat, 13 May 2023 02:34:01 GMT  
		Size: 150.5 MB (150466246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf3fb9da625022aaa467d95e802133758c80206ca35a786789bb0a461e9de82`  
		Last Modified: Sat, 13 May 2023 04:27:16 GMT  
		Size: 115.9 MB (115918773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf45fdd3e4de7943268b9bb96c7515aaf8db0d49fe285ea2b3d0382145391ef`  
		Last Modified: Sat, 13 May 2023 04:27:08 GMT  
		Size: 9.1 MB (9106168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a60d44d7941163ce4b03a6d0dd2d112e0fd85e057e3c60eaf91362f042a2a9`  
		Last Modified: Sat, 13 May 2023 04:27:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bf954a2049e6a0eaeacbe45c9572c912f4c580099bc8acf15074725499a1ce`  
		Last Modified: Sat, 13 May 2023 04:27:07 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b202f3ae07ab2e6e8d4e4f2afbb235f14b0694ac2fa2d5db7a7a8dd456de06`  
		Last Modified: Sat, 13 May 2023 04:27:07 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
