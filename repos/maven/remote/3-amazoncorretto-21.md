## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:f004b534b13f0a785ad0a904ed012606b0939b40344939fe7e4cf1be9a3f92e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:419aa2ab8fa708acf4aa6a3c7d2ef5098ce0ea3212c5c98eee530183348853e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.3 MB (385288286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2d7f41636d59e7b9cf1969861de7edd421fc0703d8903c213f3250aa57eaa7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 01 Feb 2024 23:54:01 GMT
COPY dir:2df8955a095aec5442eb78c5eb2b2d5ec8efe73514e149ef530142d09c10ab53 in / 
# Thu, 01 Feb 2024 23:54:02 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:45:21 GMT
ARG version=21.0.2.13-1
# Fri, 02 Feb 2024 00:45:48 GMT
# ARGS: version=21.0.2.13-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 02 Feb 2024 00:45:48 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 00:45:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:27aa8a7b34d9d00065712ed12b31cb2ce237d67023e031cf6617677322aff470`  
		Last Modified: Fri, 02 Feb 2024 00:55:32 GMT  
		Size: 165.7 MB (165679845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be635fb518d9875ce68cb67b656ea450428cf3a74642233a198bba83f389a3c`  
		Last Modified: Fri, 02 Feb 2024 13:13:06 GMT  
		Size: 147.5 MB (147480646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb5d88f43d49c9a4e94debd88e42deec6d0783172421939f0d7ae4cc23aaa66`  
		Last Modified: Fri, 02 Feb 2024 13:12:53 GMT  
		Size: 9.5 MB (9479932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb42cbe95352c28d8a90c2d536580c6b687612fe31f6f898a9a52d1eb13620e0`  
		Last Modified: Fri, 02 Feb 2024 13:12:53 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10f5cc89fafa19dd11f85bb409d37a9e8a91f6a28947bf06a76acd5a7c2546d`  
		Last Modified: Fri, 02 Feb 2024 13:12:53 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39128f8d2cb72212a9c80c8688a56ab8d43e664c6bac16edc9f7671816ce2877`  
		Last Modified: Fri, 02 Feb 2024 13:12:53 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:1b8cd5f4642c95c88336438db5b8bc3dc4b1feacf842aeddd9b44132ab0c1aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.0 MB (356034822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523cbfa06770860f006320ec5446dd09005db0304240d4f99d8052a3ed0ee0aa`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 01 Feb 2024 23:30:50 GMT
COPY dir:9aa2a0617061f7d0def778dac1581f965a33bb26f84a69dab1fef189d1a60261 in / 
# Thu, 01 Feb 2024 23:30:51 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:54:58 GMT
ARG version=21.0.2.13-1
# Thu, 01 Feb 2024 23:55:19 GMT
# ARGS: version=21.0.2.13-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 01 Feb 2024 23:55:21 GMT
ENV LANG=C.UTF-8
# Thu, 01 Feb 2024 23:55:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:fb59fe6197271a3523b658a82372cedfb8effaade5362f27392bad6f702f4a6a`  
		Last Modified: Fri, 02 Feb 2024 00:04:15 GMT  
		Size: 163.7 MB (163663602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df3a28e8cdef8ae6573f90dd8f94ec0d7b7a3d65bd4bc8ca1148c774e89c343`  
		Last Modified: Fri, 02 Feb 2024 03:45:40 GMT  
		Size: 118.4 MB (118436682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f3091633fd3af36ee7443be13c666cef6e89063d6dc12392ab6e41cef270ea`  
		Last Modified: Fri, 02 Feb 2024 03:45:32 GMT  
		Size: 9.5 MB (9479942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b4123c16d8af6f9f6407bfa949a86b85c1ae59461706cfa9b11f4b61f68d84`  
		Last Modified: Fri, 02 Feb 2024 03:45:31 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c00998b80186e47a5f64a1b65249645798a20c79149c2b1a24ad09e907af08`  
		Last Modified: Fri, 02 Feb 2024 03:45:31 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dd17a36bc49c3b59a535e434672cc85b2e3aca31d8de5c65b73086659bd38d`  
		Last Modified: Fri, 02 Feb 2024 03:45:31 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
