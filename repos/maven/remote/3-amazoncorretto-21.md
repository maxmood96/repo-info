## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:5fed610fef7caea1380179190fac49a9a9d0f55ba9aae106668e62aaf58ea081
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:4968217be6c366efb59f90ad20391536bbf182dd1c808c02aa48e97ae2077c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.9 MB (419890453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d9ff156c2a7bf115cb4a82c54fcefcf990863f359b62e7edb67d245c283f7a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=21.0.6.7-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=21.0.6.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:9fe0de22bd8b7f693a2d87aff899a83b863c2f1cc5f64f563c01e4537bcf04e8`  
		Last Modified: Fri, 10 Jan 2025 22:01:24 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f4f4804f0ba33928a2a9292016fccac18bd4ad4e1909ab89da3073c65759b`  
		Last Modified: Thu, 23 Jan 2025 18:27:33 GMT  
		Size: 164.7 MB (164745502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f135d51c974d9106aed9adbe7a063ee8d3cc7c5ee732d35eefd811a5e3f7458`  
		Last Modified: Thu, 23 Jan 2025 19:27:39 GMT  
		Size: 153.3 MB (153288268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87917346ee709825b0813e850f78970c3d14c1a0bbc9fa404272a4e12dcb6bd7`  
		Last Modified: Thu, 23 Jan 2025 19:27:37 GMT  
		Size: 30.0 MB (30049377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c18d928480d1d2c7546c672b92f12ec58dec6bfdd3e7bc7b6eeb05232adc353`  
		Last Modified: Thu, 23 Jan 2025 19:27:36 GMT  
		Size: 9.2 MB (9170433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a69df2be0ee798b05e7ce3628a9fa04c8b199e26bdcf351a946ad33e1b5bd04`  
		Last Modified: Thu, 23 Jan 2025 19:27:35 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfffafe94dbd0f29ac1dacfe5f6154eb6f6159baed25f4a746f32200085c6c3e`  
		Last Modified: Thu, 23 Jan 2025 19:27:37 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:d3f35c808f9b20dbe4157b874b6e29066b6756bcaf1a2286c752304bc97c3058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6925288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25740d9c7f53097402c9927f0b0b990b5333c9430426d5cd67e3d2f8be55b406`

```dockerfile
```

-	Layers:
	-	`sha256:9d20a76fdef67b0828d7f08995d8794237aac06b7e9876fd7686a9486e31d4dd`  
		Last Modified: Thu, 23 Jan 2025 19:27:36 GMT  
		Size: 6.9 MB (6907058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2a3d29b5316dbd03b9f5e093cd648f0e769f74a07ce23ce734258f9f3e7f77d`  
		Last Modified: Thu, 23 Jan 2025 19:27:35 GMT  
		Size: 18.2 KB (18230 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:742f71148949cbd0ac00f5af3203d65b72fcd2334bb337d2e8a76a5bc1e3850b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.1 MB (397127725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3b6ebb9a80ff693f414aa6c2d4649fabb2c6b0e015ac95ccc8a3caaa9de54b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=21.0.6.7-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=21.0.6.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Fri, 10 Jan 2025 22:01:38 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbfe734ed07854436c37e567b57bc647f777cba775ae3377bec6f255cc7fb706`  
		Last Modified: Thu, 23 Jan 2025 18:49:48 GMT  
		Size: 162.9 MB (162879326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c148f4fe0168299d11a90130ef5c067fcad68491eecfc0c6e7bee4b6769d5a0c`  
		Last Modified: Thu, 23 Jan 2025 19:58:26 GMT  
		Size: 129.3 MB (129288972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288438c85cec51cc1c84ed4612698b2fad9c8b553d77688c2753036b88fe72da`  
		Last Modified: Thu, 23 Jan 2025 19:58:25 GMT  
		Size: 31.2 MB (31197645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f8b89fc004380fd713c40b6463bbbc1f37e6459b6af1545d69e671ca9b9526`  
		Last Modified: Thu, 23 Jan 2025 19:58:24 GMT  
		Size: 9.2 MB (9170435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85978bc0b9f754c0de5b76ba1e16304b0d965c6823e1f076021b07e83332fb0`  
		Last Modified: Thu, 23 Jan 2025 19:58:23 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a54a6a9d61d5ff548c523618bd6c64de93936625227bc4b78df4ce50093527`  
		Last Modified: Thu, 23 Jan 2025 19:58:24 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:12832aefa254026e8fd241b1f6db8efa470b784cb8cc79b47dfd72af81393bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6922835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702cd14ccdd8dec7a89ee08b924a2d345b6337fca1ad75e4080b9b01fcaa773e`

```dockerfile
```

-	Layers:
	-	`sha256:c1ce46aa4c305954f95e9e88dbeace25a57b12f545dc66cda02b94a651ec3182`  
		Last Modified: Thu, 23 Jan 2025 19:58:24 GMT  
		Size: 6.9 MB (6904457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5acf7b700cc1d907a04f392bb30bda1a2adb171176691058b7b4b709c3e12b93`  
		Last Modified: Thu, 23 Jan 2025 19:58:23 GMT  
		Size: 18.4 KB (18378 bytes)  
		MIME: application/vnd.in-toto+json
