## `maven:3-amazoncorretto-8-debian-trixie`

```console
$ docker pull maven@sha256:99babb9cf6fbe08283dbc07b85a1fbe228226418cf837a58384f6c6e5822e765
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:95bf2c549d77fa9d153f5dee6e6401eab044cd0b4c0dba16a7a88590ccfcebb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164790750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a3bc1df6228db4bba464be737003421c84937c0bea58dcec6bec37b755d38f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:04:06 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:04:06 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:04:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Wed, 20 May 2026 00:04:06 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 20 May 2026 00:04:06 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 20 May 2026 00:04:06 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 20 May 2026 00:04:06 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 20 May 2026 00:04:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 20 May 2026 00:04:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 20 May 2026 00:04:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 20 May 2026 00:04:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 20 May 2026 00:04:06 GMT
ARG USER_HOME_DIR=/root
# Wed, 20 May 2026 00:04:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 20 May 2026 00:04:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 20 May 2026 00:04:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028cd505fc68163c6ab874f1adb1d4b61c3e549ca45efd46e4a53dfc8bbeb5ea`  
		Last Modified: Wed, 20 May 2026 00:04:24 GMT  
		Size: 125.6 MB (125649845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777c2c2b704a9585f6e5a3bcb82d5be0854474fb59559ebdfd4c2f4ea8970384`  
		Last Modified: Wed, 20 May 2026 00:04:21 GMT  
		Size: 9.4 MB (9359974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab31722a9e4de5382fdb99bc405bd8190dd9dba807ab693d4172c22b2cbfaf1`  
		Last Modified: Wed, 20 May 2026 00:04:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf69c83880df391608eec958542320dfe062d93c02183f0ff2734f66d1caa33`  
		Last Modified: Wed, 20 May 2026 00:04:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:9d46ce955d0a7cb64e8751197922214e58967d290fe626b969d52c7c766aec1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2999671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9610cfbbe972536de8dae2f9dbb344b076f5285db0e84634cc895d6ee50ada`

```dockerfile
```

-	Layers:
	-	`sha256:8443c5f540fb27513917aa6fd32c2d8102a2a4c12c15bd0febf4ba383f437cb1`  
		Last Modified: Wed, 20 May 2026 00:04:21 GMT  
		Size: 3.0 MB (2982138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d04f5b17f4d89fea672e43a8d078f17cbf0f19701afbf041dd6af5b8c57427`  
		Last Modified: Wed, 20 May 2026 00:04:21 GMT  
		Size: 17.5 KB (17533 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b57feb45df96c61f5fcf28113a82938d1e97f1ac1212726fe2ec5d74c2bc5176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148871669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9d808c5fb7464a114ac173f873024468a530eb836eb72b3557b905df51fe97`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:10:41 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:10:41 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:10:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Wed, 20 May 2026 00:10:41 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 20 May 2026 00:10:41 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 20 May 2026 00:10:41 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 20 May 2026 00:10:41 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 20 May 2026 00:10:41 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 20 May 2026 00:10:41 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 20 May 2026 00:10:41 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 20 May 2026 00:10:41 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 20 May 2026 00:10:41 GMT
ARG USER_HOME_DIR=/root
# Wed, 20 May 2026 00:10:41 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 20 May 2026 00:10:41 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 20 May 2026 00:10:41 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c3c95b16bd01bfb13f35de960df138613d3d8e4d301989d594d8f5d038e447`  
		Last Modified: Wed, 20 May 2026 00:11:01 GMT  
		Size: 109.4 MB (109368772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f57ec7d3e2c3e1facb376967258d328053aad37a8e2291fca7eacdaa98ca72`  
		Last Modified: Wed, 20 May 2026 00:10:57 GMT  
		Size: 9.4 MB (9359974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4787aad4fc120a8ca2d149db35dd9da95da676519e57de7203e90681ce44840e`  
		Last Modified: Wed, 20 May 2026 00:10:57 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c8ce12a0df5d57c0dd8351c899a673a683a7462a420a62044364450123b53f`  
		Last Modified: Wed, 20 May 2026 00:10:57 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:4f568203a8bdad32953c2b823e39c8ad05de1d4661a13afd76bf63e1712d2914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01840b70f148703bb8c2fd1706394f481d237a8b7dbd4448329eca7394191676`

```dockerfile
```

-	Layers:
	-	`sha256:48b1a782611180a8a5c4433446599a1f4ad78fc8f51c38e7ea84497a89a73d04`  
		Last Modified: Wed, 20 May 2026 00:10:57 GMT  
		Size: 3.0 MB (2964951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1ebeec175ebc13bb467b32ffee5a67f656189d1c6368e40b6d71d18e6a44c9f`  
		Last Modified: Wed, 20 May 2026 00:10:57 GMT  
		Size: 17.7 KB (17702 bytes)  
		MIME: application/vnd.in-toto+json
