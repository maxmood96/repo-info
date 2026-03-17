## `maven:3-amazoncorretto-8-debian-trixie`

```console
$ docker pull maven@sha256:b5a4440428c6c5d5f6de4c2a1f8882c87901dc5a7a55eb141a6c997e4c49110a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:31a592b123601f1c1e8c94e44417b5a77b47fb24c2c503441612c2ccc753d248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164733988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f58fc68347a6303c0468e36d211e43db85a4222215c73806892dc94a72a3f98`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:50:26 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:50:26 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 03:50:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Tue, 17 Mar 2026 03:50:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Mar 2026 03:50:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:50:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:50:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Mar 2026 03:50:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Mar 2026 03:50:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Mar 2026 03:50:27 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 03:50:27 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Mar 2026 03:50:27 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Mar 2026 03:50:27 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 17 Mar 2026 03:50:27 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Mar 2026 03:50:27 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Mar 2026 03:50:27 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Mar 2026 03:50:27 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33003b89cf820398d1e73b3dce69c48a8ed1476d8a73278983b84ba52ac120b`  
		Last Modified: Tue, 17 Mar 2026 03:50:45 GMT  
		Size: 125.6 MB (125646277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a593a506f515e9f9052cc2247d9b15e52ca76b001011387fdd19140875f6236a`  
		Last Modified: Tue, 17 Mar 2026 03:50:42 GMT  
		Size: 9.3 MB (9311179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d36dca5c8f9b87c92fcc1dd4101d67d5c037a7bbaf6084c5245dede25c11eb3`  
		Last Modified: Tue, 17 Mar 2026 03:50:42 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69972146cd2e203cafdc998fb651032560bc65ef09af6458e1abd205799e587f`  
		Last Modified: Tue, 17 Mar 2026 03:50:42 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:43f0c20592e768ffb9e2625f1c188d6124572003b9c2019e1ae93cca9184808c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3001305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458f671e9315e2806fe82b16a2aac68a1fca2205f410e7a2fb49a3630f4567a5`

```dockerfile
```

-	Layers:
	-	`sha256:3c2272579d74ef529b9a4d50a51d1d70acd6ddf3cd74c7abaf6a84efe412d370`  
		Last Modified: Tue, 17 Mar 2026 03:50:42 GMT  
		Size: 3.0 MB (2982093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82f90a6d96128b9d46e7b0b116ccaffb9959d37821dd42c31b644cdba983db3a`  
		Last Modified: Tue, 17 Mar 2026 03:50:42 GMT  
		Size: 19.2 KB (19212 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c9b4852b1c944a26fba4874c7650b1f654ac8a83995a7da9c38d0ed1de6b458e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148822650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d00539dc1ee13002369736314b10bdef9124ed6ab419bcf5423e5617d2d043d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:50:15 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:50:15 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 03:50:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Tue, 17 Mar 2026 03:50:15 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Mar 2026 03:50:15 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:50:15 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:50:15 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Mar 2026 03:50:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Mar 2026 03:50:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Mar 2026 03:50:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 03:50:16 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Mar 2026 03:50:16 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Mar 2026 03:50:16 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 17 Mar 2026 03:50:16 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Mar 2026 03:50:16 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Mar 2026 03:50:16 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Mar 2026 03:50:16 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffe3fe040cc07fef81f81c3a3a3b000febafbcde3d2896eb00eee67b987cb34`  
		Last Modified: Tue, 17 Mar 2026 03:50:32 GMT  
		Size: 109.4 MB (109372022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95f66fd8c6cd75b37aa84c3e1ea5e3712e3bc15bab6be3d0805567030bf0b9c`  
		Last Modified: Tue, 17 Mar 2026 03:50:30 GMT  
		Size: 9.3 MB (9311179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded3ae8bcfa1e30d74d38b5ad38c48a6d5ac949d4e8c29b780de2d0a3ee65699`  
		Last Modified: Tue, 17 Mar 2026 03:50:29 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa274d2e12db254b1a191a22c5de7cff5ffb59d8b4db80c4f2a8b2efca124c8`  
		Last Modified: Tue, 17 Mar 2026 03:50:29 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:f4fdd18dbb664903e004341b1aaf9bb5d1189d52a7c87130ed6bf7f6f44d26e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087afeb232bb1f8aa0eb2ab583a27e9ca8bd90723e6c7828b9ac1f6ea7cc3ce1`

```dockerfile
```

-	Layers:
	-	`sha256:b812effe5c382e7507119652d7a7a8005a01af85fc26a8d09b8ab3a47f82a4f9`  
		Last Modified: Tue, 17 Mar 2026 03:50:29 GMT  
		Size: 3.0 MB (2964914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ea5f22a3c6724ca26ad9768249abc0af12424ba24ff562ecc58b06a47eb3c7e`  
		Last Modified: Tue, 17 Mar 2026 03:50:29 GMT  
		Size: 19.4 KB (19381 bytes)  
		MIME: application/vnd.in-toto+json
