## `maven:3-amazoncorretto-21-alpine`

```console
$ docker pull maven@sha256:0f6d9d54e2ad3cdab042136f1d3721816b897ea790ba4ce9f1a660abaca4fa06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-alpine` - linux; amd64

```console
$ docker pull maven@sha256:0d0b43e2721a9aa04890e8707d0c5e90a8edc8fb514ca38a2df41a859dad82ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177187982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a2b22fcb77a57733bcf6aacbdc90a253ef7a1a5ef8b2f21646366ceecffc47`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:20 GMT
ARG version=21.0.10.7.1
# Wed, 15 Apr 2026 20:16:20 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 15 Apr 2026 20:16:20 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:16:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 15 Apr 2026 20:16:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 21 Apr 2026 18:12:03 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 21 Apr 2026 18:12:03 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:12:03 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:03 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:03 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:12:03 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:12:03 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:12:03 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:12:03 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:12:03 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:12:03 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:12:03 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:12:03 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71448d6e675e667655615378e72942f52abaf0b0bca7c6602dc0fbe187e2c587`  
		Last Modified: Wed, 15 Apr 2026 20:16:38 GMT  
		Size: 161.6 MB (161590450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0dbabfc360caf6e442538b165d771d109e070ea3c888b14940d950c5149562`  
		Last Modified: Tue, 21 Apr 2026 18:12:12 GMT  
		Size: 2.4 MB (2420138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b34d1db5deb44c9fade320f19c70afc0a3a390f21863bdb45291b3488deeeaa`  
		Last Modified: Tue, 21 Apr 2026 18:12:12 GMT  
		Size: 9.3 MB (9312198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c912d0110495bd64f5fa29aa77181461bb933fe5681300793bfd60dd77f7afd6`  
		Last Modified: Tue, 21 Apr 2026 18:12:11 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a9efa7402ae924cbcbc9668ed39ea753cd4cb98b99a2ee67ebe7d1b826313a`  
		Last Modified: Tue, 21 Apr 2026 18:12:11 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:5cfdeda5fb389096b51d2971119a7d07c2d3548897d4257347cab9958268b367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.2 KB (742169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5ab2eba402ad1de39873a7fe5bdf1ea0b8fe82c10e0c1ad15ce1f1cb04bd20`

```dockerfile
```

-	Layers:
	-	`sha256:e91e215f0633a730637d6fde2c8795e9c4333e2597b0e3f559393805550b632e`  
		Last Modified: Tue, 21 Apr 2026 18:12:12 GMT  
		Size: 727.6 KB (727643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8c3254ae651dd6c2add4d7a82398ffac7a433e659fe9292ddd99931e14f308d`  
		Last Modified: Tue, 21 Apr 2026 18:12:11 GMT  
		Size: 14.5 KB (14526 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:78b1179c7486996513f75908f63c176466bcd0dff9c508840abd5f780fb0210f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175590022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706a9ed87f5e194c7b38394468808533f458745387a0994bca7c421df49e7a0b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:23:46 GMT
ARG version=21.0.10.7.1
# Wed, 15 Apr 2026 20:23:46 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 15 Apr 2026 20:23:46 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:23:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 15 Apr 2026 20:23:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 21 Apr 2026 18:11:55 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 21 Apr 2026 18:11:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:11:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:11:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:11:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:11:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:11:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:11:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:11:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:11:55 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:11:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:11:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:11:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1cf2342851f77ea9f415795ed3cd8dada823b419d754c75ab485a6a7a59996`  
		Last Modified: Wed, 15 Apr 2026 20:24:06 GMT  
		Size: 159.6 MB (159615722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96d68a1747949a59345153e519ecff7ecee35307b9edc653dd93a8ea545975d`  
		Last Modified: Tue, 21 Apr 2026 18:12:03 GMT  
		Size: 2.5 MB (2461168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63745fa2162f45dbd6adb2379b8c59ede0075d7779caabfdbf032cbaab7d145f`  
		Last Modified: Tue, 21 Apr 2026 18:12:03 GMT  
		Size: 9.3 MB (9312254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256657bf7a2ac88d62b215ac1d1afea4749e524752e6b448493e7b34fa13fc8b`  
		Last Modified: Tue, 21 Apr 2026 18:12:03 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c200d621b7c00e38538063b9776cf421d1e763c9a765f188d22f971555c591`  
		Last Modified: Tue, 21 Apr 2026 18:12:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:d560f066b03f9b48bfa7b263c2f2dae1f93aecd527fcda04e6a52a2e3d395186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **741.1 KB (741059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da0b9fef5dc69886acf76336c6c05a614a3ff860c0e682ffa349591c2dff02d`

```dockerfile
```

-	Layers:
	-	`sha256:626f6d88e8e8d0e83cfcedb633bba355210d07f526b549687f71cdaaed9a74ea`  
		Last Modified: Tue, 21 Apr 2026 18:12:03 GMT  
		Size: 726.4 KB (726400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28283ee13ad9f41ddb9194bf54b2cbd73c39ba94f979c5379d0b1b9efe3bcb4c`  
		Last Modified: Tue, 21 Apr 2026 18:12:03 GMT  
		Size: 14.7 KB (14659 bytes)  
		MIME: application/vnd.in-toto+json
