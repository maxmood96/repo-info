## `maven:3-amazoncorretto-21-debian-trixie`

```console
$ docker pull maven@sha256:3118f8073f16312e81b713dfbfe16bbc66b624f7ccdeebaa7b71e6c7ec77b94c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:01f9f2ddd872f00242bb3e7ee2b071724c11aec4932160d8bc610a8efef01f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.0 MB (256020367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7ebd30db07e4103fda3c3ccc32f6c8bbf4f472f36f973c92351003fc580d1c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:03:27 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:03:28 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:03:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 20 May 2026 00:03:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 20 May 2026 00:03:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 20 May 2026 00:03:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 20 May 2026 00:03:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 20 May 2026 00:03:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 20 May 2026 00:03:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 20 May 2026 00:03:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 20 May 2026 00:03:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 20 May 2026 00:03:28 GMT
ARG USER_HOME_DIR=/root
# Wed, 20 May 2026 00:03:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 20 May 2026 00:03:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 20 May 2026 00:03:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eba16bbbe89338b5aea6019a9167bae0017365a67d5459fbcfa99299b2da427`  
		Last Modified: Wed, 20 May 2026 00:03:53 GMT  
		Size: 216.9 MB (216879463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9bc6879513f4dab3256f892421b4416f4a036b8d7f8de842dbe707cfc152243`  
		Last Modified: Wed, 20 May 2026 00:03:48 GMT  
		Size: 9.4 MB (9359974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaaaa5869cb37504e589d8fac080da7fde8ade891a4125e47b79844afd98f2b`  
		Last Modified: Wed, 20 May 2026 00:03:48 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43c4f98e34c14efa4aced775c7ee1d05ffe72e68af03e18f7fdf4f7d2e74f78`  
		Last Modified: Wed, 20 May 2026 00:03:48 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:c0518933961bea8569ce7f4e967e72f18110c7ef6ea1a27de348edea800315f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77963843dc894b61ba267d0c51cc68d99866ddf4fb1424e33f3cded1a531dbda`

```dockerfile
```

-	Layers:
	-	`sha256:cc77492bf9f886ff8a84777b1f477e274b0edf5fdff2175235064456e76b1d99`  
		Last Modified: Wed, 20 May 2026 00:03:48 GMT  
		Size: 3.1 MB (3104681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ed4f07487d8543b1bfd0b6f394c9ea747f4c08e20530d621fa64bbcfd5870ec`  
		Last Modified: Wed, 20 May 2026 00:03:48 GMT  
		Size: 17.5 KB (17525 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:e3b6b10402dcd16ff748bedce959822e9925883438c0ea001cdda3962007dd15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 MB (254432634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd3020f4191bd050d0589bd9c03ee5bf8dff5537633366fd815aba2aa0ac50b6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:10:20 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:10:20 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:10:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 20 May 2026 00:10:20 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 20 May 2026 00:10:20 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 20 May 2026 00:10:20 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 20 May 2026 00:10:20 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 20 May 2026 00:10:20 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 20 May 2026 00:10:20 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 20 May 2026 00:10:20 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 20 May 2026 00:10:20 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 20 May 2026 00:10:20 GMT
ARG USER_HOME_DIR=/root
# Wed, 20 May 2026 00:10:20 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 20 May 2026 00:10:20 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 20 May 2026 00:10:20 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c91655458189052e0324311509113c9b8f9ada76f64a2781ba33377814f70b`  
		Last Modified: Wed, 20 May 2026 00:10:46 GMT  
		Size: 214.9 MB (214929736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88654f8862cbe54e6c912638d6a5f96fa7fbb1e979d245e38b0e06ae36b946d`  
		Last Modified: Wed, 20 May 2026 00:10:41 GMT  
		Size: 9.4 MB (9359974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b4bdee2253699cc35d9b43c156403c9765cd674a2676e30088930df86df964`  
		Last Modified: Wed, 20 May 2026 00:10:40 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf33aefbf64c4ceee4ca542dc176ea408ae74fbe518dde4dba2aaa9527b99bd`  
		Last Modified: Wed, 20 May 2026 00:10:40 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:8cc9c2ba5375aeeedd2d3cf53dfecb447058763f28cd60b2cfa8758e517c4d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b3f50b68b38b9b28f3d737a38841936c0ea9b818cfec433f550af2c5921bfb`

```dockerfile
```

-	Layers:
	-	`sha256:9709e6e07e9f76933be35bb929429705e1f4a86963ba334a623f7af10fe3e923`  
		Last Modified: Wed, 20 May 2026 00:10:40 GMT  
		Size: 3.1 MB (3104336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a3ad53a97a6f70832795fa2df723e723506c716d97bcfc2be3a1aba00556a40`  
		Last Modified: Wed, 20 May 2026 00:10:40 GMT  
		Size: 17.7 KB (17694 bytes)  
		MIME: application/vnd.in-toto+json
