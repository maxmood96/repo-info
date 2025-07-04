## `maven:amazoncorretto`

```console
$ docker pull maven@sha256:ddcc294e0a57f5fdfbbe6aa7e24c7dbef3ef279922bb513716d751bd5264df96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:4e0fdc42e996b77cc91e1e60cf2a2e438505d327d2892c19557594a06f863d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.1 MB (416075228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b748645ab808febaf414f48cdfb8dc88849e887fdd94d59b9a8beb12872ad7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=17.0.15.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sun, 22 Jun 2025 10:21:55 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN yum install -y openssh-clients # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ARG MAVEN_VERSION=3.9.10
# Sun, 22 Jun 2025 10:21:55 GMT
ARG USER_HOME_DIR=/root
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 22 Jun 2025 10:21:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 22 Jun 2025 10:21:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:59c3b062666ba29c100bd47e4ef63a7010fdd4d56e4483d5f68f9ba709e6f55c`  
		Last Modified: Wed, 25 Jun 2025 09:50:04 GMT  
		Size: 63.0 MB (62962854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82300c0b516b05fd33e5ee80103c72571455470c886da1e8007c97667bd2b934`  
		Last Modified: Fri, 04 Jul 2025 00:15:23 GMT  
		Size: 151.7 MB (151747120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9534f643137105c810e559f4864b99f29688bde3d2325514f96cb23e77e945dd`  
		Last Modified: Fri, 04 Jul 2025 02:27:43 GMT  
		Size: 162.3 MB (162330924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a4dcaf2ee57f0723f54acd1aa62cd0e1a9e2540354e52bf6f7311bbe5ec2ec`  
		Last Modified: Fri, 04 Jul 2025 00:17:29 GMT  
		Size: 30.1 MB (30079896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b1fe30466e79f3978f2db1a99cb39786c97a6173beb84de40c79391338ecbd`  
		Last Modified: Fri, 04 Jul 2025 00:17:27 GMT  
		Size: 9.0 MB (8953392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6943cc8d90bdde5d7099cafb916d64b68d73eed2e359216e5fa0206455950b`  
		Last Modified: Fri, 04 Jul 2025 00:17:26 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580635778352f69f4262046fdf1d6eb4a837694b376445388f01263f46052421`  
		Last Modified: Fri, 04 Jul 2025 00:17:26 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:7aecc3533ee12a2348600183b2e879424bb5b7569a5eb7dae51493add72fd6dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6947251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a391697e5db2263723818c3c5c975c2210768fbe607ba066c61a3d1d0ed752`

```dockerfile
```

-	Layers:
	-	`sha256:2f6d87c4d7bd7135770e96d94ba3c86b6990e0893e86d3f907a72fe27ec6621c`  
		Last Modified: Fri, 04 Jul 2025 02:27:22 GMT  
		Size: 6.9 MB (6927740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f9b0b81a318846000be5cda5c0f04297476a978407f2ca83e240368746f3424`  
		Last Modified: Fri, 04 Jul 2025 02:27:23 GMT  
		Size: 19.5 KB (19511 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:91a0cf20cb9bee31e7e660ef42da577d305f126216691e7ab2e4f42314ed0c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.6 MB (393552863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb2c3ea79c95e05a16efdeac6da260e9ee7d6bfaf58a9bae595f77ddf1b5b29`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=17.0.15.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sun, 22 Jun 2025 10:21:55 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN yum install -y openssh-clients # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ARG MAVEN_VERSION=3.9.10
# Sun, 22 Jun 2025 10:21:55 GMT
ARG USER_HOME_DIR=/root
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 22 Jun 2025 10:21:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 22 Jun 2025 10:21:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a3a141bfe5627b562a870ad931fe1cdc50d3dbf733a0568d089499010c9116cb`  
		Last Modified: Fri, 13 Jun 2025 17:05:27 GMT  
		Size: 64.8 MB (64790746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2534511df3b1b94ec92acd716dffc7823ca552c1555323f56c677e626d70179d`  
		Last Modified: Fri, 13 Jun 2025 20:08:56 GMT  
		Size: 150.4 MB (150388484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0299d45aa4d8aaa99f6897d14efe59f3b031958171886e01788741fec15a81`  
		Last Modified: Wed, 02 Jul 2025 17:37:08 GMT  
		Size: 138.2 MB (138231199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbddac9aa0fdf738985c407274d0ae8c15a7357441de273aa32d29c790480f2`  
		Last Modified: Wed, 02 Jul 2025 15:59:13 GMT  
		Size: 31.2 MB (31188008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b967a5586a63022e8b7091925a3553def0ca693978897f5209fffa86d43a22`  
		Last Modified: Wed, 02 Jul 2025 15:59:11 GMT  
		Size: 9.0 MB (8953384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f3318f11d2e1968cb2a1f9a53413aed3d66975f76eb43338fba0472fb28f31`  
		Last Modified: Wed, 02 Jul 2025 15:59:10 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8e6a77d05d34cd4264439096f77752f5892ca14ce6f5bf17b1575f6aa76566`  
		Last Modified: Wed, 02 Jul 2025 15:59:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:c8ce29661473ad6ce0974cafa3dcb04e2e0dd9922d8363cfc920bbcb6811c148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6944894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44187fdb3ee832978dc2a7f161614577a8df1a011677986005bc931f3671505`

```dockerfile
```

-	Layers:
	-	`sha256:f4f397b267667ef2172402c23cf1a819659651551251892a01662cafaeb9afe9`  
		Last Modified: Wed, 02 Jul 2025 17:27:31 GMT  
		Size: 6.9 MB (6925187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2387076534889c2868a664693b6060084d36a45dd11cedd00cc8c7c98cf94338`  
		Last Modified: Wed, 02 Jul 2025 17:27:31 GMT  
		Size: 19.7 KB (19707 bytes)  
		MIME: application/vnd.in-toto+json
