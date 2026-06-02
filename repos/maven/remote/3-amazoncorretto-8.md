## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:ffccccb5bb968316333e5d2fae16bcf8765159eeaba353edc49c195a8fc4205b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:a73f4ab77679346fd69c76d7b2d4bfcb49b018fc4c2568f5ee5824988dd5aead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.4 MB (358372251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1559cbb9df193df6282597bd127cac7100db203d4df01ab56a8e4380dcf81fd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 30 May 2026 00:27:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:27:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:10:18 GMT
ARG version=1.8.0_492.b09-2
# Sat, 30 May 2026 01:10:18 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 30 May 2026 01:10:18 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:10:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 02 Jun 2026 10:28:21 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 02 Jun 2026 10:28:30 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 02 Jun 2026 10:28:30 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 02 Jun 2026 10:28:30 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:28:30 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:28:30 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 02 Jun 2026 10:28:30 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Jun 2026 10:28:30 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 02 Jun 2026 10:28:30 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:28:30 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 02 Jun 2026 10:28:30 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Jun 2026 10:28:30 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Jun 2026 10:28:30 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Jun 2026 10:28:30 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf014bc5c79b2f534d915f84aac636fa5ebd127f2eea997472261c971c4bc8ed`  
		Last Modified: Sat, 30 May 2026 01:10:33 GMT  
		Size: 76.1 MB (76114509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5135192bd0117f00c681608b74e9765e11f84655be5ddc6927243631cf64d2`  
		Last Modified: Tue, 02 Jun 2026 10:28:58 GMT  
		Size: 179.9 MB (179891127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8708028fc4011213fc06fba5bdc5cec2a071328c1f2b21a8d0417ecad71e3229`  
		Last Modified: Tue, 02 Jun 2026 10:28:55 GMT  
		Size: 30.1 MB (30063682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4846c2ea9287e9f43b40bd336fd0e718be3596915ecdd3ffe28bbdd4ee4a1474`  
		Last Modified: Tue, 02 Jun 2026 10:28:54 GMT  
		Size: 9.4 MB (9359972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fa5bc7b9c42b40f692c954c918b9484ecdf32fc61ddf0f8069ca265cbcf4f9`  
		Last Modified: Tue, 02 Jun 2026 10:28:53 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebcfce0fc050b1b7c4adca4b1dd8aaf124743abc769829780fe6ccbdda5a1b7`  
		Last Modified: Tue, 02 Jun 2026 10:28:55 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:bad8dbc32863508f4199e442ee698bda2e41a0b204c68ab90ea4aafc3a1e390e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6789890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2359bbbdf7b70c413d1b58c75430b1906d241b2fbe8d73ba2fcb59ac2a8b6721`

```dockerfile
```

-	Layers:
	-	`sha256:aa964607b02cf51efaf741a58c0959b4ebe9521db0f4a5e2def466262b482981`  
		Last Modified: Tue, 02 Jun 2026 10:28:54 GMT  
		Size: 6.8 MB (6773705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd83593409211d5022b989919b47edf1ac48782afa3bdda54f6bfaad3248506e`  
		Last Modified: Tue, 02 Jun 2026 10:28:53 GMT  
		Size: 16.2 KB (16185 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f53d53e6d1dc295714195dc8e801244346aa98157545d9af4ff294693ad8ce39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.7 MB (320748261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91983638f678c5915db6edc96ab9603cf51301e2402a486910955559d7927519`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 30 May 2026 00:29:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:10:19 GMT
ARG version=1.8.0_492.b09-2
# Sat, 30 May 2026 01:10:19 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 30 May 2026 01:10:19 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:10:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 02 Jun 2026 10:25:20 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 02 Jun 2026 10:25:27 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 02 Jun 2026 10:25:27 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 02 Jun 2026 10:25:27 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:25:27 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:25:27 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 02 Jun 2026 10:25:27 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Jun 2026 10:25:27 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 02 Jun 2026 10:25:27 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:25:27 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 02 Jun 2026 10:25:27 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Jun 2026 10:25:27 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Jun 2026 10:25:27 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Jun 2026 10:25:27 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdab7eeb22e07597e24f8d98c9bb7b21deae088a4ffb5ab1a8c89bdd3e7cf72`  
		Last Modified: Sat, 30 May 2026 01:10:34 GMT  
		Size: 59.9 MB (59947957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2a82af9a7828e3384ea8b6ee0a31a6148ec84449adcc05d61bd78b9c4f2384`  
		Last Modified: Tue, 02 Jun 2026 10:25:56 GMT  
		Size: 155.5 MB (155458087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a115c679c674b3c0a7e22d11fe72cfdd1b440c68460e4f09f6041e0bdc38aa`  
		Last Modified: Tue, 02 Jun 2026 10:25:52 GMT  
		Size: 31.2 MB (31190531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1912bd7cc161bf6f2737403b8c8d0b31727ebfcba7255e993817cd2e222bee02`  
		Last Modified: Tue, 02 Jun 2026 10:25:52 GMT  
		Size: 9.4 MB (9359969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199de224917953460fd571fe2da1ee18de5104f030b0d46f5e5a5246b6cc8666`  
		Last Modified: Tue, 02 Jun 2026 10:25:51 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e614ec266e7ae77005fa57b4f6873c6b5f280b1f0cdae3ae4f0b6572535e57f0`  
		Last Modified: Tue, 02 Jun 2026 10:25:52 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:c61f06a4c6da7831f03d87be01c09d60d5baff506bd77990845d7a68726f5798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6767236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5006f863fc39f72a1ea8df28afeabc88b71f9c3ede9ed8542338ae5b668ce3b1`

```dockerfile
```

-	Layers:
	-	`sha256:fa8d5b35acd806f800f6f7fa7aa86fe5aa05bc44707db9deab0592b6af525bdd`  
		Last Modified: Tue, 02 Jun 2026 10:25:51 GMT  
		Size: 6.8 MB (6750902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa39a18dd98f8c5549aa836a21e2967a3b95d798e26b4f9083c0c60198fe3c1e`  
		Last Modified: Tue, 02 Jun 2026 10:25:51 GMT  
		Size: 16.3 KB (16334 bytes)  
		MIME: application/vnd.in-toto+json
