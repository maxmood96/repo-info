## `maven:3-amazoncorretto-21-debian`

```console
$ docker pull maven@sha256:4556ebf2b058c6e972c11f0c6db2f0ec8a5c6f713fcc76094af79fed6d3b6e58
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-debian` - linux; amd64

```console
$ docker pull maven@sha256:cb4d16d9dc6ce8cc1871911b82bb066fe0687d93fde2fafd09db3b18bbc67417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.1 MB (254139405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d5f6499cd7ee9e34cad52e6805ad12ade49efaf967bd2b1bbb6b1f1173edde`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Sat, 07 Dec 2024 17:04:44 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '18bbe2461ff5acb1212f95f3e41034c503460532de21c24f5f935359b2303586 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sat, 07 Dec 2024 17:04:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 07 Dec 2024 17:04:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 07 Dec 2024 17:04:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 07 Dec 2024 17:04:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 07 Dec 2024 17:04:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 07 Dec 2024 17:04:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
ARG MAVEN_VERSION=3.9.9
# Sat, 07 Dec 2024 17:04:44 GMT
ARG USER_HOME_DIR=/root
# Sat, 07 Dec 2024 17:04:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 07 Dec 2024 17:04:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 07 Dec 2024 17:04:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525b5720295b79ebac3495aaaf60011b11c43238507d7ce087160256bc6fd97b`  
		Last Modified: Mon, 09 Dec 2024 20:31:43 GMT  
		Size: 216.7 MB (216736348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f376598fd0822e8fefd016b6267bf83a0580985ef1e3b84440af37d48c489759`  
		Last Modified: Mon, 09 Dec 2024 20:31:40 GMT  
		Size: 9.2 MB (9170441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62da7db1ad086623eb81c8d1011258a160bcfcb884da2c7716d4f9efbea8418`  
		Last Modified: Mon, 09 Dec 2024 20:31:40 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386c25cf85a2c5a83d35ed983fa02b99f2d337dfb4ff7cc970877de045353c56`  
		Last Modified: Mon, 09 Dec 2024 20:31:40 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian` - unknown; unknown

```console
$ docker pull maven@sha256:d9e8e30534f70656e4562544b4d6d84e856880629608d77403486391f8d17559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3018510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c21ca3c550304d2dc7abfa58b2ebbe7e444c9a862e2ac29471d6f151ab0b28`

```dockerfile
```

-	Layers:
	-	`sha256:b0fac53a856d432f4b51bc1e8db81568555bb10a5320851f3e5399b5c4799075`  
		Last Modified: Mon, 09 Dec 2024 20:31:40 GMT  
		Size: 3.0 MB (2999297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b147d26747209b63652a4020fac924ee12582c000c43802972eefd67b5fcbf7e`  
		Last Modified: Mon, 09 Dec 2024 20:31:40 GMT  
		Size: 19.2 KB (19213 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:9f69f8478b9b5fd63bc4a8dbb4b4616d612b3a8179d979d53d4e9b5eb1204421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.7 MB (251701138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f2f0a7fe9e6bcba158f2b2a7bce47ab1666be298267678cb36cc7d009edb28`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6987027eb280447b52b9a8a4e5ca0e950e42cf6d17bf852cb495af796d277001`  
		Last Modified: Wed, 04 Dec 2024 01:09:53 GMT  
		Size: 214.5 MB (214470869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c2a291e552a4dfd411e5b044f12d52d093359cff3aa0b0c02af0d95d85427c`  
		Last Modified: Wed, 04 Dec 2024 01:09:48 GMT  
		Size: 9.2 MB (9170423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba8fe08be27407d045aaa2e17bf4b90f9ef0cc8a88839b8032907b6817f9957`  
		Last Modified: Wed, 04 Dec 2024 01:09:47 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6984caa9ea0f784380743fef8ab38dc2f363085b32034ab324ae18cb4671e4`  
		Last Modified: Wed, 04 Dec 2024 01:09:48 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian` - unknown; unknown

```console
$ docker pull maven@sha256:8e883fea8343b64867da8f37757b3d2dd0cfd0eb6fd66547908f0c99de9478a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3017806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77c8466c2a30e6ece8dbdeea59dbf20c000c1766610fe284b2c4f0ac198195b2`

```dockerfile
```

-	Layers:
	-	`sha256:c0a1b882a111839a2cf86fdd91fffa58026d07789016062e1ac95773121fbe5d`  
		Last Modified: Wed, 04 Dec 2024 01:09:48 GMT  
		Size: 3.0 MB (2998955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d170000fd82bab20f8cb2f6713d09cff893d0be31fd21f0f0f2417103eab30dd`  
		Last Modified: Wed, 04 Dec 2024 01:09:47 GMT  
		Size: 18.9 KB (18851 bytes)  
		MIME: application/vnd.in-toto+json
