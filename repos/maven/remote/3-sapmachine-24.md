## `maven:3-sapmachine-24`

```console
$ docker pull maven@sha256:55c597d0f0f0f686915c36f3c2b2a557969ad637cd4bfeea65841c5278113c52
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
$ docker pull maven@sha256:b2addd492f558111ed12d2e15b93407a76bb87bc9db5de61c7ee128c14f3a175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296558162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c4efbe9d4744bb3484003a17a31df1a7ea649040c809d9086eb8a083b41565`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
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
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efac1039d1e2555cc9f0d9d9247db11581ba7624d284fe94446a2a8f5243270`  
		Last Modified: Wed, 02 Jul 2025 05:12:49 GMT  
		Size: 232.4 MB (232427021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bdc11fcefe8f27edddf9247532c479828885fd69d0f417700435a6d95e5d20`  
		Last Modified: Wed, 02 Jul 2025 09:39:20 GMT  
		Size: 25.5 MB (25458352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1ca4a6733ec3096194c1fea7fa907939ca7226b33b92c6e7add03de789650f`  
		Last Modified: Wed, 02 Jul 2025 09:39:20 GMT  
		Size: 9.0 MB (8953384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f919054c3ab331748139e2bea20f36833c21ee663207538bdf9861d027130693`  
		Last Modified: Wed, 02 Jul 2025 09:39:17 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a1e6e9a1510d8f2d881b7c8c54513fcc1dbb7b6aba459fe052172c2e7c2cff`  
		Last Modified: Wed, 02 Jul 2025 09:39:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-24` - unknown; unknown

```console
$ docker pull maven@sha256:78bf8f383250862839f82f8b9c51da6829854f18d154dbd2a93b68cfef665b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf1d3543712becc0005ad6dd84aaad12784ac82ed45daf94f7c19bf2a1616ba`

```dockerfile
```

-	Layers:
	-	`sha256:4713b1bb8c2b9ee3bc328482861dc480a33342eb5da55eaa67b7c4a1e8494a4b`  
		Last Modified: Wed, 02 Jul 2025 08:30:42 GMT  
		Size: 4.3 MB (4308116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5334f869f1625f694208b4af1d84b5fb0d90ed58a160f54e99ab3cbd09569cd5`  
		Last Modified: Wed, 02 Jul 2025 08:30:42 GMT  
		Size: 16.5 KB (16546 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-24` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:697ba24a66265b28accc39a5ca02e8d8f1652d58407d483291aeffa5c012b241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293699255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ad3fc87fc2927b5b809f27c124d676e76f5ea3d8a21c4d4a5271e4ca89136d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
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
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb90c874e6b82633b8fb9367c0edbbeb9e74a2aa19846449660bf716f9545e20`  
		Last Modified: Wed, 02 Jul 2025 12:10:29 GMT  
		Size: 230.4 MB (230357366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfabee1d07db0352228ad30173f76cb526438b31da4c06c3100f7fd51d7829b`  
		Last Modified: Wed, 02 Jul 2025 16:11:26 GMT  
		Size: 25.5 MB (25531450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019369c47522948d28292a7a6f870afa953f267d1d23cc20bba0c1977754b2ca`  
		Last Modified: Wed, 02 Jul 2025 16:11:24 GMT  
		Size: 9.0 MB (8953383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c7bb3a0742fd60b2e183161f95a617dc1b22f21d4c5d68aaf836d602247607`  
		Last Modified: Wed, 02 Jul 2025 16:11:23 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260761f4ea868cb0d899f824ee851cc80df08b90be5cd4cbda9f7a9a21837b1b`  
		Last Modified: Wed, 02 Jul 2025 16:11:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-24` - unknown; unknown

```console
$ docker pull maven@sha256:543d048e3dafbbedd5d4fee5cda616f39ed019568ef92feb8fc0115fb79c1d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4331314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7992d14a87cd6a033b2308900bcf32dad2a5a1381906c4cf292413efaf058e61`

```dockerfile
```

-	Layers:
	-	`sha256:1587528cce90e7dde361c093be3bf27e3467b4925413c26ddae299b95d332c2b`  
		Last Modified: Wed, 02 Jul 2025 17:30:55 GMT  
		Size: 4.3 MB (4314635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b19f86d1e4cc4454f033c3414d6cef5e40f0c009869c85b472a537baa7d8589`  
		Last Modified: Wed, 02 Jul 2025 17:30:55 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-24` - linux; ppc64le

```console
$ docker pull maven@sha256:535d3873b2ecd7ebdee8dc2b3937b1c9eede2799f1c719db6c9abe24d8dcd449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307018146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:879bf48dba30ac6512cb21d6ba4e71b89bc411be136ba1ba735f041b5b38cea4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
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
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0ee2ad4851a2865bf2427f712dc71191e5619527646a7b6b65f7a76ecb4289`  
		Last Modified: Wed, 02 Jul 2025 04:36:20 GMT  
		Size: 233.8 MB (233758055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4852e940d2fd61002e9bee74fbbb86c0b9c08aa22fd75f585afcc09ac96e67e`  
		Last Modified: Wed, 02 Jul 2025 17:18:21 GMT  
		Size: 30.0 MB (29984153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cb74f6cc5a28b04ea36a901a5b47804ae1c32f36893b598465b2ffbaa451dd`  
		Last Modified: Wed, 02 Jul 2025 17:18:21 GMT  
		Size: 9.0 MB (8953394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd75aaa8944b9dab3dea3441c7c5d5f164cffece35328432f948b372ebbfd63a`  
		Last Modified: Wed, 02 Jul 2025 17:18:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98babab294de8e0ca18d36fa91af586a5f963c570c06f6f294b24daa90260f8e`  
		Last Modified: Wed, 02 Jul 2025 17:18:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-24` - unknown; unknown

```console
$ docker pull maven@sha256:3f9157aea8e321c2b8248a6e9d13f6deda6b75d7bc8cb92b9a5d7dad0bcd4c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4329122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3daa992d09c21f1ab6cbc39bf1f397850498404a64730b7815f62d8501a94725`

```dockerfile
```

-	Layers:
	-	`sha256:315efe892b15045360bb69f77778a5421230fa3a582bb8a445d22c58d92761e8`  
		Last Modified: Wed, 02 Jul 2025 20:29:09 GMT  
		Size: 4.3 MB (4312526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16d540b673be60fdd490ea26304e53e7efecca3856329d641409c0427d2caea0`  
		Last Modified: Wed, 02 Jul 2025 20:29:10 GMT  
		Size: 16.6 KB (16596 bytes)  
		MIME: application/vnd.in-toto+json
