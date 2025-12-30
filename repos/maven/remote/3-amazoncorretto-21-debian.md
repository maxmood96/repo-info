## `maven:3-amazoncorretto-21-debian`

```console
$ docker pull maven@sha256:cd95fadfe2eb6b99507e646cd4711494ead2e72afa4608c7fa133d77b2c0aa4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-debian` - linux; amd64

```console
$ docker pull maven@sha256:286a37e6f817809353ed146db45908458e27629de415dd3f9f33f9b6f52cf9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255691646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7692e123b7c1752087efed0b80aa31c179dbc8f5aac843217d732e63b4a63241`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:11:08 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:11:09 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:11:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 30 Dec 2025 01:11:09 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 30 Dec 2025 01:11:09 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 30 Dec 2025 01:11:09 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 30 Dec 2025 01:11:09 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 30 Dec 2025 01:11:09 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 30 Dec 2025 01:11:09 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 30 Dec 2025 01:11:09 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:11:09 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 30 Dec 2025 01:11:09 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 30 Dec 2025 01:11:09 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 30 Dec 2025 01:11:09 GMT
ARG USER_HOME_DIR=/root
# Tue, 30 Dec 2025 01:11:09 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 30 Dec 2025 01:11:09 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 30 Dec 2025 01:11:09 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07d61ca531763ecf51995995b57e635f04bea1950e8bc893e40422e0073ef9f`  
		Last Modified: Tue, 30 Dec 2025 01:12:14 GMT  
		Size: 216.6 MB (216601831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb1bbaca8fb958c2d5654ec12be882be76e0d40035851a5fb1984f198282e21`  
		Last Modified: Tue, 30 Dec 2025 01:11:46 GMT  
		Size: 9.3 MB (9312246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d840d6473f996af04a3b7e087b9c7c2a9103b56cc50915f07423ae7674480729`  
		Last Modified: Tue, 30 Dec 2025 01:11:43 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a816b0d2e0a3f0e27d78442c18e58a88c3c95934b7581a332cdc2dfd0fc068ff`  
		Last Modified: Tue, 30 Dec 2025 01:11:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian` - unknown; unknown

```console
$ docker pull maven@sha256:11a7723bf4114d97729a4c3caaea0b911edb4324dc2da6c6c9a9f7264d722b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3123064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead1201ecdce98b0ae4bc68ec6b2e8833f13bb00da3d35731857660ee4385c83`

```dockerfile
```

-	Layers:
	-	`sha256:057403b3bac44f448cd5bc49cd52cfc6da1cc255f329cee6ede09442fc98b5b3`  
		Last Modified: Tue, 30 Dec 2025 03:28:55 GMT  
		Size: 3.1 MB (3103864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53eb48026f3eda60db6f87b6a7118a4d0c03d7a59eab46b8a53124a4a7dbd4b6`  
		Last Modified: Tue, 30 Dec 2025 03:28:55 GMT  
		Size: 19.2 KB (19200 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:df957da572d8255759dead7b9543ff9eb0596d71300d73f5325e8adb061277c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (254007477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ba822b472ad5ad5096687885ced0e962fe3ba5b79883f994285166ade3fff0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:12:27 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:12:27 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:12:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 30 Dec 2025 01:12:27 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 30 Dec 2025 01:12:27 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 30 Dec 2025 01:12:27 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 30 Dec 2025 01:12:27 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 30 Dec 2025 01:12:27 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 30 Dec 2025 01:12:27 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 30 Dec 2025 01:12:27 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:12:27 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 30 Dec 2025 01:12:27 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 30 Dec 2025 01:12:27 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 30 Dec 2025 01:12:27 GMT
ARG USER_HOME_DIR=/root
# Tue, 30 Dec 2025 01:12:27 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 30 Dec 2025 01:12:27 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 30 Dec 2025 01:12:27 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417e9cb453ed63b7cfc11d2c6ac1392950e156aad7aa24050b98bc6c02621e3d`  
		Last Modified: Tue, 30 Dec 2025 01:14:32 GMT  
		Size: 214.6 MB (214555564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5414420b7093090a6cba86281d68ea520e65300634fa6dd178138604b878f9`  
		Last Modified: Tue, 30 Dec 2025 01:13:01 GMT  
		Size: 9.3 MB (9312239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b0583b02e836cbaf33957540fb7a8ee70ee2b8811b8a3abbc5f41e8e0e5e86`  
		Last Modified: Tue, 30 Dec 2025 01:12:59 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1a260418119e9482e8c30946db9bfa85928e8213d458e2ebc4341aa56e2627`  
		Last Modified: Tue, 30 Dec 2025 01:12:59 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian` - unknown; unknown

```console
$ docker pull maven@sha256:41742b32e17bae34ef4ef79ec9dcb93266a01cf274afb638e2a27e428a128577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0697d6a8829360aa3e3d4d21b8e12835c5fd48b83f61cd97fa849b762b80b2e`

```dockerfile
```

-	Layers:
	-	`sha256:78cbd98e892e8ad12407e8e68413cb57fa4a93196fa01cfba85d7bf9c162ca09`  
		Last Modified: Tue, 30 Dec 2025 03:28:59 GMT  
		Size: 3.1 MB (3103527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:add59d9b216db2e8855f2ba0e4a43919588a1a6a3da72f41ebcdac11e3872706`  
		Last Modified: Tue, 30 Dec 2025 03:29:00 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json
