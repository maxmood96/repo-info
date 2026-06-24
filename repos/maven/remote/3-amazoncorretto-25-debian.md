## `maven:3-amazoncorretto-25-debian`

```console
$ docker pull maven@sha256:e23deeb3084eb9f4ef1658c3aeffaa703e1948ce1d2724a968d12ece02f58944
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-debian` - linux; amd64

```console
$ docker pull maven@sha256:749ed18493ed59db5a3f9f1b3a7e1a9519b525e4401b5d2afd19fb97f69df540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274689931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90ba55143cddc1678edbd9bdf81f5a69d3b0e96699276e02f8cb4e75807bbf7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:24:44 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:24:44 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 02:24:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 24 Jun 2026 02:24:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 24 Jun 2026 02:24:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 24 Jun 2026 02:24:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 24 Jun 2026 02:24:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 24 Jun 2026 02:24:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 24 Jun 2026 02:24:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 24 Jun 2026 02:24:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 24 Jun 2026 02:24:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 24 Jun 2026 02:24:44 GMT
ARG USER_HOME_DIR=/root
# Wed, 24 Jun 2026 02:24:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 24 Jun 2026 02:24:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 24 Jun 2026 02:24:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd7e40764845760feb25e6a4c43a37ffa5afd9daea21a398f00f3a9a3063417`  
		Last Modified: Wed, 24 Jun 2026 02:25:11 GMT  
		Size: 235.5 MB (235543539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416657303add6b928a4f515c0e75da0646ed91754e6d5b7a51c73b99d0cdc0ad`  
		Last Modified: Wed, 24 Jun 2026 02:25:06 GMT  
		Size: 9.4 MB (9359967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e175ac041e0d9dff1806a842bb6017922ccc72d68968f177eb6032b001e991bc`  
		Last Modified: Wed, 24 Jun 2026 02:25:06 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d584c487547f9f56d7bd654e3a5a6bd2303304717e7a3820a36e91db17b2332`  
		Last Modified: Wed, 24 Jun 2026 02:25:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian` - unknown; unknown

```console
$ docker pull maven@sha256:68638ad7bf024f51620d89f2b8f4c72f755d8d9faf879841d61e53fc959cb995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fefa0ae87d83f8580501665ff6a4a1217eb344dcb18b49d5a19aa145c4da2960`

```dockerfile
```

-	Layers:
	-	`sha256:473f90cba61af398391866d900ef38ee6923282dd422e6e28678803438e2fd28`  
		Last Modified: Wed, 24 Jun 2026 02:25:06 GMT  
		Size: 3.1 MB (3113885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a10be1bafecc5caca6e80510b8e451a83deb535aded17564b42ef168c439a06`  
		Last Modified: Wed, 24 Jun 2026 02:25:06 GMT  
		Size: 17.5 KB (17525 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:1f5200db77055a0bf16c9c90c7b033b482fed1d3848c2c1bc3abc3bae385c2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272797230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bf13cb0069799ba45b4893d49ca0e14e776c9b340f25e0f9823cb512ce917e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:31:14 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:31:15 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 02:31:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 24 Jun 2026 02:31:15 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 24 Jun 2026 02:31:15 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 24 Jun 2026 02:31:15 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 24 Jun 2026 02:31:15 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 24 Jun 2026 02:31:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 24 Jun 2026 02:31:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 24 Jun 2026 02:31:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 24 Jun 2026 02:31:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 24 Jun 2026 02:31:15 GMT
ARG USER_HOME_DIR=/root
# Wed, 24 Jun 2026 02:31:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 24 Jun 2026 02:31:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 24 Jun 2026 02:31:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543bf288676ee54240ae620da757557faa6b81741e098583acb8c9b5ff35bc3c`  
		Last Modified: Wed, 24 Jun 2026 02:31:43 GMT  
		Size: 233.3 MB (233287705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5620f446622dc0a566a1686baac58d393da9150d88eff4d135872415016ee559`  
		Last Modified: Wed, 24 Jun 2026 02:31:38 GMT  
		Size: 9.4 MB (9359970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83163466b6cf6d4e92347d1a03c9072198107eb41a2c4ea9ac3bcf9deb7f36f`  
		Last Modified: Wed, 24 Jun 2026 02:31:37 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85275ad98bfd635697c3283b762b42b0324d46ba3e86dafc1a0b5109badb7142`  
		Last Modified: Wed, 24 Jun 2026 02:31:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian` - unknown; unknown

```console
$ docker pull maven@sha256:fa6e60e1e70f5e8091b217c3330e5c81e24fcfbb4c58f0ae9f6cd7f96db17413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70c685d288ff4c102a34bb3841216f443228512b0186def0bddc0aefa576285`

```dockerfile
```

-	Layers:
	-	`sha256:86f50e3e893957cd15918d2547816eb2bd3114887cb9c0d44af93dae7c47e3b1`  
		Last Modified: Wed, 24 Jun 2026 02:31:38 GMT  
		Size: 3.1 MB (3113537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4754171a7198f9cde1515846cb1f96d4f3b63302709f363b52c59a0813b0be4`  
		Last Modified: Wed, 24 Jun 2026 02:31:37 GMT  
		Size: 17.7 KB (17694 bytes)  
		MIME: application/vnd.in-toto+json
