## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:dcbf542019fee2c27f3dd0ffb8652e359e631f824614ef0bb56fe9b0927d99c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:22e5b463166ca7b7be86e7e3dfcf6ec943028764e18cc714dbf1601e03291a6d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (219988193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d87cbed2ea957b1fe82f12ff9b1015696492365432ff757979561e6b03115e0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 31 Jul 2020 22:19:45 GMT
ADD file:92220f428664788288d5cda805c94b48f6a5e957d4c7724085f3278d0a864f6d in / 
# Fri, 31 Jul 2020 22:19:46 GMT
CMD ["/bin/bash"]
# Fri, 31 Jul 2020 22:43:23 GMT
ARG version=11.0.8.10-1
# Fri, 31 Jul 2020 22:43:47 GMT
# ARGS: version=11.0.8.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 31 Jul 2020 22:43:48 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jul 2020 22:43:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 31 Jul 2020 22:46:48 GMT
ARG MAVEN_VERSION=3.6.3
# Fri, 31 Jul 2020 22:46:48 GMT
ARG USER_HOME_DIR=/root
# Fri, 31 Jul 2020 22:46:48 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Fri, 31 Jul 2020 22:46:48 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Fri, 31 Jul 2020 22:46:59 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Fri, 31 Jul 2020 22:47:01 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 31 Jul 2020 22:47:01 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 31 Jul 2020 22:47:01 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 31 Jul 2020 22:47:01 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 31 Jul 2020 22:47:01 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 31 Jul 2020 22:47:02 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 31 Jul 2020 22:47:02 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:37373184fe69e0fc20370c26317bf4c5b9b843c60b375563d4ee1c7766a89782`  
		Last Modified: Fri, 31 Jul 2020 22:20:37 GMT  
		Size: 61.7 MB (61716540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8bf440f7cb963ac775c46ed051bc640e2bff5a973c8f315f7f57b8319f2d261`  
		Last Modified: Fri, 31 Jul 2020 22:44:29 GMT  
		Size: 145.2 MB (145151522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0530a5b7cb3d0dae19a35a30706610e7f9421eb115eae378aaaea6b0ba677d`  
		Last Modified: Fri, 31 Jul 2020 22:48:03 GMT  
		Size: 3.5 MB (3537702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f45831f8b32ad7e5d2e44f009adf9f96c8d608064dd5fd0b9e403919489d3f0`  
		Last Modified: Fri, 31 Jul 2020 22:48:04 GMT  
		Size: 9.6 MB (9581217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44d20cfdadf2a9505e6926bdd646ead814595f80d4e6ebac69fcff5476e5598`  
		Last Modified: Fri, 31 Jul 2020 22:48:03 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04582ecfefd051da201381bf7fe4853fefa8c6378e554ba954172ca394b2e84f`  
		Last Modified: Fri, 31 Jul 2020 22:48:03 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:581674381dac39da1f32c5a2c90a11a6b1c069047133a4c2fd9086c53965d3cd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 MB (220347581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0687dfe09614fbd9f3f6f68abb0172d4cdceaa0106da1e9e605d169becb298`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 30 Jun 2020 21:59:07 GMT
ADD file:c597ed16b945b44bdc9a607ac9730b470dd169fb94a5ca4e000d07318157d4f8 in / 
# Tue, 30 Jun 2020 21:59:09 GMT
CMD ["/bin/bash"]
# Wed, 15 Jul 2020 22:40:45 GMT
ARG version=11.0.8.10-1
# Wed, 15 Jul 2020 22:41:16 GMT
# ARGS: version=11.0.8.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 15 Jul 2020 22:41:17 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jul 2020 22:41:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 15 Jul 2020 23:53:58 GMT
ARG MAVEN_VERSION=3.6.3
# Wed, 15 Jul 2020 23:53:58 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Jul 2020 23:53:59 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Wed, 15 Jul 2020 23:54:00 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Tue, 28 Jul 2020 21:40:52 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Tue, 28 Jul 2020 21:40:56 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 28 Jul 2020 21:40:56 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 28 Jul 2020 21:40:57 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 28 Jul 2020 21:40:58 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 28 Jul 2020 21:40:58 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 28 Jul 2020 21:40:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 28 Jul 2020 21:40:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6c0fd36c9881cb99dbcd7fe98cfd04a4a653e35c4c1195b7cb7d339eaec9dd79`  
		Last Modified: Tue, 30 Jun 2020 22:00:22 GMT  
		Size: 63.2 MB (63163782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d329972c97e180a09a54e02486d5abb2b8b9e7b3218dcbc1431b24d8e61e1152`  
		Last Modified: Wed, 15 Jul 2020 22:42:32 GMT  
		Size: 144.0 MB (144017548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7985211b5dbdf2c8aea4d9a4e883ddc1906b9b086b5f8dde0c69acf673f58966`  
		Last Modified: Tue, 28 Jul 2020 21:41:55 GMT  
		Size: 3.6 MB (3583838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6529fabd8aff886180468a9de6f7b5fd00822165f60b97b5d4e04ee1eca95605`  
		Last Modified: Tue, 28 Jul 2020 21:41:55 GMT  
		Size: 9.6 MB (9581202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9baa09a64b2e03cf0d621fdad1b2228780e1f5a37232bce5fb5b084dc90c26f`  
		Last Modified: Tue, 28 Jul 2020 21:41:54 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6550c0960d5d602ab51eace24bb0f731adaff713066476859d119d4e112a60a`  
		Last Modified: Tue, 28 Jul 2020 21:41:54 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
