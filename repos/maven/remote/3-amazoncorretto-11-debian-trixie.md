## `maven:3-amazoncorretto-11-debian-trixie`

```console
$ docker pull maven@sha256:9b37364b92733d55c492f2646c739ff869b7879ba366aa9262160fa8402e2424
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:05d1e9058bf7d84c523e11d9a2ab795bea0067411da00388b05530f9617cd9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241896401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e6dd22cc2dd6326e164b1bbfa4c55116d271003d09442d35e9d502ec48d283`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:22:56 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:22:56 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:22:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 11 Jun 2026 01:22:56 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 11 Jun 2026 01:22:56 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 11 Jun 2026 01:22:56 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 11 Jun 2026 01:22:56 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 11 Jun 2026 01:22:56 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 11 Jun 2026 01:22:56 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 11 Jun 2026 01:22:56 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 11 Jun 2026 01:22:56 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 11 Jun 2026 01:22:56 GMT
ARG USER_HOME_DIR=/root
# Thu, 11 Jun 2026 01:22:56 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 11 Jun 2026 01:22:56 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 11 Jun 2026 01:22:56 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e4ae9a09f8e378a557065f0c3535f0a2e40fc56082af7e3bfde8d340c4e62b`  
		Last Modified: Thu, 11 Jun 2026 01:23:19 GMT  
		Size: 202.8 MB (202750024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dcc72b123c66bbd438204ba4a58d760bf12fa2b732932a8ba9cdaf9dca9905`  
		Last Modified: Thu, 11 Jun 2026 01:23:15 GMT  
		Size: 9.4 MB (9359958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0b4aae5938574f1563e098163bdfcc4edbf4c72fbd1b8bfb736c18e515caf3`  
		Last Modified: Thu, 11 Jun 2026 01:23:14 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6870050d1e8bdc76c3355987d86aa9a8b6a6226e5bcc5f120137a865ae8b5745`  
		Last Modified: Thu, 11 Jun 2026 01:23:14 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:a85f225db356b182e00a47c3f3b41278e9c6e6e1f46ee2fedae1b85d02e78ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32599148a4b6e98f072711c1b6f9ec9981983723689a83497879c21e078f2e21`

```dockerfile
```

-	Layers:
	-	`sha256:418ce8b31e39c224f7110de50d4ae8f71da260aea6f55aa9304c9935d9e85438`  
		Last Modified: Thu, 11 Jun 2026 01:23:14 GMT  
		Size: 3.1 MB (3110035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e458b9fcbc5a8600fe7338f1ea2ccc11ec40e53a539dde98be736258d1772d45`  
		Last Modified: Thu, 11 Jun 2026 01:23:14 GMT  
		Size: 17.5 KB (17525 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b6b519b269f61107cbfe7f464754f6d92ba763d8c9649401d7f2d326d551e96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.3 MB (239327689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316494f1b6f78ae26afcc22616b99d3d52b9abbdf16791f5ee81d1777de22603`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:27:19 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:27:19 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:27:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 11 Jun 2026 01:27:19 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 11 Jun 2026 01:27:19 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 11 Jun 2026 01:27:19 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 11 Jun 2026 01:27:19 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 11 Jun 2026 01:27:19 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 11 Jun 2026 01:27:19 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 11 Jun 2026 01:27:19 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 11 Jun 2026 01:27:19 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 11 Jun 2026 01:27:19 GMT
ARG USER_HOME_DIR=/root
# Thu, 11 Jun 2026 01:27:19 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 11 Jun 2026 01:27:19 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 11 Jun 2026 01:27:19 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d729bda47f8728e7212aa8730f2a1f86037bd4d16eb61dc30f9636a641966200`  
		Last Modified: Thu, 11 Jun 2026 01:27:44 GMT  
		Size: 199.8 MB (199818184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54776bddc525ee5317e3185c3f2fdbe12d44c5c94fbc3fc9d5c5fa388c1b9a23`  
		Last Modified: Thu, 11 Jun 2026 01:27:39 GMT  
		Size: 9.4 MB (9359970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54bb32e0cc670c1e0fe434f2374db2c1f6c74a8284060058afa9cf3ecaadd0`  
		Last Modified: Thu, 11 Jun 2026 01:27:38 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eafdbe267ccbdee12a0dff0c1ce313f415047709d0c6530b695bcedb6daa00`  
		Last Modified: Thu, 11 Jun 2026 01:27:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:8c348960c16249fa346aa1384ae1484b863d28a22e3a5858874eebf9e041c9b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08689205f8d5bdb2fdbe3607afbabb19656f35fa7a2c6b918ebc30d8bf6355cd`

```dockerfile
```

-	Layers:
	-	`sha256:b330099369b794ba06dc70e2c5c92871723e8abaa4be3c29f110601aa504b0a8`  
		Last Modified: Thu, 11 Jun 2026 01:27:38 GMT  
		Size: 3.1 MB (3110327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c36e472684ad8a1af49dc148381b8f638a7b7380256eba4b21195a07b55092cb`  
		Last Modified: Thu, 11 Jun 2026 01:27:38 GMT  
		Size: 17.7 KB (17694 bytes)  
		MIME: application/vnd.in-toto+json
