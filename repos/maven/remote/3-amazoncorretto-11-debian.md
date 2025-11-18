## `maven:3-amazoncorretto-11-debian`

```console
$ docker pull maven@sha256:7d1e2be6d67ebabba81bc79b3f134ff68d86949f258bdfa8d60573316bb1ceb7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-debian` - linux; amd64

```console
$ docker pull maven@sha256:1b01713a93e3bd40f8e5fc38cadc2824d00f34530ff2072364338a5c8414902a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.6 MB (241610509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b438878e2bec030ade82fa128e1e7d350a22aff7418c23e1b80f0c774c0a8ee3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 01:41:55 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:41:55 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 01:41:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 14 Nov 2025 01:41:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 01:41:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:41:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:41:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 01:41:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 01:41:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 01:41:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:41:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 01:41:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 01:41:55 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 01:41:55 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 01:41:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 01:41:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 01:41:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624e9d33585bf9c3457d45104f45410cb219a426cdf8159bffbe8957242f400`  
		Last Modified: Fri, 14 Nov 2025 04:40:40 GMT  
		Size: 202.6 MB (202588792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344d38df70ee72c1d8c017dabd6cadaae0e98b80689aaa50845512d1e950cc5b`  
		Last Modified: Fri, 14 Nov 2025 01:42:25 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62ae2ac0e80b58b146443f89487e2be9871d99a9a9111b87feabf9607070dcd`  
		Last Modified: Fri, 14 Nov 2025 01:42:24 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1498904d58152485d57c869f71ced6598da197a9b5a646629b1e5a3f07bbf0`  
		Last Modified: Fri, 14 Nov 2025 01:42:24 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian` - unknown; unknown

```console
$ docker pull maven@sha256:ed9047a030b82f05758554a005060ae1391a0b85afcb60a18f4d41c80461dbe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b8f17076e8f0d538338dff1eedcbfa6a2ab5137bed7bb4f3d6c84fb0a87d162`

```dockerfile
```

-	Layers:
	-	`sha256:4a8362d547b1d939a34aabc50b1acd39877765464184ff1063447af0e4298ac5`  
		Last Modified: Fri, 14 Nov 2025 03:27:55 GMT  
		Size: 3.1 MB (3109759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab9a530252badfbee808cf85008dd32ff3d0c31c454dd82cc34a1b70373ba7bc`  
		Last Modified: Fri, 14 Nov 2025 03:27:56 GMT  
		Size: 19.2 KB (19200 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c33cb8d31bfaa0f50ed8728e37f7e2d6f3e65869e050faad74373d1975b01fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238948271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85665f8b29cbd14097317a9073e211d35b68f929be903b8829d8b0922ef8427e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:17:52 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:17:52 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:17:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 18 Nov 2025 05:17:52 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 18 Nov 2025 05:17:52 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 18 Nov 2025 05:17:52 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 18 Nov 2025 05:17:52 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 18 Nov 2025 05:17:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 18 Nov 2025 05:17:52 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 18 Nov 2025 05:17:52 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:17:52 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 18 Nov 2025 05:17:52 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 18 Nov 2025 05:17:52 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 18 Nov 2025 05:17:52 GMT
ARG USER_HOME_DIR=/root
# Tue, 18 Nov 2025 05:17:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 18 Nov 2025 05:17:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 18 Nov 2025 05:17:52 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90cf59eaeb8b384a45d66ec2f748c647266069475bf7d0dadcfe6c6de1a16c1`  
		Last Modified: Tue, 18 Nov 2025 07:48:06 GMT  
		Size: 199.6 MB (199566025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eef4b7a21a7e1a62b134b8abd254b506424ef745d059616d73957f4185b3f3b`  
		Last Modified: Tue, 18 Nov 2025 05:18:24 GMT  
		Size: 9.2 MB (9242603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54094b9995e5f52f64115ad3a6970b35c104fea81b3947cf63e114844b50b307`  
		Last Modified: Tue, 18 Nov 2025 05:18:22 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69eb70eb07e606138117811693d5d5cd1c7f3947b86c2dfde1e04d1638ab0b51`  
		Last Modified: Tue, 18 Nov 2025 05:18:22 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian` - unknown; unknown

```console
$ docker pull maven@sha256:7e1e2370c85d490404953ef2bfe58795ef4f61e8ccdd70752b1013b46aa42933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8cdd04d942971f809a48734f74ce873d689d03f52bd0fbdff10330647d0e2a`

```dockerfile
```

-	Layers:
	-	`sha256:77afe96e69712788f8db22c7bfdaa414448916ed94dc7fe9dfc72cec8b6744f0`  
		Last Modified: Tue, 18 Nov 2025 06:28:59 GMT  
		Size: 3.1 MB (3110053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03471e34661e84d4012a6da735b4a957b22385571aa791379509190a3fcc2172`  
		Last Modified: Tue, 18 Nov 2025 06:29:00 GMT  
		Size: 19.4 KB (19367 bytes)  
		MIME: application/vnd.in-toto+json
