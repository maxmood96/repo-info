## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:a2abe66a2c5b7333d9861c2b32a48de809a1ca0063631ad28c55811ea721e69e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:d506f7a78f4f2cc6d6613391f2e7aaf32b5ba25171c09a67d47284b9e0358d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.8 MB (426798153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b420ca1ef0edc32bba564ee61f822d9188183cf2b68090d60018e4dce1da98b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:30 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:30 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:23:37 GMT
ARG version=17.0.17.10-1
# Wed, 03 Dec 2025 20:23:37 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 03 Dec 2025 20:23:37 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:23:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 03 Dec 2025 21:14:45 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 03 Dec 2025 21:14:53 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 03 Dec 2025 21:14:53 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 03 Dec 2025 21:14:53 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 03 Dec 2025 21:14:53 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 03 Dec 2025 21:14:53 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 03 Dec 2025 21:14:53 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 03 Dec 2025 21:14:53 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 03 Dec 2025 21:14:53 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 03 Dec 2025 21:14:53 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 03 Dec 2025 21:14:53 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 03 Dec 2025 21:14:53 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 03 Dec 2025 21:14:53 GMT
ARG USER_HOME_DIR=/root
# Wed, 03 Dec 2025 21:14:53 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 03 Dec 2025 21:14:53 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 03 Dec 2025 21:14:53 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c812675ee7a0cc001d1d82d60b5dfb2f3f3194d136e044e78985b38b47dc8593`  
		Last Modified: Wed, 03 Dec 2025 21:11:35 GMT  
		Size: 152.4 MB (152415886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4221e0c60c5c994f4e88a06fd1f2eb40be39f7fae65b1ea11eeefcdf107012d5`  
		Last Modified: Thu, 04 Dec 2025 00:29:45 GMT  
		Size: 172.1 MB (172147525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b847ac3655b52752992679227a57e8fce99088d6c5866d406102abaa81317c`  
		Last Modified: Wed, 03 Dec 2025 21:15:31 GMT  
		Size: 30.1 MB (30060548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760a6e04edb4539daaedaeec60eaad3efacfba99e30748f767a85e6fafe84229`  
		Last Modified: Wed, 03 Dec 2025 21:15:29 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e83bca6b8e68f37dd17561fe3e0f3bb40657ece0d2d19428a18f19e157933dc`  
		Last Modified: Wed, 03 Dec 2025 21:15:28 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30e24c5e66d8c0f0239b64c9c47dca3a5154b8dc917171d5187ef88d6c14628`  
		Last Modified: Wed, 03 Dec 2025 21:15:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:dd9767bff809bc153429d6432df85597c79454d7bc113dc5b6dbebfd2fd22cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6950456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9800b9f224486cc1bb3f90a8c0ea292ba31949dac3a01d5051d39f3e1c26c250`

```dockerfile
```

-	Layers:
	-	`sha256:81a305e6fa81eac2dd67bfd268fa78ed5dda8c3cf6d14925fd297361b287436e`  
		Last Modified: Thu, 04 Dec 2025 00:27:51 GMT  
		Size: 6.9 MB (6932262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:700786ad9877516109ad972a8493a5caacdd4c4b5ef9a58cf68e3a812fccaca6`  
		Last Modified: Thu, 04 Dec 2025 00:27:51 GMT  
		Size: 18.2 KB (18194 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:14cbf834584f76027f7a016754b44a42cbcfda76c6c0aca44a469f9d14956d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.2 MB (404246706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27f5a31e486158ab44a7a0209dec6b97ed92e854ebbcf4d1b156c0707ca7834`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 03 Dec 2025 20:03:07 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:03:07 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:28:20 GMT
ARG version=17.0.17.10-1
# Wed, 03 Dec 2025 20:28:20 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 03 Dec 2025 20:28:20 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:28:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 03 Dec 2025 21:15:16 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 03 Dec 2025 21:15:24 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 03 Dec 2025 21:15:24 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 03 Dec 2025 21:15:24 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 03 Dec 2025 21:15:24 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 03 Dec 2025 21:15:24 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 03 Dec 2025 21:15:24 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 03 Dec 2025 21:15:24 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 03 Dec 2025 21:15:24 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 03 Dec 2025 21:15:24 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 03 Dec 2025 21:15:24 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 03 Dec 2025 21:15:24 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 03 Dec 2025 21:15:24 GMT
ARG USER_HOME_DIR=/root
# Wed, 03 Dec 2025 21:15:24 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 03 Dec 2025 21:15:24 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 03 Dec 2025 21:15:24 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c51bdf8dfbd567f53f8643ce1104dbc668297329338c373c1c566070d1b7768`  
		Last Modified: Wed, 03 Dec 2025 21:11:47 GMT  
		Size: 151.0 MB (150988198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d9957145bfc509c078f9d3e8e068930e95f887619a9b8698b148cf197e9954`  
		Last Modified: Wed, 03 Dec 2025 22:33:09 GMT  
		Size: 148.0 MB (148024098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda7f89e541ba683bc45ceecb4c42c3eb815903ac2575ab352ac69ed4b03e70f`  
		Last Modified: Wed, 03 Dec 2025 21:15:58 GMT  
		Size: 31.2 MB (31197988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f724f03d7e68d2cda217f808c132e7786cedd5eed8192dfad0342af85dc28e33`  
		Last Modified: Wed, 03 Dec 2025 21:15:56 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3223aef2af96ff95845959f4056e420cdf0116e6e8db329af07ac05720c8f624`  
		Last Modified: Wed, 03 Dec 2025 21:15:55 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2de590116d12ee6a0a6d28d2ebd50eb3b9efdc77cb4194c6efba0d2a2d2f3ff`  
		Last Modified: Wed, 03 Dec 2025 21:15:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:d93d59f2ee7573283fae136c5d7464e68c1a38adea7e1a5e6695980acbdd3fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6948003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aeb25b0c5acbffac41f994daea239c3750ea42d51207c2570a2ed5c534c0bf3`

```dockerfile
```

-	Layers:
	-	`sha256:1c0bfd0a4ba7fda7f00138a7287408c6fbc04ea8d6f724ec3810dff327f96973`  
		Last Modified: Thu, 04 Dec 2025 00:28:01 GMT  
		Size: 6.9 MB (6929661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6754582af33644f74897841e9769a82a6f52da8293ef1255adf639e54c579096`  
		Last Modified: Thu, 04 Dec 2025 00:28:02 GMT  
		Size: 18.3 KB (18342 bytes)  
		MIME: application/vnd.in-toto+json
