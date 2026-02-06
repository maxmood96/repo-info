## `maven:3-sapmachine-21`

```console
$ docker pull maven@sha256:52d7b6cd02c1bbd65637a664fd89e86ce7e9de9e9e57e2a7f8529ebed10f4ec5
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
$ docker pull maven@sha256:c26dce69ea4be3577611637ff2b30a80310648652b5146ae185c727da170e645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.3 MB (283279837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e492475bb5727de09c44ccd6bb34471d2a86e8e83a72afc5a49e3791900270de`
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
# Wed, 21 Jan 2026 20:03:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:03:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 21 Jan 2026 20:03:37 GMT
CMD ["jshell"]
# Thu, 05 Feb 2026 23:31:35 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 23:31:35 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 05 Feb 2026 23:31:35 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:31:35 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:31:35 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 05 Feb 2026 23:31:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 05 Feb 2026 23:31:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 05 Feb 2026 23:31:35 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 23:31:35 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 05 Feb 2026 23:31:35 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 05 Feb 2026 23:31:35 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 05 Feb 2026 23:31:35 GMT
ARG USER_HOME_DIR=/root
# Thu, 05 Feb 2026 23:31:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 05 Feb 2026 23:31:35 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 05 Feb 2026 23:31:35 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231628878931cb2e916a9a678eb219b283e31fcf07667b01271007b0ac0f8193`  
		Last Modified: Wed, 21 Jan 2026 20:03:59 GMT  
		Size: 216.4 MB (216380392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d69dc44c4b9de585e002718a74771c7d0356774ddc5468560ee29c58011799`  
		Last Modified: Thu, 05 Feb 2026 23:31:48 GMT  
		Size: 27.9 MB (27860156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f287b603af220c1b27cbf3ade2b57625545948b8beecc38ce472c2cb14b9682d`  
		Last Modified: Thu, 05 Feb 2026 23:31:48 GMT  
		Size: 9.3 MB (9312241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6dbcaa8f834517a34463cf79ba6ff53f24e2db1541ca650d805e4ceedfd764`  
		Last Modified: Thu, 05 Feb 2026 23:31:47 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6142cf4a9e5b7a07918ecb1aa82a5ad18676b05b5bde328fe60e7435a15a75a1`  
		Last Modified: Thu, 05 Feb 2026 23:31:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:c8ac0e8618b24f37b79f20cc388e2054dc66d2774afbbb3be5737c548caafe9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4338871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4de51b4206f3962fdb33c710bbf47c6f473d376bcb7330da567b0198305f422`

```dockerfile
```

-	Layers:
	-	`sha256:a394e4750f326f0098ce40889f1b67c3ef434d28fb5cc475afa5efad3a5e9955`  
		Last Modified: Thu, 05 Feb 2026 23:31:48 GMT  
		Size: 4.3 MB (4322368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf7284700bf4e857ebd488688b15e9f0fe9695a0d1afce440c7ca28efa54e5ee`  
		Last Modified: Thu, 05 Feb 2026 23:31:47 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:eca631a4a8caa6f788f56fc5443b16e051d77e94e5afa61793826f7b3bdc6ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280566207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4076936f0cbbe21d90e056353c6ef4ebb5c054649a49fed31b10d283a2fe4bf3`
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
# Wed, 21 Jan 2026 20:08:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:08:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 21 Jan 2026 20:08:44 GMT
CMD ["jshell"]
# Thu, 05 Feb 2026 23:42:30 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 23:42:30 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 05 Feb 2026 23:42:30 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:42:30 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:42:30 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 05 Feb 2026 23:42:30 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 05 Feb 2026 23:42:30 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 05 Feb 2026 23:42:30 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 23:42:30 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 05 Feb 2026 23:42:30 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 05 Feb 2026 23:42:30 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 05 Feb 2026 23:42:30 GMT
ARG USER_HOME_DIR=/root
# Thu, 05 Feb 2026 23:42:30 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 05 Feb 2026 23:42:30 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 05 Feb 2026 23:42:30 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17aed308a18be2682cf6747a9bb1dd7d30e1cc7149e7d58d69df0423dbd2bdae`  
		Last Modified: Wed, 21 Jan 2026 20:09:37 GMT  
		Size: 214.6 MB (214637070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffe12f080e048f222f21eba8e83511502e9982e02d19fefc2b3ca3d810e8d91`  
		Last Modified: Thu, 05 Feb 2026 23:42:44 GMT  
		Size: 27.8 MB (27752022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd2411bf960a9adf141ce7b2b9b64c2cf2176b7ef3b4568a558d7082a618078`  
		Last Modified: Thu, 05 Feb 2026 23:42:44 GMT  
		Size: 9.3 MB (9312251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d85928ae54a6c8062df470259f04505babf3ef2f6b48b6e3179bf393e1595f`  
		Last Modified: Thu, 05 Feb 2026 23:42:43 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffc4285206ddb42d206c0e968ce18ec85dc19d56ec7f68e9bc39d44dac56bf9`  
		Last Modified: Thu, 05 Feb 2026 23:42:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:680678063d72ab2a07cc558cd9234638435ae13fbea1a81f3bcf3e3567c5141c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4345526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0229da38b98c8e92de1316af0ab380834baf1eba926a8f76b720ff6434618073`

```dockerfile
```

-	Layers:
	-	`sha256:962696848131485eec4b74223b70d960ecc1aa0a9ba8e28b11ca4d76d24a86f1`  
		Last Modified: Thu, 05 Feb 2026 23:42:43 GMT  
		Size: 4.3 MB (4328890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38fd5409431d88da3d560eb396bf082968f90a847e44de5b075dd774091a66e0`  
		Last Modified: Thu, 05 Feb 2026 23:42:43 GMT  
		Size: 16.6 KB (16636 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-21` - linux; ppc64le

```console
$ docker pull maven@sha256:caa4a36ed12ca3999be47c9db453ff8a2109e667e5d577e45bdd62b4f6df06ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291027386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a954d21c2f17cdb0fbad400347d885d95bff857af88f7540a1a624902a70b800`
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
# Wed, 21 Jan 2026 21:19:10 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 21:19:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 21 Jan 2026 21:19:10 GMT
CMD ["jshell"]
# Wed, 21 Jan 2026 21:52:17 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 21:52:18 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 21 Jan 2026 21:52:18 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 21:52:18 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 21:52:18 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 21 Jan 2026 21:52:18 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 21 Jan 2026 21:52:18 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 21 Jan 2026 21:52:18 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 21 Jan 2026 21:52:19 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 21 Jan 2026 21:52:20 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 21 Jan 2026 21:52:20 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 21 Jan 2026 21:52:20 GMT
ARG USER_HOME_DIR=/root
# Wed, 21 Jan 2026 21:52:20 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 21 Jan 2026 21:52:20 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 21 Jan 2026 21:52:20 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a634db121cb7f6686c4bcd6d6270267ca72f83f4fd8798790d329df147ca0630`  
		Last Modified: Wed, 21 Jan 2026 21:20:07 GMT  
		Size: 217.4 MB (217421208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb28a65da0746fc2054c4bf9e76618ca8daa333dcf01d49a473f98260d5270f0`  
		Last Modified: Wed, 21 Jan 2026 21:52:52 GMT  
		Size: 30.0 MB (29986747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb6d7bce99667ca069b5cede9858e9ab82b1ec59a37f6b0b1089f3597940180`  
		Last Modified: Wed, 21 Jan 2026 21:52:51 GMT  
		Size: 9.3 MB (9312232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58be255304957aac75db73b56f2d0f080cec90724d747bd807e1daf91f8668ca`  
		Last Modified: Wed, 21 Jan 2026 21:52:50 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038b149f308946a1c7fb89b004fe48a86c19fc761c31da8005ae0eec48beb254`  
		Last Modified: Wed, 21 Jan 2026 21:52:50 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:d44d40d319d1273e222de1e227898e8f68b6962090e17ac6fc9fdc19aca94413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4339342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25143a064393a6baa08a9c91281d328a4c678f302d9fba96d9ba7cc08548ad17`

```dockerfile
```

-	Layers:
	-	`sha256:507268f8e04823f6f13fb56d8ce7b1fc6d188d29f450d461854de1accd5fb686`  
		Last Modified: Wed, 21 Jan 2026 21:52:50 GMT  
		Size: 4.3 MB (4322789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce3674727e74e2cf94c97b28c44f75886d7785d4e413a4385ef237b3883706a7`  
		Last Modified: Wed, 21 Jan 2026 21:52:50 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json
