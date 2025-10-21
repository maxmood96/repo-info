## `maven:3-amazoncorretto-11-debian-trixie`

```console
$ docker pull maven@sha256:a5c0a9664247045c70b44b9b9cffea9c610a8572dde29ad97b0b212ae3437e8f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:035975a10bd0c485a50d8cd35a85cc14378872fa07d1e9a38cbaefadff6f6c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241867339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2cbc0d4553d7edd01b19c1aba27abe26d82c8979a68d9917deac63d6b91718`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 17 Sep 2025 20:58:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
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
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141d1d9d12943d0dddb3097377390efb33d7bef05488e870c4e43bd4701d278f`  
		Last Modified: Tue, 21 Oct 2025 11:45:53 GMT  
		Size: 202.8 MB (202845787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c155af61a19716927155a050d8910570ee331412607f61e8c25cf667f681c3f0`  
		Last Modified: Tue, 21 Oct 2025 02:24:59 GMT  
		Size: 9.2 MB (9242593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93631322585533cbd9e00bc7c6e170d4ef889463461ee3b73aefc1b643ff04f`  
		Last Modified: Tue, 21 Oct 2025 02:24:59 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a6af5c1213ba698cbfd31809bc9c48af2ac884704a0b5ab0b838c024d065a7`  
		Last Modified: Tue, 21 Oct 2025 02:24:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:851ee14c48f9fe06b2e30d5b763795593c23b42bef3cc790767689fd2f5f0672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3126447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ccabc53e94ab99fdf72e5b1dfdd1743f0a043d70c95d2efa05468e51c32d77b`

```dockerfile
```

-	Layers:
	-	`sha256:8866690a62e33ede265f583563cbf117678a1e4c1cca145ea3946184652ef6fc`  
		Last Modified: Tue, 21 Oct 2025 11:27:20 GMT  
		Size: 3.1 MB (3107204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3486f7a3dc0f7ac008ccc8ca63625fe6c34f2e380dbe3f13023c3f5b80065135`  
		Last Modified: Tue, 21 Oct 2025 11:27:21 GMT  
		Size: 19.2 KB (19243 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-debian-trixie` - linux; arm64 variant v8

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

### `maven:3-amazoncorretto-11-debian-trixie` - unknown; unknown

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
