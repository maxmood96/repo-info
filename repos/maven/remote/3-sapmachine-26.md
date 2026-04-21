## `maven:3-sapmachine-26`

```console
$ docker pull maven@sha256:9d60b8cec389a72e71e197a8d800b3f74c56dbb5de62b09ba80a8c71effc180b
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
$ docker pull maven@sha256:1fc06cc6cdb0b35476728a80a95e5024e264d30bd5f15c39b2e8fa24722ca570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290874715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa8eb1feb28f0ab6cefcf7a8a1491cdd90d1e127d778f28fefa9bdebdac37c9a`
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
# Tue, 21 Apr 2026 18:13:13 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 18:13:13 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:13:13 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:13:13 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:13:13 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:13:13 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:13:13 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:13:13 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:13:13 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:13:13 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:13:13 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:13:13 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:13:13 GMT
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
	-	`sha256:eb139627cb36c66d5b52bd60b1756553e0faaf2295f83d6248f62ab7c624a0a1`  
		Last Modified: Tue, 21 Apr 2026 18:13:27 GMT  
		Size: 25.5 MB (25470157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a2ab95650581d194d364814e77f18920f58b77f9971320d83c7dd2e3fcc15e`  
		Last Modified: Tue, 21 Apr 2026 18:13:26 GMT  
		Size: 9.3 MB (9312201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c386b2af43e7f210f1b75e74a113283c2dba069ff50bedac2a9a3d1dc69f5f3`  
		Last Modified: Tue, 21 Apr 2026 18:13:27 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bddd7c1b84c4dd28620a5369300ffddedfd1a37752ad4b548dc70a4fd3f7c2b8`  
		Last Modified: Tue, 21 Apr 2026 18:13:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-26` - unknown; unknown

```console
$ docker pull maven@sha256:ddaffe4b1256ef3b34b8dd10dcf1ba82526708ef74a12fd89d146a365aa8c7d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820fabcd910c3a72863abc1b4d98e8d45cd15a81d6b2fe5dda957372e00f3aa1`

```dockerfile
```

-	Layers:
	-	`sha256:c2da1a44a41ef43c13a01ec8eca74fa15edb0d49a685f5917e719b1e8c1c1085`  
		Last Modified: Tue, 21 Apr 2026 18:13:26 GMT  
		Size: 4.3 MB (4311173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b14cd230741139cbd1b30e559d58f49b76169faf0e5f0a986502712441ff55cb`  
		Last Modified: Tue, 21 Apr 2026 18:13:26 GMT  
		Size: 15.9 KB (15907 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-26` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c7b8c418b5ed811610ab50e9e45740e72c795c27214983578d95b83144b13b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.0 MB (287957800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e0109f185ad7bd4da2b4af67d9f5799857dad0e352f86bb0bf3741125b9ee9`
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
# Tue, 21 Apr 2026 18:13:12 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 18:13:12 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:13:12 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:13:12 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:13:12 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:13:12 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:13:12 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:13:12 GMT
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
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98811f1f7f1b906ec42bbfac81da12f49a09c9edd0bbea284b80e9cd8a244ab`  
		Last Modified: Wed, 15 Apr 2026 21:06:36 GMT  
		Size: 224.2 MB (224235296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee715880cb433b82df4c9e50ea4c195baebc05bdf8d4d1a748592c23b2139cab`  
		Last Modified: Tue, 21 Apr 2026 18:13:26 GMT  
		Size: 25.5 MB (25533460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ad80c88d92ee4b228f7b7e0b20fc8eeed2944b7481941208d28dfd263933c5`  
		Last Modified: Tue, 21 Apr 2026 18:13:26 GMT  
		Size: 9.3 MB (9312254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9900b22e6e99caafe629171debca440475e6145dc425354681c22b28ae0247d`  
		Last Modified: Tue, 21 Apr 2026 18:13:25 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd7e5f2b13cdbf2179a4291a19bcb456e74cac53d5fba0eb3c6c0a3d67d98f8`  
		Last Modified: Tue, 21 Apr 2026 18:13:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-26` - unknown; unknown

```console
$ docker pull maven@sha256:ef66500959139c00a8627ad14f14e175c16a1ad499aff47bdbdfb23a4b8860e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4333828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcfb7213ae860073c33cbe4865e744e89049b8f2e50466de2091ccfb1cdfa55`

```dockerfile
```

-	Layers:
	-	`sha256:04e2581f0a09e3f6e85f929bb252bc85071ebcca137b8524d1a20a97a49c8330`  
		Last Modified: Tue, 21 Apr 2026 18:13:25 GMT  
		Size: 4.3 MB (4317740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:284404828581bfd046127350090bc56679155fcce4e0063663ed8a78742499ff`  
		Last Modified: Tue, 21 Apr 2026 18:13:25 GMT  
		Size: 16.1 KB (16088 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-26` - linux; ppc64le

```console
$ docker pull maven@sha256:2abb08ed36dbf76b6f499d0139e0cfefb6b928fa12f517ece250d77e16070fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.2 MB (301240333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5ded3c98a9c78eb8c167b96f745b7d2ef72962e265571d34efd3976af481a5`
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
# Tue, 21 Apr 2026 18:13:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:13:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:13:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:13:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:13:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:13:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:13:49 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:13:50 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:13:50 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:13:50 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:13:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:13:50 GMT
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
	-	`sha256:635da408522680a09c3977c1dcf54844219dfbb40b6e9bed586a316f941cf8a5`  
		Last Modified: Tue, 21 Apr 2026 18:14:14 GMT  
		Size: 9.3 MB (9312257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b72d81238b5f05b7950e1e6caed12988342a79fba2cd774cf796ac11ec8857`  
		Last Modified: Tue, 21 Apr 2026 18:14:14 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce5196c98471493d1741fb7bccf3acf1eb00600407f6eb91e26a3c916ff4e98`  
		Last Modified: Tue, 21 Apr 2026 18:14:14 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-26` - unknown; unknown

```console
$ docker pull maven@sha256:74fac2131ea57a36c13785852f81cee1a5564adb5fdcf342888fb9bf56d3d01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4326989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0ad4d3b4daf4d1c80384f345cfd0876dc34f6e754111898fa04a4d04478c73`

```dockerfile
```

-	Layers:
	-	`sha256:9c45e520588248b2a60563d255805eb48c473a174440782c7a273a8602a809ac`  
		Last Modified: Tue, 21 Apr 2026 18:14:14 GMT  
		Size: 4.3 MB (4311008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e59b93eb68cb8f0132753bd33253a4a771135885e65ce2dde86e80c57b433797`  
		Last Modified: Tue, 21 Apr 2026 18:14:14 GMT  
		Size: 16.0 KB (15981 bytes)  
		MIME: application/vnd.in-toto+json
