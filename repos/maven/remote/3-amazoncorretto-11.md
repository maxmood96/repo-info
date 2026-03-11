## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:b8c2e0599232c19a243ecbb483e860d9af84c32d6bc88d012b5ee864a75de600
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:80c2e0dba41967011fdf00b55f6c6bb13328b26066033282f42d91cb55efd8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.0 MB (426021940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e406fed267e118a59f1912bdd720dcf71d51802520bd3190f13fce8fa9192cd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 11 Mar 2026 18:22:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:22:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:32:07 GMT
ARG version=11.0.30.7-1
# Wed, 11 Mar 2026 18:32:07 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 11 Mar 2026 18:32:07 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:32:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 11 Mar 2026 19:15:55 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 11 Mar 2026 19:16:03 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 11 Mar 2026 19:16:03 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 11 Mar 2026 19:16:03 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 11 Mar 2026 19:16:03 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 11 Mar 2026 19:16:03 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 11 Mar 2026 19:16:03 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 11 Mar 2026 19:16:03 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 11 Mar 2026 19:16:03 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 11 Mar 2026 19:16:03 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 11 Mar 2026 19:16:03 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 11 Mar 2026 19:16:03 GMT
ARG MAVEN_VERSION=3.9.13
# Wed, 11 Mar 2026 19:16:03 GMT
ARG USER_HOME_DIR=/root
# Wed, 11 Mar 2026 19:16:03 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 11 Mar 2026 19:16:03 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 11 Mar 2026 19:16:03 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:94fc983b0f2661f620fb3c97c279be6e7a6a21ff4a004bf4df15272612aed901`  
		Last Modified: Sat, 07 Mar 2026 04:10:35 GMT  
		Size: 63.0 MB (62956510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b20d6ad17bf5a5e6c795a6bafe254f811eb55ef5f45999fe7ad9419d1a2c4a`  
		Last Modified: Wed, 11 Mar 2026 18:32:27 GMT  
		Size: 148.1 MB (148126018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7784451577b0aedecc0563344c56aa690e1e4fd518598fb3dfe5f8f6f4d85b29`  
		Last Modified: Wed, 11 Mar 2026 19:16:29 GMT  
		Size: 175.2 MB (175156508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a3a0d813dec4aeae177fded8d89c3e041fc0621ec48be37a77533fa4cad55b`  
		Last Modified: Wed, 11 Mar 2026 19:16:26 GMT  
		Size: 30.1 MB (30084340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6f146720ced70fe94ec00718768c1a2f0fda7ea5d8cd0bb76a6acfb6ee1b6d`  
		Last Modified: Wed, 11 Mar 2026 19:16:25 GMT  
		Size: 9.7 MB (9697523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6c13741b7371492bfddd04f669f6386f7ae7e0d65e3837820bd53d0006f730`  
		Last Modified: Wed, 11 Mar 2026 19:16:24 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3dc697cd376dc8f0c8a376b4768804eef693d9d001738ab12b2c6786edd331`  
		Last Modified: Wed, 11 Mar 2026 19:16:26 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:a88c9caef6f7ec220596622c07271fcd6a60bdcecb0a2ac2eaa07b2438c8c263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6964235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c70c3295e51b60d1bb5ccc80eca1a349923b52949d7df1729d57f11c1998859`

```dockerfile
```

-	Layers:
	-	`sha256:ff5924aad16ee47d79dcc79f162f848f4161fc9b4c0e39e420a270da3d129930`  
		Last Modified: Wed, 11 Mar 2026 19:16:25 GMT  
		Size: 6.9 MB (6946043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb47e922f3a35fbfd6ad3c30bbf01c55b6c5f4ceade61689f785a7a5a44e4ad6`  
		Last Modified: Wed, 11 Mar 2026 19:16:24 GMT  
		Size: 18.2 KB (18192 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:da6eb94b4a19114616f72696b3b3d1f333e9b245b0f530dda21786d2daf2d96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.7 MB (401679862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe85c5f94822b7a48abf96d8b9133bd15913a445937ed95e4fb9045093f0541`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:38 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:32:21 GMT
ARG version=11.0.30.7-1
# Wed, 11 Mar 2026 18:32:21 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 11 Mar 2026 18:32:21 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:32:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 11 Mar 2026 19:16:04 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 11 Mar 2026 19:16:12 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 11 Mar 2026 19:16:12 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 11 Mar 2026 19:16:12 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 11 Mar 2026 19:16:12 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 11 Mar 2026 19:16:12 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 11 Mar 2026 19:16:12 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 11 Mar 2026 19:16:12 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 11 Mar 2026 19:16:12 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 11 Mar 2026 19:16:12 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 11 Mar 2026 19:16:12 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 11 Mar 2026 19:16:12 GMT
ARG MAVEN_VERSION=3.9.13
# Wed, 11 Mar 2026 19:16:12 GMT
ARG USER_HOME_DIR=/root
# Wed, 11 Mar 2026 19:16:12 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 11 Mar 2026 19:16:12 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 11 Mar 2026 19:16:12 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1331e22401e9e6f680f618ca7ac295b00616904425c0ac818294801fd11443e3`  
		Last Modified: Mon, 09 Mar 2026 09:10:03 GMT  
		Size: 64.8 MB (64803149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7932995bd594e75f8d5178d3e3fd2c3400b84edd2f1cf6db87ccb7b6cd9e798`  
		Last Modified: Wed, 11 Mar 2026 18:32:47 GMT  
		Size: 145.2 MB (145212347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20d88d37376bbfd2590b5cb4448bff47dd68feee72677ef6f165a929341f91f`  
		Last Modified: Wed, 11 Mar 2026 19:16:39 GMT  
		Size: 150.8 MB (150767836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5a6b9aaa1fc28ff9d24f460b66724b00dde3c3d6702c639e49c810ed9ba49d`  
		Last Modified: Wed, 11 Mar 2026 19:16:36 GMT  
		Size: 31.2 MB (31197926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6079dc18679c7bb1046bc72b58e30e26376e029641d0e3c2904e08af633593`  
		Last Modified: Wed, 11 Mar 2026 19:16:35 GMT  
		Size: 9.7 MB (9697559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb09901e2af1b344ea25220f11575109c581f2c3090c6f28284f81a922b65394`  
		Last Modified: Wed, 11 Mar 2026 19:16:35 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affba2d52308d5770544e29f4109b4481e0a15691519e59be7b4e08337a1709e`  
		Last Modified: Wed, 11 Mar 2026 19:16:36 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:c63d43e2b421813b8cb4edf5c4f3d7baaa0b8d7ee6482e2c105ee7ba9af0858a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6962589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306a63e89fcaf7c92527b9422245d244cce5d0d81d27c5d649baf024d8a6d007`

```dockerfile
```

-	Layers:
	-	`sha256:ca5b29b2b6c5b882c870640ab3e4ad36cf220ff9aa5ca85c00f522803e04312a`  
		Last Modified: Wed, 11 Mar 2026 19:16:35 GMT  
		Size: 6.9 MB (6944247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8abd57097da1ca393ea77872cdd09bf93ea0a0ccefae32a0e4613c1a2a0e290d`  
		Last Modified: Wed, 11 Mar 2026 19:16:35 GMT  
		Size: 18.3 KB (18342 bytes)  
		MIME: application/vnd.in-toto+json
