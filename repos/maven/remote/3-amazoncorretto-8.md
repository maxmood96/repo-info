## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:bb72174154c454ae1ed1652ac85f3776802250de76ba68c5576aec83efb5b379
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:41c4dbb0a36ea7f3c10d22ed9a4dbfdc40f20ee5d5efeadab01279d7e148880e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.9 MB (354850286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c602614a2071d6519e2af82021622583b39672ad4837766641d089cc0882ece`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 Apr 2026 22:16:57 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:16:57 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 22:47:05 GMT
ARG version=1.8.0_482.b08-1
# Mon, 13 Apr 2026 22:47:05 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 13 Apr 2026 22:47:05 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 22:47:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 13 Apr 2026 23:43:47 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 13 Apr 2026 23:43:56 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 13 Apr 2026 23:43:56 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 13 Apr 2026 23:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 13 Apr 2026 23:43:56 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 13 Apr 2026 23:43:56 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 13 Apr 2026 23:43:56 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 13 Apr 2026 23:43:56 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 13 Apr 2026 23:43:56 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 13 Apr 2026 23:43:56 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 13 Apr 2026 23:43:57 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 13 Apr 2026 23:43:57 GMT
ARG MAVEN_VERSION=3.9.14
# Mon, 13 Apr 2026 23:43:57 GMT
ARG USER_HOME_DIR=/root
# Mon, 13 Apr 2026 23:43:57 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 13 Apr 2026 23:43:57 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 13 Apr 2026 23:43:57 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5a3a1a219789b0285ea1d6a41ad03e6fab76f369592968c458dbfffd408719dd`  
		Last Modified: Thu, 09 Apr 2026 08:25:08 GMT  
		Size: 63.0 MB (62955266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a794e049eea4656f53218f0a128a5ac86b2b1d0ecba2ae7bcacfb35ebf5a1a`  
		Last Modified: Mon, 13 Apr 2026 22:47:20 GMT  
		Size: 76.1 MB (76123704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dce9946d640c1a817008b4ff51430539a402bddf6d14346d09b3215bae8497a`  
		Last Modified: Mon, 13 Apr 2026 23:44:24 GMT  
		Size: 176.4 MB (176385430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed30180af21397b359c80ae42426046f627c5dd9e428cf8e363afb06f886ab81`  
		Last Modified: Mon, 13 Apr 2026 23:44:21 GMT  
		Size: 30.1 MB (30073654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150badff6b54eb3862d820ba909c8ad3f3298a54fc9e434bbfaba2769d83b0bb`  
		Last Modified: Mon, 13 Apr 2026 23:44:21 GMT  
		Size: 9.3 MB (9311192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d260d7727b583acfbd7ab539f70518737450e531eb052ebe3c8bfed5b556f2`  
		Last Modified: Mon, 13 Apr 2026 23:44:20 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32534ce69e05984307e3b76e2a34d60e5d4756e0723001b03abb99c51081f637`  
		Last Modified: Mon, 13 Apr 2026 23:44:21 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:b924a2f4004104aa641582af820560acc9b475a8fb431bbffd91f16829cb19a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6791889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1be3f64ed7efd22f654c8ee3d7897543b7b4905be6d4f9c76f7edc379fc2fa`

```dockerfile
```

-	Layers:
	-	`sha256:efc366f1cc2c18d4c40f4dd0f9c8a4a6a1bdd80eccd27685007b0faf2f13433e`  
		Last Modified: Mon, 13 Apr 2026 23:44:20 GMT  
		Size: 6.8 MB (6773702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d67d8b28bd9316ecec78b132791e21256845084b492aecfc453440031db5fa53`  
		Last Modified: Mon, 13 Apr 2026 23:44:20 GMT  
		Size: 18.2 KB (18187 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:72361ad14997fc968dcd4772992456cbdf78ecdae6be8b7b60292aa29a0d0042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.2 MB (317177310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ac9eb81c362cf5850344ea275b58049e1471936f283da4be6e518e9601ae3b6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 Apr 2026 22:22:09 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:22:09 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 23:10:05 GMT
ARG version=1.8.0_482.b08-1
# Mon, 13 Apr 2026 23:10:05 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 13 Apr 2026 23:10:05 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 23:10:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 13 Apr 2026 23:57:09 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 13 Apr 2026 23:57:17 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 13 Apr 2026 23:57:17 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 13 Apr 2026 23:57:17 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 13 Apr 2026 23:57:17 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 13 Apr 2026 23:57:17 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 13 Apr 2026 23:57:17 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 13 Apr 2026 23:57:17 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 13 Apr 2026 23:57:17 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 13 Apr 2026 23:57:17 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 13 Apr 2026 23:57:17 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 13 Apr 2026 23:57:17 GMT
ARG MAVEN_VERSION=3.9.14
# Mon, 13 Apr 2026 23:57:17 GMT
ARG USER_HOME_DIR=/root
# Mon, 13 Apr 2026 23:57:17 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 13 Apr 2026 23:57:17 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 13 Apr 2026 23:57:17 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f1f2697b3535de3cb27d338e724d6283baf064a258669349257ede7e5670fff3`  
		Last Modified: Thu, 09 Apr 2026 08:25:15 GMT  
		Size: 64.8 MB (64802975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4147bf2fb905861a3018f299d8138ed0cae5ebe1b7d027943acb9616ee34ebb2`  
		Last Modified: Mon, 13 Apr 2026 23:10:20 GMT  
		Size: 59.9 MB (59923053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830f0b31f46951a39c30eb0c5ad4daa2a56131579cef4f18bd17d423470c69b0`  
		Last Modified: Mon, 13 Apr 2026 23:57:44 GMT  
		Size: 151.9 MB (151928917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc9f132c2a72e3c28f4f70493ce7d0f961a43ec35bf0bd1f4b303227ae32160`  
		Last Modified: Mon, 13 Apr 2026 23:57:40 GMT  
		Size: 31.2 MB (31210145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a607e9174bc0316ef8663eda9f416046674cc57b909b2d0383e7ce8a00c19bc4`  
		Last Modified: Mon, 13 Apr 2026 23:57:39 GMT  
		Size: 9.3 MB (9311176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b5b3738060148e5757285b4498725735148e7114ba5b65f0528eecc806d3ec`  
		Last Modified: Mon, 13 Apr 2026 23:57:39 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1361f06175463349c6d33cdac8065db508e8d616310b6b41aa7a0c7fe30d5382`  
		Last Modified: Mon, 13 Apr 2026 23:57:40 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:fd15056b213beb4cde2717ffbfe692bbd630f939e3b66a2b5215c48f6d3b33f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6769234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef923ca0545ea8424bd8a1fe56284277f79fc2ed6a07e0bdd456304b88990f4a`

```dockerfile
```

-	Layers:
	-	`sha256:841b27f4d0ad6a07deb312a198b0764ec2b2b3d1d13be8fefd66dbf19f58b451`  
		Last Modified: Mon, 13 Apr 2026 23:57:39 GMT  
		Size: 6.8 MB (6750899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b05c2d4c11fed0e6bb4c4dce2ef525bbb482057702d1fa8d171914791bf82ed2`  
		Last Modified: Mon, 13 Apr 2026 23:57:38 GMT  
		Size: 18.3 KB (18335 bytes)  
		MIME: application/vnd.in-toto+json
