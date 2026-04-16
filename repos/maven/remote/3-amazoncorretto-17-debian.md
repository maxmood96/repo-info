## `maven:3-amazoncorretto-17-debian`

```console
$ docker pull maven@sha256:7194829290fea977d18201ddfae3824d9cebe0f630308e2f2621e5582534f814
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-debian` - linux; amd64

```console
$ docker pull maven@sha256:b57d7db7e7a39f79f0b58d2c4807caed73cec8714ee8bfca07128da9d759dda9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243573745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f45a4656286839c4903002c85813b74016acc7d88ce3f717d8c2e3cec48ae4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:50:47 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:50:48 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 22:50:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 15 Apr 2026 22:50:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 15 Apr 2026 22:50:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:50:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:50:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 15 Apr 2026 22:50:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Apr 2026 22:50:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 15 Apr 2026 22:50:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 22:50:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 15 Apr 2026 22:50:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 15 Apr 2026 22:50:48 GMT
ARG MAVEN_VERSION=3.9.14
# Wed, 15 Apr 2026 22:50:48 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Apr 2026 22:50:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Apr 2026 22:50:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Apr 2026 22:50:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e0ad6d1fd7e27c8b9d5d3302babf00edb6dbb735589c50525d0afd92323a18`  
		Last Modified: Wed, 15 Apr 2026 22:51:11 GMT  
		Size: 204.5 MB (204485890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f096b27c955c94cad616094578579d9ef8655bff7f79b896db61ab41a1eb785e`  
		Last Modified: Wed, 15 Apr 2026 22:51:08 GMT  
		Size: 9.3 MB (9311181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff42b4d4aad1ba3c0e36479b4ec364adbf123a3734a3db7ebd7c8035daf6844`  
		Last Modified: Wed, 15 Apr 2026 22:51:07 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22b4bbcb1c3809668f0ebc0ca12acec98c00326b3a82408bf9ebb5237189317`  
		Last Modified: Wed, 15 Apr 2026 22:51:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian` - unknown; unknown

```console
$ docker pull maven@sha256:776ef724d60f921660fdd46b90762d0a983e2bf380de038b247e4f66b73ddd89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3123287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a55fb05c3b049f804c68372bb8870f7d7ceb00b830329c935a6ff39a27e6d7a`

```dockerfile
```

-	Layers:
	-	`sha256:c295ff0d59e2def06e66380e897f29405d37bb1e7fd31a629a7476310300bfdf`  
		Last Modified: Wed, 15 Apr 2026 22:51:07 GMT  
		Size: 3.1 MB (3104087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a36eb4a22504121d27aa220f9961294e6c772d85d9fe8f8532e232bb6bdc16`  
		Last Modified: Wed, 15 Apr 2026 22:51:07 GMT  
		Size: 19.2 KB (19200 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:597d3f12744f952b8345bdab89a55df65e3180255068363b50aaa4e66775142f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.7 MB (242740218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd80977d7307fff96bfcba4c4f7d29f47e1cd3cb4c59ddc5683ba4a840d6bee`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 23:17:30 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:17:30 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 23:17:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 15 Apr 2026 23:17:30 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 15 Apr 2026 23:17:30 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 23:17:30 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 23:17:30 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 15 Apr 2026 23:17:30 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Apr 2026 23:17:30 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 15 Apr 2026 23:17:30 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 23:17:30 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 15 Apr 2026 23:17:30 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 15 Apr 2026 23:17:30 GMT
ARG MAVEN_VERSION=3.9.14
# Wed, 15 Apr 2026 23:17:30 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Apr 2026 23:17:30 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Apr 2026 23:17:30 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Apr 2026 23:17:30 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2612f021f8c093fd0ee8e2afdc74597ef22c69bee87c0896bd7edfb8e8857d99`  
		Last Modified: Wed, 15 Apr 2026 23:17:54 GMT  
		Size: 203.3 MB (203289437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7938c804c32efa28ed4995459bd2215b33224858c95086a933e55d557f031a`  
		Last Modified: Wed, 15 Apr 2026 23:17:50 GMT  
		Size: 9.3 MB (9311193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be31c46e0f66928f9112ef7f89d6ce26af1f13de9e84f6342ed5f16323584350`  
		Last Modified: Wed, 15 Apr 2026 23:17:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec45d8720d6e68bb3bd242d45b58130ed6a9473323946fc0dec050e9a425a0c5`  
		Last Modified: Wed, 15 Apr 2026 23:17:50 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian` - unknown; unknown

```console
$ docker pull maven@sha256:39921345105335b647ac66b4fb5e0c20228c805f9fce67fdf944e5343b8ec06b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3123118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb031033fc097448af921b14fa44599eacaf05ba679713e3afa0f2cc52b8786`

```dockerfile
```

-	Layers:
	-	`sha256:75a94d839438bdb8faef6e130737b27f25647941c8ee452603fb6517a18f1bcd`  
		Last Modified: Wed, 15 Apr 2026 23:17:50 GMT  
		Size: 3.1 MB (3103750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:029c69e86b7affdd4dd4b0c12cde2715cad4c1eac76fd68ea6df062a53af123a`  
		Last Modified: Wed, 15 Apr 2026 23:17:50 GMT  
		Size: 19.4 KB (19368 bytes)  
		MIME: application/vnd.in-toto+json
