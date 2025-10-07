## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:98da5649684bf75817c8b5b58e76ca8dc46d112122bd7aac1ab703cbc8d85059
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:7917ead4f2c78d6138557a401a95620ee2eb3c630b543edd5fb9b55df7d98e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.3 MB (436318919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00b0f57c400282d640c063c93bb90e4949157331b5440b7303ecdc6b6db802e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=21.0.8.9-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=21.0.8.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sun, 21 Sep 2025 11:32:02 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Sun, 21 Sep 2025 11:32:02 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Sun, 21 Sep 2025 11:32:02 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 21 Sep 2025 11:32:02 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 21 Sep 2025 11:32:02 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 21 Sep 2025 11:32:02 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 21 Sep 2025 11:32:02 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 21 Sep 2025 11:32:02 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 21 Sep 2025 11:32:02 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 21 Sep 2025 11:32:02 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 21 Sep 2025 11:32:02 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 21 Sep 2025 11:32:02 GMT
ARG MAVEN_VERSION=3.9.11
# Sun, 21 Sep 2025 11:32:02 GMT
ARG USER_HOME_DIR=/root
# Sun, 21 Sep 2025 11:32:02 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 21 Sep 2025 11:32:02 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 21 Sep 2025 11:32:02 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:91f0f90aeef889cedc2e056e6976319ec5d96df70bf35b1d46092d2c1f375f2b`  
		Last Modified: Sat, 04 Oct 2025 04:29:16 GMT  
		Size: 62.9 MB (62940620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abd3da4721c571a064607ac8230042118beba854149f9b89f55bb43cb1512a6`  
		Last Modified: Mon, 06 Oct 2025 22:11:19 GMT  
		Size: 165.1 MB (165050979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e773d631560154aec97068b13bb07f96ca8eeab1f98603fdf7d5a20881ece8`  
		Last Modified: Mon, 06 Oct 2025 23:31:41 GMT  
		Size: 169.0 MB (169009646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a5b8d1a3668a9f02388c334dbd7986d9bed2bab0cbf6e38a49be2553c9955b`  
		Last Modified: Mon, 06 Oct 2025 22:15:08 GMT  
		Size: 30.1 MB (30074046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f6bb3cd9a71ac1ccb42e2b94dbdf6cbc1c69e0bc58470c3f9e2a95abbe8395`  
		Last Modified: Mon, 06 Oct 2025 22:15:03 GMT  
		Size: 9.2 MB (9242584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5a3bce6133d19462eb394031d30e4da882a1e23744d0985ac71fe9cce6255f`  
		Last Modified: Mon, 06 Oct 2025 22:15:03 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015c88d7847228fe05225eb2c0934f8d714deacb50190b269ffbfe948cc4173b`  
		Last Modified: Mon, 06 Oct 2025 22:15:02 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:c5084ef297b6eeaed37298d2436a2cd5f109a3600fca22a440f780e978e1a62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6947183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfdbd13c1094a31ec18a8a368abc53f526c2e7baf75eb88b31202d5b3b7d1fe6`

```dockerfile
```

-	Layers:
	-	`sha256:5858b585f9b47bb8d3f51fd18fe5e1c1192e6ff0cac2e4951eadef84091295bf`  
		Last Modified: Mon, 06 Oct 2025 23:28:10 GMT  
		Size: 6.9 MB (6928924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb727426db95e6c2a21b2464ef4a97c69e32daa7943ef342597e1bcbec4440e1`  
		Last Modified: Mon, 06 Oct 2025 23:28:11 GMT  
		Size: 18.3 KB (18259 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:e024021b8fbffd1ee10da8c076ef34cf3830ca9c099db5376ae76190c27f33e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.3 MB (413266362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4766db1cecc357cb58e29d78dfe87331e6e5c1d54fedf10b50db8dc9c1fe23f0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=21.0.8.9-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=21.0.8.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sun, 21 Sep 2025 11:32:02 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Sun, 21 Sep 2025 11:32:02 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Sun, 21 Sep 2025 11:32:02 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 21 Sep 2025 11:32:02 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 21 Sep 2025 11:32:02 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 21 Sep 2025 11:32:02 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 21 Sep 2025 11:32:02 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 21 Sep 2025 11:32:02 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 21 Sep 2025 11:32:02 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 21 Sep 2025 11:32:02 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 21 Sep 2025 11:32:02 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 21 Sep 2025 11:32:02 GMT
ARG MAVEN_VERSION=3.9.11
# Sun, 21 Sep 2025 11:32:02 GMT
ARG USER_HOME_DIR=/root
# Sun, 21 Sep 2025 11:32:02 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 21 Sep 2025 11:32:02 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 21 Sep 2025 11:32:02 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8b6c0dce7361457a1cee4518c5dc9c75ff3fa343c4460bdb254d7bd18bc1bf03`  
		Last Modified: Sat, 04 Oct 2025 18:25:08 GMT  
		Size: 64.8 MB (64793208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3602182be132a4d99034a4d5d48cb562b07140ee58186cb12024f7f5df2c29d`  
		Last Modified: Mon, 06 Oct 2025 22:12:36 GMT  
		Size: 163.1 MB (163112624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9807b3ea4e93c63b2875236046340033bb318f5af6cbcc96bd3afc7e8f693e32`  
		Last Modified: Mon, 06 Oct 2025 23:29:23 GMT  
		Size: 144.9 MB (144931553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ee697303d30adf3000486cba8d1b2d1eae8e16893184fac3c16309bae6f6db`  
		Last Modified: Mon, 06 Oct 2025 22:15:25 GMT  
		Size: 31.2 MB (31185355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ed57360d2b6ab65b4efae55fe2de222d10ef2f1f93554132074c9a1bfa96b3`  
		Last Modified: Mon, 06 Oct 2025 22:15:16 GMT  
		Size: 9.2 MB (9242576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb04e46e30459a101e40d45105e04d4cc59b12ea8a0deb42dee7bd16cda1d8b6`  
		Last Modified: Mon, 06 Oct 2025 22:15:14 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1fa0940c4bee686aab90e9431271d6007d2935091e7f804d0265c45f8f9d6b`  
		Last Modified: Mon, 06 Oct 2025 22:15:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:3a63064f8b4b638e323a7ab254f02efea983e631da940e4651b9ef6e572ca40e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6944730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7feac5c9b020893e8029347a053db190f1658dee94f78183457093317e1ebefb`

```dockerfile
```

-	Layers:
	-	`sha256:850a5b6640144c77b32c34a4812a187e58ca59dc1d4f88d51adc3af2fd31b690`  
		Last Modified: Mon, 06 Oct 2025 23:28:16 GMT  
		Size: 6.9 MB (6926323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a3883a553f5aeb7b2394afd9a0e05c357a34ddc56d5fede1767dbf71703736`  
		Last Modified: Mon, 06 Oct 2025 23:28:17 GMT  
		Size: 18.4 KB (18407 bytes)  
		MIME: application/vnd.in-toto+json
