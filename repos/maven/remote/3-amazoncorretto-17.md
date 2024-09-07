## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:e2a54bb3e1c20cc9c3886dd12e19d758c48b9d8a3b378dddf12f6dde5d3dc5c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:4bc7aa23b6647dd5218ad1bed56753867cbe55612717142af59179e3d33aa03e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.5 MB (402458200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7ec6d0b9a72a03176312ec27d401fa6c2e2f41befa3cf49c7c8aee284899e3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 19 Aug 2024 08:57:28 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7f8efc14a219454ff8f309d236d31a55327a6ff05dda42df51689619d9a34fdc`  
		Last Modified: Fri, 06 Sep 2024 18:59:36 GMT  
		Size: 62.7 MB (62695547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387e286eea9fd83af4986c4a394dd768831fd092063ae1bece6cc56acf8d77b4`  
		Last Modified: Sat, 07 Sep 2024 01:05:56 GMT  
		Size: 152.3 MB (152263145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91820b7a7c7770ea8a55f8308c7545bfbaafa5f651479d7e7e1309c3a275199e`  
		Last Modified: Sat, 07 Sep 2024 01:56:34 GMT  
		Size: 148.2 MB (148244796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bddee47581ce65e670b0184e07dab9cc067db8786399caff475b10bc8969be9b`  
		Last Modified: Sat, 07 Sep 2024 01:56:32 GMT  
		Size: 30.1 MB (30083232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c388e6e1a6ff5b0b60220a5cea37a066cb10b56f4e6a74e92850c8521b603c10`  
		Last Modified: Sat, 07 Sep 2024 01:56:32 GMT  
		Size: 9.2 MB (9170440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7cc3d8efc5714465fb96fa182b41a0953e32abad361193d54314497e3d02379`  
		Last Modified: Sat, 07 Sep 2024 01:56:32 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884228b30b5150460c0c086438ea6bfd3ce2e41d1fdfff14e87b1e349debf6aa`  
		Last Modified: Sat, 07 Sep 2024 01:56:32 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:b58e31b8680c8de620b7cee69d4ed58f2b7c37c87102ce5b48e1b793746b9c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6934170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf5fc3f3a7d096a1731d79d15d358970f08fb2c055236ae83058d47746d67b6`

```dockerfile
```

-	Layers:
	-	`sha256:4c1e9ceec3c7b4296be89f76e93f9f43696308c75d3c2a642fca0c8e12b7a8d2`  
		Last Modified: Sat, 07 Sep 2024 01:56:32 GMT  
		Size: 6.9 MB (6915974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e793cdb5693d0e6a7ab824b07bbfc4eac5c62ac73890987070609de02747048`  
		Last Modified: Sat, 07 Sep 2024 01:56:32 GMT  
		Size: 18.2 KB (18196 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:417148f9470a26fe4e4fed7a5b9522864dc65d7ac0595c4b7969ddc3e3dbb09d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.2 MB (379198983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbe66346df0789e7c4b93e669fa7bbb4163b08f2d5f05ec4a1c81bb89cc0266`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 19 Aug 2024 08:57:28 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:90f49a0942af5d23537faf4773696e5a1ede92273c5b8379a6acc52111436bb8`  
		Last Modified: Tue, 20 Aug 2024 21:34:48 GMT  
		Size: 64.6 MB (64587135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38474b5c05d2b77230fffc123167a19f2ef0528eacc20ac5d5c44d6fd1fadfe5`  
		Last Modified: Fri, 23 Aug 2024 02:26:18 GMT  
		Size: 150.9 MB (150865193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dec828142625d6d0d29c1eb848b616bb56e2d1b467c47c393f56ec968c7e6b`  
		Last Modified: Fri, 23 Aug 2024 03:01:33 GMT  
		Size: 123.4 MB (123407020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34eae921b6da603e9e9ad5723ce55b79eadac3857090b245a7474548257dbd8e`  
		Last Modified: Fri, 23 Aug 2024 03:01:30 GMT  
		Size: 31.2 MB (31168163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971a931ca8b44110d85ad23a1c1613fc86670a5c583dd7afae1a00d6c2ac8e88`  
		Last Modified: Fri, 23 Aug 2024 03:01:30 GMT  
		Size: 9.2 MB (9170430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4613ab2502eb979b3d4d4f3754dd17e8697e7b160470abd543ebe2fe16a4bc`  
		Last Modified: Fri, 23 Aug 2024 03:01:29 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2e753b8ac0fe4c79df2052f98711cfda9f74a8c47a628ddb93d079c360c461`  
		Last Modified: Fri, 23 Aug 2024 03:01:30 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:56b91f587bf9e6da4e6a2898ea2bd17a7b99d18f00ada83327d5cbfc9f2583ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6932290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c07a3111583708c8365a3ed87bf7108305fedcd916bb4416c6fef184b60c5d5`

```dockerfile
```

-	Layers:
	-	`sha256:45a80d781a7acd00a25e4cd169003e5749097d1478233efa7c15648f0f70d4af`  
		Last Modified: Sat, 24 Aug 2024 03:17:31 GMT  
		Size: 6.9 MB (6913369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:660f370e0ca8600a34bf62008d2675ef614c04166ad418468eb39a9dc0b2491b`  
		Last Modified: Sat, 24 Aug 2024 03:17:22 GMT  
		Size: 18.9 KB (18921 bytes)  
		MIME: application/vnd.in-toto+json
