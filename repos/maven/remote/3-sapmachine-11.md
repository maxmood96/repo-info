## `maven:3-sapmachine-11`

```console
$ docker pull maven@sha256:47bbdc18e267e40c669197525707d9e7ab40ea5a5fa1b8a8fbb317fd9174cf4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-sapmachine-11` - linux; amd64

```console
$ docker pull maven@sha256:d7c0076380e23b4a21f88689d6241c6978134e4665e9e5451348b043a702547b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265207156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0eb465a267a16d6845800834448cfb678894e6965a59b67e01f0e8e1838927`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:26:02 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.30 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:26:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 17 Mar 2026 02:26:02 GMT
CMD ["jshell"]
# Tue, 17 Mar 2026 03:50:53 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:50:53 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Mar 2026 03:50:53 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:50:53 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:50:53 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Mar 2026 03:50:53 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Mar 2026 03:50:53 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Mar 2026 03:50:53 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 03:50:53 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Mar 2026 03:50:53 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Mar 2026 03:50:53 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 17 Mar 2026 03:50:53 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Mar 2026 03:50:53 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Mar 2026 03:50:53 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Mar 2026 03:50:53 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a36b8f28c763c55de73ab40f32f8708ac2b9f31e568b6103812d9a7da75f32c`  
		Last Modified: Tue, 17 Mar 2026 02:26:24 GMT  
		Size: 200.7 MB (200692777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac82c9ffe746ca79111f96880f32e7f4419567f252e6e6f456b6301415662323`  
		Last Modified: Tue, 17 Mar 2026 03:51:07 GMT  
		Size: 25.5 MB (25470169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ba2ad69dc384f1a54c8838ec08e9f075703f323135ee578994e92dcb249128`  
		Last Modified: Tue, 17 Mar 2026 03:51:06 GMT  
		Size: 9.3 MB (9311179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93dd74d40b7339591cb31564df15eeb77b24bfc37b822c2167eaaebc70b67c1`  
		Last Modified: Tue, 17 Mar 2026 03:51:06 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09807515e98a4fa5025db77e1be58530bcad4755233544b6b9af7d1921cba74b`  
		Last Modified: Tue, 17 Mar 2026 03:51:06 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-11` - unknown; unknown

```console
$ docker pull maven@sha256:5d629132b825d65db665b413b4ed036065481af62db7b2138c2123fc55308ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4347404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d45b9cb3b38c66cc771ddc537c610483f01fea645ce3967f8df79da99d1fb3`

```dockerfile
```

-	Layers:
	-	`sha256:7cf9befe3f8136f7023c198ac2ac253fdf200e670b71383f9b0c28ce87dfc381`  
		Last Modified: Tue, 17 Mar 2026 03:51:06 GMT  
		Size: 4.3 MB (4330901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81a20c2cefd0c458568d93bef8ac4ff1c19922c88514cefccbc08ff4eb39b86f`  
		Last Modified: Tue, 17 Mar 2026 03:51:06 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json
