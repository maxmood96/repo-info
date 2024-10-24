## `maven:3-amazoncorretto-21-alpine`

```console
$ docker pull maven@sha256:ca2a5b821262b5e590d0c269da71112e5a8b8499f85f8656f2249101655ed0d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-alpine` - linux; amd64

```console
$ docker pull maven@sha256:a3a69f3388f1c303c2602d33291024d8bf1e334c87075e9712c4dfe191a039bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.0 MB (174045098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a86c7c4e1d02c07a449063b5eae6a4972ad01ff7886c5b1babfd7a8118e9fc0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 24 Sep 2024 11:57:06 GMT
ARG version=21.0.5.11.1
# Tue, 24 Sep 2024 11:57:06 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:bfb2972ecae7a9dd2f51282c368df744040af6055effeff6fe1f6c73abf3a003`  
		Last Modified: Wed, 16 Oct 2024 17:57:22 GMT  
		Size: 158.9 MB (158930191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ab8eabb62d9bbb19861ffb59550ef22ed88d713f0ea202f6ce4e8de3d63104`  
		Last Modified: Thu, 24 Oct 2024 02:55:43 GMT  
		Size: 2.3 MB (2319622 bytes)  
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

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:b067196cb4cf21330d3e8e7d2463228d923f01016a3cf8c61af571516c502bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.8 KB (533754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a348cfad979a3ac215341394bd326e135af64f4fd7b69824c0185a8774d686`

```dockerfile
```

-	Layers:
	-	`sha256:577e42da47c291688e2076c7990cd4ea8cbf846d99a75f192a6e5e9c61888a05`  
		Last Modified: Thu, 24 Oct 2024 02:55:43 GMT  
		Size: 517.4 KB (517356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37f2e5717158932f152c458a23999ccf87b7b22a4a3dca2290a520ee76eaf8c6`  
		Last Modified: Thu, 24 Oct 2024 02:55:42 GMT  
		Size: 16.4 KB (16398 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5356a7941f797618bf4713e3d7fae923dc05ec8f0651e74643260af59c6ad932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172522638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b60c5fbb968e87e723d300f8e69137d6a29114dc85bbb2aba3c3efa88d45d0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 24 Sep 2024 11:57:06 GMT
ARG version=21.0.5.11.1
# Tue, 24 Sep 2024 11:57:06 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:5caf0a1ffd86bb63189c72afc5447c3e4d36fe0f610c98f82c31d967535a4628`  
		Last Modified: Wed, 16 Oct 2024 18:38:39 GMT  
		Size: 156.9 MB (156880010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5874c311c224d0264651fc8ff6cddab1a24956eb67003956cc1f571b22cebe0`  
		Last Modified: Thu, 24 Oct 2024 13:25:40 GMT  
		Size: 2.4 MB (2383512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0779f2579f38f37b5acd673d8eae15a5edfd802864d37a718fd8d95b0f2fc26c`  
		Last Modified: Thu, 24 Oct 2024 13:25:40 GMT  
		Size: 9.2 MB (9170433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849d2db3ba13764b60e273179edb31e4769b0ea620e536240eff88dcb4a2f912`  
		Last Modified: Thu, 24 Oct 2024 13:25:40 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ed717ff450d4dd48eee017e90c375b8f76b48d483b9040045ff7d5c171c848`  
		Last Modified: Thu, 24 Oct 2024 13:25:40 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:de08661735e581343cd320063fa17d8fddc4b914a99a1d4b7d11d582b4160393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.3 KB (533328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c2d61af64748ceeab58f4f377c2a24f05a872657626dcc3d2af13896be5f29`

```dockerfile
```

-	Layers:
	-	`sha256:b4e0385e09345ca98793586d418c038e5b6a38ff99d0f0d70e666838f038402e`  
		Last Modified: Thu, 24 Oct 2024 13:25:40 GMT  
		Size: 516.8 KB (516762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0822b3d5b3b5a79357a44ea0eba996a34ba92810c12f32c40203ab86e73d48af`  
		Last Modified: Thu, 24 Oct 2024 13:25:40 GMT  
		Size: 16.6 KB (16566 bytes)  
		MIME: application/vnd.in-toto+json
