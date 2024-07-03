## `maven:3-amazoncorretto-21-debian`

```console
$ docker pull maven@sha256:c0279a044a5bc488b02fe8bf441a437876b46fc0f96c590246bb36d9f17469c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-debian` - linux; amd64

```console
$ docker pull maven@sha256:51959dccc0a68c17f4dac7f384dd47a893dd0ab61b31e128531f1624a4f09ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251932445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:860781ab4565ab6af0e702d88d1b3c78b778e45f8f90437251f5f0ebc7059c29`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284c3988db6d41315286e3d8578e0f2df8f5d0540934100f4fdfc4439bcd92ef`  
		Last Modified: Tue, 02 Jul 2024 09:15:32 GMT  
		Size: 213.6 MB (213643321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b15f58a28b9be9f59712f5f0f43261793431a7619c22a07fd8967f838bf07ab`  
		Last Modified: Tue, 02 Jul 2024 09:15:29 GMT  
		Size: 9.2 MB (9161812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db383ca2f5d171867ed72f9255fdb63dd0471ac1ea460301e719e27006edbd9`  
		Last Modified: Tue, 02 Jul 2024 09:15:29 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6220cccc725af33e0803cf0111cad7abc6886f8204cb76995339b858230fe5`  
		Last Modified: Tue, 02 Jul 2024 09:15:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian` - unknown; unknown

```console
$ docker pull maven@sha256:dd3f5fb4a4ea16188928bf84593ffbb57302b8d0e6ce3b7d97daab2d0bce27d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2708847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3402453f7a578f9bbad64f9bbab081227cc54664429b69dfcd80cacece1dc31f`

```dockerfile
```

-	Layers:
	-	`sha256:713f7399da65298d85be86ccc505d1382e852a835b9cfd740e1e50ce764285a8`  
		Last Modified: Tue, 02 Jul 2024 09:15:29 GMT  
		Size: 2.7 MB (2690433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6242b81a2eb4602bc51bfae70f36a6d6f59c95a58f39477e622621a8ba1dc9f8`  
		Last Modified: Tue, 02 Jul 2024 09:15:29 GMT  
		Size: 18.4 KB (18414 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:422fd79168ef7effb8ef54f119d3d1581c6cec8d76f4fa7b9c18b36f9a4910bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 MB (249724375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1dbc643306f214c9eb609e569d3ebcbf7a3bf667084f86659d0137efc357767`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70a328d11e8e2037b27688bfa63254432eee933141809966a5ca4298161506b`  
		Last Modified: Wed, 03 Jul 2024 10:38:41 GMT  
		Size: 211.4 MB (211404997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b729f4da30305fa4b65d1771210eacf1f9febac65857f08687017da3b3b55b`  
		Last Modified: Wed, 03 Jul 2024 10:38:36 GMT  
		Size: 9.2 MB (9161778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6592b73c3e924c336ab8d8757c7be5d1a58fb255aa41dae27f42c70084cce150`  
		Last Modified: Wed, 03 Jul 2024 10:38:36 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3a5af7b6b7f1b1bb51f9cb7e91d5b5cd5eb68e0650ca975a78c58a9372dafb`  
		Last Modified: Wed, 03 Jul 2024 10:38:36 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian` - unknown; unknown

```console
$ docker pull maven@sha256:b411ff3ee34c059affcb29ea554d06f653cc4c63b2b13bc1ca0bba41ba6fd2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2709174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a4b47522d243eefe8a69e704ff684fdecf64007aae79ea0365050a03bde1b9`

```dockerfile
```

-	Layers:
	-	`sha256:d0fa515ff35301641185566e3568e592a4a7e0dda543c66a94cac911558888e1`  
		Last Modified: Wed, 03 Jul 2024 10:38:36 GMT  
		Size: 2.7 MB (2690075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38adc9dcd8bc5b0bcf46cc3fc87cf4c9714613ed82378708491f6404f246128d`  
		Last Modified: Wed, 03 Jul 2024 10:38:35 GMT  
		Size: 19.1 KB (19099 bytes)  
		MIME: application/vnd.in-toto+json
