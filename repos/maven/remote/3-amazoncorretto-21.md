## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:250f8e8e60e3f7818e1b0aca93db8a7802ecb4428e9c57699b0a530146204047
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:ea8e6b146bafc6434a9de5725cc9dd00283b44c38807416599a92c60dfb5a99d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.7 MB (445719520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3786f41b9868d1861486ad1f6f1c101ac3a674b354aaa2de29e82c3ca2ad3eb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 08 May 2026 22:56:20 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:56:20 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:18:41 GMT
ARG version=21.0.11.10-1
# Sat, 09 May 2026 00:18:41 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 09 May 2026 00:18:41 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:18:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sat, 09 May 2026 01:25:18 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Sat, 09 May 2026 01:25:26 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Sat, 09 May 2026 01:25:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 09 May 2026 01:25:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 09 May 2026 01:25:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 09 May 2026 01:25:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 09 May 2026 01:25:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 09 May 2026 01:25:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 09 May 2026 01:25:27 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 09 May 2026 01:25:27 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 09 May 2026 01:25:27 GMT
ARG USER_HOME_DIR=/root
# Sat, 09 May 2026 01:25:27 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 09 May 2026 01:25:27 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 09 May 2026 01:25:27 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3f708fc5705625846e206621966842bfead7ee5b8e4fc20aab0c77c563600126`  
		Last Modified: Wed, 06 May 2026 07:46:46 GMT  
		Size: 62.9 MB (62859738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9cfa01f6f50186ff951fe8a5adec9b1754ff3c7f4cade9ab86b8404fb53c876`  
		Last Modified: Sat, 09 May 2026 00:19:01 GMT  
		Size: 165.7 MB (165695497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f2572fcd50dfdaf514eaaee0ad4591624f427f91598fe6ef1c3c9683a17786`  
		Last Modified: Sat, 09 May 2026 01:25:56 GMT  
		Size: 177.8 MB (177772385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5010e0c7f3fe916ebf1b8382f0e98e447d6c307c8ad88ddc224b1f7d927a5964`  
		Last Modified: Sat, 09 May 2026 01:25:54 GMT  
		Size: 30.1 MB (30078636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582bf4a2dcaf84d1bce5710e664a1f98aaccd379518141d5ad51d1929d9d6f8b`  
		Last Modified: Sat, 09 May 2026 01:25:53 GMT  
		Size: 9.3 MB (9312254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191be499dd0971dc5deb5c9e54c19ddad8b3959d877634ebfa0b20fc1551b0a6`  
		Last Modified: Sat, 09 May 2026 01:25:52 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4944bbcf8623efff26b32f8bf4e0cb056d2b5f350f8c784114f05684cdf0ce74`  
		Last Modified: Sat, 09 May 2026 01:25:53 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:f5bf94c112a496714dab851a82effcb49c44296271f06aad5fa17c7ba5e9fdcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6949437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299deb897257852c551c3729f7eefb85eae58e2f902d54621969fa8434046a8c`

```dockerfile
```

-	Layers:
	-	`sha256:931dd05f9b587c8505aaa357493b2f204fc4328f2d1cd5e3696c66729c5f09fc`  
		Last Modified: Sat, 09 May 2026 01:25:52 GMT  
		Size: 6.9 MB (6933065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f578c6ba5af8d622d29a961bc1e75c996a0d64aff972496ede7f823774cf926a`  
		Last Modified: Sat, 09 May 2026 01:25:52 GMT  
		Size: 16.4 KB (16372 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:367b31ae45586bdeb80fadbb596e181f62b93f527f70f8afcf6ac6b2a89dd722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.6 MB (422618627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff3910a3ca71b8ffdb7fa4d140486187a5246d6c4ca81fe6bf663e453ec04cb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 08 May 2026 22:48:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:14 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:16:16 GMT
ARG version=21.0.11.10-1
# Sat, 09 May 2026 00:16:16 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 09 May 2026 00:16:16 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sat, 09 May 2026 01:48:56 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Sat, 09 May 2026 01:49:03 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Sat, 09 May 2026 01:49:03 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 09 May 2026 01:49:03 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 09 May 2026 01:49:03 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 09 May 2026 01:49:03 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 09 May 2026 01:49:03 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 09 May 2026 01:49:03 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 09 May 2026 01:49:03 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 09 May 2026 01:49:03 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 09 May 2026 01:49:03 GMT
ARG USER_HOME_DIR=/root
# Sat, 09 May 2026 01:49:03 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 09 May 2026 01:49:03 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 09 May 2026 01:49:03 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:835dd3779a793c24eeba54a176badcbf0ecf82042603b5459dd57e14ad679d47`  
		Last Modified: Wed, 06 May 2026 07:46:52 GMT  
		Size: 64.8 MB (64808915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f87a0855aa50b62231df0a7450bc85e3a796b7e5ecb8e320d2afeb62f477b5`  
		Last Modified: Sat, 09 May 2026 00:16:38 GMT  
		Size: 163.9 MB (163907987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c72d45dacda1777ed2ab56ab3fdfc58d6402aad727804231d368b9770733dbe`  
		Last Modified: Sat, 09 May 2026 01:49:29 GMT  
		Size: 153.4 MB (153381012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d830dd4489652e07a8837130b7fad80c266ab03da560a9ac1f5a0d51e01a2165`  
		Last Modified: Sat, 09 May 2026 01:49:27 GMT  
		Size: 31.2 MB (31207445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27be6f1abfaf2f2803383639e901e8f7a0474fb615d7a75f33c2947c8a96359`  
		Last Modified: Sat, 09 May 2026 01:49:26 GMT  
		Size: 9.3 MB (9312259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f203d8504c7c0a113a4005fa56153d8f21a10e202773480b077206fc70a7df5`  
		Last Modified: Sat, 09 May 2026 01:49:25 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe5c30fca9f5f63a6cc58d51d0855078b3774b9e4b635f2d7a068bd3e08fff8`  
		Last Modified: Sat, 09 May 2026 01:49:26 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:3f6237b1232ddbb79dfbc8657f6b34912147da58db08a24e1984d630b096ea05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6946983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb0f1c485c92fea66efe2266d27ae13b3a74a609a2aa02f2e12a00f2c7ab911`

```dockerfile
```

-	Layers:
	-	`sha256:e03068b28c03ca1e397d2065beda4dcb0a8eba9bc3c159a49ed43bef513d7932`  
		Last Modified: Sat, 09 May 2026 01:49:26 GMT  
		Size: 6.9 MB (6930464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d626c1df76cf8e8b1ae9ea6f094df0e01dacf2720ed715ff93ea7d26aa556618`  
		Last Modified: Sat, 09 May 2026 01:49:25 GMT  
		Size: 16.5 KB (16519 bytes)  
		MIME: application/vnd.in-toto+json
