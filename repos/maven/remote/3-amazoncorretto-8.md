## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:34aec889d81e3f3975e9aa6fa3fb943e7fa6d5ca5f3f82419e764e252404f76f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:cd6479284f3aca038287ed5e1728633312c59776273a8ba72854dc41d18d231b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360285495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c5e90b8464bd6065ff48863cd926e92c98bed0ba7b52accbcdda2919536f77`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Jun 2026 00:09:40 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:09:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:14:08 GMT
ARG version=1.8.0_492.b09-2
# Tue, 16 Jun 2026 01:14:08 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jun 2026 01:14:08 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:14:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 16 Jun 2026 02:23:25 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 16 Jun 2026 02:23:32 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 16 Jun 2026 02:23:32 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 16 Jun 2026 02:23:32 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 16 Jun 2026 02:23:32 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 16 Jun 2026 02:23:32 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 16 Jun 2026 02:23:32 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 Jun 2026 02:23:32 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 16 Jun 2026 02:23:32 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 16 Jun 2026 02:23:32 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 16 Jun 2026 02:23:32 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 Jun 2026 02:23:32 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 Jun 2026 02:23:32 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 Jun 2026 02:23:32 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c7775f65660d08f273f774ab9700528cfb2a04b08038ea58cfe6c736cc0aa5`  
		Last Modified: Tue, 16 Jun 2026 01:14:23 GMT  
		Size: 76.1 MB (76114392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7548f59bab401a2b7f3072a437207ba5bf810aaeb54a5c01806bf71c94d01dd1`  
		Last Modified: Tue, 16 Jun 2026 02:23:59 GMT  
		Size: 181.8 MB (181804400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffbc9b857c6dfabcf5034cc15226093e80c2aac559623e0e7fc20aa1d0c841c`  
		Last Modified: Tue, 16 Jun 2026 02:23:56 GMT  
		Size: 30.1 MB (30063776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cbe793e9e8ea8c4f13def0b1191cfe9aeee7e3421f216629f7a9180440067d`  
		Last Modified: Tue, 16 Jun 2026 02:23:55 GMT  
		Size: 9.4 MB (9359966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b788ab054b8822462d097213c739112d897cbb1283a1219d2d3d51e6b464a23`  
		Last Modified: Tue, 16 Jun 2026 02:23:54 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c1b06e350e030fafa8ca89e4af68b925da5038e5ddeacd99d74bb5606527b2`  
		Last Modified: Tue, 16 Jun 2026 02:23:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:0cc737899f68784b42f44f9ab4fa346c98df79553f0b78f522238fdc39edfd7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6789889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba29bf6694ab45a7ec86ddca0d9b6de802c40c12e438c53b7f60975a880e3d7`

```dockerfile
```

-	Layers:
	-	`sha256:302ca54792c3404d056b8bd93a74f4da2111fd50bf35de8b9d2ae8daaf57b2d8`  
		Last Modified: Tue, 16 Jun 2026 02:23:54 GMT  
		Size: 6.8 MB (6773705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a024eb33eb9203a187254d5f46644ea72f693ddaeb5e2776cc10b8281c72367`  
		Last Modified: Tue, 16 Jun 2026 02:23:54 GMT  
		Size: 16.2 KB (16184 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:12739ab5df952850f91a8e1ce0f0daea1ec5cb73619703930fa2ca47c05c85d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.6 MB (322641916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76bc5c7171a3664c1fe15c6bdb8d6e76c066494868fc6211d70fd1e339f4df01`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Jun 2026 00:10:52 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:10:52 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:15:28 GMT
ARG version=1.8.0_492.b09-2
# Tue, 16 Jun 2026 01:15:28 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jun 2026 01:15:28 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:15:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 16 Jun 2026 02:24:11 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 16 Jun 2026 02:24:18 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 16 Jun 2026 02:24:18 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 16 Jun 2026 02:24:18 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 16 Jun 2026 02:24:18 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 16 Jun 2026 02:24:18 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 16 Jun 2026 02:24:18 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 Jun 2026 02:24:18 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 16 Jun 2026 02:24:18 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 16 Jun 2026 02:24:18 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 16 Jun 2026 02:24:18 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 Jun 2026 02:24:18 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 Jun 2026 02:24:18 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 Jun 2026 02:24:18 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c533ad9cab38894ffa6218a4bf8a324e76f5906c221461f03313ee2920efef7c`  
		Last Modified: Tue, 16 Jun 2026 01:15:44 GMT  
		Size: 59.9 MB (59947943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e0ba4438f90b0c5c4764ab849d167e7e34f939479a8454842e8d11703e330b`  
		Last Modified: Tue, 16 Jun 2026 02:24:44 GMT  
		Size: 157.4 MB (157352344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96d04c0fb2ff261d1c1b3d8ea4f35bdf878d3b4f698a736494a7917ef45c9d5`  
		Last Modified: Tue, 16 Jun 2026 02:24:42 GMT  
		Size: 31.2 MB (31189939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71c700e6b9ca6a000597ffa182bff04a9c6f6af2386e5fe4f9d54ddb0193db3`  
		Last Modified: Tue, 16 Jun 2026 02:24:41 GMT  
		Size: 9.4 MB (9359970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daed1ea0044ac219ca8228b6243856b6b81c42685a67aa877e92de54f00d54a0`  
		Last Modified: Tue, 16 Jun 2026 02:24:40 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1dc583e231ff0213a9e14cf695799154a2d2026046866d48ea4713ad06a4ebb`  
		Last Modified: Tue, 16 Jun 2026 02:24:41 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:a3919e6b55365282f20cd8237d2c2f5d072409c9b57c2911b08cee083a0bc089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6767236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26476ead211c3ba0700bbf594604e172a6cc951a26066b5240ffdd073df1928`

```dockerfile
```

-	Layers:
	-	`sha256:2b229926d238e456df6c1470a158a50654b4756c7b1b1459cfc5d1b26591a6c3`  
		Last Modified: Tue, 16 Jun 2026 02:24:40 GMT  
		Size: 6.8 MB (6750902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:246ded7df4a98539438de30a484b7dce890a8e26097fa7f69450e1ba9fef3334`  
		Last Modified: Tue, 16 Jun 2026 02:24:40 GMT  
		Size: 16.3 KB (16334 bytes)  
		MIME: application/vnd.in-toto+json
