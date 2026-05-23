## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:6fc62a568b008e6a15791cb6722ed2342c17041daf0f8c352ded3503a4801746
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:0ca2118ba877ddb301cd601a3a2f1f5e00f9a8c3840a84aaa5ffe02c039c2abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.2 MB (358228551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f223af2b5f5235bdcfe42ad6c6fd53d67a137ce981b72193976d94fb756ac0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 22 May 2026 20:12:28 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:28 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:10:17 GMT
ARG version=1.8.0_492.b09-2
# Fri, 22 May 2026 21:10:17 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 22 May 2026 21:10:17 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:10:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 22 May 2026 22:09:42 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 22 May 2026 22:09:50 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 22 May 2026 22:09:50 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 22 May 2026 22:09:50 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 22 May 2026 22:09:50 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 22 May 2026 22:09:50 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 22 May 2026 22:09:50 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 22 May 2026 22:09:50 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 22 May 2026 22:09:50 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 22 May 2026 22:09:50 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 22 May 2026 22:09:50 GMT
ARG USER_HOME_DIR=/root
# Fri, 22 May 2026 22:09:50 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 22 May 2026 22:09:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 22 May 2026 22:09:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:45dd431b24e3561020a83f5e29dd2642d9ec2f2788c6826e5b1e9ee25ee38759`  
		Last Modified: Sat, 16 May 2026 04:14:19 GMT  
		Size: 63.0 MB (62951975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1515b31f1cd911fcad46dfa29290c8fe924a5b786aecc7eae1a76d33a0cb8d`  
		Last Modified: Fri, 22 May 2026 21:10:33 GMT  
		Size: 76.1 MB (76129995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48d77d65fea83f66d4994c505f56b9ad8d8401436c13c12242232f571161769`  
		Last Modified: Fri, 22 May 2026 22:10:20 GMT  
		Size: 179.7 MB (179706565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b73cce6418ea90d9c37f0b06ced492643fd411aa4c049c76a55577b8f13b970`  
		Last Modified: Fri, 22 May 2026 22:10:16 GMT  
		Size: 30.1 MB (30079034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b956722daef9267a179f3a92ce38cb0f88f463921a119b4472ee4d3f52ba1e4`  
		Last Modified: Fri, 22 May 2026 22:10:16 GMT  
		Size: 9.4 MB (9359974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab96c4ac00e8970978096d44d90123e61fa67be75598b829a945f265c40c150`  
		Last Modified: Fri, 22 May 2026 22:10:15 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849edbf85701677e7b4fa81797a89eb56d2d9d6de1658558b4fa5d653b042c3f`  
		Last Modified: Fri, 22 May 2026 22:10:16 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:ef05b608729f1cbbd63a8e18bd750c1eef9a12d208a473f690a79ec38ac4a61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6789890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0800ad8d18a94c1855c3bec95b45a8fb01d004a147be381159ebbf541273add`

```dockerfile
```

-	Layers:
	-	`sha256:6ca29399bd2f97969eaf8f24d1a5e8b588b36e7b488a7929f0e1d2f0755d373c`  
		Last Modified: Fri, 22 May 2026 22:10:15 GMT  
		Size: 6.8 MB (6773705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1ffe407b5c52e8894b50a48cb640e3a12b373a6002b64220686e370f1d2c142`  
		Last Modified: Fri, 22 May 2026 22:10:15 GMT  
		Size: 16.2 KB (16185 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:46d5afebf3f91595f8dbc80afd53d4f77f6846f8f959c15844a80d313fd2cf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.6 MB (320553493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81129f6fed14eff0eaf05dde1e6c926985ae148fde4cf37fa499e22cb121507`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 22 May 2026 20:12:43 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:43 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:09:55 GMT
ARG version=1.8.0_492.b09-2
# Fri, 22 May 2026 21:09:55 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 22 May 2026 21:09:55 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:09:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 22 May 2026 22:10:12 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 22 May 2026 22:10:19 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 22 May 2026 22:10:19 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 22 May 2026 22:10:19 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 22 May 2026 22:10:19 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 22 May 2026 22:10:19 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 22 May 2026 22:10:19 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 22 May 2026 22:10:19 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 22 May 2026 22:10:19 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 22 May 2026 22:10:19 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 22 May 2026 22:10:19 GMT
ARG USER_HOME_DIR=/root
# Fri, 22 May 2026 22:10:19 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 22 May 2026 22:10:19 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 22 May 2026 22:10:19 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9b55de233aca71116430038a4df795c9fbcd988648b5d3ff05692945d681a5dc`  
		Last Modified: Sat, 16 May 2026 15:07:44 GMT  
		Size: 64.8 MB (64790017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf726afbc53a0c500f417329c2d905be4d6f8922eb4fd9609e59686819f9aaf`  
		Last Modified: Fri, 22 May 2026 21:10:10 GMT  
		Size: 59.9 MB (59947854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da6701472b359317ca01f118581e7690c510b2193b292c4fffc14dfed09ad7c`  
		Last Modified: Fri, 22 May 2026 22:10:45 GMT  
		Size: 155.3 MB (155263410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c704be0d9af2fdd3a6429139a84af3b728f1d53cabac11af8c964fca02d7cb5`  
		Last Modified: Fri, 22 May 2026 22:10:43 GMT  
		Size: 31.2 MB (31191228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3ec74a26f6c8bcb2290144f7830c87aa4d09cb1c5c758c482dd86e86823d4b`  
		Last Modified: Fri, 22 May 2026 22:10:42 GMT  
		Size: 9.4 MB (9359974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a112fb6fca8879d9da84479be3e3ea69091f0b9bc3da7eacc1d16873a1ac6f2`  
		Last Modified: Fri, 22 May 2026 22:10:41 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4ddc4051910c5b0f627564c3434dd4994a6de5f83ff0d276cb7f9e5f97a110`  
		Last Modified: Fri, 22 May 2026 22:10:43 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:7ebb683dbbb71292e53633cbfefbcd0ad44a1ae2013c2c27deb3d30cb33a5447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6767236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da2aa0c2bc290e29f66ce2c95fd61e310ad58edcd02e058597a92a5da3ab944`

```dockerfile
```

-	Layers:
	-	`sha256:9abb02684eab80d11bc0ae7995042a1c921cd8fdbe6f3dbf1d1f9c54180bf37f`  
		Last Modified: Fri, 22 May 2026 22:10:42 GMT  
		Size: 6.8 MB (6750902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b080773891b86a2ca42faf7740fbce989567f056d4a0fe241e57602eb7898487`  
		Last Modified: Fri, 22 May 2026 22:10:41 GMT  
		Size: 16.3 KB (16334 bytes)  
		MIME: application/vnd.in-toto+json
