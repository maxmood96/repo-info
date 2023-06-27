## `maven:3-amazoncorretto-20`

```console
$ docker pull maven@sha256:553fd33597fd4af2e598ad24741060cd15cb598e859c1d3ba3086247e3664d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-20` - linux; amd64

```console
$ docker pull maven@sha256:8ca4ff6e2f22cb298693de1fa4af2e6d7fe742885e7e29519d6f03590ec3c20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.6 MB (386629331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0dec079acef81af7fe4bbd853a2e606d9fcb52888319bd0c03b59d24711cf1b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Jun 2023 22:20:15 GMT
COPY dir:129c77392b447afbaa234a34f434bed5ec790278efd165e1d59d4425216de49b in / 
# Tue, 20 Jun 2023 22:20:16 GMT
CMD ["/bin/bash"]
# Tue, 20 Jun 2023 22:57:14 GMT
ARG version=20.0.1.9-1
# Tue, 20 Jun 2023 22:57:37 GMT
# ARGS: version=20.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 20 Jun 2023 22:57:38 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jun 2023 22:57:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
# Mon, 26 Jun 2023 13:48:06 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 26 Jun 2023 13:48:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
ARG MAVEN_VERSION=3.9.3
# Mon, 26 Jun 2023 13:48:06 GMT
ARG USER_HOME_DIR=/root
# Mon, 26 Jun 2023 13:48:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 26 Jun 2023 13:48:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 26 Jun 2023 13:48:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0086aac11276884f299f6c13a98f93369cc50f7c0518989c2d4a29dd999feb70`  
		Last Modified: Fri, 16 Jun 2023 00:07:41 GMT  
		Size: 62.5 MB (62487611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a67431843d9e5854a588042bb3ab1dea757eb095a929ea60bef489fc4f13e9`  
		Last Modified: Tue, 20 Jun 2023 23:03:25 GMT  
		Size: 160.8 MB (160763226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b564b4dd7dc6d7da9b62aa718be45e90bde32c37bc24131b7dd89148629d40c`  
		Last Modified: Tue, 20 Jun 2023 23:40:43 GMT  
		Size: 154.0 MB (154049544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb17807de1b89c3f855d163ffbb960b0eece2ad7e327ef1356d615cfacbac623`  
		Last Modified: Tue, 27 Jun 2023 01:18:41 GMT  
		Size: 9.3 MB (9327576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f604dc58e450290de42beb98b62d6999db751baa877f0396c1161e90bddbf3`  
		Last Modified: Tue, 27 Jun 2023 01:18:41 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0847b3c4a0d0feecea867f43d6cc25c6e6b2405a3b38ff8010c08759b95cb5af`  
		Last Modified: Tue, 27 Jun 2023 01:18:41 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d3e65f8cc15fb80f2da180fb49f8c8a79f0655c619dcfcaf8e2bb1cf92bf1a`  
		Last Modified: Tue, 27 Jun 2023 01:18:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-20` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:0b396ab82c471e46b860d30a0f893b9a2449a549db5c908ada30dd0c36cecb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.2 MB (351199893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1cc086d6aee4dca6dbef890384e36152e4fe6013704e7ef578399bf8f3600b5`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Jun 2023 22:40:04 GMT
COPY dir:ff562af1eb403156d540f974a5832a6973c9f08f4a181bdb7b2f5a2faf708d9c in / 
# Tue, 20 Jun 2023 22:40:05 GMT
CMD ["/bin/bash"]
# Tue, 20 Jun 2023 23:26:12 GMT
ARG version=20.0.1.9-1
# Tue, 20 Jun 2023 23:26:33 GMT
# ARGS: version=20.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 20 Jun 2023 23:26:35 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jun 2023 23:26:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
# Mon, 26 Jun 2023 13:48:06 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 26 Jun 2023 13:48:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
ARG MAVEN_VERSION=3.9.3
# Mon, 26 Jun 2023 13:48:06 GMT
ARG USER_HOME_DIR=/root
# Mon, 26 Jun 2023 13:48:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 26 Jun 2023 13:48:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 26 Jun 2023 13:48:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:322949bc3f462f25edd57d234e2687af2a359a973c83b2d139df37b10dda65be`  
		Last Modified: Fri, 16 Jun 2023 18:06:42 GMT  
		Size: 64.1 MB (64129772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ce14cd66ceb90d76b657ab4ad5fb1fd02f1c4c50a40c9cb0adc1f8e0f57ba4`  
		Last Modified: Tue, 20 Jun 2023 23:31:26 GMT  
		Size: 158.8 MB (158795002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e6268a299d942e7935c5a079baf4e6179910ac2a0158c87f052242b18ee5b0`  
		Last Modified: Tue, 20 Jun 2023 23:55:25 GMT  
		Size: 118.9 MB (118946184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a68b7100073622d27fcfb1cde4c822fe0cd2ca41a165c51d36e5206655c75a6`  
		Last Modified: Mon, 26 Jun 2023 21:51:45 GMT  
		Size: 9.3 MB (9327565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50bb5810a15498a85bdfbc795cdd504b354054e680d2dbd2a82e24eef82a839d`  
		Last Modified: Mon, 26 Jun 2023 21:51:44 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a538b587bead3e3b288a7691cba6ec27a3cfae5c96ec20823dca51dd5160002a`  
		Last Modified: Mon, 26 Jun 2023 21:51:44 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd61606aa6fcfc1264c8b15a7cd907b43a61993cd0f1ea37f54617be42a8915`  
		Last Modified: Mon, 26 Jun 2023 21:51:44 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
