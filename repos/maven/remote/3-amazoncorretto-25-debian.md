## `maven:3-amazoncorretto-25-debian`

```console
$ docker pull maven@sha256:29194df0a710fe3ed82f821ef74b831fe97dd5f849124c8f54acfcfe71faa45a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-debian` - linux; amd64

```console
$ docker pull maven@sha256:af5b188010c38a24907d8514900d5ac84eff653caa5135db90b515b1a5685c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277327633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6c1d2ebf0921cc7bb1dd2991d86b6db3ab9b174faeb46b7d329bd988a820e4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 21 Apr 2026 18:12:48 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 18:12:48 GMT
ENV LANG=C.UTF-8
# Tue, 21 Apr 2026 18:12:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 21 Apr 2026 18:12:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:12:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:12:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:12:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:12:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:12:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:12:48 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:12:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:12:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:12:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba145fcbe443436304d64476144bd4ed698f311602b96d5fe46fbe9fdb231f67`  
		Last Modified: Tue, 21 Apr 2026 18:13:18 GMT  
		Size: 238.2 MB (238238788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11cf0551a92ef95bdf4d20adb31c045ec53f311ab854963373d522492cfab4b5`  
		Last Modified: Tue, 21 Apr 2026 18:13:10 GMT  
		Size: 9.3 MB (9312201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a1d5236b3590b10f9194ef10c854238354993e5ea50bf463099115decf8602`  
		Last Modified: Tue, 21 Apr 2026 18:13:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3f5e99f6bf53b743d3ab0010dc0a6d0cd3fe41d8523f2ddfc4cac182320cea`  
		Last Modified: Tue, 21 Apr 2026 18:13:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian` - unknown; unknown

```console
$ docker pull maven@sha256:0d8d6e197b301868e7b00cc901aa4467ebc0dfee6a67b45fd1f74735e0595f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3130615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca44059f9cc55844be9a0e29e2640409779c798562baf0da7663178dcf203d5`

```dockerfile
```

-	Layers:
	-	`sha256:b258018cc7652aed23824534a8b8eeac8404b5fe49f0b782ef05785c57e40d03`  
		Last Modified: Tue, 21 Apr 2026 18:13:10 GMT  
		Size: 3.1 MB (3113090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56392667ae8adbd34b887e6aefe936c422d8f534c67d55935afe154493ce37ca`  
		Last Modified: Tue, 21 Apr 2026 18:13:09 GMT  
		Size: 17.5 KB (17525 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6e13403cbf9baf930d5616546df9075c21e0546cb3f22ea5d83a78b447744a49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272737974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb52605a01633849a0eae6b709c76158f73645d62ab1e0aea8c951f898f4b976`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:26:13 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:26:13 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 02:26:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 22 Apr 2026 02:26:13 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 22 Apr 2026 02:26:13 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 02:26:13 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 02:26:13 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 22 Apr 2026 02:26:13 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 22 Apr 2026 02:26:13 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 22 Apr 2026 02:26:13 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:26:13 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 22 Apr 2026 02:26:13 GMT
ARG USER_HOME_DIR=/root
# Wed, 22 Apr 2026 02:26:13 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 22 Apr 2026 02:26:13 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 22 Apr 2026 02:26:13 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3052364c2d31a846749d6ccc4a8bf8f8c2b2effc60854aa13f5c375be7248896`  
		Last Modified: Wed, 22 Apr 2026 02:26:42 GMT  
		Size: 233.3 MB (233281113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b675f2177a7988e5cb51f812c04bd76ca21271264892db6e3691710890433b4`  
		Last Modified: Wed, 22 Apr 2026 02:26:37 GMT  
		Size: 9.3 MB (9312253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3113693d321a06eaddbe53a719065829c6f3b764634a1494df4586df32f53186`  
		Last Modified: Wed, 22 Apr 2026 02:26:35 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f5cb8fc2a77b8fdc7a1c4d22ea95315472a64acde7e72c36cc25654b646dd1`  
		Last Modified: Wed, 22 Apr 2026 02:26:36 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian` - unknown; unknown

```console
$ docker pull maven@sha256:50ae448432f161300cc5d2c0c80befc2b6dc4a7b494b8c4e0db737d3cbf982d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43726b4806bd310b3796c55516b9057a272267c17d85e30e1bbe9266cfd83150`

```dockerfile
```

-	Layers:
	-	`sha256:8a8ec939dabbd8dc15bd27abff939ab3abfc36439dbb1c890d0e381086960b3e`  
		Last Modified: Wed, 22 Apr 2026 02:26:36 GMT  
		Size: 3.1 MB (3113392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:935c60715f9d43c5c6a96cb778a3a6ecb798990749d14aa99184e966eafadc2a`  
		Last Modified: Wed, 22 Apr 2026 02:26:35 GMT  
		Size: 17.7 KB (17693 bytes)  
		MIME: application/vnd.in-toto+json
