## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:87bdad9ddfc2631ab8857b56c1aa9542a15580b5ca36513770979e42f35c3934
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:492b311840e12a007dac96c5dffa2ca03da07df3c203551e93bd78e298df3fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.8 MB (354840700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732cf6f8e0200f69fd723e434fde90ae07921b00686bedbafb5f952cad5ca649`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 03 Apr 2026 22:00:43 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:00:43 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:11:57 GMT
ARG version=1.8.0_482.b08-1
# Fri, 03 Apr 2026 22:11:57 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 03 Apr 2026 22:11:57 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:11:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 03 Apr 2026 23:15:13 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 03 Apr 2026 23:15:23 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 03 Apr 2026 23:15:23 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 03 Apr 2026 23:15:23 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 03 Apr 2026 23:15:23 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 03 Apr 2026 23:15:23 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 03 Apr 2026 23:15:23 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 03 Apr 2026 23:15:23 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 03 Apr 2026 23:15:23 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 03 Apr 2026 23:15:23 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 03 Apr 2026 23:15:23 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 03 Apr 2026 23:15:23 GMT
ARG MAVEN_VERSION=3.9.14
# Fri, 03 Apr 2026 23:15:23 GMT
ARG USER_HOME_DIR=/root
# Fri, 03 Apr 2026 23:15:23 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 03 Apr 2026 23:15:23 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 03 Apr 2026 23:15:23 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5e0c2ef2594e62ec562f5df2ec3efec8dcb41bc052b756c68995456ef5a13ec6`  
		Last Modified: Thu, 02 Apr 2026 08:04:33 GMT  
		Size: 63.0 MB (62955301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aed3b592a48445e98eb3cbef3f221e49ddff0fb5de500494feceb697bdf859c`  
		Last Modified: Fri, 03 Apr 2026 22:12:13 GMT  
		Size: 76.1 MB (76123555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3c6bdc86e667ee8956a2f62c5ee1a0ba625eca7a526b748ed517f8addc478e`  
		Last Modified: Fri, 03 Apr 2026 23:15:53 GMT  
		Size: 176.4 MB (176375666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e960eac27673d23b144273f73c142a89b7c02ccc055c01b8d0509e3481f0a96`  
		Last Modified: Fri, 03 Apr 2026 23:15:49 GMT  
		Size: 30.1 MB (30073948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8064594319157f6cfd7767eeef13d6b286a052f718de96814e624eb0d423ccbd`  
		Last Modified: Fri, 03 Apr 2026 23:15:48 GMT  
		Size: 9.3 MB (9311187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed834742f5c374d9294af957a6f1c5e9d6110e53b328f2e6f0c32f8606c5359d`  
		Last Modified: Fri, 03 Apr 2026 23:15:47 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ff6d27402a429c17cb20320a62cb4bf8f01e65891a20021ac0a3078f296610`  
		Last Modified: Fri, 03 Apr 2026 23:15:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:237717b82d1ca8c70877c8685d6ed5d33579bc7768abd22e22f38c89715cb095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6791889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c518d148c8c0f9969596437a05bd623c70dba2695e4e1f42142cddcf950153c`

```dockerfile
```

-	Layers:
	-	`sha256:52229bf8cbe8f9408af1b48e6ca38dffaed764d0e13885ceafa7bd9144853a01`  
		Last Modified: Fri, 03 Apr 2026 23:15:47 GMT  
		Size: 6.8 MB (6773702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b0b4e9da870665c21f1da31931b5c1957fe1917f9984900041a8080f292c728`  
		Last Modified: Fri, 03 Apr 2026 23:15:47 GMT  
		Size: 18.2 KB (18187 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:08c2ba64175f10c5a0d9033db113e191bb5ed140139b46dee1f33fd369da6c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.2 MB (317150060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66d65abbf3e20979561329239d5209b916db2b48e7614c423a9de2a6bf2ce58`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:12 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:09:58 GMT
ARG version=1.8.0_482.b08-1
# Fri, 03 Apr 2026 22:09:58 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 03 Apr 2026 22:09:58 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:09:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 03 Apr 2026 23:15:38 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 03 Apr 2026 23:15:46 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 03 Apr 2026 23:15:46 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 03 Apr 2026 23:15:46 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 03 Apr 2026 23:15:46 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 03 Apr 2026 23:15:46 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 03 Apr 2026 23:15:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 03 Apr 2026 23:15:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 03 Apr 2026 23:15:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 03 Apr 2026 23:15:46 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 03 Apr 2026 23:15:47 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 03 Apr 2026 23:15:47 GMT
ARG MAVEN_VERSION=3.9.14
# Fri, 03 Apr 2026 23:15:47 GMT
ARG USER_HOME_DIR=/root
# Fri, 03 Apr 2026 23:15:47 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 03 Apr 2026 23:15:47 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 03 Apr 2026 23:15:47 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2f277ffe2904df7c0598e4c64e34d0fbf604645e12c7f6d64d32c23097854f29`  
		Last Modified: Thu, 02 Apr 2026 08:04:39 GMT  
		Size: 64.8 MB (64802839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3d731049d7c23d3810364ce54f552fe15f577c03087e2ce9ad61877eee7ff9`  
		Last Modified: Fri, 03 Apr 2026 22:10:13 GMT  
		Size: 59.9 MB (59923156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2337844987b245675222eb4adfda9bdeafd188837bcbc4f3b7e7f1b292de128a`  
		Last Modified: Fri, 03 Apr 2026 23:16:15 GMT  
		Size: 151.9 MB (151901481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666fc4b7e86643270c137d32a059ea6ed55631a2aaa88ad9a05eaa719119c20f`  
		Last Modified: Fri, 03 Apr 2026 23:16:11 GMT  
		Size: 31.2 MB (31210355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1fe148f25703e1ff130bce200b83571383643c021b631a1e0bc6c5aa6ae930`  
		Last Modified: Fri, 03 Apr 2026 23:16:10 GMT  
		Size: 9.3 MB (9311185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f77ffe616bcf8aad34bce6d6741dd6c92a2bf1c78b456b8468a8bccdd901b4`  
		Last Modified: Fri, 03 Apr 2026 23:16:09 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49144a6027d382e8040ac6e96724611480c6c7e33f94ef1478be1b47ea69729a`  
		Last Modified: Fri, 03 Apr 2026 23:16:11 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:f97afa7880ee56606e4861d8d131e70f86fdf2301678e748da54b2468bcb43b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6769234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa36d69d6d88925bcdf8029f80b9366b59114b9510c7d42bc320699bf8c829f`

```dockerfile
```

-	Layers:
	-	`sha256:f876685cae36e97f5ff1542921f4279e7e8274823627eee30f66f5d3c62b284e`  
		Last Modified: Fri, 03 Apr 2026 23:16:10 GMT  
		Size: 6.8 MB (6750899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03dd6be7208d2703a6cc8ae6cb5e6e77eef8b63cf7ad9f750cbe9d00719c1bf8`  
		Last Modified: Fri, 03 Apr 2026 23:16:09 GMT  
		Size: 18.3 KB (18335 bytes)  
		MIME: application/vnd.in-toto+json
