## `maven:3-amazoncorretto-8-alpine`

```console
$ docker pull maven@sha256:e38e6b55e3543318e2b6bc501eddaebbd602898818b3adac237b81d8dd57ccd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-alpine` - linux; amd64

```console
$ docker pull maven@sha256:791be38ffb28ba1b26c5b055e09c05caf71d2cee73725872dd73109344c5b7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116370841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9401211cc4c34e1504c767c1f79058d370382129b120b2d24fe15a7c4a015c51`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:33:09 GMT
ARG version=8.492.09.1
# Wed, 22 Apr 2026 21:33:09 GMT
# ARGS: version=8.492.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:33:09 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:33:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 08 May 2026 00:31:59 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Fri, 08 May 2026 00:31:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 08 May 2026 00:31:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:31:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:31:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 08 May 2026 00:31:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 08 May 2026 00:31:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 08 May 2026 00:31:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 08 May 2026 00:31:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 08 May 2026 00:31:59 GMT
ARG USER_HOME_DIR=/root
# Fri, 08 May 2026 00:31:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 08 May 2026 00:31:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 08 May 2026 00:31:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228516198dcf71bb7973cf0e588a55b084e664ca989f408ecf3dd4a0ff9f028d`  
		Last Modified: Wed, 22 Apr 2026 21:33:25 GMT  
		Size: 100.8 MB (100787224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dc470d90db8074073fe1c7137157096b5ce054cad3ac0da0ec961dbcaa7e9b`  
		Last Modified: Fri, 08 May 2026 00:32:08 GMT  
		Size: 2.4 MB (2406167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88742acfc4b97b299eccb0f33c2df39ad4e8ca1fb08d087b4ac2f5a3483de7f8`  
		Last Modified: Fri, 08 May 2026 00:32:08 GMT  
		Size: 9.3 MB (9312253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af45e80d8842d27fc181477b07cc56aba7bf84d178fc212b52abf4ec71fd069e`  
		Last Modified: Fri, 08 May 2026 00:32:07 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5946b43d6297aab16645dc28a0e0c19212a894a522791997c4bb88e9aaac7b12`  
		Last Modified: Fri, 08 May 2026 00:32:07 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:e8c9e80f21a62305d7e3963c2593b05828c9ff7ecce78777f7358e07313e36f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.9 KB (406949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98bfeb721962f4b4c94593ccb294b4d492dba7f19e3c1dae7557f9a8cb57969`

```dockerfile
```

-	Layers:
	-	`sha256:d920aa2a4ad9909277e0bb0ffe2ef84f1dac964f12a6cc03b28328422094838c`  
		Last Modified: Fri, 08 May 2026 00:32:07 GMT  
		Size: 392.3 KB (392282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:444bbf4fcee5138ccfe1fee71897b9883c9b566db6eea4e7ea1d9531e7bbd0e5`  
		Last Modified: Fri, 08 May 2026 00:32:07 GMT  
		Size: 14.7 KB (14667 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:ac20b5a9abfd9784c88300146d3bd3ab09e0a436a2d7417d17cc95e5adb8a9a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116533391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973dc69460685e89068b402c12f55090008066bb965ad907fce5f2424201b6f4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:33:16 GMT
ARG version=8.492.09.1
# Wed, 22 Apr 2026 21:33:16 GMT
# ARGS: version=8.492.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:33:16 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:33:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 08 May 2026 00:30:23 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Fri, 08 May 2026 00:30:23 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 08 May 2026 00:30:23 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:30:23 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:30:23 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 08 May 2026 00:30:23 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 08 May 2026 00:30:23 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 08 May 2026 00:30:23 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 08 May 2026 00:30:23 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 08 May 2026 00:30:23 GMT
ARG USER_HOME_DIR=/root
# Fri, 08 May 2026 00:30:23 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 08 May 2026 00:30:23 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 08 May 2026 00:30:23 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcce3fd15c9d9eafd7fb5c5782c31fca73f6c459593a4bcb43e6b505a41d156d`  
		Last Modified: Wed, 22 Apr 2026 21:33:31 GMT  
		Size: 100.6 MB (100571524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625405da43ac272067ea195fe39d247228e1a01845661e98569279061c8f6fc4`  
		Last Modified: Fri, 08 May 2026 00:30:31 GMT  
		Size: 2.4 MB (2448761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47621a72864e3d8c2639348cdc72e8eed3bb94094e9107a3f8c21b3a130d19de`  
		Last Modified: Fri, 08 May 2026 00:30:32 GMT  
		Size: 9.3 MB (9312231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d9c222ba69b2a0423ceac11c4912979a74d3e1a32252906c2584b87c37ebce`  
		Last Modified: Fri, 08 May 2026 00:30:31 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7e4342caedb181e697aea53763e58c0d1d330cc6030317bacd59fe8145db29`  
		Last Modified: Fri, 08 May 2026 00:30:31 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:0adbcaed7f3bee5fec0437244af2e40f8d06e159b8e389676a1d0d0f8149ac72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.6 KB (406552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2735091537d8dff5780c071c023382296da18cb61f979d44d298237d7614833`

```dockerfile
```

-	Layers:
	-	`sha256:8776cfe30a8ee5b93850ff57715cb01a8d40774db07950b69351c467ba3f6341`  
		Last Modified: Fri, 08 May 2026 00:30:31 GMT  
		Size: 391.8 KB (391752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c0fa8fd1fa29e4ad3cb6e0f2768a5c4258792af752cc34b69d5843a10602aa`  
		Last Modified: Fri, 08 May 2026 00:30:31 GMT  
		Size: 14.8 KB (14800 bytes)  
		MIME: application/vnd.in-toto+json
