## `maven:3-amazoncorretto-17-alpine`

```console
$ docker pull maven@sha256:3501523585b3fed89e5d6eb6a9dee191b4b5877af9f9d67c383e567a1804c0be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-alpine` - linux; amd64

```console
$ docker pull maven@sha256:d7ac9752578325d73c0018c3e33155877e84bc0d58a8810c00cceafa58ddd851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160754368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d372802e80e2e7ffd6df13bd8dec90a61034339830f3aacfd21d06264f1423b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 24 Sep 2024 11:57:06 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacd015f7c1503cd701121ba71569d133f255bffa779a04e5fb151071146062a`  
		Last Modified: Tue, 07 Jan 2025 03:30:26 GMT  
		Size: 145.6 MB (145649292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7404e1f357eaad96f4b3b2ebb755cae472d19289da6f992d751cf4582b86fb`  
		Last Modified: Tue, 07 Jan 2025 04:23:29 GMT  
		Size: 2.3 MB (2319604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46bd0f609a6d9e45388f5018ef5d28caf1076f7be55ce2e5b31d2632f890d37`  
		Last Modified: Tue, 07 Jan 2025 04:23:30 GMT  
		Size: 9.2 MB (9170434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee7b22891729fc023a795964246a61f496a35ab3216586cd79eacd9cff90c71`  
		Last Modified: Tue, 07 Jan 2025 04:23:29 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705429f73e5d1b2a3fd52c5e1fa13e8431427dce6d764aeda1b0246b9eced3c1`  
		Last Modified: Tue, 07 Jan 2025 04:23:29 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:d63563d0dda62ec4e9cb35f4676868ff7f4d0ba0ee924ad5b7032d1b9b632ad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.8 KB (531834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de258443c3330325867c26048bd2301f66bc3ecdc8ff7ef99f79b30d6b239f0`

```dockerfile
```

-	Layers:
	-	`sha256:472a8f6b1e4be7b171b5f8dd38d4f63fe47da1442528081949446dbcbef729f3`  
		Last Modified: Tue, 07 Jan 2025 04:23:30 GMT  
		Size: 515.4 KB (515437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bc8166638d58da94b851c2849d2d6fbd6c94edc3354372050318597669a7b54`  
		Last Modified: Tue, 07 Jan 2025 04:23:29 GMT  
		Size: 16.4 KB (16397 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:ab64376b142634ecc064478a35946e63048e2da754e21fb65595a6c60aa3510d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159577315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed08ea7603da9161c39fcac9a50fb6eb3c799f201b9ac991300b42ebad16da20`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Tue, 07 Jan 2025 19:45:03 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0052ba8722e483dc5f301c56915d49a286849a6e3e240007b8bf07dadfb85bb3`  
		Last Modified: Tue, 12 Nov 2024 11:10:25 GMT  
		Size: 143.9 MB (143934744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0311b0a04a4dc5036cf5e84d373400ba1a464c58f3baba04ab62fd264db36a41`  
		Size: 2.4 MB (2383371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c973a4dc64f67174c5398d30ab3beca2eb91591ca3552646ba9e6f242643e12`  
		Last Modified: Tue, 10 Dec 2024 02:20:58 GMT  
		Size: 9.2 MB (9170433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e357f21b97ebeb7bb24b1ec1e2492b081262c23eb9365b176aa1e8d13032bbc7`  
		Last Modified: Tue, 10 Dec 2024 02:20:57 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21291da4211878e805e31869c20c8e35cbd6ce3284dfb9b5a68ff1b7491b0de1`  
		Last Modified: Tue, 10 Dec 2024 02:20:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:0020cf837d876134275d4f4eb52f7c5ad2b77981834306aaecfc4a63b5a607cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.4 KB (533394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e30c704d1c3ac623c5ecd3e653bb3bd46af79241e017ce4d8bdb586f4ed3c5`

```dockerfile
```

-	Layers:
	-	`sha256:6309b0691ddca97f3d9697b70e0f1e468dccbeb615c46167e531750f1cc9c21a`  
		Size: 516.9 KB (516863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c62e76104e3d6822aef504550008219a46d83b4a32e3d6f813ef56fa8935dd46`  
		Last Modified: Tue, 10 Dec 2024 02:20:57 GMT  
		Size: 16.5 KB (16531 bytes)  
		MIME: application/vnd.in-toto+json
