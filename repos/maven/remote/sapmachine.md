## `maven:sapmachine`

```console
$ docker pull maven@sha256:e42e5283300312cdd2a85415c374ab85114977f4d489e34a254712c852653872
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
$ docker pull maven@sha256:e3309d88553388ccd26b0fdb9e8cf1b7fdcd5525822e31ae2d80c48e7e354fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278054762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f463e7b00496bc4b040de0af3b4b23086962e9dcc74dff5fbf591c4b8e9f370c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffde96ed1f059e28dcf91573757466b291c6bbfa831eb6b9283dc9f81ea369ba`  
		Last Modified: Tue, 25 Jun 2024 22:58:57 GMT  
		Size: 215.5 MB (215455806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da130a7c9e4705769d4e045a29e97f29da949106ccf62610906425b49698a50`  
		Last Modified: Tue, 02 Jul 2024 09:09:42 GMT  
		Size: 23.7 MB (23730949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc763de102673545f7b0e88579fa5812eda82c9c5fd8780939aeeef3d70a8c2`  
		Last Modified: Tue, 02 Jul 2024 09:09:41 GMT  
		Size: 9.2 MB (9161815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fd793bcead6141ecbb03729a129e8b83bdf7018841bd6de7f075e9f6e19615`  
		Last Modified: Tue, 02 Jul 2024 09:09:41 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce26db886c058f9f0ef66772321c1967bcbe4e606452c1c51894196ad886ea0`  
		Last Modified: Tue, 02 Jul 2024 09:09:41 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:55c582b993ccde0d045b9cef8d78e12c80d0fdf27a763285f44ebcea7fbdb0d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4066443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d84bf8f0b54ba71b3963bfcb0db83c024ab2cbe841a159acbc5f78d705e8902`

```dockerfile
```

-	Layers:
	-	`sha256:87457d0bf164d2f96fd510a23a438d156e0bc8b50764d5726d502c0e4d34bff7`  
		Last Modified: Tue, 02 Jul 2024 09:09:41 GMT  
		Size: 4.0 MB (4048734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5bfc39b6e3889d3857d6f8d73ed5e3765ea4e0bb4b1bc8c67639c6c32818764`  
		Last Modified: Tue, 02 Jul 2024 09:09:41 GMT  
		Size: 17.7 KB (17709 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:sapmachine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5abf3f0b565dc16e8038c1f94de08bf652f8818518925d9e992b75efe4dd5722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275383952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0cda39ef1e7890c7334d5fc8d805758c55881d6e66c944568babcae3641980`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2677f3515230e572a08622f5a0bea8ef48085540a56a214c4fb1e0b52b2a63ef`  
		Last Modified: Wed, 26 Jun 2024 00:03:00 GMT  
		Size: 213.6 MB (213558915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c665a4846952bac8c82479eb3e1d52ed85578a3bbdc15cce2ec03424e916a7`  
		Last Modified: Wed, 03 Jul 2024 10:43:38 GMT  
		Size: 23.8 MB (23819170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ae1a28ac599dfcfc777c83cfa0a77ff50116da8b9cb456202957d8ba2ceaff`  
		Last Modified: Wed, 03 Jul 2024 10:43:37 GMT  
		Size: 9.2 MB (9161784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f79d175c4a30a88f1203129ea3bf8161e3378fd045de1d7e771f000e35d858`  
		Last Modified: Wed, 03 Jul 2024 10:43:37 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63338ba155e3362d221627fb2c3c6f4e45eeee3469d9499a388bb513b472b4f`  
		Last Modified: Wed, 03 Jul 2024 10:43:37 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:cfdb1054f0bce77b0a73909dc938e26d0a122f4ae5edcd8bc7566640ee30dabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4073788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4c00fcf6e1feb599715cd86b2304e3ea8872493d387d6c5560af858a52df91`

```dockerfile
```

-	Layers:
	-	`sha256:d6885eafcccd6bf24d584ebd6f1396cbd67fa51a03d757188bfcd9afc6504034`  
		Last Modified: Wed, 03 Jul 2024 10:43:37 GMT  
		Size: 4.1 MB (4055307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a82aa79bc4fb5e6f6a63fb4877e8acf11f7778800c70179ffdd8b8ae11506bb`  
		Last Modified: Wed, 03 Jul 2024 10:43:37 GMT  
		Size: 18.5 KB (18481 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:sapmachine` - linux; ppc64le

```console
$ docker pull maven@sha256:0d22a36776b38d87601c8b4aaffe20bbc0bcb4fdb3c9c38a97e2ca5003d09b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288442936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc4c10c65d7aab02d5ce6ae318a1839cd2a15e00811768875bc6ed03e0cfff9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7412a1960288eb7288f1a43f168ed6eba52de00d601789ca3300c977a21d191`  
		Last Modified: Wed, 26 Jun 2024 00:26:56 GMT  
		Size: 216.9 MB (216914551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bec1a021dbdd62493d0b0169996af316fb89343dcb86d267618f37970ad8d11`  
		Last Modified: Thu, 27 Jun 2024 19:12:28 GMT  
		Size: 27.9 MB (27859530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d441a6807e003160499d9a835328eae96c143ebb0c095293ac989460e256be26`  
		Last Modified: Thu, 27 Jun 2024 19:12:28 GMT  
		Size: 9.2 MB (9161782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54f32f29248548f670ece07fe6fd8fb94b456dff76ae0aec96baa301ba05b94`  
		Last Modified: Thu, 27 Jun 2024 19:12:27 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9363735020a9bb8d5d9c8235836b5abc54846f879408d7b049f8964d6fd33d6`  
		Last Modified: Thu, 27 Jun 2024 19:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:23b9f0b01b26f42e1a141c73332bed5450649e51877b4c8e28afa6954cbfd4c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4071399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d97cbd47692e7c887a1ee26730d9e5809c0ae140ed12363dffc3348d6d2bfc`

```dockerfile
```

-	Layers:
	-	`sha256:a82115a5ee618dd5a8aa08f05a443ab7c3fd78d04f1db9515b442ee1764b1102`  
		Last Modified: Thu, 27 Jun 2024 19:12:27 GMT  
		Size: 4.1 MB (4053587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98f7cf2e659ffd9f3f38c1fe7358ebdefd24d882eff5a813f1d940e99ddf7d0a`  
		Last Modified: Thu, 27 Jun 2024 19:12:27 GMT  
		Size: 17.8 KB (17812 bytes)  
		MIME: application/vnd.in-toto+json
