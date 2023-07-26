## `maven:3-amazoncorretto`

```console
$ docker pull maven@sha256:808bc12964c0323469dd5621b41b41ae3b1e24c499ee30bd1da5f7f12f9f64d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:b12d4f36808cfd8a6d2e4fc17e5b9d1cdc3d30d3aa216f457f7dd8beb6c4fd35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 MB (377789271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd65af733d633191131d6334f640d5022036b07cb71c1d0dd7c4382178ffb2b1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 26 Jul 2023 19:20:31 GMT
COPY dir:eb203b2e14f406c161ffae3b2fa7ec59db3f5a04437b6e040395c2bc34835c5f in / 
# Wed, 26 Jul 2023 19:20:31 GMT
CMD ["/bin/bash"]
# Wed, 26 Jul 2023 20:15:50 GMT
ARG version=11.0.20.8-1
# Wed, 26 Jul 2023 20:16:14 GMT
# ARGS: version=11.0.20.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 26 Jul 2023 20:16:15 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jul 2023 20:16:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 26 Jun 2023 13:48:06 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 26 Jun 2023 13:48:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
ARG MAVEN_VERSION=3.9.3
# Mon, 26 Jun 2023 13:48:06 GMT
ARG USER_HOME_DIR=/root
# Mon, 26 Jun 2023 13:48:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 26 Jun 2023 13:48:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 26 Jun 2023 13:48:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a8d554425610d474f28e23ecfc3224dd78fca045a5c09515dbf51a8606c33d8f`  
		Last Modified: Tue, 25 Jul 2023 11:25:06 GMT  
		Size: 62.5 MB (62451920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174e9a45c51abe09a7f25455b6e5379965f9937355361f9760bfad7aa1ff4ba6`  
		Last Modified: Wed, 26 Jul 2023 20:26:58 GMT  
		Size: 147.8 MB (147787043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92df9bad1d901cc3258ae44dba36110d3cb3e18010d927b938e5112485c22fa4`  
		Last Modified: Wed, 26 Jul 2023 21:00:15 GMT  
		Size: 158.2 MB (158221317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c0d70e8177d632d40809b3c6c5f76aa336ceb380d79ce1a59b9276aef643e0`  
		Last Modified: Wed, 26 Jul 2023 21:00:04 GMT  
		Size: 9.3 MB (9327608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f119cf506da91619588cc0c882af36fd963471bec24dae8846161cfc5048f5a4`  
		Last Modified: Wed, 26 Jul 2023 21:00:02 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b51442fc12c7f4e6a034853adb1bf3f54f0ffecf3fc1fc743bf0601be238daa`  
		Last Modified: Wed, 26 Jul 2023 21:00:02 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4c4fb92711e7dffa4618e84ca9ac13d0af826b745047fcdf95f8355bdf3f82`  
		Last Modified: Wed, 26 Jul 2023 21:00:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6eeb0a26890d2b87ebc087aa5117e64eb923e73815d2a57e75756e35b60a8e7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.2 MB (341166167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854f2980e1643313b8c2519a0bae824ac142e43da24b4eaf08196d4fc3fbed34`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 26 Jul 2023 19:39:59 GMT
COPY dir:680654fa7b59b44a83c6e6e3392ca226b5dd93f22761e5f1147351db4c3466cc in / 
# Wed, 26 Jul 2023 19:40:00 GMT
CMD ["/bin/bash"]
# Wed, 26 Jul 2023 20:19:03 GMT
ARG version=11.0.20.8-1
# Wed, 26 Jul 2023 20:19:23 GMT
# ARGS: version=11.0.20.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 26 Jul 2023 20:19:25 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jul 2023 20:19:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 26 Jun 2023 13:48:06 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 26 Jun 2023 13:48:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
ARG MAVEN_VERSION=3.9.3
# Mon, 26 Jun 2023 13:48:06 GMT
ARG USER_HOME_DIR=/root
# Mon, 26 Jun 2023 13:48:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 26 Jun 2023 13:48:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 26 Jun 2023 13:48:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:51a637e5b43ccbed5bec2958dc012693f30cc3c6b3a2760e6d675bedbae44e84`  
		Last Modified: Wed, 26 Jul 2023 19:40:35 GMT  
		Size: 64.1 MB (64129279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b17b5eebd6c82ddcb88fa2d048cb3b49d0a6d35f016831171e8f5ef11022d8c`  
		Last Modified: Wed, 26 Jul 2023 20:27:49 GMT  
		Size: 144.9 MB (144929943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb4df70c425419f8837bf520ce3ec5c8862af5505ad96b68d26ff94763f3410`  
		Last Modified: Wed, 26 Jul 2023 20:55:54 GMT  
		Size: 122.8 MB (122777950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495377b5970b437377016a77369e3dd7418871f905aa37901c2674ac9daaf4ad`  
		Last Modified: Wed, 26 Jul 2023 20:55:46 GMT  
		Size: 9.3 MB (9327612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960428845b0422e4ca79b8e5648323285682b143492b03efc2c2cb348ce778ac`  
		Last Modified: Wed, 26 Jul 2023 20:55:45 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5f5dff44fdb12820b2b09aca9e21c533c59b297bdd9aee0f1ac56aea5c23c1`  
		Last Modified: Wed, 26 Jul 2023 20:55:45 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681adf30cd2569c776bde662dc0cfe08c618f2ab13b364490d9d74bc691e4955`  
		Last Modified: Wed, 26 Jul 2023 20:55:45 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
