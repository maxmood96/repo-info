## `maven:3-amazoncorretto-11-debian-trixie`

```console
$ docker pull maven@sha256:2e35a7b5ec381dba9c2ff5d977feb546bd38398d1f674178b4918825477c7621
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:f064a379116deaad7308bbb472e720d57e5be6f8c2e41f73c1991b4f9b1fc4af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241745810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b44c350480d0bec11e63728edbba491dc04a537e1ad1a01305d53f5eaa3fcdd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:07:42 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:07:42 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 05:07:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 07 Apr 2026 05:07:42 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 05:07:42 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:07:42 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:07:42 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 05:07:42 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 05:07:42 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 05:07:42 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:07:42 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 05:07:42 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 05:07:42 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 05:07:42 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 05:07:42 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 05:07:42 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 05:07:42 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dba6853f2fead9d8748120c26339d2ee94492e0543d2197f7549fc3713f795b`  
		Last Modified: Tue, 07 Apr 2026 05:08:04 GMT  
		Size: 202.7 MB (202657944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e756deef55e38a76be000dfdebd171cd66dbd05249cf4939386285cb99bb66f`  
		Last Modified: Tue, 07 Apr 2026 05:08:00 GMT  
		Size: 9.3 MB (9311188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166613fd4a51e0e06706a64a4b9adada03ae8a403e0865863d9a7e6ff6f4b90a`  
		Last Modified: Tue, 07 Apr 2026 05:07:59 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4815c23adfc5eb450d9029e15126b89346b2fc3615aa5a2a35b6bdd7363c964`  
		Last Modified: Tue, 07 Apr 2026 05:08:00 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:6551bc6db5b7f3fe288e4c57e5b419e7dcb17206a58a5105c3f5d91a0f3a77e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854a9ca95f63a5865d77ece94f8cdcac25451786be9579500a4a376273010aeb`

```dockerfile
```

-	Layers:
	-	`sha256:d1f1e1873f8cfd8eb207e20fe606c557d6a14c8a5710b0ee781e17f6e87b420e`  
		Last Modified: Tue, 07 Apr 2026 05:08:00 GMT  
		Size: 3.1 MB (3109880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9804d17e42deef0cd95ff742d8a8b7c7ebdf67dd2772e3763c6f92c12a484d3a`  
		Last Modified: Tue, 07 Apr 2026 05:07:59 GMT  
		Size: 19.2 KB (19200 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f680c1a798d8be89851da49f7d895bd345c035d9534a8ff02a25f98d2da14613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.1 MB (239108748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54d236537309f0e84b8bb16991525e451eb35894d9a513905e8a29a474b9370`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:13:51 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:13:52 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 05:13:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 07 Apr 2026 05:13:52 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 05:13:52 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:13:52 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:13:52 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 05:13:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 05:13:52 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 05:13:52 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:13:52 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 05:13:52 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 05:13:52 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 05:13:52 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 05:13:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 05:13:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 05:13:52 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f27bb1f959b6a644b7951ed85523ea61474b10f85bd55c7f16703d144f5f849`  
		Last Modified: Tue, 07 Apr 2026 05:14:14 GMT  
		Size: 199.7 MB (199657967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ff46d288ad5eed620d747e6992e9af1d7cc83cf1d709b00a7b24bce303ca12`  
		Last Modified: Tue, 07 Apr 2026 05:14:10 GMT  
		Size: 9.3 MB (9311195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49c8fdb99c4baae1b96ffe2a1c04a6d7f5269e634b97e66db81e6947dcc0d11`  
		Last Modified: Tue, 07 Apr 2026 05:14:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d7c8886aa25317eb0879884a26cb6e57fa3eb83f2566d1aec4bb89c084d865`  
		Last Modified: Tue, 07 Apr 2026 05:14:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:d2c9b07fdadff8991495c43ef461d0ac96c2d2dfa516275e707c01bae8048431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b226d713b5247b72081f47ff62e3973a93f8f6aa62083cc77a40fed56d3f2bb`

```dockerfile
```

-	Layers:
	-	`sha256:9da294e14c5463839da4b256fac0a76319f261db9b254438985def077ad93d36`  
		Last Modified: Tue, 07 Apr 2026 05:14:10 GMT  
		Size: 3.1 MB (3110180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b801fa689811af576c9d3a5a7ba0bbaeae641d686e6af9f989065c935059f28e`  
		Last Modified: Tue, 07 Apr 2026 05:14:10 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json
