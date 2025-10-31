## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:750d345095b3f027870e7db62fe2c716b22bbde9d5ba2acaa8f8043b1b09e0e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:ee79c3c308043538e9a195939476791d528666a7aa9dc887bb6491442c7309f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.7 MB (425728662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cedd48104f86a1a8de5639c871bb1c7660edbd44f44b819c2dd391eb7959a64`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:45 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:11:47 GMT
ARG version=17.0.17.10-1
# Fri, 31 Oct 2025 00:11:47 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 31 Oct 2025 00:11:47 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:11:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 31 Oct 2025 01:14:40 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 31 Oct 2025 01:14:49 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 31 Oct 2025 01:14:49 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 31 Oct 2025 01:14:49 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:14:49 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:14:49 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 31 Oct 2025 01:14:49 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 31 Oct 2025 01:14:49 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 31 Oct 2025 01:14:49 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 31 Oct 2025 01:14:49 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 31 Oct 2025 01:14:49 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 31 Oct 2025 01:14:49 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 31 Oct 2025 01:14:49 GMT
ARG USER_HOME_DIR=/root
# Fri, 31 Oct 2025 01:14:49 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 31 Oct 2025 01:14:49 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 31 Oct 2025 01:14:49 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2e3ea9592aad33f5f11ca8c65604905de30de68b0c38dfad7dee51b605c2a2c5`  
		Last Modified: Thu, 30 Oct 2025 03:52:34 GMT  
		Size: 62.9 MB (62934068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11cee90354531f4ca16570052264d74542e465a82e38fdafa8b2ffb35f381810`  
		Last Modified: Fri, 31 Oct 2025 01:12:54 GMT  
		Size: 152.4 MB (152409108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e903026157f787d2bb6cc406a4a22373a5048f79b16b18b39d48ea2e47418b2d`  
		Last Modified: Fri, 31 Oct 2025 02:31:48 GMT  
		Size: 171.1 MB (171077354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6de367e2bb59aeb467a2b6e65803e53bb86366c69d09cd95927d979cace7ad`  
		Last Modified: Fri, 31 Oct 2025 01:15:25 GMT  
		Size: 30.1 MB (30064496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8887718698414f2b40155622969f8275d0142609fd7e21a23037bee4743eeb9`  
		Last Modified: Fri, 31 Oct 2025 01:15:22 GMT  
		Size: 9.2 MB (9242593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79742ac2d7f54dced92430c9cb882cd172a8fd6d5dbea59ec1ac78be8c6d6e1f`  
		Last Modified: Fri, 31 Oct 2025 01:15:21 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc9daa22db45a908db5e3af81717e0839b689a5f86895ccfa5cbfc621440853`  
		Last Modified: Fri, 31 Oct 2025 01:15:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:a13e88742f16aa0af2223621d0005a392855f050090074067d06327cb4921c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6950450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9366badd051eef183539518ccb0912c774476bece88360740d71efe9d43868bf`

```dockerfile
```

-	Layers:
	-	`sha256:4130f4b1f14d9afc3503e7e842e4e6273ccf02af62c90d9509c914376c6de21a`  
		Last Modified: Fri, 31 Oct 2025 02:27:50 GMT  
		Size: 6.9 MB (6932258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ec28484de101af4586b01521d57234c969238ea201cac5317325a7cef8b5566`  
		Last Modified: Fri, 31 Oct 2025 02:27:51 GMT  
		Size: 18.2 KB (18192 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:44578886cc0f25feec243eee5d2f6b65cc4d1d2daac81734d5448974a54ed11f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.2 MB (403239728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957169ec2772f40e7ab419b4c5338ebfd2295617ace8046a6cc592b411f1d33e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:47 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:47 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:09 GMT
ARG version=17.0.17.10-1
# Fri, 31 Oct 2025 00:12:09 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 31 Oct 2025 00:12:09 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 31 Oct 2025 01:14:44 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 31 Oct 2025 01:14:51 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 31 Oct 2025 01:14:51 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 31 Oct 2025 01:14:51 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:14:51 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:14:51 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 31 Oct 2025 01:14:51 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 31 Oct 2025 01:14:51 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 31 Oct 2025 01:14:51 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 31 Oct 2025 01:14:52 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 31 Oct 2025 01:14:52 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 31 Oct 2025 01:14:52 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 31 Oct 2025 01:14:52 GMT
ARG USER_HOME_DIR=/root
# Fri, 31 Oct 2025 01:14:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 31 Oct 2025 01:14:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 31 Oct 2025 01:14:52 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2875a69d1768080ef2331610c2aea8f8cfff54b5df360eb9feb01240a7526ff5`  
		Last Modified: Thu, 30 Oct 2025 23:15:16 GMT  
		Size: 64.8 MB (64793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fe77ddb74850a2a8eb934a6793b84365d9be75189f7d257ddd3bf0519b0fb0`  
		Last Modified: Fri, 31 Oct 2025 01:13:14 GMT  
		Size: 151.0 MB (150988225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169151840e87c698208ad63b9afe55e7b39b7c33788e9e04428c3c253b5af55a`  
		Last Modified: Fri, 31 Oct 2025 03:46:30 GMT  
		Size: 147.0 MB (147017992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894dfed8d2917c851a2e7da6d3075d94dae97308ac4b43d8227e1c7450cb4690`  
		Last Modified: Fri, 31 Oct 2025 01:15:26 GMT  
		Size: 31.2 MB (31196421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983e39ed3c7bc450b40f3a8bf1c0e501f454a9680e9bb8ea8f7bfd47a80562ba`  
		Last Modified: Fri, 31 Oct 2025 01:15:24 GMT  
		Size: 9.2 MB (9242587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a60a9206b2605bda65069ebe7953a6b6e472a4c5d31d99522164fbd57d87f1`  
		Last Modified: Fri, 31 Oct 2025 01:15:23 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09119ebfd7812306159b54542520791990f30f7ee79d7d99dcbbadf5c3821fd`  
		Last Modified: Fri, 31 Oct 2025 01:15:24 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:caafe81cf704244548c74a183099124eec56c4ac1fa7ef3f44dd96da096f6aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6947999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f31681bb76d52eecf62a83553c114052c9b163cf3d56a625993a5fb5d742f1`

```dockerfile
```

-	Layers:
	-	`sha256:f16a34a8fa1e663d1349af1a57ef3eced51d8fc995585ef5183114a7709d5018`  
		Last Modified: Fri, 31 Oct 2025 02:27:56 GMT  
		Size: 6.9 MB (6929657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c66c7bd69258ab5488a5cb94d4330d3e1cc44b99d454a945eb51b5044a00291`  
		Last Modified: Fri, 31 Oct 2025 02:27:57 GMT  
		Size: 18.3 KB (18342 bytes)  
		MIME: application/vnd.in-toto+json
