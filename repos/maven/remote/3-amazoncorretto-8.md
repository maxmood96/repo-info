## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:c726d7934765820d1d396ba24496bedb08b3eab7b4fa162b2b7cfe3e806e6ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:80bf81cda53bf576fd6acfd3959b5565ec0c1170cda6b7a53dfca4d8f7a3c15d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150430435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee986e2cc936b1f32c0a835a553fe567d8dff0661fcadb51ef9e0b68bf03b938`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 23 Dec 2020 20:20:09 GMT
ADD file:15991ffbefc01e13f134972ce0eabc6b7901ea9ab4d56347bee5057302cf4848 in / 
# Wed, 23 Dec 2020 20:20:09 GMT
CMD ["/bin/bash"]
# Wed, 23 Dec 2020 20:45:11 GMT
ARG version=1.8.0_275.b01-1
# Wed, 23 Dec 2020 20:45:27 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 23 Dec 2020 20:45:28 GMT
ENV LANG=C.UTF-8
# Wed, 23 Dec 2020 20:45:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 23 Dec 2020 21:06:21 GMT
ARG MAVEN_VERSION=3.6.3
# Wed, 23 Dec 2020 21:06:21 GMT
ARG USER_HOME_DIR=/root
# Wed, 23 Dec 2020 21:06:22 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Wed, 23 Dec 2020 21:06:22 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Wed, 23 Dec 2020 21:06:29 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Wed, 23 Dec 2020 21:06:32 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 23 Dec 2020 21:06:33 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 23 Dec 2020 21:06:33 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 23 Dec 2020 21:06:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 23 Dec 2020 21:06:33 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 23 Dec 2020 21:06:33 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 23 Dec 2020 21:06:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 23 Dec 2020 21:06:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4232b9ee675bb1f9a32337ec3f266a570b75c54c3c3f173b1abb998e9984ad8c`  
		Last Modified: Wed, 23 Dec 2020 20:21:42 GMT  
		Size: 62.0 MB (62007428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ea7e15410319a2389a5b932219d5ab0141e3f7b94e0673066287ea2891d852`  
		Last Modified: Wed, 23 Dec 2020 20:47:16 GMT  
		Size: 75.3 MB (75272583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d9d7bb18126c161876e1f5e528de55ab20779a23f07f01ebb94ea3dd6ffdc3`  
		Last Modified: Wed, 23 Dec 2020 21:08:55 GMT  
		Size: 3.6 MB (3568008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1e905c30b73cf0c6e20a272d3007a3c07317930b3e7b898cc75d2e1055263c`  
		Last Modified: Wed, 23 Dec 2020 21:08:55 GMT  
		Size: 9.6 MB (9581208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754acd210d2421507971b723a1bccd171e145c73e4b5ee6caf36353ac94a31dc`  
		Last Modified: Wed, 23 Dec 2020 21:08:54 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c003d2a3c29129a9f19eb9f9cd19065f5667755a4e6190bb5510bc13442a31`  
		Last Modified: Wed, 23 Dec 2020 21:08:54 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:a0ee6ad30ad04e05fe7e8cf4c96fa2830a5d010ed92f0897e978cd946183078c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136204629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd5c1bd8998f4d2ae8f964be62b0f87162a48f26bcc2be0f8264d5c4faefaa8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 23 Dec 2020 19:39:59 GMT
ADD file:d991483ad4376be5e4327b3789511ab9266db8b87fc4b5327f0cabd1016ba00a in / 
# Wed, 23 Dec 2020 19:40:02 GMT
CMD ["/bin/bash"]
# Wed, 23 Dec 2020 20:46:01 GMT
ARG version=1.8.0_275.b01-1
# Wed, 23 Dec 2020 20:46:27 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 23 Dec 2020 20:46:28 GMT
ENV LANG=C.UTF-8
# Wed, 23 Dec 2020 20:46:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 23 Dec 2020 21:24:01 GMT
ARG MAVEN_VERSION=3.6.3
# Wed, 23 Dec 2020 21:24:02 GMT
ARG USER_HOME_DIR=/root
# Wed, 23 Dec 2020 21:24:03 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Wed, 23 Dec 2020 21:24:03 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Wed, 23 Dec 2020 21:24:14 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Wed, 23 Dec 2020 21:24:18 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 23 Dec 2020 21:24:18 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 23 Dec 2020 21:24:19 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 23 Dec 2020 21:24:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 23 Dec 2020 21:24:20 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 23 Dec 2020 21:24:21 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 23 Dec 2020 21:24:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 23 Dec 2020 21:24:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3307d2ab2034125075f0b058dcc32d6bf3e2c0595f1306de08d9e4a0287ddd76`  
		Last Modified: Wed, 23 Dec 2020 19:40:59 GMT  
		Size: 63.7 MB (63707914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97ee9a6cb0a50e12d673c7a5c748cf068a65df722197a6d97afb1cafac34201`  
		Last Modified: Wed, 23 Dec 2020 20:48:34 GMT  
		Size: 59.3 MB (59343572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6553a33373399e2025c8cb535e2a5f29998d7a5e48c1d2dcc42cbcc1bbc2d96`  
		Last Modified: Wed, 23 Dec 2020 21:26:22 GMT  
		Size: 3.6 MB (3570716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875f9503d00edfdc4afef8c402d845d98fb02284ea9712b5f997841d4bc4c166`  
		Last Modified: Wed, 23 Dec 2020 21:26:23 GMT  
		Size: 9.6 MB (9581212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cc8c40d9a933d4d3bd3cfa3ae3b96ba7ad3cf930a1571328dec6b9a7d68cfa`  
		Last Modified: Wed, 23 Dec 2020 21:26:21 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1089957d329bc4cd9a2e6ff6f69c20707c6a03e113937255c8c749663b22cfab`  
		Last Modified: Wed, 23 Dec 2020 21:26:22 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
