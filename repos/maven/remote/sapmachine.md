## `maven:sapmachine`

```console
$ docker pull maven@sha256:d01b04ed2672b70b726e54238e27f7a470913692a2ba8c207f8c68506e7b9bd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:sapmachine` - linux; amd64

```console
$ docker pull maven@sha256:9583658ef0311cc920d04c9b7a548f8baecf3029aeb6d4742d2647c7aeac8dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.3 MB (288349097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699042a5eea447a4d2065ec79bb02068c9683d900915c0c7a153748f75b24551`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 20:02:43 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:02:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 20:02:43 GMT
CMD ["jshell"]
# Thu, 05 Feb 2026 23:31:37 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 23:31:37 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 05 Feb 2026 23:31:37 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:31:37 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:31:37 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 05 Feb 2026 23:31:37 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 05 Feb 2026 23:31:37 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 05 Feb 2026 23:31:37 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 23:31:37 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 05 Feb 2026 23:31:37 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 05 Feb 2026 23:31:37 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 05 Feb 2026 23:31:37 GMT
ARG USER_HOME_DIR=/root
# Thu, 05 Feb 2026 23:31:37 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 05 Feb 2026 23:31:37 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 05 Feb 2026 23:31:37 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166a188c954e02cb107f6f7af69649f2eb170ffdf79a4a1df2f2e7dfe512ea7f`  
		Last Modified: Wed, 21 Jan 2026 20:03:04 GMT  
		Size: 221.4 MB (221449061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd0d961527b23078e42fcee8105db8699df3d522b39b130585a8d6df5c9f361`  
		Last Modified: Thu, 05 Feb 2026 23:31:51 GMT  
		Size: 27.9 MB (27860737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b620950b10f96a93ba1a43648b8ebfd4eb89aef081b6b87abefe4949ff49f4a4`  
		Last Modified: Thu, 05 Feb 2026 23:31:51 GMT  
		Size: 9.3 MB (9312251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727a09930a7b99dde9cdceccd4d116c1944cd619ccfd317a7727855142689797`  
		Last Modified: Thu, 05 Feb 2026 23:31:51 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92af6cda8564a719a6112935f55439761535323328608db8c60994628d41cdae`  
		Last Modified: Thu, 05 Feb 2026 23:31:51 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:9283ac093ebfb545bbb5b5241cba0d3519087b1786a18807b94fb26f228b2490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4330805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd4207848f9b74f04efd46e1ec30415e03369f62d181094041112c16e55536d`

```dockerfile
```

-	Layers:
	-	`sha256:bd332a9d86f71c6dff1d982f30d46520b29aeee5cfda7ced850b3f87e9e8f3bc`  
		Last Modified: Thu, 05 Feb 2026 23:31:51 GMT  
		Size: 4.3 MB (4313060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e12dc7b2e711d024b694c8d890d77f8e6b30bc18d616d25e5c15818934547e99`  
		Last Modified: Thu, 05 Feb 2026 23:31:50 GMT  
		Size: 17.7 KB (17745 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:sapmachine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5d58875b8d29aef373d5f671bb8f9eae00e594ada19ef97deece6e51cc310722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285192497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a125180606eb512b6f51791767acf532b634ae5b0608d341c6677e4fedef4b50`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 20:05:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:05:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 20:05:35 GMT
CMD ["jshell"]
# Thu, 05 Feb 2026 23:42:31 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 23:42:31 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 05 Feb 2026 23:42:31 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:42:31 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:42:31 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 05 Feb 2026 23:42:31 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 05 Feb 2026 23:42:31 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 05 Feb 2026 23:42:31 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 23:42:31 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 05 Feb 2026 23:42:31 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 05 Feb 2026 23:42:31 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 05 Feb 2026 23:42:31 GMT
ARG USER_HOME_DIR=/root
# Thu, 05 Feb 2026 23:42:31 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 05 Feb 2026 23:42:31 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 05 Feb 2026 23:42:31 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc36bb5ef69434c4feef5be6306492cf245860d3dded017911c99182ab4f9b2`  
		Last Modified: Wed, 21 Jan 2026 20:09:00 GMT  
		Size: 219.3 MB (219263347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e35f3e36d8e95db6c67159d1417f228be1fd0e452ed7806030b878dd03c3d2`  
		Last Modified: Thu, 05 Feb 2026 23:42:45 GMT  
		Size: 27.8 MB (27752037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2362953354ed677805a40b5f0e5770ef6b6b8d67cf397d9c0cd13be67ee1ef`  
		Last Modified: Thu, 05 Feb 2026 23:42:45 GMT  
		Size: 9.3 MB (9312251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b16a1358369c7de55afec9e88c24831d83c5ffb3b41790a7f9ef4b34343e51`  
		Last Modified: Thu, 05 Feb 2026 23:42:44 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4ab7897883383b35f7afbfadd01f45bb23464711a654e86e43d3cb022fa6b3`  
		Last Modified: Thu, 05 Feb 2026 23:42:45 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:1f177977beb58c2a39cb7641b99bc1722fb7f2f8e7bbd5701f65f190d8f37d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4337553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c869c79fbbbe1d09ee8dc2de8efdb9f39fe724f863a219fafec9c9d68830b98`

```dockerfile
```

-	Layers:
	-	`sha256:3e1c4441f42f78342b5a4d1f7a4b53d17092b1bb61f1ee541c4284423a85de6c`  
		Last Modified: Thu, 05 Feb 2026 23:42:45 GMT  
		Size: 4.3 MB (4319627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e6bcdbe571acc8004128e2d0899ccbe117cf6cc9e350de84d4cdc2e6a78a00`  
		Last Modified: Thu, 05 Feb 2026 23:42:44 GMT  
		Size: 17.9 KB (17926 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:sapmachine` - linux; ppc64le

```console
$ docker pull maven@sha256:5589d9937749c49069399a764b5cd76bd40562ac50f62d8cf8a8282a8817c428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298605487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8d7ceeeae78be92c6cc986244cce22734f8b1c5776c9414f3b11fb7ce7782e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 21:08:50 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 21:08:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 21 Jan 2026 21:08:50 GMT
CMD ["jshell"]
# Fri, 06 Feb 2026 01:26:58 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Feb 2026 01:26:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 06 Feb 2026 01:26:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 06 Feb 2026 01:26:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 06 Feb 2026 01:26:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 06 Feb 2026 01:26:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 06 Feb 2026 01:26:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 06 Feb 2026 01:27:02 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 06 Feb 2026 01:27:03 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 06 Feb 2026 01:27:04 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 06 Feb 2026 01:27:04 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 06 Feb 2026 01:27:04 GMT
ARG USER_HOME_DIR=/root
# Fri, 06 Feb 2026 01:27:04 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 06 Feb 2026 01:27:04 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 06 Feb 2026 01:27:04 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9785c838943c455dacbd1904b35930cbf043e7af6e17b5ee6873ee451b8864e`  
		Last Modified: Wed, 21 Jan 2026 21:09:39 GMT  
		Size: 222.4 MB (222367616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3791dd3f1bac41713f6866afbfd77af90b8cfd87fcf6d4b5f8c1a35703f6252c`  
		Last Modified: Fri, 06 Feb 2026 01:27:46 GMT  
		Size: 32.6 MB (32618430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9456d41760c0c6be36095d13223233c5faf5b61a2eb6ce156a149488d36bb8e4`  
		Last Modified: Fri, 06 Feb 2026 01:27:45 GMT  
		Size: 9.3 MB (9312246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40f929f607ff053e55058a644710c28747f9477601e8dadd9900b38c8674f87`  
		Last Modified: Fri, 06 Feb 2026 01:27:44 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29a2c7300ef00d6c70a19297124449b95cb1f3ee76debb77cb8c53fd6c91ede`  
		Last Modified: Fri, 06 Feb 2026 01:27:44 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:b45b7614070909952684b5d946a76b0af33f8a9d90fa5a476b1298b78f8120da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4330714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15a6fe6102de17d7bd8eaf7e0fbd1666571e61855b7d16288fedb2d61f394ef`

```dockerfile
```

-	Layers:
	-	`sha256:83f663f76c1c0232e454e576cfda3e9699c3618d020bbcef05fbec4b02807415`  
		Last Modified: Fri, 06 Feb 2026 01:27:45 GMT  
		Size: 4.3 MB (4312895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b108967767766d3c83d2af4f3b050ebf0d3b8ff7b6796a557aac3d4f6009e75e`  
		Last Modified: Fri, 06 Feb 2026 01:27:44 GMT  
		Size: 17.8 KB (17819 bytes)  
		MIME: application/vnd.in-toto+json
