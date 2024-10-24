## `maven:3-amazoncorretto-17-alpine`

```console
$ docker pull maven@sha256:23ab027b727f94ffaa47ee4a2ed77fa1005501ef65c4ab1b2e23071b25e86f65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-alpine` - linux; amd64

```console
$ docker pull maven@sha256:e333afb14ef46972cd98cbb805561059de3048dc47da64ce92d2ac775fcf9011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160764189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcc7e3573c3de307709a2533e9fb5f72579680288f61dafbcb1a3efafa197d51`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 24 Sep 2024 11:57:06 GMT
ARG version=17.0.13.11.1
# Tue, 24 Sep 2024 11:57:06 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
ENV LANG=C.UTF-8
# Tue, 24 Sep 2024 11:57:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 24 Sep 2024 11:57:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 24 Sep 2024 11:57:06 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 24 Sep 2024 11:57:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 24 Sep 2024 11:57:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 24 Sep 2024 11:57:06 GMT
ARG USER_HOME_DIR=/root
# Tue, 24 Sep 2024 11:57:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 24 Sep 2024 11:57:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 24 Sep 2024 11:57:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed661954c40c6df4b0773f9ed2104f02a996d32057e419223cc5c193a5446ab7`  
		Last Modified: Wed, 16 Oct 2024 17:57:29 GMT  
		Size: 145.6 MB (145649284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b7f5bbeb2359627af2b02252a898e494aee3b0aa9b64fbc5ef370841fd0be5`  
		Last Modified: Thu, 24 Oct 2024 02:55:47 GMT  
		Size: 2.3 MB (2319620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc6d41ceed8db603a65a5ca170955985f9ded351f9e9033e0697eedc381d0e0`  
		Last Modified: Thu, 24 Oct 2024 02:55:43 GMT  
		Size: 9.2 MB (9170439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a96b4cf78dde00fdb17855db051a18f332fee270e15a0e3d5f72c321cc8aa4`  
		Last Modified: Thu, 24 Oct 2024 02:55:42 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894dc9d9d3d8180e8f8acb1723abd5a90413a1e842ddf051b28d8223ba3a2a16`  
		Last Modified: Thu, 24 Oct 2024 02:55:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:cca3c28c6d8c3840b69a3075499ae4e4af36e2955f51c7b8384f00156c636a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.9 KB (533855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d0043c5c14c174e7777a02d5972959c4a7715c0514f0a7ac7629b66996c1f7`

```dockerfile
```

-	Layers:
	-	`sha256:f9bfb11f4726cf7cc71052f4b2f96463fd9ab5e13e8fac5ad78e9ee67c609994`  
		Last Modified: Thu, 24 Oct 2024 02:55:47 GMT  
		Size: 517.5 KB (517457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06ae6c2bd519a196de9dd1edd98270d32ec084827d1f6ec4d37822a5460d4fab`  
		Last Modified: Thu, 24 Oct 2024 02:55:47 GMT  
		Size: 16.4 KB (16398 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c4c2af84fb93d5208dda2c6f54f0158817ef110afa01ada476b835b4058dbcd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159577144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b00ce6b393edab9475b0a4b53cb9db3631ea3402b524c182422d4532a401d4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 24 Sep 2024 11:57:06 GMT
ARG version=17.0.13.11.1
# Tue, 24 Sep 2024 11:57:06 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
ENV LANG=C.UTF-8
# Tue, 24 Sep 2024 11:57:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 24 Sep 2024 11:57:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 24 Sep 2024 11:57:06 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 24 Sep 2024 11:57:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 24 Sep 2024 11:57:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 24 Sep 2024 11:57:06 GMT
ARG USER_HOME_DIR=/root
# Tue, 24 Sep 2024 11:57:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 24 Sep 2024 11:57:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 24 Sep 2024 11:57:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644f628d973a703645cb2f2b4a6afac3e28403d169cf5a085cecafb375b39792`  
		Last Modified: Wed, 16 Oct 2024 18:30:37 GMT  
		Size: 143.9 MB (143934633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386389eb95e7303ce4549cd0da5f94a78b9dc8dfd671206fc92fe559d325452f`  
		Last Modified: Thu, 24 Oct 2024 13:21:03 GMT  
		Size: 2.4 MB (2383393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1996dceecf9fa8bba7754a923b2182452a6249b11e8c54d0873cd6959d0ef4cb`  
		Last Modified: Thu, 24 Oct 2024 13:21:04 GMT  
		Size: 9.2 MB (9170433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a50b7774fa02e7b4f82ad2ee7d302b681bc38759ea60da43dc6e5f234ecc3e`  
		Last Modified: Thu, 24 Oct 2024 13:21:03 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a0b19bc41bdd0a4db837f6f495056f8f7c2f71820a9c46c06720340c882e69`  
		Last Modified: Thu, 24 Oct 2024 13:21:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:9da4067c24bf053a6c9396099ef66d0776ab5300bee35f782d387bf3ad4fa35a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.4 KB (533430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75bca0498231d492ebd883e69baa9ef768b44a39bcc6347e41c1af4fdc6a08f0`

```dockerfile
```

-	Layers:
	-	`sha256:c3e9428cdac777fb8b07d1d4b4748af1360ddcb9a9940d76c201d9c9f3a9c942`  
		Last Modified: Thu, 24 Oct 2024 13:21:03 GMT  
		Size: 516.9 KB (516863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efe836be254c6018031da68e13cadd7d1d818da5b7df9b2b0ea52f68632392f7`  
		Last Modified: Thu, 24 Oct 2024 13:21:03 GMT  
		Size: 16.6 KB (16567 bytes)  
		MIME: application/vnd.in-toto+json
