## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:a2acdf317e7ce7aaf5c5d1a96176a7170967138dab865f455fa6a05a4775ee23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:9d278a28ba90c906db4f64ecd1f35ddeb520c60de7a922be0cd500105797b4f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.8 MB (434763466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906a35bb7d97dd5ddc75f9e2b09972d8bed6f9b95dfe241400ea45d828ad1739`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 22 May 2026 20:12:28 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:28 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:37 GMT
ARG version=17.0.19.10-1
# Fri, 22 May 2026 21:11:37 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 22 May 2026 21:11:37 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 22 May 2026 22:08:45 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 22 May 2026 22:08:52 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 22 May 2026 22:08:52 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 22 May 2026 22:08:52 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 22 May 2026 22:08:52 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 22 May 2026 22:08:52 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 22 May 2026 22:08:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 22 May 2026 22:08:52 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 22 May 2026 22:08:52 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 22 May 2026 22:08:52 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 22 May 2026 22:08:52 GMT
ARG USER_HOME_DIR=/root
# Fri, 22 May 2026 22:08:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 22 May 2026 22:08:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 22 May 2026 22:08:52 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:45dd431b24e3561020a83f5e29dd2642d9ec2f2788c6826e5b1e9ee25ee38759`  
		Last Modified: Sat, 16 May 2026 04:14:19 GMT  
		Size: 63.0 MB (62951975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1c70d1c6953a128a159df107482ccf05c002cb93693078cb9080127ce0eeff`  
		Last Modified: Fri, 22 May 2026 21:12:00 GMT  
		Size: 152.7 MB (152670549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcedbca917ef15ea7d5e5c1081a1f7a1e6ddca5c9acfbf6d73efc777033b1c8`  
		Last Modified: Fri, 22 May 2026 22:09:17 GMT  
		Size: 179.7 MB (179700051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d1d6c399111ee2b046fbaf33e1df547bafff08ef8159eba12b7fce20128761`  
		Last Modified: Fri, 22 May 2026 22:09:14 GMT  
		Size: 30.1 MB (30079914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140c58ac26756e83daa5e8be27082a76478427b31f58cbc5f147e4d879023035`  
		Last Modified: Fri, 22 May 2026 22:09:13 GMT  
		Size: 9.4 MB (9359967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2952fe5d681ec86337426d21ab42220275ed140ab57f51af4947e51683196dba`  
		Last Modified: Fri, 22 May 2026 22:09:12 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43271321edfea308d08c5d51670dc56211c1869d3e8ad344e27a060a4cdee92b`  
		Last Modified: Fri, 22 May 2026 22:09:14 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:21cf197af4d82699ee1778cb532b68dfc49a3dab1c9027aa99dd7cf8ee2227ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6949360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25891d6af06f43db85a9a1254dae859025f3920069171655f4927cc324b5809c`

```dockerfile
```

-	Layers:
	-	`sha256:349841c10c9e36153f7edb1082920b7f8fd647bc9d1aca3ad073deffd7950231`  
		Last Modified: Fri, 22 May 2026 22:09:13 GMT  
		Size: 6.9 MB (6933165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3e6dcd0efe216b8278ce11bf539490ee9aafff72c4ca34692062d723a0009b`  
		Last Modified: Fri, 22 May 2026 22:09:12 GMT  
		Size: 16.2 KB (16195 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:456a32663e9a1a01c7c9c0be4f44448031ebfc3a384f40f7375f0e9ce8304809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.9 MB (411942955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3618b989d0035e82bb74d7566702b94b5fbb925940a393ecae5616ce9bc137ef`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 22 May 2026 20:12:43 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:43 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:04 GMT
ARG version=17.0.19.10-1
# Fri, 22 May 2026 21:11:04 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 22 May 2026 21:11:04 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 22 May 2026 22:09:21 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 22 May 2026 22:09:28 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 22 May 2026 22:09:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 22 May 2026 22:09:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 22 May 2026 22:09:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 22 May 2026 22:09:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 22 May 2026 22:09:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 22 May 2026 22:09:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 22 May 2026 22:09:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 22 May 2026 22:09:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 22 May 2026 22:09:28 GMT
ARG USER_HOME_DIR=/root
# Fri, 22 May 2026 22:09:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 22 May 2026 22:09:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 22 May 2026 22:09:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9b55de233aca71116430038a4df795c9fbcd988648b5d3ff05692945d681a5dc`  
		Last Modified: Sat, 16 May 2026 15:07:44 GMT  
		Size: 64.8 MB (64790017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d876074273e0cd4b6cf1c24604ff033565872c6d506da1298267fccc360c96`  
		Last Modified: Fri, 22 May 2026 21:11:25 GMT  
		Size: 151.3 MB (151318380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77ae72bce116f2c6c93c359990b5d6f85497134d497cc629ff647da6e4de38d`  
		Last Modified: Fri, 22 May 2026 22:09:56 GMT  
		Size: 155.3 MB (155270047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af766659bc7f89919e14e5570ded7d453fb53260723da408c3f3a26b84be8b9`  
		Last Modified: Fri, 22 May 2026 22:09:53 GMT  
		Size: 31.2 MB (31203541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbece4574c78e4884adb18af81a899ecb12098fbaeff8d269267ab4b0d4d813`  
		Last Modified: Fri, 22 May 2026 22:09:52 GMT  
		Size: 9.4 MB (9359964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb883faa23caeea995297c7a6330d769c3bcaf3c72da2e246656505257f77fb`  
		Last Modified: Fri, 22 May 2026 22:09:51 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9c1d80bc5efd45e04ff67096ad77034e6f52530fbbead8905d4673a6023fae`  
		Last Modified: Fri, 22 May 2026 22:09:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:b2e31aad716004a931306bb6934485c4dc93a724ee6398830f4715a0cff889ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6946907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f820f70e0148e929c0818cf05ade70c0e499ea146ad4e6fde01161e1fb1312`

```dockerfile
```

-	Layers:
	-	`sha256:2a36378cff67912bcaf55885df1a76c94c8305a48e7ad8f7345739e71a0b17ef`  
		Last Modified: Fri, 22 May 2026 22:09:52 GMT  
		Size: 6.9 MB (6930564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62da554865c912ba27089267f93d904becb91ecc1346f9d89f3ed982d56bbbc1`  
		Last Modified: Fri, 22 May 2026 22:09:51 GMT  
		Size: 16.3 KB (16343 bytes)  
		MIME: application/vnd.in-toto+json
