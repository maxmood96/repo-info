## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:c1602cd07f4720f1a686c9fe7f6df4ae73ed0d2dcb71ae621339a8e69df61114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:7f52e2cbce4b9ad3c85a9b8b333d537357dc48e9cc621046fc391e317fbb2057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.1 MB (299050389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33e04ec3c49e03c61c28f7fe8e45bd06944f57b067076de7f98c9c0b0eeccea`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 11 Mar 2024 23:50:32 GMT
COPY dir:40a794c5e13cc08a029a91ecc5d045abb1bd5b12f20c10640fe8595ecfefa662 in / 
# Mon, 11 Mar 2024 23:50:33 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 02:44:56 GMT
ARG version=1.8.0_402.b08-1
# Sat, 16 Mar 2024 02:45:19 GMT
# ARGS: version=1.8.0_402.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 16 Mar 2024 02:45:19 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 02:45:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 11 Dec 2023 11:12:11 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 11 Dec 2023 11:12:11 GMT
ARG USER_HOME_DIR=/root
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 11 Dec 2023 11:12:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 11 Dec 2023 11:12:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fbbe555f6365629780fee590c2a87f84df704cf88725f26d12c40efd06a20308`  
		Last Modified: Mon, 11 Mar 2024 23:51:11 GMT  
		Size: 62.7 MB (62650553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb10560a8f9e801648fa61c9413f00f01ca9391d5179e10ee7601c19e003c76`  
		Last Modified: Sat, 16 Mar 2024 03:01:51 GMT  
		Size: 75.5 MB (75529685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e108304d3533ffb6b45789fa1e1808de912d1b8e06f35b989962448762328ef`  
		Last Modified: Sat, 16 Mar 2024 11:14:32 GMT  
		Size: 151.4 MB (151388818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e35d9083db2abbdca5c531c53f27b2eb28f463b907cdc7365f53e1d7432aa9`  
		Last Modified: Sat, 16 Mar 2024 11:14:20 GMT  
		Size: 9.5 MB (9479949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e2c9b4309d038f99882918f33fa3a71a28d9ba6cee6622bc8fa81d3266b90f`  
		Last Modified: Sat, 16 Mar 2024 11:14:19 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f21e8b1da0bc2c1265bd72e4cf013116c3f7c6eaefceb4f690dd96a22136e1`  
		Last Modified: Sat, 16 Mar 2024 11:14:19 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cee243bf68de4851356fe4de6a02d4fd92fd98d92ac727376c61971d5d78725`  
		Last Modified: Sat, 16 Mar 2024 11:14:19 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:4b1d82cba332c748a081137ada636f8b9e64092c436f76e00471bcc07f8cc1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256056352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ecc8ed40d3c929195211daf8cbf25640d1a8fb3f7d5080063881b4f0b4bfb3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 11 Mar 2024 22:39:58 GMT
COPY dir:60a98a70510e647cb179bdf64e415936867e1b536f6e2209b88df6cf5ebf8753 in / 
# Mon, 11 Mar 2024 22:39:59 GMT
CMD ["/bin/bash"]
# Mon, 11 Mar 2024 23:10:11 GMT
ARG version=1.8.0_402.b08-1
# Mon, 11 Mar 2024 23:10:28 GMT
# ARGS: version=1.8.0_402.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 11 Mar 2024 23:10:28 GMT
ENV LANG=C.UTF-8
# Mon, 11 Mar 2024 23:10:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 11 Dec 2023 11:12:11 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 11 Dec 2023 11:12:11 GMT
ARG USER_HOME_DIR=/root
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 11 Dec 2023 11:12:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 11 Dec 2023 11:12:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1210c2cda2cd148732bb93623044ab07d9ead686e335afc95ffa891e3032d56b`  
		Last Modified: Mon, 11 Mar 2024 22:40:31 GMT  
		Size: 64.6 MB (64576374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6159e5430f33d9753d1e2bb2b880f94d26d09993e0ce8077a80c0270112713dc`  
		Last Modified: Mon, 11 Mar 2024 23:20:27 GMT  
		Size: 59.6 MB (59640342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a35d4fc8c907cd3cafa3fc18c9a69363e9b53ae987d06e5c8259901452d4ae`  
		Last Modified: Tue, 12 Mar 2024 00:21:20 GMT  
		Size: 122.4 MB (122358327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98b27f86535ee7ae90c48fb80a7267fe49d1b6583ea675e3b1683edcb484569`  
		Last Modified: Tue, 12 Mar 2024 00:21:11 GMT  
		Size: 9.5 MB (9479928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f50ffbafb755f731378b9802facfe19caaf31cc2e4ddf441f18255c4cb4065`  
		Last Modified: Tue, 12 Mar 2024 00:21:10 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec45db47e31a43439e7a3a71858471f93cf5a75b0f71a06b9c6651a1e1a5efe`  
		Last Modified: Tue, 12 Mar 2024 00:21:10 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326d0b8f2ee332b21507607001a3a2664713ed697dcc2c4ba3ff1b7f4f405845`  
		Last Modified: Tue, 12 Mar 2024 00:21:10 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
