## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:c6003acdd39670161e3c40097ae618fd8b1dd5de5f84f415b9d9b28d8875a965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:6b0c6259be51fd649ca4530dc51a81894f50ce749d958a13a601c26257b78ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.6 MB (371588953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628400bcb6614d2befe8e96520076b9c00cf5ac9de2977f5e8135820c02a796e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 01 Feb 2024 23:54:01 GMT
COPY dir:2df8955a095aec5442eb78c5eb2b2d5ec8efe73514e149ef530142d09c10ab53 in / 
# Thu, 01 Feb 2024 23:54:02 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:41:33 GMT
ARG version=17.0.10.7-1
# Fri, 02 Feb 2024 00:41:57 GMT
# ARGS: version=17.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 02 Feb 2024 00:41:57 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 00:41:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 11 Dec 2023 11:12:11 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 11 Dec 2023 11:12:11 GMT
ARG USER_HOME_DIR=/root
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 11 Dec 2023 11:12:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 11 Dec 2023 11:12:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7c46e61fc0317cccadde1288fd50789f5fcc06bddf47082f5ba5894613f35b38`  
		Last Modified: Thu, 01 Feb 2024 03:07:26 GMT  
		Size: 62.6 MB (62646486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a5b4b3ba0577d3a5abe5d2151f49b917f2b765af4eba45d781c0750c35041a`  
		Last Modified: Fri, 02 Feb 2024 00:52:51 GMT  
		Size: 152.0 MB (151980697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ed8e5d28dabf5da7b395ab857d38d23481f91cfec8fc0c5011639c9f3f68f7`  
		Last Modified: Fri, 02 Feb 2024 13:12:25 GMT  
		Size: 147.5 MB (147480460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4ad99e2136d361222c95707c97b92dd37fcb03e137be9014aa63513680a2bd`  
		Last Modified: Fri, 02 Feb 2024 13:12:13 GMT  
		Size: 9.5 MB (9479933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a00a89644d1db4d5b61738b59e71f87a88745ae181f05bcf05395de6afd705`  
		Last Modified: Fri, 02 Feb 2024 13:12:12 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591501a0d7a5aef9468cdffc06f91ddbc036b9c8f703661c86b3dfe570f02a45`  
		Last Modified: Fri, 02 Feb 2024 13:12:12 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c407fc50434243506969febbd4909a00712b161856de0519c71c7284e6a9da2`  
		Last Modified: Fri, 02 Feb 2024 13:12:12 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:085f1c75674d0c2907f92a23ee78fb1d761e68317041e76b7493c8051abd833b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.9 MB (342923295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1ceced761c8bfe3d4999792e0daea3366ed37f64fda101401f1351452f2e8a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 01 Feb 2024 23:30:50 GMT
COPY dir:9aa2a0617061f7d0def778dac1581f965a33bb26f84a69dab1fef189d1a60261 in / 
# Thu, 01 Feb 2024 23:30:51 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:51:43 GMT
ARG version=17.0.10.7-1
# Thu, 01 Feb 2024 23:52:02 GMT
# ARGS: version=17.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 01 Feb 2024 23:52:04 GMT
ENV LANG=C.UTF-8
# Thu, 01 Feb 2024 23:52:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 11 Dec 2023 11:12:11 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 11 Dec 2023 11:12:11 GMT
ARG USER_HOME_DIR=/root
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 11 Dec 2023 11:12:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 11 Dec 2023 11:12:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:47443cfd9c92429d14dc57cc7a23137f39c4c124ae6551bb1f992c8dfbaee707`  
		Last Modified: Thu, 01 Feb 2024 08:21:29 GMT  
		Size: 64.5 MB (64453219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcc9a1a8335d60be2724428ee2f6a031fbb6649441064dbdd470a3d4be58e66`  
		Last Modified: Fri, 02 Feb 2024 00:01:31 GMT  
		Size: 150.6 MB (150552624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97072005c2f172272db15f8dae9514d3b703f98ef6647a2645d63e370fad699a`  
		Last Modified: Fri, 02 Feb 2024 03:45:02 GMT  
		Size: 118.4 MB (118436139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5cc0f3fd7ef8d543781c1a5658cc19d4d91c7cf5793ac637d2059acc06b316a`  
		Last Modified: Fri, 02 Feb 2024 03:44:53 GMT  
		Size: 9.5 MB (9479935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f4755c3d0ab956923822ccd23a54c78963463fb3c32dfd98224d0748f8fc9d`  
		Last Modified: Fri, 02 Feb 2024 03:44:52 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe8689d904430f31eb950ccdfe628985b5b62a98c4fc3d0e58fc70d8e8e6069`  
		Last Modified: Fri, 02 Feb 2024 03:44:51 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9fbbdb736178c1683730b17e5d15a6ea6fd584fa885c5592a9ae20ed65c23b`  
		Last Modified: Fri, 02 Feb 2024 03:44:51 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
