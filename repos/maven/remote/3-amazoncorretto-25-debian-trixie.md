## `maven:3-amazoncorretto-25-debian-trixie`

```console
$ docker pull maven@sha256:d36a7dac4e8bae1654eb4237db46c1fda579b348b095e3c98c8c37059f7ea4ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:549e114fb760bb50adadaf3568159ba60c5cbd12f4f71e774a4fddb3be283acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274684473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8015a0e5bcd131c98b376af0085c20545ae2a5587600c0a3aa3823843b7971aa`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:03:36 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:03:36 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:03:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 20 May 2026 00:03:36 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 20 May 2026 00:03:36 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 20 May 2026 00:03:36 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 20 May 2026 00:03:36 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 20 May 2026 00:03:36 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 20 May 2026 00:03:36 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 20 May 2026 00:03:36 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 20 May 2026 00:03:36 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 20 May 2026 00:03:36 GMT
ARG USER_HOME_DIR=/root
# Wed, 20 May 2026 00:03:36 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 20 May 2026 00:03:36 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 20 May 2026 00:03:36 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d079f0eafdf7b89bf9c0be7770c324e5a09fd7e85f24521fc18c30b44af3c08`  
		Last Modified: Wed, 20 May 2026 00:04:01 GMT  
		Size: 235.5 MB (235543570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2808c1a786ef0be5df3b23d0f07c647cd187cf5097dc0ef1fb83088705d7c99f`  
		Last Modified: Wed, 20 May 2026 00:03:56 GMT  
		Size: 9.4 MB (9359973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88dbd81fc7825dd5116f3911c5f11b8b6be0f4f51a5b3c5fd5fa2d3fa965dd2a`  
		Last Modified: Wed, 20 May 2026 00:03:56 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e504b869698b76761e4bbcfcb533e812288afc8de0dd8cb323f78aa2d5cf96c`  
		Last Modified: Wed, 20 May 2026 00:03:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:46daefd9d842c20b71ca35b29b5c433f41761f7f30005183a2706ec3b1f4ef0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5712dfacbb65a1c6b01532e93b9d61a1ce250f7f6a51ac8045564c4c48d3e1`

```dockerfile
```

-	Layers:
	-	`sha256:84446ae3b4e4d05424871d09b36040b63b3025ec0a09fb1be9b5e788dcbe0969`  
		Last Modified: Wed, 20 May 2026 00:03:56 GMT  
		Size: 3.1 MB (3113777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64734e79598b0f36074ae75410571917e9686b1d85eb954b214607544228d6cf`  
		Last Modified: Wed, 20 May 2026 00:03:56 GMT  
		Size: 17.5 KB (17525 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:7647d73ae3665c1a965c6e8814ff249fe3de9b33b8a695666c3ff88eaa1bf102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272790642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a946e0a8c13d8e9e782b467299122d55963c0b7fcaea5383beaa43a9cbe8ae4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:10:35 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:10:35 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:10:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 20 May 2026 00:10:35 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 20 May 2026 00:10:35 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 20 May 2026 00:10:35 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 20 May 2026 00:10:35 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 20 May 2026 00:10:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 20 May 2026 00:10:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 20 May 2026 00:10:35 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 20 May 2026 00:10:35 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 20 May 2026 00:10:35 GMT
ARG USER_HOME_DIR=/root
# Wed, 20 May 2026 00:10:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 20 May 2026 00:10:35 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 20 May 2026 00:10:35 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d00375edccb21a3d3a0be9b9f49cd4d354780de974d843d7277dc6a66b27ed9`  
		Last Modified: Wed, 20 May 2026 00:11:04 GMT  
		Size: 233.3 MB (233287744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13603bfc52dade984bf24fcbcc856f82be7e5bd6431886c3777888b77a87b2b2`  
		Last Modified: Wed, 20 May 2026 00:10:58 GMT  
		Size: 9.4 MB (9359974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e01da6154fd1df1060a5c76c5fd84967dbadb972af5af3755dc072a7c918be2`  
		Last Modified: Wed, 20 May 2026 00:10:57 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afa37bbaa57442c5013121a84f3e49fc6c856957b21d925565a21c06effd201`  
		Last Modified: Wed, 20 May 2026 00:10:58 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:65f765cb337971d4aa1c47cdd43136fa441b9f902cee5c05cb4b7bab78e2637e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b7a7994b8635c9aff47f2fc11f67dfbb0dcc621ede935935c5ac0e52cca493`

```dockerfile
```

-	Layers:
	-	`sha256:e0406917641c7f43b01bfdca2087fc1c519549c596547980123af55faa2a146d`  
		Last Modified: Wed, 20 May 2026 00:10:58 GMT  
		Size: 3.1 MB (3113429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2b62edde024f51b962cdfecb854281086709fc8afba7a4c77b4650272ed581a`  
		Last Modified: Wed, 20 May 2026 00:10:57 GMT  
		Size: 17.7 KB (17693 bytes)  
		MIME: application/vnd.in-toto+json
