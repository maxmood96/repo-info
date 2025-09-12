## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:e2d145396855bc17b8d2778b052c03de10032d6ab384116ec10648d69bbd9240
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:86a09bc5945da0ce3488f050573b7e81ef69ff15a1629a3ab077ed31997b0e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.6 MB (434610331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed8c60c5c2be5cdf19ba59a40c9571266818d41807c68bc0b52d69f7653298f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=21.0.8.9-1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=21.0.8.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0c31e84362b17be00ccd03302ca56ddbf8561b17d46e8c82bc87c21d389e7731`  
		Last Modified: Mon, 08 Sep 2025 20:24:26 GMT  
		Size: 63.0 MB (62983288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b36f57401d22c5ce3a8b17949794d2930d081991fe213b74b1e21a17a967cc5`  
		Last Modified: Fri, 12 Sep 2025 02:10:45 GMT  
		Size: 165.1 MB (165095601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de208ec6cc2b235a53a7bc2711311db75e0af840961b72d8cbd202ba7d36da76`  
		Last Modified: Fri, 12 Sep 2025 05:30:56 GMT  
		Size: 167.2 MB (167173499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec13eff2edb4c7b345f6af2e663e716ef75be65320fc100c1f8c2041cb178f7`  
		Last Modified: Fri, 12 Sep 2025 03:11:22 GMT  
		Size: 30.1 MB (30114327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69e2a2fe7e0c92aa5d800733843410721135d1be6d1e235298a05d700a1c58`  
		Last Modified: Fri, 12 Sep 2025 02:55:40 GMT  
		Size: 9.2 MB (9242573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700577cf554b9674e713d9b81d85188eb259d4a10b5096f189885d58ad4d17d8`  
		Last Modified: Fri, 12 Sep 2025 02:55:38 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191be6c117d950a65ab1180163c953bb0f85ca88af0077b093fa74bd5e9b641a`  
		Last Modified: Fri, 12 Sep 2025 02:55:38 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:41ef685edac688167715f1e731284cbad21414a5aea3a6306c976d9a5fd6cfdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6947161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba43d33892fec4a9db28cb4f3241d8e33ea1f2eebab662617bfe09353d8b4394`

```dockerfile
```

-	Layers:
	-	`sha256:8a812911f783425fd702256b025ae88d32880d2ed4ea25bf5555f0c326381d4d`  
		Last Modified: Fri, 12 Sep 2025 05:28:06 GMT  
		Size: 6.9 MB (6928924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24ee181554165a118b47811d6897cd2ba7cb4f2d0b05d4821ffa5d15d4af197a`  
		Last Modified: Fri, 12 Sep 2025 05:28:07 GMT  
		Size: 18.2 KB (18237 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:73398815089571ec6870e2f6b614790b1e66f0e4e3c2056fee4908d48fcc5ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.4 MB (411391353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93a8085409226cc8c71f15c4e49a359135a5bdadf7f1678015af932c2f3744a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=21.0.8.9-1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=21.0.8.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:44fb931604a5509dd2f5cbf8d1604d64dd0f56962f61bf6cd3f092bce2e7687a`  
		Last Modified: Wed, 10 Sep 2025 17:52:55 GMT  
		Size: 64.8 MB (64791723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa6d86317b028a9d36113d2947c4a0e9c1745da57a94c18fe9fcc2c6108b279`  
		Last Modified: Fri, 12 Sep 2025 02:12:46 GMT  
		Size: 163.1 MB (163109940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f10edfe5a768a16818276bdfe0246ca53bd03ecbab640736bf791fc117d5a5`  
		Last Modified: Fri, 12 Sep 2025 05:29:51 GMT  
		Size: 143.1 MB (143051956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a11db309fba0f89a77ea64fab8dc269b49a78e8c421872f1d66c8f85d193dc2`  
		Last Modified: Fri, 12 Sep 2025 05:29:45 GMT  
		Size: 31.2 MB (31194112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d5db2de3e6f27f8ba78b1bc9b08cfb488a4fd9ca2883b8b248ddf7f23889d1`  
		Last Modified: Fri, 12 Sep 2025 02:59:58 GMT  
		Size: 9.2 MB (9242581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f674c4ccbc3d60beff51e5edd29e68eab2f84cc55b00329e72aada297aa4f4e`  
		Last Modified: Fri, 12 Sep 2025 02:59:57 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2f47f0741699d1073e7ffbe4ee8f6a2e9531b4a0ed22d3e52789d7ec1dc4c3`  
		Last Modified: Fri, 12 Sep 2025 02:59:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:56f57ab821c1361609ae1b7e4765e6e923f5b7fe899cf4a7f7f103cd743ab172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6944708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6daa5b37eafcafbeb590f12d9be05c21a642eb61fc3fde245c1903747ab20593`

```dockerfile
```

-	Layers:
	-	`sha256:38e960b1b858e1b201a3089f1746119676b4846e159152a06f7426bd4fedf748`  
		Last Modified: Fri, 12 Sep 2025 05:28:12 GMT  
		Size: 6.9 MB (6926323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05232c4538f25ab2f74536d5943772ae64fb8d5dd353fd9a66cefc8e383ca104`  
		Last Modified: Fri, 12 Sep 2025 05:28:12 GMT  
		Size: 18.4 KB (18385 bytes)  
		MIME: application/vnd.in-toto+json
