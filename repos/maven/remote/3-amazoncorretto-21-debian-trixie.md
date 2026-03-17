## `maven:3-amazoncorretto-21-debian-trixie`

```console
$ docker pull maven@sha256:5307bc9a30a3f523016977df35479e369845633894e942a4547e5e4bd001c416
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:28b51c8ea8a882a1c20c3a37096b614487bd4d4723778657cb71c4a3513f61fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255740898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f73e97ae32e172bc3e38200dffba359fe3d14ce3b080e44241164a0875ed7d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:48:21 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:48:21 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 03:48:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 17 Mar 2026 03:48:21 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Mar 2026 03:48:21 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:48:21 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:48:21 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Mar 2026 03:48:21 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Mar 2026 03:48:21 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Mar 2026 03:48:21 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 03:48:21 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Mar 2026 03:48:21 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Mar 2026 03:48:21 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 17 Mar 2026 03:48:21 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Mar 2026 03:48:21 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Mar 2026 03:48:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Mar 2026 03:48:21 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37053185fdf474768359632437078b50c19335f19a98a13cac806d0ac341ba04`  
		Last Modified: Tue, 17 Mar 2026 03:48:44 GMT  
		Size: 216.7 MB (216653187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0bf74c84045360376bffda37c0100bee051181cbe9efc0bd5076e57ddbb6f`  
		Last Modified: Tue, 17 Mar 2026 03:48:40 GMT  
		Size: 9.3 MB (9311179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e475bb66dc0da47c82bda7a72a8014eed8a7e0e8739dd0c6588c11819e8399`  
		Last Modified: Tue, 17 Mar 2026 03:48:40 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53d421494218def161649816c679b65d232f77878a9f114e5d1383229846a23`  
		Last Modified: Tue, 17 Mar 2026 03:48:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:1bd7aa7cf43168753a6c151ef760e1721c4703d5b51c56f416ad05c2df683eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3123190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52158af0d0803eab83adb5011ab92fadb5d89cadab0b28515578ffac9000a7c`

```dockerfile
```

-	Layers:
	-	`sha256:30c9c213e6fcdb0818e68f8a276931003fa8b6b2973166c6eba208af6ea2c265`  
		Last Modified: Tue, 17 Mar 2026 03:48:40 GMT  
		Size: 3.1 MB (3103990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ece44a9ed2455adfbec0c665823af933e9d352ffd2bb40494dfa96142e70204`  
		Last Modified: Tue, 17 Mar 2026 03:48:40 GMT  
		Size: 19.2 KB (19200 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:0c22f751fe9a01eb174678fc9921b575df82e03692703793ed7d31182f9db70f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.1 MB (254065501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e03e4de9bd52f2e17e028e689c6d836b03e594d8ee5581f71d06bfecb20e3d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:49:19 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:49:19 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 03:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 17 Mar 2026 03:49:19 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Mar 2026 03:49:19 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:49:19 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:49:19 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Mar 2026 03:49:19 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Mar 2026 03:49:19 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Mar 2026 03:49:19 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 03:49:19 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Mar 2026 03:49:20 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Mar 2026 03:49:20 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 17 Mar 2026 03:49:20 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Mar 2026 03:49:20 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Mar 2026 03:49:20 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Mar 2026 03:49:20 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d49533adced1f482247a904bcccf311bc6834d258c2a5f69ae7553df572ad4`  
		Last Modified: Tue, 17 Mar 2026 03:49:46 GMT  
		Size: 214.6 MB (214614873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0328227eaa11534ea7946d2bd3e693ecfd25b73e31d8ac3ea0f5789ce7b06e95`  
		Last Modified: Tue, 17 Mar 2026 03:49:40 GMT  
		Size: 9.3 MB (9311179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff4d99cf0e14a35238e559fe5de7e01e77d9b49492076d0c60a3924061b144c`  
		Last Modified: Tue, 17 Mar 2026 03:49:39 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4521c60a05183179fbd9a964ea4ffaa996a0b84d41c052c129d67e6a7d3cf1d3`  
		Last Modified: Tue, 17 Mar 2026 03:49:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:633dee828ddd1eec4cdbac778916b4f84d3e2b599b712a45c2cafc4f63a95898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3123021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b14de691a3a82997dacce38c53eaee332efac252c2e93fdaf9578cc12a0750d5`

```dockerfile
```

-	Layers:
	-	`sha256:9a5a8e02cda3beb289f1259a5dc1f52698183cc7fa73adadb93bf0be70af6e78`  
		Last Modified: Tue, 17 Mar 2026 03:49:39 GMT  
		Size: 3.1 MB (3103653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2a38c01996985b1af21ad80e4429a665da988dbc4a7915349325e96ab93f9ca`  
		Last Modified: Tue, 17 Mar 2026 03:49:39 GMT  
		Size: 19.4 KB (19368 bytes)  
		MIME: application/vnd.in-toto+json
