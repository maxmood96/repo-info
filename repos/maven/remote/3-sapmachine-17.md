## `maven:3-sapmachine-17`

```console
$ docker pull maven@sha256:fbae487c47a853256905c6c3df1abb5711ef2cab801909603df5852044f49496
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine-17` - linux; amd64

```console
$ docker pull maven@sha256:14e00f8de349972b7714b8b720bc3f9a45e47307ebcea9f6a7c8b783d9b6364c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264532082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db13de68099c666e7c663c9b896b01993069bd4890be1fe68a3fc66e6d52915f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
# Sun, 22 Jun 2025 10:21:55 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ARG MAVEN_VERSION=3.9.10
# Sun, 22 Jun 2025 10:21:55 GMT
ARG USER_HOME_DIR=/root
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 22 Jun 2025 10:21:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 22 Jun 2025 10:21:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9ed21bf16d010109638fdb04fb6f85601b38565ea6e4713380e1c10f66d362`  
		Last Modified: Tue, 03 Jun 2025 13:36:10 GMT  
		Size: 200.4 MB (200403912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd454503be68032a088dc3f8784f16f9c113e9c0e76a3ece4f26f10ffa60981`  
		Last Modified: Mon, 23 Jun 2025 17:31:16 GMT  
		Size: 25.5 MB (25458390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b607a21069f4cd6629422a0a3c88a6c5199280c1cb9b222d6a9e0faae06d746`  
		Last Modified: Mon, 23 Jun 2025 17:31:12 GMT  
		Size: 9.0 MB (8953407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54bde67fc469f67b5c801fa20f3e4a95ce332c549a4de0579fb48bd77a6e401`  
		Last Modified: Mon, 23 Jun 2025 17:31:11 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42c303eb0abadd04377798b2841ed17a15efe7f214b2a2281b2346c9587fb00`  
		Last Modified: Mon, 23 Jun 2025 17:31:12 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-17` - unknown; unknown

```console
$ docker pull maven@sha256:1e5010f99fc5ca9b39a60849a23b3827dc7907981aa3b64e384f9fd95ac7a54d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4332051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e16117981f3dc77cc6d356a9ca889de2ce442aac831b066d2669fc1b842d03`

```dockerfile
```

-	Layers:
	-	`sha256:2c4d00e4a5ccb1136505787d454a39ac22de65e4d906644c1d80d4167173db18`  
		Last Modified: Mon, 23 Jun 2025 20:34:17 GMT  
		Size: 4.3 MB (4315505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:659a1ec4eb6895cc5a34bee31fcc18e8e65a21e3f33f334c8a4e497cb88b33e0`  
		Last Modified: Mon, 23 Jun 2025 20:34:18 GMT  
		Size: 16.5 KB (16546 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:8fdcccdd9d97f0a2053b46fa8cc67a6cf85c068062eb1acdbfb5ca5002619757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.5 MB (262497669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf5f12e8a28e54d3b1289f451a9811ad11d980e804d1f095e9aa8ca790f4a86`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
# Sun, 22 Jun 2025 10:21:55 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ARG MAVEN_VERSION=3.9.10
# Sun, 22 Jun 2025 10:21:55 GMT
ARG USER_HOME_DIR=/root
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 22 Jun 2025 10:21:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 22 Jun 2025 10:21:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78af24ea68b2c2dbda63a9cc98e6286719db1bcb545d1b053b0dd9faeb870ed1`  
		Last Modified: Tue, 03 Jun 2025 14:40:33 GMT  
		Size: 199.2 MB (199159865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4250c66c1c5ed0028933fc69f7cdcd45c2423cd4cbec77b7e80bfe57dd6540`  
		Last Modified: Mon, 23 Jun 2025 17:48:45 GMT  
		Size: 25.5 MB (25531460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3515ebc1ff92926daa7c645857be9f1cd297581ab401506a4e1aebe7d0d3a166`  
		Last Modified: Mon, 23 Jun 2025 17:48:37 GMT  
		Size: 9.0 MB (8953406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e39ce04d9c950188754bf8e1881d72fcb2ebe61f20bf2c7638ff1bbb2cb45c4`  
		Last Modified: Mon, 23 Jun 2025 17:48:40 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c8880d518649e7d6d6508abd657f0f816b9e9c1eeeac4deb28e5b5b03f2033`  
		Last Modified: Mon, 23 Jun 2025 17:48:39 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-17` - unknown; unknown

```console
$ docker pull maven@sha256:ec24a248e627d2b4bc7076d9b7f426e9d4df20ee2122267fd2ede3da2f1d1cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4338706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0e54f9ba530763fb0fa3fc7eb41cef41ffced90ab51b45d4435ce55242d7360`

```dockerfile
```

-	Layers:
	-	`sha256:45714f81669e0586d7998ea834f366790230decbe9f0c9c133bff6c5b2c4e5e2`  
		Last Modified: Mon, 23 Jun 2025 20:34:23 GMT  
		Size: 4.3 MB (4322027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eae925d6f097a944299fd937aa8f411fc2d41710e8ddad9adb34b465043c8944`  
		Last Modified: Mon, 23 Jun 2025 20:34:24 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-17` - linux; ppc64le

```console
$ docker pull maven@sha256:30d7eb5b1025f12261738f8d6b25b4cffda94707ba50b5bd583cc2611462c9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.9 MB (274855766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c552ce46bb1460e4592c611fd27072250854bb75cbdd553d60c36b2f5bbc458e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
# Sun, 22 Jun 2025 10:21:55 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ARG MAVEN_VERSION=3.9.10
# Sun, 22 Jun 2025 10:21:55 GMT
ARG USER_HOME_DIR=/root
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 22 Jun 2025 10:21:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 22 Jun 2025 10:21:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74596d1c35eb463e5bc9e393d197b58daf08688bf438293ca27d2070bfeda15`  
		Last Modified: Tue, 03 Jun 2025 17:21:53 GMT  
		Size: 201.6 MB (201591821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b983a5795917b71e87def655307c9d02bfe56ba62a427ccaa49cab1fabc09220`  
		Last Modified: Tue, 24 Jun 2025 03:57:54 GMT  
		Size: 30.0 MB (29984290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4de441e2bd5054c6320c626f95317e86469048739ab17ae19f0a029d0fe10b`  
		Last Modified: Tue, 24 Jun 2025 03:57:45 GMT  
		Size: 9.0 MB (8953405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a4764e026772ae5069d34159901facedba72defe2fc8c5e3c47d4bf37c1bae`  
		Last Modified: Tue, 24 Jun 2025 03:57:41 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e3bd1ea7ed8f088529d5799c7ffda49a543c0f1251f6f406220e94037285fa`  
		Last Modified: Tue, 24 Jun 2025 03:57:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-17` - unknown; unknown

```console
$ docker pull maven@sha256:9250cb02d9047fbaafdd99b5c32425863203c15e6dabc75defd1ca0ce2004aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4337129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d6df1e31f864a9d42db957c89a5b9bd05a73de0cc10308856de12c04948c53`

```dockerfile
```

-	Layers:
	-	`sha256:c0eb0bc2598c21027704c2c34b5b21ee2a3008df6acbf5e6175f46da865d24b6`  
		Last Modified: Mon, 23 Jun 2025 20:34:28 GMT  
		Size: 4.3 MB (4320533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edd81f224c5d1dde816819a142cf6d33dfadcdc8eca45ac67e6ca2ac2ec2256a`  
		Last Modified: Mon, 23 Jun 2025 20:34:29 GMT  
		Size: 16.6 KB (16596 bytes)  
		MIME: application/vnd.in-toto+json
