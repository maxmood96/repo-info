## `maven:3-amazoncorretto-23-debian-bookworm`

```console
$ docker pull maven@sha256:dda99d1b7b96b105d50bc958a5e7ed460c239ea75e58dc79d5782ed1cffb0a05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-23-debian-bookworm` - linux; amd64

```console
$ docker pull maven@sha256:db9909e9731b825e8a07e23aa16baa4f86ed4355c3e31e911f24ab20f53629d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.9 MB (261852865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f844c5decec488582fe1cf6596b9d3903ea947c90460bdc316bef304618766f8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 25 Jan 2025 20:08:38 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Sat, 25 Jan 2025 20:08:38 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-23-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 25 Jan 2025 20:08:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ARG MAVEN_VERSION=3.9.9
# Sat, 25 Jan 2025 20:08:38 GMT
ARG USER_HOME_DIR=/root
# Sat, 25 Jan 2025 20:08:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 25 Jan 2025 20:08:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 25 Jan 2025 20:08:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b26c08944acce114c4328638c125dd36c3b94da417ee514f3357621c0de15ca`  
		Last Modified: Tue, 04 Feb 2025 06:15:58 GMT  
		Size: 224.5 MB (224469091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3682f582de35d4b22628bb24f16c8313aae3244776a93f49b4a489a66c5c63e9`  
		Last Modified: Tue, 04 Feb 2025 06:15:50 GMT  
		Size: 9.2 MB (9170436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c4365734b02a42c2ec66be6fd11d85de1293e87b50b02e56d6236a1e134b2b`  
		Last Modified: Tue, 04 Feb 2025 06:15:50 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb9d703a739784dcdf92d33ed343b450beed62671ac4a7753daf8bd7ed3835b`  
		Last Modified: Tue, 04 Feb 2025 06:15:50 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:b8fbeb033e2472721dc95c09d66194aba3a4b51ce0d2cb39fb9e27f580cca932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3016220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cea8ea52859ba85bc2e8584f865156a00f9e3b717c48bb1c96daf9aa131934a`

```dockerfile
```

-	Layers:
	-	`sha256:1653fe7429b1ff127ed8b910ef4cb76b51572e04c453f9eec900f81c72c8b37f`  
		Last Modified: Tue, 04 Feb 2025 06:15:50 GMT  
		Size: 3.0 MB (2997007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed781b8973834214054170ffbad9824d7e0cadb4ec8f00701607445263987eb8`  
		Last Modified: Tue, 04 Feb 2025 06:15:50 GMT  
		Size: 19.2 KB (19213 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-23-debian-bookworm` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f8972dc1f6b58b5b7fcf91dc28f254209812fc82a3010fe73716295bac084010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.3 MB (259272429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c129a067ec41ba86eaf688a1926cf7b6b632ccc8c113206febdfa3f020c153b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Sat, 25 Jan 2025 20:08:38 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-23-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 25 Jan 2025 20:08:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ARG MAVEN_VERSION=3.9.9
# Sat, 25 Jan 2025 20:08:38 GMT
ARG USER_HOME_DIR=/root
# Sat, 25 Jan 2025 20:08:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 25 Jan 2025 20:08:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 25 Jan 2025 20:08:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c6708f38c93109f8aceadce7e6400438122ab9f6be9fdf8541399db0270620`  
		Last Modified: Mon, 27 Jan 2025 20:23:12 GMT  
		Size: 222.1 MB (222059927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f496a544e7a88e0f40dcaf7f1bf71df0736a8117914828ad6ef985d3194a3cf`  
		Last Modified: Mon, 27 Jan 2025 20:23:07 GMT  
		Size: 9.2 MB (9170434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8694903d8a2ee7687a4b58797814bd8d5dccdfef3e642793ee83ad15e18189`  
		Last Modified: Mon, 27 Jan 2025 20:23:07 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4445c37d1a5e9a9259e9675b858bfb144f38e440a51c97e8be4b223fa60d5a44`  
		Last Modified: Mon, 27 Jan 2025 20:23:07 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:6469a559773a4824f4fbfe0f1d2b05614fb9e3b40fd1d2faee4124a91ec96c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28725f51212c02a2ae8c72adb25de4fe54eb7266026728ae86ff7e3ddb26e9cf`

```dockerfile
```

-	Layers:
	-	`sha256:94f48343747971debf42a8a1bfad48547a4cf56ae058b82a18c6440e79758b7a`  
		Last Modified: Fri, 31 Jan 2025 06:43:26 GMT  
		Size: 3.0 MB (2996027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbe0802ad3fd69d9665ef1c2c36ed831d720696eefcc640b46a01cfd097a388f`  
		Last Modified: Fri, 31 Jan 2025 06:43:26 GMT  
		Size: 19.4 KB (19382 bytes)  
		MIME: application/vnd.in-toto+json
