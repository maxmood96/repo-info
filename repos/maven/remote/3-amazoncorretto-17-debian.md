## `maven:3-amazoncorretto-17-debian`

```console
$ docker pull maven@sha256:740789f481a00fc5160ba35afac7f77d84739f1e914f099dddfb407248bdb614
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-debian` - linux; amd64

```console
$ docker pull maven@sha256:b6050279d4201aef2def6950f35d67f1dfb906dbf5fe9f99af8f3d4cadac721e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240863926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047b0f7fc9ff9167c4689eb77359e7a3e93992c1c7b2ca88a794fecb3ff83033`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:21:26 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:21:26 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 20:21:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 08 May 2026 20:21:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 08 May 2026 20:21:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 20:21:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 20:21:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 08 May 2026 20:21:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 08 May 2026 20:21:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 08 May 2026 20:21:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 08 May 2026 20:21:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 08 May 2026 20:21:26 GMT
ARG USER_HOME_DIR=/root
# Fri, 08 May 2026 20:21:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 08 May 2026 20:21:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 08 May 2026 20:21:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4396a00b48726dd1d9e8b4aba0e80bedd2007bcd35706481ce9b5a063c3dae67`  
		Last Modified: Fri, 08 May 2026 20:21:50 GMT  
		Size: 201.8 MB (201770453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4844134ca4868fce5da57c371708c22162eaf20bd08ac4fb7317726812e6fd32`  
		Last Modified: Fri, 08 May 2026 20:21:46 GMT  
		Size: 9.3 MB (9312243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b000e53a514683245e901b3acb7735ef7eab2e84a2a13bbdfa40e86530f7731`  
		Last Modified: Fri, 08 May 2026 20:21:45 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41a0dc659c7363c4c05d44c764c877332e00e7af8c805972ea4669145fdafd0`  
		Last Modified: Fri, 08 May 2026 20:21:45 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian` - unknown; unknown

```console
$ docker pull maven@sha256:72c3e7e07d9bdea8975ca203cb98da4bdf61502ddcc15120c5567cbe03bbddd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43c2c748c3a062a5b11b7a2690d20d5eddfd1e74bd41e58fe9675403d90feac`

```dockerfile
```

-	Layers:
	-	`sha256:9807ec2cc03770320ed02e52b5b2de0a617e21b7cde3001bca3cf2717b896122`  
		Last Modified: Fri, 08 May 2026 20:21:45 GMT  
		Size: 3.1 MB (3104733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:490ee377ee7273f2f740959836c22b65b438eff34ab57fc95f926792e334e314`  
		Last Modified: Fri, 08 May 2026 20:21:45 GMT  
		Size: 17.7 KB (17679 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:a00b0edafdaf40e0094ce6551625cc6d77de001b115cb24e547ac8314cd833bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239762205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5536d1125f8721ee9e3c443ca396f4cbe40dd8a1c10274c268f280f988c02f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:25:28 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:25:28 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 20:25:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 08 May 2026 20:25:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 08 May 2026 20:25:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 20:25:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 20:25:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 08 May 2026 20:25:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 08 May 2026 20:25:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 08 May 2026 20:25:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 08 May 2026 20:25:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 08 May 2026 20:25:28 GMT
ARG USER_HOME_DIR=/root
# Fri, 08 May 2026 20:25:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 08 May 2026 20:25:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 08 May 2026 20:25:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bb3d561ba2e02df082cd2add96863984a8b2c71f335692d8c34a3f1932c6d2`  
		Last Modified: Fri, 08 May 2026 20:25:52 GMT  
		Size: 200.3 MB (200305308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78e6c381d54a3bd636d9bb8ff4482f3ab056d6732b71bdd8df981ad46de2398`  
		Last Modified: Fri, 08 May 2026 20:25:48 GMT  
		Size: 9.3 MB (9312250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251b57b01a86247e6acd7e05ee8f509a66161ac35720deb2bd5408220f219a76`  
		Last Modified: Fri, 08 May 2026 20:25:47 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37eb7f41ac3e7cb67e0c34c45a5d36a227aaf1ea2a4d48cc264408a4a0909433`  
		Last Modified: Fri, 08 May 2026 20:25:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian` - unknown; unknown

```console
$ docker pull maven@sha256:79acd75ebd6884d67bd0ae04c6c1a451f82d25f1fbc354b62fe9bed18b285fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9913fe81c41094682ec3221292330b41f321ce4be29ef7ad5d032742d7c86fa`

```dockerfile
```

-	Layers:
	-	`sha256:cf6d2547b8d35dcd474ea7b7e2eb65a2ec72104bbfc819f23630c5626823453b`  
		Last Modified: Fri, 08 May 2026 20:25:47 GMT  
		Size: 3.1 MB (3104396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92341ecf48d8ccb30a37ae5707ca81dd5509eeeae8d69b51ac3cb536631b3701`  
		Last Modified: Fri, 08 May 2026 20:25:47 GMT  
		Size: 17.8 KB (17848 bytes)  
		MIME: application/vnd.in-toto+json
