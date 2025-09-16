## `maven:3-sapmachine-24`

```console
$ docker pull maven@sha256:81392d4194a726f1cc860eb71dd7bf2b150396cb6b6590d68212286ff3670872
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine-24` - linux; amd64

```console
$ docker pull maven@sha256:b53fd5895a5dd11fa84216a0723309ceef8dc6ceb09e37269cb96b81d7e97238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 MB (296885749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf54e69635a0bccb64cfc764379eebc032d046b6e66f48d687723f8350aee1e1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f43c5ad22e047eb3d4d8d99db6279185802accee08f3780715801d579ee850`  
		Last Modified: Tue, 16 Sep 2025 00:17:58 GMT  
		Size: 232.5 MB (232456780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cba75c631b1cdcfc78466afd64249699a6cc48564bc00da8b9d39d12791db31`  
		Last Modified: Tue, 16 Sep 2025 00:18:47 GMT  
		Size: 25.5 MB (25461910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21d3b3a32b1a54d232e5904a8bc7167273cf1235637fdd356d4e63677ad8653`  
		Last Modified: Tue, 16 Sep 2025 00:18:45 GMT  
		Size: 9.2 MB (9242574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c97101fee8052aa5c8b9c263fec2e7f0e40ae75cbfef65771b556ef31224a89`  
		Last Modified: Tue, 16 Sep 2025 00:18:45 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3c3feee2a115b2f798ad82d1f7ddc5228fda9d1b53de031c3187d65f61db47`  
		Last Modified: Tue, 16 Sep 2025 00:18:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-24` - unknown; unknown

```console
$ docker pull maven@sha256:3aa35f8f64d51bde32f5bf4efa0d5b305fc6263d1485524d924e9b7fe6ad714f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3191108e8a4ba5f0c04826842cbf823d28a533f1d2b1c87aea3cc21beea107`

```dockerfile
```

-	Layers:
	-	`sha256:d7c4bfe90f370caa4251d26543bb2c58437865f44826ab2404e22322b061dbde`  
		Last Modified: Tue, 16 Sep 2025 02:33:13 GMT  
		Size: 4.3 MB (4310703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be6fce678ab28c8796604701b2b9d442b8725fadeddfddf4952c065af1f3ee09`  
		Last Modified: Tue, 16 Sep 2025 02:33:14 GMT  
		Size: 16.5 KB (16546 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-24` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:787282bffe116f2e5b0147c57915f70226958d7b0af55ac48a9f5064672133ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.0 MB (294038678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64cb43ae6966c50d38c4c8c5dedfd28d502c7361ad4f4f2cc04f1ee6c2d998a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5757bea5988e31f35dca2f6b5174875f29df13bc4d7dc6f42569da99c46f30`  
		Last Modified: Tue, 16 Sep 2025 00:17:16 GMT  
		Size: 230.4 MB (230401344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04e8863e33f47263dc3593274db979a43f27817c28b2450fb0c5dc218fbfb10`  
		Last Modified: Tue, 16 Sep 2025 00:17:58 GMT  
		Size: 25.5 MB (25532401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fc6e610db77ec21a1cbde3abbfbf4388e468ff11a3f3d3c981a3e5fa8c5cee`  
		Last Modified: Tue, 16 Sep 2025 00:56:38 GMT  
		Size: 9.2 MB (9242578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c82f1e84f4d3e6434209378e08f95b29485b27d2f4ef9e26b616dfa00b451fd`  
		Last Modified: Tue, 16 Sep 2025 00:56:38 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb50119d6ba81a160926b35555ee6e40cbb6a4a650ba93a24ac38bef13b4db85`  
		Last Modified: Tue, 16 Sep 2025 00:56:37 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-24` - unknown; unknown

```console
$ docker pull maven@sha256:d368935731ab71acc25d79c3e36c482d62e6666bae5cc4683a1591667d92252f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4333901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f978506fdbddee05e3619223911e0d5f054dd7b505c8ef9bdba592b1b484cb04`

```dockerfile
```

-	Layers:
	-	`sha256:f3d15401bfa33b6c1285ca417e53e10c7df301e3443d8c8ddaa6938bd7a92c1c`  
		Last Modified: Tue, 16 Sep 2025 02:33:18 GMT  
		Size: 4.3 MB (4317222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28677a824f700311f2f9d68b7f78fabb2e28a47304036df161a6c8da62e95d6c`  
		Last Modified: Tue, 16 Sep 2025 02:33:19 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-24` - linux; ppc64le

```console
$ docker pull maven@sha256:e15f9b19180d04177af1ab9c1413cece9f7d898b32de84cb37c97b2d07508821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.9 MB (306890289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58156287cda78a264b0b7b9f45b1f26fdc4e9a5b7011f7537059cbaa639bffc3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2abb1f24e2eefeaf4a66364d16532336fa01b9d3de85a6d97cf96d2b39aafd7`  
		Last Modified: Tue, 02 Sep 2025 14:50:57 GMT  
		Size: 233.3 MB (233331441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3864a025ab0c0318e41c423490eaf6269284a5141d2ec99d6661dddcc3f98bad`  
		Last Modified: Tue, 02 Sep 2025 12:15:48 GMT  
		Size: 30.0 MB (29985681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04603c322baa12b2da725348285dbc8f8f3f3dfca0fa92e60dd6130e507787f4`  
		Last Modified: Tue, 02 Sep 2025 12:15:43 GMT  
		Size: 9.2 MB (9242596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd7250853d0f5c0606c484c4704eeb6c54ac4f5a6bcecda1c71220ae8ddf423`  
		Last Modified: Tue, 02 Sep 2025 12:15:43 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15878abfa000cbe92e92b02a626ccc304799136bf62d832c936bec0c294ff7f8`  
		Last Modified: Tue, 02 Sep 2025 12:15:43 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-24` - unknown; unknown

```console
$ docker pull maven@sha256:958e3317ef75c59cd1155921f10a774a3600a6b6ffa94b2aa1b990c5950e6c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4325689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20e2191e1d2ce0e6dd4aaa28da77a61d350cb3ff5fa98c2820e07117bcb3256`

```dockerfile
```

-	Layers:
	-	`sha256:8be41e85d92ec420dea37788d3dae2d4bf9958d0681a6fb86c20d566440fd689`  
		Last Modified: Tue, 02 Sep 2025 14:30:47 GMT  
		Size: 4.3 MB (4309093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84604a2a4ef30ed1992ef8ebcdbe682df57adbc2125af2f00cb2f1e899e1bbc9`  
		Last Modified: Tue, 02 Sep 2025 14:30:47 GMT  
		Size: 16.6 KB (16596 bytes)  
		MIME: application/vnd.in-toto+json
