## `maven:3-amazoncorretto-8-alpine`

```console
$ docker pull maven@sha256:7c087469efe147db11244f95b34a4eaf2d16c0f63023c08c34c57b4632a65373
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-alpine` - linux; amd64

```console
$ docker pull maven@sha256:c58b056041dfdcb87f62cefb289d8be80e69c92dab8e7f91af3684157f121538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116359459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b4baf56302d5788b64156e751f455b38521a2375c7735f6fa18ebb2992d493`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:24:14 GMT
ARG version=8.482.08.1
# Wed, 15 Apr 2026 20:24:14 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 15 Apr 2026 20:24:14 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:24:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 15 Apr 2026 20:24:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 15 Apr 2026 22:52:32 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 15 Apr 2026 22:52:32 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 15 Apr 2026 22:52:32 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:52:32 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:52:32 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 15 Apr 2026 22:52:32 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Apr 2026 22:52:32 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 15 Apr 2026 22:52:32 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 22:52:32 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 15 Apr 2026 22:52:32 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 15 Apr 2026 22:52:32 GMT
ARG MAVEN_VERSION=3.9.14
# Wed, 15 Apr 2026 22:52:32 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Apr 2026 22:52:32 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Apr 2026 22:52:32 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Apr 2026 22:52:32 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88d1dcb40680cc470fb6c04d2b258ef4349b55286064027930674dd42c7a614`  
		Last Modified: Wed, 15 Apr 2026 20:24:28 GMT  
		Size: 100.8 MB (100776894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb1b5b85460e3c053d92cb1ffad2cb9b8a3961bd90e3e8269c4f2454e1ab154`  
		Last Modified: Wed, 15 Apr 2026 22:52:41 GMT  
		Size: 2.4 MB (2406150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7761faf0240429b0320be110a6098d8ea02a3f3eadf0f3d11821ed08cec0467e`  
		Last Modified: Wed, 15 Apr 2026 22:52:41 GMT  
		Size: 9.3 MB (9311189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996d3aeafca5c2c88060be9d705fdcd2ae4a15a222ced326f75f19d83b470163`  
		Last Modified: Wed, 15 Apr 2026 22:52:41 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e834f0403bf4e19b755906da5991d7fe082c8a2fa88f156b82cadf6052a8adc`  
		Last Modified: Wed, 15 Apr 2026 22:52:41 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:8bf49b6f75ada19e213a4e57cefb234b1498242d0352e58ae4d25123f8b56036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.6 KB (408635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87a52a442116a66747bff31eff8ca9d7d2a916dae47cba179bd6731fcf96050`

```dockerfile
```

-	Layers:
	-	`sha256:39d6a2f743553c0db170f053156802041f148c8f7f2afb63680e21c78c8ced83`  
		Last Modified: Wed, 15 Apr 2026 22:52:41 GMT  
		Size: 392.3 KB (392282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d05862c99867615281cf88c286bb0402afc88f0150980a3d2431452efb32a9cf`  
		Last Modified: Wed, 15 Apr 2026 22:52:41 GMT  
		Size: 16.4 KB (16353 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:7e899153d78138a0c140ec3649b822e55bdfda85a79358917372258e16a7580a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116524478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bdf880db3ef2db8d320c97df22ebf4d09562b97dec5570b5b40e9c06b2b1df`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:23:20 GMT
ARG version=8.482.08.1
# Wed, 15 Apr 2026 20:23:20 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 15 Apr 2026 20:23:20 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:23:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 15 Apr 2026 20:23:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 15 Apr 2026 23:18:56 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 15 Apr 2026 23:18:56 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 15 Apr 2026 23:18:56 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 23:18:56 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 23:18:56 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 15 Apr 2026 23:18:56 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Apr 2026 23:18:56 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 15 Apr 2026 23:18:56 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 23:18:56 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 15 Apr 2026 23:18:56 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 15 Apr 2026 23:18:56 GMT
ARG MAVEN_VERSION=3.9.14
# Wed, 15 Apr 2026 23:18:56 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Apr 2026 23:18:56 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Apr 2026 23:18:56 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Apr 2026 23:18:56 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d31962388d49f10d3593e394a384b818c01046e78cf4213c87494773368e25`  
		Last Modified: Wed, 15 Apr 2026 20:23:34 GMT  
		Size: 100.6 MB (100563600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478419f08e3bcc16615677917cf407a5708216dd5a112827a03383b7bb45ef9b`  
		Last Modified: Wed, 15 Apr 2026 23:19:04 GMT  
		Size: 2.4 MB (2448777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6267fea9e499350b5cd96284a2522d5ed163dba774aba7a1674c9b1831990f6`  
		Last Modified: Wed, 15 Apr 2026 23:19:04 GMT  
		Size: 9.3 MB (9311194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba927fdd96620311ef3eff4f49f5ee7824b45925fe88b8fbd79323575c200c20`  
		Last Modified: Wed, 15 Apr 2026 23:19:04 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701e8e2957b1b38126eeb3c6527452c19a902388f4557997cd19c11e495bed16`  
		Last Modified: Wed, 15 Apr 2026 23:19:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:0f950906f463c9aa50c656115a5fd8241537a79f4a2d60449a75b9e8cd856818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.2 KB (408238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908deb4cb8a37bb34e68566fafeec8ca9a106dd9c6015f0c04d9b062f6154dff`

```dockerfile
```

-	Layers:
	-	`sha256:dce9bcdd981861a6bbdf167faa5083005106e7b9be75dba912bd318f38b7a5f5`  
		Last Modified: Wed, 15 Apr 2026 23:19:04 GMT  
		Size: 391.8 KB (391752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3451b4edd8e0911e237a2e09e6e2e6b0f590cfc96b7ea9f011164c5dbe2b6e9d`  
		Last Modified: Wed, 15 Apr 2026 23:19:04 GMT  
		Size: 16.5 KB (16486 bytes)  
		MIME: application/vnd.in-toto+json
