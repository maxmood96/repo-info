## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:c7fb7661ddc880221e4517cc146d3debda3fcf0142aca98b140335078fac55d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:ab9c420b7ea253539b30efae24875bf1a92d78aa35079f76d02bf1a286b0b48c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.9 MB (439877534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04409aac42987093db02fcf4852b2ec7ae3d5028e883cffa3700dd6b60cbe41a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:59 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:59 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:16:49 GMT
ARG version=21.0.9.11-1
# Fri, 14 Nov 2025 02:16:49 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 14 Nov 2025 02:16:49 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:16:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 14 Nov 2025 03:19:01 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 14 Nov 2025 03:19:09 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 14 Nov 2025 03:19:09 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 03:19:09 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 03:19:09 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 03:19:09 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 03:19:09 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 03:19:09 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 03:19:09 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 03:19:09 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 03:19:09 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 03:19:09 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 03:19:09 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 03:19:09 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 03:19:09 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 03:19:09 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a166f6cf3d563466b8593a9f7ccbd9fdded8dde0e0236e5f99fb72b2542f98f7`  
		Last Modified: Fri, 14 Nov 2025 03:12:58 GMT  
		Size: 165.5 MB (165496641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823f43549c614d72aa08c51615863d8797b413ad05fc83a7971a5c61159a0df0`  
		Last Modified: Fri, 14 Nov 2025 06:28:33 GMT  
		Size: 172.2 MB (172157329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230876605f0a6d0d00e214c9b46f4cf01047322132252143838a145b27461ecc`  
		Last Modified: Fri, 14 Nov 2025 03:20:00 GMT  
		Size: 30.0 MB (30049382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a6c5532f9881daf61e8304e38bdbb002ff6b38f1d156a65b9d95f862754fe0`  
		Last Modified: Fri, 14 Nov 2025 03:19:55 GMT  
		Size: 9.2 MB (9242569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb27be18d8e0f611d6eaf5ea1965606e4c3a1ad968ab46ac84d255c404c0813e`  
		Last Modified: Fri, 14 Nov 2025 03:19:54 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5246c8b02e6bd500029084a34ab90b012cb6cad7563f43fc5d2f941700102d26`  
		Last Modified: Fri, 14 Nov 2025 03:19:54 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:27ef96c4cbb0e4c212b525a2e9079e52639176eea9fa1381638c5a4ad47ae71e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6950374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6b3a22f994a5f6186355d691fe8c9441289f5f75a42d638ee79edcc23618af`

```dockerfile
```

-	Layers:
	-	`sha256:ad1f43043778e7a531de7f3aef4dcd69f0b1cbb2064b7f8b31e6031f871c3860`  
		Last Modified: Fri, 14 Nov 2025 06:28:11 GMT  
		Size: 6.9 MB (6932159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b19ba909cb96b8cf9eccf80baf61c37d7be5c3fe33aa7b36b02cda1ab75c72e`  
		Last Modified: Fri, 14 Nov 2025 06:28:12 GMT  
		Size: 18.2 KB (18215 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:30a8c8b3fc4c4a990ca02433d55bae2cdf1150de31ff261c6a33da7debbf75d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.8 MB (416841995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642f8c60e088e0fd1ba49e7998449dae31be8f016433a5823cd66b654c2337fe`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:55 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:55 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:19:27 GMT
ARG version=21.0.9.11-1
# Fri, 14 Nov 2025 02:19:27 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 14 Nov 2025 02:19:27 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:19:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 14 Nov 2025 03:19:09 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 14 Nov 2025 03:19:17 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 14 Nov 2025 03:19:17 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 03:19:17 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 03:19:17 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 03:19:17 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 03:19:17 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 03:19:17 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 03:19:17 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 03:19:17 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 03:19:18 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 03:19:18 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 03:19:18 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 03:19:18 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 03:19:18 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 03:19:18 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adc1065a41b23a55095b5f6e1136f60393083fb07a288894b3f8820156fe2c2`  
		Last Modified: Fri, 14 Nov 2025 03:14:28 GMT  
		Size: 163.6 MB (163582983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711eb6807d68a55c257b49e088f7021c31111dcce338b04f9e21fd5fb810669b`  
		Last Modified: Fri, 14 Nov 2025 06:30:41 GMT  
		Size: 148.0 MB (148031426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e0747789f2b4198ff2603b5d59049ffd022a9b4d03d8f2637b22d6370867a4`  
		Last Modified: Fri, 14 Nov 2025 03:20:25 GMT  
		Size: 31.2 MB (31191174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7d3e141ddbce957c074d1c766d4ce3fb8972e117bdd29ef5ee11e2f6360a5b`  
		Last Modified: Fri, 14 Nov 2025 03:20:17 GMT  
		Size: 9.2 MB (9242570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d7aad253ae8193a4c595f2ed9f73e1e2aa15277f4f15cb631ebff3e0b0b23a`  
		Last Modified: Fri, 14 Nov 2025 03:20:17 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dd47a10166e13aab3f38057e3fb672d4d25fe4d9a08074e5145ae0648f0edf`  
		Last Modified: Fri, 14 Nov 2025 03:20:16 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:03b7eea890b28f7b756e2f86f4d85a9f899519cd980596a7083a2860adbce49e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6947922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca28e081395956088501ed473376a0c0d66e60f32832d020fe6269a660f10543`

```dockerfile
```

-	Layers:
	-	`sha256:b7ede984f102d9f67f90e253b0f30a2ab208ff52a8590942b2162a2808bcc9f5`  
		Last Modified: Fri, 14 Nov 2025 06:28:17 GMT  
		Size: 6.9 MB (6929558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5a2d61b3af0e124caf628b4b5634c3e50d118a70a792639bf21f85644fb7455`  
		Last Modified: Fri, 14 Nov 2025 06:28:18 GMT  
		Size: 18.4 KB (18364 bytes)  
		MIME: application/vnd.in-toto+json
