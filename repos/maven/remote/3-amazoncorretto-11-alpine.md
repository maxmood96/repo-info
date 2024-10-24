## `maven:3-amazoncorretto-11-alpine`

```console
$ docker pull maven@sha256:3ea6f4bea9e923b3b592fb044f996988d2ad6befccb987e5917ebf9dedc377f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-alpine` - linux; amd64

```console
$ docker pull maven@sha256:edc5b8335c54e07f0333561f2fb1f3c12170650f9450958976fe581f879f18aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157023566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51616e52a6c1ace0b4af57bf98b258bc8da70b9928e8cbe7a04b50f73c98093`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 24 Sep 2024 11:57:06 GMT
ARG version=11.0.25.9.1
# Tue, 24 Sep 2024 11:57:06 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:0e37f65f08727562421b90179a5bc71a9db33e28fb6e68c95b4a998e1643d76f`  
		Last Modified: Wed, 16 Oct 2024 17:56:12 GMT  
		Size: 141.9 MB (141908598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee9151d5d4ae9a4fc6d153ec70b2d91ab923992dfceaf862c8f0671f94e9ced`  
		Last Modified: Thu, 24 Oct 2024 02:55:37 GMT  
		Size: 2.3 MB (2319687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0bd662deca9a1952d8b0820877a3742fbf5f1e8f011a381dcf431079558eee`  
		Last Modified: Thu, 24 Oct 2024 02:55:37 GMT  
		Size: 9.2 MB (9170434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a54697f177e06294db3d866b1f73c03d996533bbd58dfecf9948fde4663f1c`  
		Last Modified: Thu, 24 Oct 2024 02:55:37 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6127dd07285fd577b8dc1f0fae38c4ba06676eae995b2b70e672695cd05aa917`  
		Last Modified: Thu, 24 Oct 2024 02:55:37 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:255efacd2f3ce67075e29b25c1f20924ff06f79f53dffcef5a5e67d0a2001012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.7 KB (540660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7a44cdc0b73aa534ce019088f34ab0ee46007b3c19c91a3c7be0db5a90f941`

```dockerfile
```

-	Layers:
	-	`sha256:597406b2712f6afcbf3fdf1f948bc2d679a3bf325331259aca0c047cea5a2e22`  
		Last Modified: Thu, 24 Oct 2024 02:55:37 GMT  
		Size: 524.3 KB (524263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaee22cacb94afba29daa15ebf1e2a2127a7ed20d86cc1c86a61dec855d55de8`  
		Last Modified: Thu, 24 Oct 2024 02:55:37 GMT  
		Size: 16.4 KB (16397 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f4e7192cf8e3bde445ad8c1047432d2c751d2cb906b34c0f95ea78cf2c32cd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155673658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a48709daf574e0af27c98c46e4211489f662a56b1d7b0215ca80637ff40cca`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 24 Sep 2024 11:57:06 GMT
ARG version=11.0.25.9.1
# Tue, 24 Sep 2024 11:57:06 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:11d75e0b84f6a291f6a433e35e083f59f3d0af9f4e372a4ba452f6ad81e4ab3e`  
		Last Modified: Wed, 16 Oct 2024 18:19:12 GMT  
		Size: 140.0 MB (140030791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b11eaed66de38942468d66961f40e5d8697ff5d15687e56af0b8a758deda4a`  
		Last Modified: Thu, 24 Oct 2024 13:15:50 GMT  
		Size: 2.4 MB (2383748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85556582879ec7386dd6751f92b610e6f0e90be0a424eb786faae0c5019ab56`  
		Last Modified: Thu, 24 Oct 2024 13:15:51 GMT  
		Size: 9.2 MB (9170433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c524e537a1e357e1d418920f1a536ed0fc378b1888e6ca4ccaa8e01db6c6d39`  
		Last Modified: Thu, 24 Oct 2024 13:15:50 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06889b5c505cf30e1c2225e9c23bfe56a9dad33cc957445e2b6ba41c2ad31e25`  
		Last Modified: Thu, 24 Oct 2024 13:15:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:5b2d5fd5e472d6316983fe3f6da68936091f990bd58ce06e2d9371a01c89def4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.9 KB (540874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfebe4c04fd39f159b386ae358de54fba575ed0f7f2150daed1f04714b9b0227`

```dockerfile
```

-	Layers:
	-	`sha256:ba81f3a5858107384e52ddf2c64e2fbd3aba0a107cf7a0d4d49f9db4160cafaa`  
		Last Modified: Thu, 24 Oct 2024 13:15:50 GMT  
		Size: 524.3 KB (524307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2786ceb659767267b918fe36ee79abcf70b22fc349b7e769085f0dfc38af299f`  
		Last Modified: Thu, 24 Oct 2024 13:15:50 GMT  
		Size: 16.6 KB (16567 bytes)  
		MIME: application/vnd.in-toto+json
