## `maven:3-amazoncorretto-17-debian-trixie`

```console
$ docker pull maven@sha256:c6849261e673966bbac06828ca6e35c3b69eb203f52180f338b10aec29e3e639
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:49e06d5b4ba910484bff4a3b55d531280a392b29a6ee3227a9e9b79182993b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240612699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6afab45bc0f006fc6a9d2cadd572b52c3196d04ef1ab563cebf806d76f9bba`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:08:06 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:08:06 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 05:08:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 07 Apr 2026 05:08:06 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 05:08:06 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:08:06 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:08:06 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 05:08:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 05:08:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 05:08:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:08:06 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 05:08:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 05:08:06 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 05:08:06 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 05:08:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 05:08:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 05:08:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1718bf6a1413483bce8dfd41f3cf60009a89e2f4eb163687948a407700be8fd4`  
		Last Modified: Tue, 07 Apr 2026 05:08:29 GMT  
		Size: 201.5 MB (201524842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de26171523778ec2c2f4e8a10e5bd8c907d41af7eced1e30d2f846d0cdd531b`  
		Last Modified: Tue, 07 Apr 2026 05:08:25 GMT  
		Size: 9.3 MB (9311179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004dab9a7d2d4b0af59eb22b42cf0d6989e06892e85d4a99ec36ba69988ce10a`  
		Last Modified: Tue, 07 Apr 2026 05:08:25 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f63c0a19beaf51a98c181a91e546e96bfcd5a4dd5ceca33903860773caa997`  
		Last Modified: Tue, 07 Apr 2026 05:08:25 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:7297703d287a7facf966e3d6d1418d664cb10d8b6afc0197ba3602c0cfde8191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3123287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee0620d7f95df4b9d02ee4730d039dc74e6eed242a4fb283ae4d0c2f145e273`

```dockerfile
```

-	Layers:
	-	`sha256:be5bb4d201ddce8a00b24aa32280a94dd02da9ef93279de5fd95a43c4e44c456`  
		Last Modified: Tue, 07 Apr 2026 05:08:25 GMT  
		Size: 3.1 MB (3104087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7a29af58ba92fcf4699f8deb8500db9a9d0a1b303253dbe83e5422f2e6114b4`  
		Last Modified: Tue, 07 Apr 2026 05:08:25 GMT  
		Size: 19.2 KB (19200 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:de35a806c8967e2bceccb42571a30f9403be576dbea1bdbc56942b70c38091ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239397788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a22577e1bd82507c818127760e328540e558c3204cc14ff3957840433328f7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:14:40 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:14:40 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 05:14:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 07 Apr 2026 05:14:40 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 05:14:40 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:14:40 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:14:40 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 05:14:40 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 05:14:40 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 05:14:40 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:14:40 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 05:14:40 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 05:14:40 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 05:14:40 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 05:14:40 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 05:14:40 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 05:14:40 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16502fc0d48e20b57c34509fd3fe98895ca94f4b36b5d824ec88c0a7dd288c59`  
		Last Modified: Tue, 07 Apr 2026 05:15:04 GMT  
		Size: 199.9 MB (199947012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cca4b229660a750080dce579d0c4e919b303c3a91957383a44b0db07dd5352`  
		Last Modified: Tue, 07 Apr 2026 05:14:59 GMT  
		Size: 9.3 MB (9311192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420c48e33fc9d686a9c32a7eb02292d7992e3dfc85cee7e2746cb57595427abe`  
		Last Modified: Tue, 07 Apr 2026 05:14:59 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96f589ef0caf33a2bc8232f904a033a054b49dccca7a0f94dd26751db24d3cf`  
		Last Modified: Tue, 07 Apr 2026 05:14:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:b96add1a3ce9720bd5eb2c4d5a00505d6377e5ddc93d07e755cf329f23df047a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3123119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631a7577b3765211b8ffa450dd3ca560477660b65087a50a6099c979a750ff98`

```dockerfile
```

-	Layers:
	-	`sha256:2d7ab36dce47be3d11eb7c48a98e541f6cbb3058b35b075beef46c8f09a9d747`  
		Last Modified: Tue, 07 Apr 2026 05:14:59 GMT  
		Size: 3.1 MB (3103750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2498ed2678143efdb51e08caa1f0590a5ac9c52c1049c2e1bc9f694bf348dfd9`  
		Last Modified: Tue, 07 Apr 2026 05:14:59 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json
