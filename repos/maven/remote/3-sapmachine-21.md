## `maven:3-sapmachine-21`

```console
$ docker pull maven@sha256:ec903c9e6a85c137df4d7434bc059b4ca13b704a394ad741c8c34aa0aa6660f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine-21` - linux; amd64

```console
$ docker pull maven@sha256:0b6fe0296aea4f0e1641f377789a70770bc4b5c7bd4ddb19f078bb04f81aa5ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.0 MB (281010638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3241d19973cf90dcf342fe6cfd21395109fcf4b3c6647bf24cf78d902e44613b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:16:50 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:16:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 15 Apr 2026 20:16:50 GMT
CMD ["jshell"]
# Tue, 21 Apr 2026 18:13:21 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 18:13:21 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:13:21 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:13:21 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:13:21 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:13:21 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:13:21 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:13:21 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:13:21 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:13:21 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:13:21 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:13:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:13:21 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07edda880038f14faf7bdf8c083af072ba39fbfe944ed22b60b243c755aadca`  
		Last Modified: Wed, 15 Apr 2026 20:17:14 GMT  
		Size: 216.5 MB (216494920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc3bb0a384425fde0ba8ad203115904784e73e589700083b5b2a975297f6cf0`  
		Last Modified: Tue, 21 Apr 2026 18:13:35 GMT  
		Size: 25.5 MB (25469532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc67294b14f3d1061cad5d4443ac082601847f3aadc16c8d8869129068135d34`  
		Last Modified: Tue, 21 Apr 2026 18:13:35 GMT  
		Size: 9.3 MB (9312203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e25db1f7cc0f45dd862031da4a59202af0d9e3a83b47a947c91ed6f14d1531`  
		Last Modified: Tue, 21 Apr 2026 18:13:34 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e139879d180612a75b371603f27903fe3a7419050cca2d7833eb68a902e07c25`  
		Last Modified: Tue, 21 Apr 2026 18:13:34 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:f324b02526b3e27a34b77af035868f9dd5f732aca4635e2950f1737098895d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4337077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f144aac653057c88a15ba381dcc2a2b6f063d5cc9b23b8db215826913e8e46f`

```dockerfile
```

-	Layers:
	-	`sha256:8d930a995798602319a781d796ecbed77f260f231ef2bc92652ff80858d99f07`  
		Last Modified: Tue, 21 Apr 2026 18:13:35 GMT  
		Size: 4.3 MB (4322412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6af220f36cebe9e703a6db24f62f6bb02624284dc98c245f32ecd50fb498e5da`  
		Last Modified: Tue, 21 Apr 2026 18:13:34 GMT  
		Size: 14.7 KB (14665 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:46f13beb0601cea4d5b80cab3472f3a58b7526dd6664f319c2e1996f15db52ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278479964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:864a8f8e3a83e8c27e2a092b1c5d6306ed0d7d14f063732f141f2d944efc6a0b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:08:59 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:08:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 15 Apr 2026 21:08:59 GMT
CMD ["jshell"]
# Tue, 21 Apr 2026 18:13:04 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 18:13:04 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:13:04 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:13:04 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:13:04 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:13:04 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:13:04 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:13:04 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:13:04 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:13:04 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:13:04 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:13:04 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:13:04 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1f01acc0dd797cbe5018cfd7b43708d4cc44f7d615696571ae019ac02a084d`  
		Last Modified: Wed, 15 Apr 2026 21:09:24 GMT  
		Size: 214.8 MB (214757430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a571e4c2e91bf4c501aee0996e85ed0f9b1463ddc996fab4a365b11f86cc437d`  
		Last Modified: Tue, 21 Apr 2026 18:13:18 GMT  
		Size: 25.5 MB (25533488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea99001a26116ccd0903b009cc1ff2f8156d47cc6f7b90da0384c9f83467660d`  
		Last Modified: Tue, 21 Apr 2026 18:13:17 GMT  
		Size: 9.3 MB (9312254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995bb57ca4f47fdeac7ec67b9c759b87e4d9a5065f0fa05e13be165e6122f7aa`  
		Last Modified: Tue, 21 Apr 2026 18:13:17 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ac49373a6d039600e1c8215b0b5fec9e9daf4aa4724945194a1c675598edc3`  
		Last Modified: Tue, 21 Apr 2026 18:13:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:4cd59d5da604d25787b75792a977cfa95f0054b1fdc2c7d50403f2925e8c0759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4343732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7a81478cc3d6004dba873cfcfa155519b69cd9026f2202459c0ae688c8f959`

```dockerfile
```

-	Layers:
	-	`sha256:c3185245934affad633f30b8d8103e9f962bfbe9e83a148b64e7235423c0fb01`  
		Last Modified: Tue, 21 Apr 2026 18:13:17 GMT  
		Size: 4.3 MB (4328934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de222f852439ca18d5805948a5cca8867554fe37aaf82f71760296484055a5ed`  
		Last Modified: Tue, 21 Apr 2026 18:13:17 GMT  
		Size: 14.8 KB (14798 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-21` - linux; ppc64le

```console
$ docker pull maven@sha256:f4d82b5a26d2a5d0f03eaac6f2197253f37cc05037e237dc61ad0c41f84f7b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.2 MB (291172982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893009506b18090b46423708f984949bd47b057f83e8c93ff375883ebd0eedc6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 23:32:43 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:32:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 15 Apr 2026 23:32:43 GMT
CMD ["jshell"]
# Thu, 16 Apr 2026 05:46:00 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 18:13:10 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:13:10 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:13:10 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:13:10 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:13:10 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:13:10 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:13:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:13:12 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:13:12 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:13:12 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:13:12 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:13:12 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97c02826fb95077af5a8efe575b06d8b01b0a456d6b55eceb311bf0f7bd2fee`  
		Last Modified: Wed, 15 Apr 2026 23:33:24 GMT  
		Size: 217.5 MB (217549863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204fdb8261bb10a8c1af673d13b6aaec8a6661368d8036dac82c8ee532ddfe8d`  
		Last Modified: Thu, 16 Apr 2026 05:46:35 GMT  
		Size: 30.0 MB (29995685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc954dc98a2a2774f433364bb9b4f63bca7c8c930e69a086b238e933cdf17881`  
		Last Modified: Tue, 21 Apr 2026 18:13:37 GMT  
		Size: 9.3 MB (9312255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544975fe4064e67d4f5131afbc5911ae515376eedd2fe21e9d616c30530a7393`  
		Last Modified: Tue, 21 Apr 2026 18:13:37 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aac50b5cd22950eb69944516b5bf450fbc9e0ebe6bc81c123b99e26c6dd9f12`  
		Last Modified: Tue, 21 Apr 2026 18:13:36 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:41f32eb86aa4faa14e6a40039c4adf22b9ac5e993f9975a43e56bde377934a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4337556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f581fdafd80b7bda59d503262a8c4356707c4f5210153c7f2ff7f7b6cdbb9175`

```dockerfile
```

-	Layers:
	-	`sha256:5dd45e856fb660540ed552263a2d327c8e8fe57839707f28d711dcefd551a793`  
		Last Modified: Tue, 21 Apr 2026 18:13:37 GMT  
		Size: 4.3 MB (4322841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b35ca13272ac708516601e7b6a6a86716097cc990730fbff56e72f708f94448f`  
		Last Modified: Tue, 21 Apr 2026 18:13:36 GMT  
		Size: 14.7 KB (14715 bytes)  
		MIME: application/vnd.in-toto+json
