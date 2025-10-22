## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:63131de3179b1cc40a72752b4c1cf0e1594887f31f8a97e10b3972be06a574d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:b58b93832b354f4c6bf1acfea5ca7f31fef031c5a303ddade8c612b735894c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.9 MB (346938783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fcbf4ecd614e3fd577fc80bfaa4d1f80c2e561bd74fc4eff2a7043734549628`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=1.8.0_462.b08-1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:91f0f90aeef889cedc2e056e6976319ec5d96df70bf35b1d46092d2c1f375f2b`  
		Last Modified: Sat, 04 Oct 2025 04:29:16 GMT  
		Size: 62.9 MB (62940620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14a39dc653189767e80d97a12ba807e012fdf9da65462a1c0893fd4997ead64`  
		Last Modified: Mon, 06 Oct 2025 22:12:04 GMT  
		Size: 75.6 MB (75613516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98fa1b105572cbf2c57a8ee050567f9b79056d14dc2bbff9fbd707bd157c562`  
		Last Modified: Fri, 10 Oct 2025 05:32:47 GMT  
		Size: 169.1 MB (169060845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5721c9df049b3dc3bd8e24adbac747b434bea7c57e1cb04ab82cb14cb09da09c`  
		Last Modified: Fri, 10 Oct 2025 05:32:37 GMT  
		Size: 30.1 MB (30080168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0491c60b1ae58bf6782c3220b7c2e097c906b690679bb12ac79f6e5442b3167`  
		Last Modified: Thu, 09 Oct 2025 23:34:13 GMT  
		Size: 9.2 MB (9242591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1302f866a417ae20652d5d2b73f5af4a22bb9063a5c6eea5cbec7761af137f15`  
		Last Modified: Thu, 09 Oct 2025 23:34:08 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805e54ff2430836c7ecef386483d3de360222f416043d5d1e7d9298e3d3ad31e`  
		Last Modified: Thu, 09 Oct 2025 23:34:09 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:109a4f8a401009c691272410ecf756697c6c51a26305cebd03ba0042f6e909d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6789417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a8552475a205aaabfb11dc8820df551f6b00ca981564d9d2c7c782480d2088`

```dockerfile
```

-	Layers:
	-	`sha256:9810387c1258531860860f52c35b1d7c1208b10833f95eaa3ddc45cce9c5e4b1`  
		Last Modified: Fri, 10 Oct 2025 05:30:36 GMT  
		Size: 6.8 MB (6771187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f35d13259a90695f2813792500838f87756d124079523b6c4d3a41206b78bd3`  
		Last Modified: Fri, 10 Oct 2025 05:30:37 GMT  
		Size: 18.2 KB (18230 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:3b4f4fc9c622a56a61461b4f6fafa048affd1862efd863e7567ae591cd6a0645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311277717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4d4cd9121854a1b62dcbfad71a36fb6343a3b3fc6d63b5c73f0ec27206f58c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=1.8.0_472.b08-1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8b6c0dce7361457a1cee4518c5dc9c75ff3fa343c4460bdb254d7bd18bc1bf03`  
		Last Modified: Sat, 04 Oct 2025 18:25:08 GMT  
		Size: 64.8 MB (64793208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c88cb600be535a907eaa9dc28f559a1379c7964a2181880f693901eeb7c460`  
		Last Modified: Tue, 21 Oct 2025 21:48:51 GMT  
		Size: 60.1 MB (60118968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6afc24ae975b329125060c1e55b8ec8f2432c9b3267980996faeee744d5971`  
		Last Modified: Tue, 21 Oct 2025 23:59:45 GMT  
		Size: 145.9 MB (145925433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200c826bd362247849a4f5e9bdfb0d37e7661dcfc21397b3776a47f799533ac2`  
		Last Modified: Tue, 21 Oct 2025 23:16:16 GMT  
		Size: 31.2 MB (31196480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2c7f958b4e28df653b0b7b032fead998af7490f6b6d83b414407ceff486c5a`  
		Last Modified: Tue, 21 Oct 2025 23:05:02 GMT  
		Size: 9.2 MB (9242584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def9548674f2fc4379e7940aa269744449479f4137383f99c74e7e805e826b78`  
		Last Modified: Tue, 21 Oct 2025 23:05:01 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f278c7eb26c6c8befefb2cba93872595a09c643797b06b5a7b2fc66355156efb`  
		Last Modified: Tue, 21 Oct 2025 23:06:31 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:72a703f831afe70db10d0d821d4cd9f837f6f15e6fb5306899a04be3246d3819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6769184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cac4bea88ce316d981aed41dbbfd136eb0162e24dbffcab7eb2ec3161c37b18`

```dockerfile
```

-	Layers:
	-	`sha256:72eb880daf18a409bee6957c8761ac4fb9ab25b97582082d81a910b02de0abc3`  
		Last Modified: Tue, 21 Oct 2025 23:28:52 GMT  
		Size: 6.8 MB (6750807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96b64b94fd38bbe138c74a62713f14103eecc174c990e27a39372fed51851048`  
		Last Modified: Tue, 21 Oct 2025 23:28:53 GMT  
		Size: 18.4 KB (18377 bytes)  
		MIME: application/vnd.in-toto+json
