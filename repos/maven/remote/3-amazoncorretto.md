## `maven:3-amazoncorretto`

```console
$ docker pull maven@sha256:edcf6047b619ab60cdda7f2ea159f97d8269bacce918b4219856fa010aaf5a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:fbffc37938d600be0578fdd1761d22ecbeaae8ffd6d69b04d0e489767d757fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.6 MB (411614037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247c6261bfd53390f32d292e7f3dd3431b108d9269540c21ca7d1d51585cd0c3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=17.0.14.7-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:68b5eef1eb563a36e20df422ee1592c70689019fdd12cc4fdc4e4b24c31c1c77`  
		Last Modified: Thu, 27 Mar 2025 19:19:22 GMT  
		Size: 62.8 MB (62752889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20ea6810da602f5c914128478327d94321883aee9b0c8a02cc20b8a8282c9c4`  
		Last Modified: Thu, 27 Mar 2025 23:58:41 GMT  
		Size: 151.7 MB (151687302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e88a5eba58a11fc827720b16d862a6439a9b04bd7b4eade3a5b9ac214252da`  
		Last Modified: Fri, 28 Mar 2025 00:09:05 GMT  
		Size: 157.9 MB (157929152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc3007cf58dd1ead30e06e8dc83ee4e2d8599aa71833f9a9128dd8bfdf8c525`  
		Last Modified: Fri, 28 Mar 2025 00:08:50 GMT  
		Size: 30.1 MB (30073214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076840d26415f198c932ba516bbdc3d12cb7681f803c64527c7eb8593b9b4123`  
		Last Modified: Fri, 28 Mar 2025 00:08:49 GMT  
		Size: 9.2 MB (9170437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c43a09a4d1ab495bd699c07ee11b0098704fb39ce86d951f17daeb8a2ac8fef`  
		Last Modified: Fri, 28 Mar 2025 00:08:48 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54c1be2209b3ad5eeee29fd8f9d1bc3cc171c7568c12555cf30969f370ce814`  
		Last Modified: Fri, 28 Mar 2025 00:08:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:b3d88493a1b1f8414950c2f39fdb162f5345bc828adc7f7a8191908f8a41797b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6927939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fe1bd257774c62f9d28f2cf059a411ef36154ea53ef81593cbf8e0ac35f133`

```dockerfile
```

-	Layers:
	-	`sha256:394a9f564de5bc267d71e5a25799113d6f376f30a3a0e15481dde3e1c5df3068`  
		Last Modified: Fri, 28 Mar 2025 00:08:49 GMT  
		Size: 6.9 MB (6908437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ecfec59a27863557ae93c0100ee8b72e513022ade3126001b3f4d59ecfd64ab`  
		Last Modified: Fri, 28 Mar 2025 00:08:48 GMT  
		Size: 19.5 KB (19502 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:141fb3e4858e4b110970a9cf62ce20a24001513565ad534068d6e0cacd8a4b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.1 MB (389148471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b07388ab043fdd50a881246315a83dfc8e23a10cc8e57686686cdddd969d6a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=17.0.14.7-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:bf0d47d55e313b24603bbdfcf71df5fce9b23e8a6af770024f7d7c0282dd1e60`  
		Last Modified: Thu, 27 Mar 2025 19:19:37 GMT  
		Size: 64.6 MB (64565822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb0a04e32045bea8a36477ff07d28428a7ae7e142505376782ccaa20b05e7b`  
		Last Modified: Fri, 28 Mar 2025 00:13:29 GMT  
		Size: 150.3 MB (150303064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7078696b030dccaacbb9a31576d851dd2d4d24b873a289b3610a932627fa18a`  
		Last Modified: Fri, 28 Mar 2025 01:42:20 GMT  
		Size: 133.9 MB (133931236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e16680cda4e5168d27d4b3812928baf788005d7fb7ea8b566c01335a442f99`  
		Last Modified: Fri, 28 Mar 2025 01:42:15 GMT  
		Size: 31.2 MB (31176866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb02711b4b99fbc3ce1683cd8405bd100a3b1049d2f8b9dfd014abe2b0e8cd3d`  
		Last Modified: Fri, 28 Mar 2025 01:42:15 GMT  
		Size: 9.2 MB (9170443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be95302f4dbd0a6b4046c8795671808815e3df69af1cde8662d431da830da3ff`  
		Last Modified: Fri, 28 Mar 2025 01:42:14 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc363d44d61fd0dc735114065530d770b416a874e1ea795653512b10a3d66782`  
		Last Modified: Fri, 28 Mar 2025 01:42:15 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:1525e014c15fedc94b1ae0b598fc3f614d98e3ffb68a375b9f3c3201f2fdf07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6925582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f562adf05637c45066d6be2d502082a9ee019638653b1d9a5476bc92acab0349`

```dockerfile
```

-	Layers:
	-	`sha256:618e83805dbb9d6cc3fd982cd523607d6b7cc52952d53c11b7ee9b34c30f4dfe`  
		Last Modified: Fri, 28 Mar 2025 01:42:15 GMT  
		Size: 6.9 MB (6905884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2fed42d38c6e38e336a4cae544e3b4385e546c36892dff9afc86f073bfd7b85`  
		Last Modified: Fri, 28 Mar 2025 01:42:14 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json
