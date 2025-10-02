## `maven:3-sapmachine`

```console
$ docker pull maven@sha256:5daa12d24b05cb681f6f2bb534f4dfb1e1a19fbf8f8805bd4cecdce8ad8e9b01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine` - linux; amd64

```console
$ docker pull maven@sha256:d68473139a1d151a05edd5ac5fb168683bf79cc5713b03219656b6f980f0d172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300459685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f427c7abfbb7f9d73984274f09a284fa3345e47bc2248cc0d41cd6696c21f8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
# Fri, 19 Sep 2025 20:27:44 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 19 Sep 2025 20:27:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 19 Sep 2025 20:27:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 19 Sep 2025 20:27:44 GMT
ARG USER_HOME_DIR=/root
# Fri, 19 Sep 2025 20:27:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 19 Sep 2025 20:27:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 19 Sep 2025 20:27:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65354830e4ea032cf75d8046f111e56c89817184619b98ccd2edbcc3b83df04`  
		Last Modified: Thu, 02 Oct 2025 09:23:43 GMT  
		Size: 236.0 MB (236031138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb57fcaadf0916ba754106a003e2fcf300d1420f7d8aebe2da938ed50bcb6fa2`  
		Last Modified: Thu, 02 Oct 2025 12:27:08 GMT  
		Size: 25.5 MB (25461916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c67a51ebd45695e1cb2c4fc7c317daa8aa392768b0125f52d1d06815a68ce8`  
		Last Modified: Thu, 02 Oct 2025 12:27:06 GMT  
		Size: 9.2 MB (9242584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d9125564833e8d4b487e6367869bb6a46a1a4d23673024f6a4405756c1bcdb`  
		Last Modified: Thu, 02 Oct 2025 12:27:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa641098cced43f0c62dfd8b87f83e18ed1bfaf37d36f52bd6d4c3a06493812`  
		Last Modified: Thu, 02 Oct 2025 12:27:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:db22c59bc317d315239e18b584ff3a83c836ac908ff782eb91fa83251264c067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4330367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdad3eb521008e6c578aaaa79c9878721444559302afbed5a98fb5243bb86074`

```dockerfile
```

-	Layers:
	-	`sha256:84371b2178db9e39edcdbc523cfa4e2556a69e3b5b270a9a612a3461fca3e33f`  
		Last Modified: Thu, 02 Oct 2025 14:31:59 GMT  
		Size: 4.3 MB (4312579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c58fa17d8eeee44165a66a21d4b309d43d74d36dd5fa214b2f40a589197a7488`  
		Last Modified: Thu, 02 Oct 2025 14:32:00 GMT  
		Size: 17.8 KB (17788 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:9c87a5188b2f01331863dcf2bc3dd0bc2d32b9d10886a82083f177b269d57525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297287833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6584f31d0d2ec5727404fd56b504651c11e5fe4e9b45daf157ab46fddfe32d12`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
# Fri, 19 Sep 2025 20:27:44 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 19 Sep 2025 20:27:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 19 Sep 2025 20:27:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 19 Sep 2025 20:27:44 GMT
ARG USER_HOME_DIR=/root
# Fri, 19 Sep 2025 20:27:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 19 Sep 2025 20:27:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 19 Sep 2025 20:27:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526072f9bf013cc544e774f4dbe054ff1f5fbaf55f176df5adc7181f772276a`  
		Last Modified: Thu, 02 Oct 2025 03:34:30 GMT  
		Size: 233.7 MB (233650164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3774b815a309055a1c80267b3bbd5639a5e90b30e37f304f529b8d294eb39d97`  
		Last Modified: Thu, 02 Oct 2025 03:34:21 GMT  
		Size: 25.5 MB (25532490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acde6d8d2f5c954267f411607eaa5988622e008213e4dfed28b40d8773677eac`  
		Last Modified: Thu, 02 Oct 2025 03:34:20 GMT  
		Size: 9.2 MB (9242567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df8edbfd9ec445b4af0358d5b138622c1bf13d37d6320f3e17569b3a9a2b10b`  
		Last Modified: Thu, 02 Oct 2025 03:34:19 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3e5b6102fe862e83e4b54561f47c7795b0d4ccd927dc7658d9924b3786d76a`  
		Last Modified: Thu, 02 Oct 2025 03:34:19 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:7e145611593dfb5b554a0f90117a5ac95c005bd58e8eef359d35bec4f201a07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4337115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3df825b87aa7ed40bf37e5f52a39577887b46fcb75989d17f49b066810805c`

```dockerfile
```

-	Layers:
	-	`sha256:e43203d190eb19075d2a48b553e84c2f0559f72c5e7dc83fc7f42f44cb10d23e`  
		Last Modified: Thu, 02 Oct 2025 05:31:29 GMT  
		Size: 4.3 MB (4319146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3381022c186d4b670ce49dd0d8f0d70a86e29927a25c3d2389895110e80d71ad`  
		Last Modified: Thu, 02 Oct 2025 05:31:30 GMT  
		Size: 18.0 KB (17969 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine` - linux; ppc64le

```console
$ docker pull maven@sha256:f393cc36decae24ee4f26e306ce05d922cacc3c4cfa556a2a405c5c66b2faaa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.0 MB (308028639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60159928aa495c761435fd64babd7c75f3e4c058766234e08cdd33e82eaeabf2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 10 Sep 2025 05:44:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:44:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:44:36 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Wed, 10 Sep 2025 05:44:36 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
# Fri, 19 Sep 2025 20:27:44 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 19 Sep 2025 20:27:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 19 Sep 2025 20:27:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 19 Sep 2025 20:27:44 GMT
ARG USER_HOME_DIR=/root
# Fri, 19 Sep 2025 20:27:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 19 Sep 2025 20:27:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 19 Sep 2025 20:27:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af7e0dcc16d048eb7780a560deb0e700e5bef5dd9d664618c27b53acfa0d586`  
		Last Modified: Wed, 17 Sep 2025 17:36:21 GMT  
		Size: 234.5 MB (234496455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20159b92bbcd1f5cf473e9ca042abd8d0427a51cc919e0246acdd5baf1ac93a`  
		Last Modified: Mon, 22 Sep 2025 17:14:32 GMT  
		Size: 30.0 MB (29985422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7690cccfdf0738aec06a4ddac8ee2bf3745f272478e7cd51c446d1596c2369e`  
		Last Modified: Mon, 22 Sep 2025 17:14:21 GMT  
		Size: 9.2 MB (9242595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7287d3c0431bd2ad4f97f0a693114a2932c51bdfb3ec02a0ce7b534e3bc3ea`  
		Last Modified: Mon, 22 Sep 2025 17:14:22 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a7a29c22807025c679fd78b5fc0e11db7d36332229b78d318f80b6ef3ff142`  
		Last Modified: Mon, 22 Sep 2025 17:14:22 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:9be9b099e8d069dc0e3b410a83acc86d345f4ae34d897ade37b7e17a1ec72ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4326327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549c9d2c34343139e5d68c0b4894fe3a8b454dfff5616f1c802a24b79cfb0bf5`

```dockerfile
```

-	Layers:
	-	`sha256:b2d87458cc85411c3cb357416eb4cf87f936d83bd981edc4ddbe2de7b30a48e5`  
		Last Modified: Mon, 22 Sep 2025 20:27:56 GMT  
		Size: 4.3 MB (4309731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13f2b703ba08d8b82547e8bf69137ec62de0dd50c4de7549dfd9f602753a9cd7`  
		Last Modified: Mon, 22 Sep 2025 20:27:57 GMT  
		Size: 16.6 KB (16596 bytes)  
		MIME: application/vnd.in-toto+json
