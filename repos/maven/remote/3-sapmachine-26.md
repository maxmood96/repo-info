## `maven:3-sapmachine-26`

```console
$ docker pull maven@sha256:da19aed0d709eb13706959d0f2838f0316964fff3f211c9d561c22f7838f0aa3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine-26` - linux; amd64

```console
$ docker pull maven@sha256:5577bf1da859c76b3bcc3697cdc496085bc45ba347e5f61947a3f76f00ac069a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290873186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a3435830af842fca38977217836ae7d872efe9dac15aeea2d44a22a360f0f1`
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
# Wed, 15 Apr 2026 20:56:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:56:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 20:56:37 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 22:53:42 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:53:42 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 15 Apr 2026 22:53:42 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:53:42 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:53:42 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 15 Apr 2026 22:53:42 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Apr 2026 22:53:42 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 15 Apr 2026 22:53:42 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 22:53:42 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 15 Apr 2026 22:53:43 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 15 Apr 2026 22:53:43 GMT
ARG MAVEN_VERSION=3.9.14
# Wed, 15 Apr 2026 22:53:43 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Apr 2026 22:53:43 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Apr 2026 22:53:43 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Apr 2026 22:53:43 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d26625260ee574b572eae3ebd5a287cc9d461ddfec5b3eb5e0d1c772174a37`  
		Last Modified: Wed, 15 Apr 2026 20:57:02 GMT  
		Size: 226.4 MB (226358375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccd5535914759574bbc5461f121601190a345b1a9c120cf6a838b38487a50e5`  
		Last Modified: Wed, 15 Apr 2026 22:53:57 GMT  
		Size: 25.5 MB (25469619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98235a66d7142c59aab6b86fa930454316b9fc44c3c7743e65d6c7d1f787fdfc`  
		Last Modified: Wed, 15 Apr 2026 22:53:57 GMT  
		Size: 9.3 MB (9311177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a4f455e6a4b1d7191c33a5bb0168b1229f8b533a9e25e296e8bd20d354c3bd`  
		Last Modified: Wed, 15 Apr 2026 22:53:56 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059df6b08fd87050a905cc62632c49d5e8868b75aa2264735aa66cdf908b1e13`  
		Last Modified: Wed, 15 Apr 2026 22:53:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-26` - unknown; unknown

```console
$ docker pull maven@sha256:16254394e114f877ff2a38178a254cd51d2559010375e5eefa8b5b45ceb17728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4328918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9004f246b7e7b1cea1324c3d9c46570fa1b7748e1839c060c037f98311fd033b`

```dockerfile
```

-	Layers:
	-	`sha256:c20569d485bbbe47622b45994cbb80635b300df57d810b042fcfe39b1dc034a2`  
		Last Modified: Wed, 15 Apr 2026 22:53:56 GMT  
		Size: 4.3 MB (4311173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3c7116cb6cb4c7d55007e55411b341822f2be057362fc0e86043314aabb7d7a`  
		Last Modified: Wed, 15 Apr 2026 22:53:56 GMT  
		Size: 17.7 KB (17745 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-26` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:4e60cec9fedd05ed46f3d2153b6cdea5dbcefe6c0dc6aeb5747801ad0e2498f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.0 MB (287956741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8582b0f8a12a3bef1801d38a4a76dd02408ff98dddf99611154fd315920c53`
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
# Wed, 15 Apr 2026 21:06:07 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:06:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 21:06:07 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 23:19:51 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:19:51 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 15 Apr 2026 23:19:51 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 23:19:51 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 23:19:51 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 15 Apr 2026 23:19:51 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Apr 2026 23:19:51 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 15 Apr 2026 23:19:51 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 23:19:51 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 15 Apr 2026 23:19:51 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 15 Apr 2026 23:19:51 GMT
ARG MAVEN_VERSION=3.9.14
# Wed, 15 Apr 2026 23:19:51 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Apr 2026 23:19:51 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Apr 2026 23:19:51 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Apr 2026 23:19:51 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98811f1f7f1b906ec42bbfac81da12f49a09c9edd0bbea284b80e9cd8a244ab`  
		Last Modified: Wed, 15 Apr 2026 21:06:36 GMT  
		Size: 224.2 MB (224235296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64bcfcdcbf8d0bdd01b2cf431604ad80577f9835cdfc4a6f0e3fa5aad285a143`  
		Last Modified: Wed, 15 Apr 2026 23:20:05 GMT  
		Size: 25.5 MB (25533424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a396b1f4c36e9f9aee6af2bbc3fafd3b9edf66cea94cfc1b65a29ef33278982`  
		Last Modified: Wed, 15 Apr 2026 23:20:05 GMT  
		Size: 9.3 MB (9311196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9467dcb9fc59d3c051d0f664a27091cd05b0a3614d22b18830ed981f5fb1a4`  
		Last Modified: Wed, 15 Apr 2026 23:20:04 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233032fa7f8f189de4fe1f0b584cdaf9b86cb0cffcc241e5d499282ee90a738d`  
		Last Modified: Wed, 15 Apr 2026 23:20:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-26` - unknown; unknown

```console
$ docker pull maven@sha256:3642e31cfb06701515d2e9e9b9bfdae0b6199e4f08bfcc34589c833b762f3c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881e3e95ec9994c68c42b7eea635d89d1759fa440f6e9f3a15f40f7f675f2053`

```dockerfile
```

-	Layers:
	-	`sha256:b1afee4b16fc54a6357589661a60e85853757b66a82588d6e9c75ec9b891f9cf`  
		Last Modified: Wed, 15 Apr 2026 23:20:05 GMT  
		Size: 4.3 MB (4317740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd3e8a2ed936fcccff63f4c265a6b90f5cec67d2e5c5e9c0220db2b594445be3`  
		Last Modified: Wed, 15 Apr 2026 23:20:04 GMT  
		Size: 17.9 KB (17925 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-26` - linux; ppc64le

```console
$ docker pull maven@sha256:717d4ca22b2ce16296eca3af555c37db1367c6c9201ccb4cdad019c89febdb4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.2 MB (301239285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed604049609319349165962aac8a48b6f9dcb7c70155cb01d0c0381e18432c2`
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
# Wed, 15 Apr 2026 23:19:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:19:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 23:19:29 GMT
CMD ["jshell"]
# Thu, 16 Apr 2026 05:48:31 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 05:48:32 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 16 Apr 2026 05:48:32 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 16 Apr 2026 05:48:32 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 16 Apr 2026 05:48:32 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 16 Apr 2026 05:48:32 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 16 Apr 2026 05:48:32 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 16 Apr 2026 05:48:32 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 16 Apr 2026 05:48:32 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 16 Apr 2026 05:48:32 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 16 Apr 2026 05:48:32 GMT
ARG MAVEN_VERSION=3.9.14
# Thu, 16 Apr 2026 05:48:32 GMT
ARG USER_HOME_DIR=/root
# Thu, 16 Apr 2026 05:48:32 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 16 Apr 2026 05:48:32 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 16 Apr 2026 05:48:32 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9664bba08b3d0249eb3c4136e07f8afc48d5b42bcd12525be99e0deb1b7729d5`  
		Last Modified: Wed, 15 Apr 2026 23:20:08 GMT  
		Size: 227.6 MB (227616933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f584e0e24df72a8036d2b1b1a0d8003fd3c3f165cf9545295d0b9d2f783d7c88`  
		Last Modified: Thu, 16 Apr 2026 05:49:13 GMT  
		Size: 30.0 MB (29995963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2e9e381734325583e059432501a5ef4f7a625ae0d679a0cc9da9d92b2f71b9`  
		Last Modified: Thu, 16 Apr 2026 05:49:13 GMT  
		Size: 9.3 MB (9311175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9398e6bd9173f6fec5cd473fab79fcea87b6568886393ba7edc5fc2c9c04215`  
		Last Modified: Thu, 16 Apr 2026 05:49:12 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e1eaf5e41a321461d8cadbfa1d344bfd9366e837918f83a221206f3cc3217c`  
		Last Modified: Thu, 16 Apr 2026 05:49:12 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-26` - unknown; unknown

```console
$ docker pull maven@sha256:1d3939bf58143e29a21bff68aea5da05e4cb0392e886f17b14078336c65da2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4328825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5429ea3e26c46fcc9e3ccbca42d190bf164ef892e4fcb6df287cf8ff3ebbf35f`

```dockerfile
```

-	Layers:
	-	`sha256:579dfb515f531de26d6e398c1973f68b36c70fe2113a8f08ec4df032315c8be7`  
		Last Modified: Thu, 16 Apr 2026 05:49:12 GMT  
		Size: 4.3 MB (4311008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87ed2179d0b09f877aa5d1fa072bf1683ffd69c133b900e6031bb8b5b079ac33`  
		Last Modified: Thu, 16 Apr 2026 05:49:12 GMT  
		Size: 17.8 KB (17817 bytes)  
		MIME: application/vnd.in-toto+json
