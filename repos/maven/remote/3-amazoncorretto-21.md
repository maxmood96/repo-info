## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:e2c9203df20c7eb5d8c7ccddea9d7200b665d8bfc9df1acacad9a7a96cee07fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:146f83e1a17b659321e3d8c44ae245544e8f9f7c70709918fc4b15e68b1de35e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.2 MB (429237859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9539b3a9ea043f8ef302bd8778c5ccf3502a95599ed75b76e96b36f9f187fb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=21.0.7.6-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=21.0.7.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:c93eb42fc1cb8cbc6518e0c84a8b5166a23b8e065c2ea156492279ccf234ec25`  
		Last Modified: Fri, 13 Jun 2025 16:58:44 GMT  
		Size: 63.0 MB (62962939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f9e34af8ecbd84622c0fbc24a367b13e7e66d52134ec026aeb549f49fd8dbc`  
		Last Modified: Fri, 13 Jun 2025 17:15:21 GMT  
		Size: 164.9 MB (164854552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3200c7db01762bb3aadf58fc896c0f6522968c7c72d6ce5243b37e68f14c954c`  
		Last Modified: Fri, 13 Jun 2025 20:30:13 GMT  
		Size: 162.1 MB (162149768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d74d5609103363ee1b5f397f115b06a18e9bd68fb119c7d5ac86224e9b530e`  
		Last Modified: Fri, 13 Jun 2025 17:23:28 GMT  
		Size: 30.1 MB (30099123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a06fdabf3cdb5d97ffe6044cc7bafaa5f13a8f001cdeb6ab8e0d68b8ea4e0e8`  
		Last Modified: Fri, 13 Jun 2025 17:23:26 GMT  
		Size: 9.2 MB (9170435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef32daf7d6ee38e01b92bbead9c15cc1c5963ccd14934bd15ad7329938aa2e9`  
		Last Modified: Fri, 13 Jun 2025 17:23:26 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b601b6b742034ef27579d83955df6574714ed33009d8cda8854f4fd4a3b759`  
		Last Modified: Fri, 13 Jun 2025 17:23:26 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:c963b0b5cb93cc85f77e4a42c60f5d8d1a12b7ee482dd5df6b869225f30ee9e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6943328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee2010c1969c54463eaed81b258df58bc0a7b624452f42245a2d2ffffdbef10`

```dockerfile
```

-	Layers:
	-	`sha256:f819a1249fedc7dce0801356ac5d2c8f49ea15e92bc263d68ac1d321ea5e19f1`  
		Last Modified: Fri, 13 Jun 2025 20:27:44 GMT  
		Size: 6.9 MB (6925098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae978401ecc69cbf1c17d297ded6b2e7cc3b262ab4f575ec9162140aecdbd733`  
		Last Modified: Fri, 13 Jun 2025 20:27:45 GMT  
		Size: 18.2 KB (18230 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:ccdbbc2a2e4d50d7ed6d8ea7cc516a521dd2dc6a971bc2ae22bf64e5e1d1e390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.9 MB (405911450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54c1b313c3795ea23d42498ea42517c1c46b8295df84af6cafcecae940ad34b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=21.0.7.6-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=21.0.7.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1b914e688cac327114c45b9a58220765af260230389654eb4d8798d0a7d9676d`  
		Last Modified: Thu, 15 May 2025 19:24:15 GMT  
		Size: 64.6 MB (64607481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5767f014b050afc587e9ad7bd97300c4413147067eec529f41a8051ad29ffd6`  
		Last Modified: Tue, 20 May 2025 00:49:43 GMT  
		Size: 162.9 MB (162936873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68bd579f785956151b9b62a46851f555d2a6f1494aa29d7dd8883e6dba2f62d`  
		Last Modified: Tue, 03 Jun 2025 17:34:12 GMT  
		Size: 138.0 MB (137992388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c905e2482d23caa806f32744adcb3ccbb3c862b597ad5f4f610144b08686cd`  
		Last Modified: Tue, 03 Jun 2025 14:22:10 GMT  
		Size: 31.2 MB (31203220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a170c25db7dad18eeeef1642162d866c969af18ebc31fcbaa1e2dd3a4bd80ec`  
		Last Modified: Tue, 03 Jun 2025 14:22:07 GMT  
		Size: 9.2 MB (9170449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b42b4e89a280fe4d9eb1efe769efacaf63a551c2476dad921b0c9ba0d406a5`  
		Last Modified: Tue, 03 Jun 2025 14:22:06 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f76cbfddb3f7287989a1fd2c16bf8ee5c7812cffc19346854882a3f5b670b33`  
		Last Modified: Tue, 03 Jun 2025 14:22:06 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:c0273f81c86f5f214e49b5752f0247041d07989f929ee0e35613021e119c8f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6936436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f64fdbd891ad614fd0052b7e4bbb3eaf16372b20c1e1ed172bb776debfc7f45`

```dockerfile
```

-	Layers:
	-	`sha256:78895ced5a3216b36cda0cbd7d1e4ec0dc9c94392da827c3cbc9283e8dfbe6d4`  
		Last Modified: Tue, 03 Jun 2025 17:28:11 GMT  
		Size: 6.9 MB (6918059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acd5ad3b75712a7219a786c507971e920e1e06d480d1633743c334a7fe55de1b`  
		Last Modified: Tue, 03 Jun 2025 17:28:12 GMT  
		Size: 18.4 KB (18377 bytes)  
		MIME: application/vnd.in-toto+json
