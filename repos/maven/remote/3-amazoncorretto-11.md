## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:6d119ff5b62b551b417536420c96e067beaffc4c628041c6f9774cc791302ffe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:0851c8cf33d8a134545aa62adc9b6cf9671d4fe896a8aacea7f5f99454a63299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.2 MB (428162606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce53bd541fdb1da77913cc0d27b4ab7713b3e1bf943c04991522aabdea6c4da5`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 08 May 2026 22:56:20 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:56:20 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:17:53 GMT
ARG version=11.0.31.11-1
# Sat, 09 May 2026 00:17:53 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 09 May 2026 00:17:53 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:17:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 09 May 2026 01:24:04 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Sat, 09 May 2026 01:24:11 GMT
RUN yum install -y openssh-clients # buildkit
# Sat, 09 May 2026 01:24:11 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 09 May 2026 01:24:11 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 09 May 2026 01:24:11 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 09 May 2026 01:24:11 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 09 May 2026 01:24:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 09 May 2026 01:24:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 09 May 2026 01:24:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 09 May 2026 01:24:12 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 09 May 2026 01:24:12 GMT
ARG USER_HOME_DIR=/root
# Sat, 09 May 2026 01:24:12 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 09 May 2026 01:24:12 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 09 May 2026 01:24:12 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3f708fc5705625846e206621966842bfead7ee5b8e4fc20aab0c77c563600126`  
		Last Modified: Wed, 06 May 2026 07:46:46 GMT  
		Size: 62.9 MB (62859738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e464088dbd5f6653e4e0c07b5f2d527d722f3bf507fd9fbb34d5e1cde22539`  
		Last Modified: Sat, 09 May 2026 00:18:14 GMT  
		Size: 148.1 MB (148131092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df604100149c948b503bb5f29d231b768c1208b08b1bc15881e6e8568defede8`  
		Last Modified: Sat, 09 May 2026 01:24:41 GMT  
		Size: 177.8 MB (177775585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af409439de71603c1e6005602d254522373ff0dab29947308f5be3193346c5dc`  
		Last Modified: Sat, 09 May 2026 01:24:37 GMT  
		Size: 30.1 MB (30082923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eff195804461e6007a3ea78c9ec06b6694ae17bfb2768465975b864cba36e12`  
		Last Modified: Sat, 09 May 2026 01:24:36 GMT  
		Size: 9.3 MB (9312258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d2b3c1509965109dc871a94376209fb60c5526707757f0243d96bd55bab630`  
		Last Modified: Sat, 09 May 2026 01:24:35 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2204ea12c857c3da100386b8ddcf1532d0ef341a64dfea1e332f5dfd2ad7776`  
		Last Modified: Sat, 09 May 2026 01:24:36 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:4b127e197eedbd4ef684304a487a08f1302c2ab0e58a09ba54b12d0c3e844c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6956005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad3c10ee0e87eb84dd49593709367291184d9195cc0c4c1ecbd47dce1550671`

```dockerfile
```

-	Layers:
	-	`sha256:2109743f90395c2251ac91f1fd9868c5db18941d43007d174be1fe6d2db9e4f2`  
		Last Modified: Sat, 09 May 2026 01:24:35 GMT  
		Size: 6.9 MB (6939655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeba9e4d17f6dd0f0296404575e7a22cd8ea1c6a6fb17f6c7d758a4a7cd86017`  
		Last Modified: Sat, 09 May 2026 01:24:35 GMT  
		Size: 16.4 KB (16350 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:da2d742d837cc36231b9bb14a7d65ecc97f34038e51109fca8d88437b47ac02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.1 MB (404082129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8490bd332f3a2f75054899c154532d3c63148d709d64bc997d1585dcfbc9d65d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 08 May 2026 22:48:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:14 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:15:11 GMT
ARG version=11.0.31.11-1
# Sat, 09 May 2026 00:15:11 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 09 May 2026 00:15:11 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:15:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 09 May 2026 01:48:39 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Sat, 09 May 2026 01:48:47 GMT
RUN yum install -y openssh-clients # buildkit
# Sat, 09 May 2026 01:48:47 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 09 May 2026 01:48:47 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 09 May 2026 01:48:47 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 09 May 2026 01:48:47 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 09 May 2026 01:48:47 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 09 May 2026 01:48:47 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 09 May 2026 01:48:47 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 09 May 2026 01:48:47 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 09 May 2026 01:48:47 GMT
ARG USER_HOME_DIR=/root
# Sat, 09 May 2026 01:48:47 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 09 May 2026 01:48:47 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 09 May 2026 01:48:47 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:835dd3779a793c24eeba54a176badcbf0ecf82042603b5459dd57e14ad679d47`  
		Last Modified: Wed, 06 May 2026 07:46:52 GMT  
		Size: 64.8 MB (64808915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb0a5f3a3c9dc710ff191a89cf4a8c47f22b985f703039c16f8aa64c070c82c`  
		Last Modified: Sat, 09 May 2026 00:15:32 GMT  
		Size: 145.4 MB (145369524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf87cac4b6cde5a971ee111e8a2fd3b7fcf26bfb36537a75ad9a06518d6cec34`  
		Last Modified: Sat, 09 May 2026 01:49:15 GMT  
		Size: 153.4 MB (153376836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0d33aab35e79cd8ea98cf0fe8236ef8de4d3138d0536a758fbc38d983d9b31`  
		Last Modified: Sat, 09 May 2026 01:49:13 GMT  
		Size: 31.2 MB (31213598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60e5257c75a4487fdc2b8af455a3df8bc44c1ce0524b49cd89f415b787a022a`  
		Last Modified: Sat, 09 May 2026 01:49:12 GMT  
		Size: 9.3 MB (9312247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12064c8d4e7120963c766da57957b7436bbcd0c8378d0f1efe833a3e3c85196e`  
		Last Modified: Sat, 09 May 2026 01:49:11 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b22ed22b903f0b86f1e0a77cc17baf58d31ff3d9154c81bbbb30f31501e81c`  
		Last Modified: Sat, 09 May 2026 01:49:12 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:ac1c723588b6dd8586459beacc98cb6940c00757640dc75c99192daa8bc92c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6954357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85b3f7d3293080b5cb87fc5c40818e31922242e8b9dde4cd386d55e333417f62`

```dockerfile
```

-	Layers:
	-	`sha256:c07751142624f948e082c800ff5ca21e13f0f45e684cc13797a9acbda0889966`  
		Last Modified: Sat, 09 May 2026 01:49:11 GMT  
		Size: 6.9 MB (6937859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:076912778ee64c71c9f5be98fcd8f739ef2dc087d0790b786b34cbe3711b2cf9`  
		Last Modified: Sat, 09 May 2026 01:49:11 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json
