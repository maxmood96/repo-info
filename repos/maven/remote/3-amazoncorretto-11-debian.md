## `maven:3-amazoncorretto-11-debian`

```console
$ docker pull maven@sha256:b25df8857194c3ccec89630f6d452b44f7440e62620d459363fd5e31dfabec60
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-debian` - linux; amd64

```console
$ docker pull maven@sha256:0855488d20828a88c682087497af9fb3a8f7b1649412c2cef419be3030525092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.6 MB (241610471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd08628764abcded45eb8c4a13ce6d10dfefb53400d33acf04e3eb2f100f502a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:34:34 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:34:35 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 04:34:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 04 Nov 2025 04:34:35 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 04 Nov 2025 04:34:35 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 04 Nov 2025 04:34:35 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 04 Nov 2025 04:34:35 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 04 Nov 2025 04:34:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 04 Nov 2025 04:34:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 04 Nov 2025 04:34:35 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 04 Nov 2025 04:34:35 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 04 Nov 2025 04:34:35 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 04 Nov 2025 04:34:35 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 04 Nov 2025 04:34:35 GMT
ARG USER_HOME_DIR=/root
# Tue, 04 Nov 2025 04:34:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 04 Nov 2025 04:34:35 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 04 Nov 2025 04:34:35 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2560e76fd86e64cb517d61ae3e1caaa817e01f4ac7fbe26b6f4e216b33dca2`  
		Last Modified: Tue, 04 Nov 2025 04:34:56 GMT  
		Size: 202.6 MB (202588738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd45eee552682cfae3e9cd51f49f742bccd86a800cf47e3b8181b8daeabc76db`  
		Last Modified: Tue, 04 Nov 2025 04:35:03 GMT  
		Size: 9.2 MB (9242591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8192e00814057cf607a54d143a0859f0089f8f6f80a1a3005a69517c0425c2`  
		Last Modified: Tue, 04 Nov 2025 04:35:02 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ac1c71cee5d287f65aa7c18a8976af94ede8c2275312eacce50ffe1a79a289`  
		Last Modified: Tue, 04 Nov 2025 04:35:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian` - unknown; unknown

```console
$ docker pull maven@sha256:34db9de0bb6d32dd7c0692474e3ee5f55edcd1bcf23ff845c8a4ab54ad8b703a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9c8968677e8d23e9aa6fae2c87d7ba5106446fa27353892619c39d80bfe384`

```dockerfile
```

-	Layers:
	-	`sha256:8d2f840b2e46894414cb78b2a504c1042d4ac4f8057c0d98a54e5b8376dd695f`  
		Last Modified: Tue, 04 Nov 2025 09:27:21 GMT  
		Size: 3.1 MB (3109759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79335769090b99b8c129e8d6bf9d8d331da22c948063e025072f060c0f82c8d1`  
		Last Modified: Tue, 04 Nov 2025 09:27:22 GMT  
		Size: 19.2 KB (19200 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c7cfa8cc03276f94d52fd2f88d7a5e23ca8ab94ea2c3a3b3fea1b20cc2207631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.2 MB (239177384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aacc5fa81907ad46ffb2b768daf5277eab72a8ff273288d888ff81fec863591`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 17 Sep 2025 20:58:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 17 Sep 2025 20:58:48 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 20:58:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 17 Sep 2025 20:58:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Sep 2025 20:58:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Sep 2025 20:58:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Sep 2025 20:58:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Sep 2025 20:58:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Sep 2025 20:58:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 17 Sep 2025 20:58:48 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Sep 2025 20:58:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Sep 2025 20:58:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Sep 2025 20:58:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5641bc1194a8f4b58d1249bb0088b5f6ed337e7ca2a373c57c71cb6b389127a`  
		Last Modified: Tue, 21 Oct 2025 09:52:21 GMT  
		Size: 199.8 MB (199791636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8d24ce27233a49e8fa6cca649fbb924df90e7dacd56dc9aa1c8aaeeaf176db`  
		Last Modified: Tue, 21 Oct 2025 02:30:30 GMT  
		Size: 9.2 MB (9242584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d034281b17df3bf40407ec5a7447410bd30d2261c65ec6418c03a6902d7712`  
		Last Modified: Tue, 21 Oct 2025 02:30:30 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f217fe6efd6987439147e4809bbe40ef38468cf15c6e54d8b7bc91ccdfdbe0`  
		Last Modified: Tue, 21 Oct 2025 02:30:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian` - unknown; unknown

```console
$ docker pull maven@sha256:06e91c8cbe67b10414c582b4a001a1de10431496d3fe52e384168bf0a7e7d256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3126915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eec60c1bec804feca665d59a2f1d55e7aaacf484b3059313e7986cd694f9cf3`

```dockerfile
```

-	Layers:
	-	`sha256:058a105d934b3addfec0ff600afa70b89ec81fae14e79aefc584f3c36aa4ece0`  
		Last Modified: Tue, 21 Oct 2025 08:27:29 GMT  
		Size: 3.1 MB (3107504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f29766c1254ea1b1e4a6d1f54ac825f8e17bfe3907cf401eca42573bc08d42`  
		Last Modified: Tue, 21 Oct 2025 08:27:30 GMT  
		Size: 19.4 KB (19411 bytes)  
		MIME: application/vnd.in-toto+json
