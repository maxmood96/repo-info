## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:efd014cdc56a440db3da1f15c6b9b673dce08387c58491c0f2a0c6a37b97766d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:74354d7728eea7ca60847e2fd28cfe0ba2a45025c89c7e30098781ebc8269288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.3 MB (429296717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca5bec34a123c60077c07e326cd42a920a69b757b6088753df454cd95f4b067`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:03 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:07:54 GMT
ARG version=17.0.18.8-1
# Wed, 28 Jan 2026 04:07:54 GMT
# ARGS: version=17.0.18.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 28 Jan 2026 04:07:54 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:07:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 28 Jan 2026 05:36:12 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 28 Jan 2026 05:36:21 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 28 Jan 2026 05:36:21 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 28 Jan 2026 05:36:21 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 05:36:21 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 05:36:21 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 28 Jan 2026 05:36:21 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 28 Jan 2026 05:36:21 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 28 Jan 2026 05:36:21 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 28 Jan 2026 05:36:21 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 28 Jan 2026 05:36:21 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 28 Jan 2026 05:36:21 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 28 Jan 2026 05:36:21 GMT
ARG USER_HOME_DIR=/root
# Wed, 28 Jan 2026 05:36:21 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 28 Jan 2026 05:36:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 28 Jan 2026 05:36:21 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2e97d73ce2dcd3ddf3ca49bd76b8633f971d0ff9f5086086e3467c49d62b5d`  
		Last Modified: Wed, 28 Jan 2026 04:08:15 GMT  
		Size: 152.5 MB (152466718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ece8573d0a9bff6041b87721eb6794bbe120a0a267f44be9d35ab95056df67`  
		Last Modified: Wed, 28 Jan 2026 05:36:48 GMT  
		Size: 174.5 MB (174466124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d780d68d9b58ed60265d7dcadc57221dfd64c2f1b13d518664aa32a0964304`  
		Last Modified: Wed, 28 Jan 2026 05:36:45 GMT  
		Size: 30.1 MB (30086891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87b4d3f7d09957187bc93d44dda749a7bfdc47617c7d39e0aa4c12e3989ced4`  
		Last Modified: Wed, 28 Jan 2026 05:36:44 GMT  
		Size: 9.3 MB (9312235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efba80ca4ab43f79ced4bf560d67453245fc024a5dd57a176d257b2ac917b878`  
		Last Modified: Wed, 28 Jan 2026 05:36:44 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b2631532c532270a39f138b9cc88ee0f8866993e6a74c0d323d0af50fef922`  
		Last Modified: Wed, 28 Jan 2026 05:36:45 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:9e454fb5c500114a4651c2eaab85a9f8d0fd71d7d940d4c661cc9ea9652b7f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6950455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536ca8941aad6d8dfd3a0e5914a6407d3f33a1bc666aef14bd353b1673bfecd1`

```dockerfile
```

-	Layers:
	-	`sha256:e371237f654887c0f112bed863b844dbe79ec592a4f2d55d04069b51a9a8d674`  
		Last Modified: Wed, 28 Jan 2026 05:36:44 GMT  
		Size: 6.9 MB (6932261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc11cfaf6cc7c936a9eeb8e46b23f3e4e3dd6d85038641eebe235883119a2733`  
		Last Modified: Wed, 28 Jan 2026 05:36:43 GMT  
		Size: 18.2 KB (18194 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:a31a8f394a4daa4e29de3628621e9d1f08623c9f1c803554f94b0d672c7b5ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.6 MB (406590623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a25a618e0b67f4f7fd76958c06226b3f656156dc8bd8820a48cc8a93dfb3a7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:05 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:28:09 GMT
ARG version=17.0.18.8-1
# Wed, 28 Jan 2026 04:28:09 GMT
# ARGS: version=17.0.18.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 28 Jan 2026 04:28:09 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:28:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 28 Jan 2026 05:41:12 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 28 Jan 2026 05:41:20 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 28 Jan 2026 05:41:20 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 28 Jan 2026 05:41:20 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 05:41:20 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 05:41:20 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 28 Jan 2026 05:41:20 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 28 Jan 2026 05:41:20 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 28 Jan 2026 05:41:20 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 28 Jan 2026 05:41:20 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 28 Jan 2026 05:41:20 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 28 Jan 2026 05:41:20 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 28 Jan 2026 05:41:20 GMT
ARG USER_HOME_DIR=/root
# Wed, 28 Jan 2026 05:41:20 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 28 Jan 2026 05:41:20 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 28 Jan 2026 05:41:20 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da4c2e85453456072839dee22d819df60d20ada601be7fd4fd0190527e11fcf`  
		Last Modified: Wed, 28 Jan 2026 04:28:30 GMT  
		Size: 151.0 MB (150977675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30784ace12798d645765fc375d2bfa67f852d96e886688b27dca8a54dbc29be`  
		Last Modified: Wed, 28 Jan 2026 05:41:46 GMT  
		Size: 150.3 MB (150311345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663b60daecbf684ac17eac86f0c59a46e032b7df31855091935976550a46a24e`  
		Last Modified: Wed, 28 Jan 2026 05:41:43 GMT  
		Size: 31.2 MB (31189423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bce7677b1c02c706fb7e774a0a0c2ecd203a91b44b2d96c4c0c66e99e8db18a`  
		Last Modified: Wed, 28 Jan 2026 05:41:42 GMT  
		Size: 9.3 MB (9312250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49246acb6283fb83f65976a82d25572a7b0704a15ecbd17796cf062898c881c3`  
		Last Modified: Wed, 28 Jan 2026 05:41:41 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879b78d246c19c6821f08aa75234e7a6c2d8d3384236b62eae591a00a6e167ff`  
		Last Modified: Wed, 28 Jan 2026 05:41:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:1c79ec6dcb140586e05543cc5001dcc652f9660400712cf3c9b0088a6e5abf7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6948002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c77aaddf2ffea5b7953fbff95a9f5e335d69c6fdd83c788b67bb6b4a77e337f`

```dockerfile
```

-	Layers:
	-	`sha256:b5234aba025128a7b8cfb98f7a0b2efcb782d0a4c39b102eab2de37175898e31`  
		Last Modified: Wed, 28 Jan 2026 05:41:42 GMT  
		Size: 6.9 MB (6929660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb1c8a4bd0b2d1f81105bae3b7e8e2f611d08d9253e4eca98a97c2685ad298c4`  
		Last Modified: Wed, 28 Jan 2026 05:41:41 GMT  
		Size: 18.3 KB (18342 bytes)  
		MIME: application/vnd.in-toto+json
