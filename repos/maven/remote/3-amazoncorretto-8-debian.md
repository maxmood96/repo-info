## `maven:3-amazoncorretto-8-debian`

```console
$ docker pull maven@sha256:7a7a21c5f99fb4983c6890e5f8ecdf089f5f7f9cf09f8b3faf9d2d39f6bf1425
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-debian` - linux; amd64

```console
$ docker pull maven@sha256:2e970978f09ed7bc3bd543fb47346abc8d38de582d044fa113f54513062115d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164612509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1abfcc02012c17604af0d5a37ea73dbff023afc7e80770e0a45a5c725f71c771`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:35:23 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:35:23 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 04:35:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Tue, 04 Nov 2025 04:35:23 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 04 Nov 2025 04:35:23 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 04 Nov 2025 04:35:23 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 04 Nov 2025 04:35:23 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 04 Nov 2025 04:35:23 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 04 Nov 2025 04:35:23 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 04 Nov 2025 04:35:23 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 04 Nov 2025 04:35:23 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 04 Nov 2025 04:35:23 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 04 Nov 2025 04:35:23 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 04 Nov 2025 04:35:23 GMT
ARG USER_HOME_DIR=/root
# Tue, 04 Nov 2025 04:35:23 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 04 Nov 2025 04:35:23 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 04 Nov 2025 04:35:23 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317fbb3cee23fb7fdffbd53e48ca51354a5c3dffb327f56bedb8af2d2badf5c2`  
		Last Modified: Tue, 04 Nov 2025 04:35:55 GMT  
		Size: 125.6 MB (125590773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58a0055f636a8efb2c50252ff41e89fbd83f66524b99eee2534320cb6d47be6`  
		Last Modified: Tue, 04 Nov 2025 04:35:47 GMT  
		Size: 9.2 MB (9242595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e3b5624162723ed1d9c82c653c1a0935a0d28c1677f2078c624817546979db`  
		Last Modified: Tue, 04 Nov 2025 04:35:47 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfeabb48b2acc012d2576771fdda55af8bc3afd0f31002cce67b78f8b60c643`  
		Last Modified: Tue, 04 Nov 2025 04:35:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian` - unknown; unknown

```console
$ docker pull maven@sha256:f1ad967016354192bfb7ceea0ef52ac6a3a2fa6ca7e61ed8652f0144f2650450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3001184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab53a38067921d9df293e1a93fa917c7b00294fc90efbe66461747ed7eaed084`

```dockerfile
```

-	Layers:
	-	`sha256:f5c1850a41de2bbf87c405f066d77a5dcdc390d1943478e40ce747c91724a419`  
		Last Modified: Tue, 04 Nov 2025 09:27:56 GMT  
		Size: 3.0 MB (2981972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0791db632c163a0d065aec38670e6a18310545285d567dd9588000c93e19f094`  
		Last Modified: Tue, 04 Nov 2025 09:27:57 GMT  
		Size: 19.2 KB (19212 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:68a4c4775fcb14df35de9fbf24f8a013d85f73142ed8c7234ef654b87a537d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (148952004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58253df907e5cc8d6ae371f1cfcec89d571bcb75db52c84e9fc3b5362d1b500`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:51:06 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:51:06 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:51:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Tue, 04 Nov 2025 01:51:06 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 04 Nov 2025 01:51:06 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 04 Nov 2025 01:51:06 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 04 Nov 2025 01:51:06 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 04 Nov 2025 01:51:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 04 Nov 2025 01:51:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 04 Nov 2025 01:51:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 04 Nov 2025 01:51:06 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 04 Nov 2025 01:51:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 04 Nov 2025 01:51:06 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 04 Nov 2025 01:51:06 GMT
ARG USER_HOME_DIR=/root
# Tue, 04 Nov 2025 01:51:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 04 Nov 2025 01:51:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 04 Nov 2025 01:51:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d013ed533267c26e1323e4e8318c4b1885e2f069038d631437d61431e3444d9c`  
		Last Modified: Tue, 04 Nov 2025 01:51:38 GMT  
		Size: 109.6 MB (109566086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f687bdc899a93e1e289bfb36a1e1a4b7694feb75264024f816e699ba0845a03e`  
		Last Modified: Tue, 04 Nov 2025 01:51:30 GMT  
		Size: 9.2 MB (9242584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7025f68d607a6c61e8e21df1be0dade433548c90c806b6b4430617975d59a27e`  
		Last Modified: Tue, 04 Nov 2025 01:51:28 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7c15c3e10d87a54eac2ea2443bf96c562589bcde474ae6cc0fc60b04198c0e`  
		Last Modified: Tue, 04 Nov 2025 01:51:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian` - unknown; unknown

```console
$ docker pull maven@sha256:98a92c4614a28d7e9a5a74e53035f1b80f00b70a07581a51c173f29a9019b64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d33d848b4b268848c27fcbe4cfe393abf9d491731d95c28a9db3938ae949a5`

```dockerfile
```

-	Layers:
	-	`sha256:f441f2fd49e0204237efed66e4060bf5a32557d0b775847c9b9d7bb9ccdda290`  
		Last Modified: Tue, 04 Nov 2025 12:28:04 GMT  
		Size: 3.0 MB (2964793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e6dfceb41faa4a89a040a15358d32dbda50c8a6e0b76a865a020888822d1e7d`  
		Last Modified: Tue, 04 Nov 2025 12:28:04 GMT  
		Size: 19.4 KB (19381 bytes)  
		MIME: application/vnd.in-toto+json
