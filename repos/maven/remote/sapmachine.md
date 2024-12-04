## `maven:sapmachine`

```console
$ docker pull maven@sha256:5b417ca92ab30caf691f640d086e7c7237eb78bcf6323c13411ae2c13483c217
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
$ docker pull maven@sha256:8835b31aeea6645f4522e851dba693f92aed143f45e269e9c2cdac4d2449a44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279313337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1474dae82dd6e8ccb6e45ed39350e85425671ada76e60747e4c638a1198b067f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ARG RELEASE
# Tue, 20 Aug 2024 18:12:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["jshell"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4665ddf8590cff01ed85dad480fe139cbc7547245750193897acc91288ab5a`  
		Last Modified: Tue, 03 Dec 2024 02:35:49 GMT  
		Size: 214.9 MB (214943612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb86dc20f20064977036fd3285892862c1169daec7e25c8d909ed52eb27580e`  
		Last Modified: Tue, 03 Dec 2024 04:32:44 GMT  
		Size: 25.4 MB (25446283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fcf328b20f8a008eefba7d8fafc3156bf92e39a8119c654c15cd745af388b5`  
		Last Modified: Tue, 03 Dec 2024 04:32:44 GMT  
		Size: 9.2 MB (9170436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc3a85fc1d9e0c2d700eeb9a0deba371f7bd2c8906b24006dd3e47c933ecb1c`  
		Last Modified: Tue, 03 Dec 2024 04:32:44 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d87b2ea88582ade1abfae4cb3cc362d12f373326846da1fa8f3d90f8c40046`  
		Last Modified: Tue, 03 Dec 2024 04:32:44 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:df1d7487305271660259d9fbd5df9431c875142603643410ae4177a58ce25f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4180752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebfa7b9b0c73e0ee49ceb47ba1dfc268580d2ba4bde9157108a4843cc225e3d7`

```dockerfile
```

-	Layers:
	-	`sha256:9d344154c967ca45da95933e05526b6d18550c8dc4a484edbdf1001b753f237a`  
		Last Modified: Tue, 03 Dec 2024 04:32:44 GMT  
		Size: 4.2 MB (4162974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9b1160a330250713811ce57038aea5479718f9fa9724186b5e5ce71ba67200c`  
		Last Modified: Tue, 03 Dec 2024 04:32:43 GMT  
		Size: 17.8 KB (17778 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:sapmachine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:7c9b8ce4c43334e9ec00ee5e2d8ef487a603969ed52ae4b8dc1ec5741dc5fdb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276734565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e53c6affb2bd27ff483b02b05828d6bdb9f68f8cfb23211f72abcc1605d612f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ARG RELEASE
# Tue, 20 Aug 2024 18:12:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["jshell"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c778935a0b47d72cae383e9d4fc4831f38fd060bbaca4476cf0becef046700db`  
		Last Modified: Sat, 16 Nov 2024 03:47:13 GMT  
		Size: 213.1 MB (213145423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25832265f156c45df965de45595778cd5bd14c0ba0625dbd06278e03899797e7`  
		Last Modified: Sat, 16 Nov 2024 08:07:08 GMT  
		Size: 25.5 MB (25525251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5924f79ee827aa1a9add8d798f5a8a3a69f180c51acdbd51b68fcf93e66d24a4`  
		Last Modified: Sat, 16 Nov 2024 08:07:08 GMT  
		Size: 9.2 MB (9170429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe9c3acad8fc9739370d712dd3cf7d003c3b83964de101a303cd2b873117a10`  
		Last Modified: Sat, 16 Nov 2024 08:07:08 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d328cea2bc1978829877b149f9b90ad365a4cdaeea45e032b8a9be3e97f687f8`  
		Last Modified: Sat, 16 Nov 2024 08:07:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:6f78cfea7309def59d9212933b1159cf69a0d83a3fc2cf41dd9675f0f4757105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4187490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc110d8921f7798dec85ddfc455c1a03c0a36089989b777a2137b5b6100c4d61`

```dockerfile
```

-	Layers:
	-	`sha256:90c4c5f40e431661a7002e062b31cdb0a01200749c2209f4cfc9708d45810f66`  
		Last Modified: Sat, 16 Nov 2024 08:07:08 GMT  
		Size: 4.2 MB (4169530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cce0c614ae032d33be1149687bca23d993ca40647ac621bb558ecbaeddcccbb7`  
		Last Modified: Sat, 16 Nov 2024 08:07:08 GMT  
		Size: 18.0 KB (17960 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:sapmachine` - linux; ppc64le

```console
$ docker pull maven@sha256:338e21006b5dfc9297e4e4d510c4ac20ec4eddba207d5bdc15ea679b1b43ef4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.1 MB (290066463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949e421376e1f76e2d89e8102824411bbac5ee6746ac019ac4e0f0d0d53e4776`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ARG RELEASE
# Tue, 20 Aug 2024 18:12:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["jshell"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b106e86f46944f37ef70bcbbcd8cf9c35dac2857840b740b6b6e106e42e3101`  
		Last Modified: Tue, 03 Dec 2024 08:32:08 GMT  
		Size: 216.4 MB (216394622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52af7f29271fe651dca1b3136560c47b6f4531627430edbbe2ca04b183c3116c`  
		Last Modified: Tue, 03 Dec 2024 23:15:45 GMT  
		Size: 30.1 MB (30111557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de987623fbc6e0fc01640b4b4341f471fae4aea19a61fe8908040927e3e595b`  
		Last Modified: Tue, 03 Dec 2024 23:15:45 GMT  
		Size: 9.2 MB (9170426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc2a42036185fd511b3bf0081e54d45a04ea7e179e53dbe7732ee89b8cd99dc`  
		Last Modified: Tue, 03 Dec 2024 23:15:44 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c66f1b77a0f474168b39d61a5a7a8fdc7fc91108894ce85e250ad8e3e847d6`  
		Last Modified: Tue, 03 Dec 2024 23:15:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:6c4b491fc3b1e0d0e16367ee2a1c280abac07cd0e8aa3491d3d04485160d4ec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4185699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921eedb6856ddf40ac60ad36d985322266a03aa0bd15da4c4bf79ff7a95f8b42`

```dockerfile
```

-	Layers:
	-	`sha256:e4e8f2088d29d90d8b075319b8376b0d1a26f383e8427de938a3c4097dc00102`  
		Last Modified: Tue, 03 Dec 2024 23:15:44 GMT  
		Size: 4.2 MB (4167848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e5afd709fdbc5d26296809cccaa6a4aeface7e12b1f010cd214d43357c05e50`  
		Last Modified: Tue, 03 Dec 2024 23:15:44 GMT  
		Size: 17.9 KB (17851 bytes)  
		MIME: application/vnd.in-toto+json
