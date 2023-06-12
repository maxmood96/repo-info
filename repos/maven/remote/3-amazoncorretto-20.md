## `maven:3-amazoncorretto-20`

```console
$ docker pull maven@sha256:c2f67f0e0181bc9e11fda1c7b49a228e975c19b377291a4ed9565e31e9808729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-20` - linux; amd64

```console
$ docker pull maven@sha256:6c3686088503d8247d2e1197679cb30d456a9ad89a02c01437d7cadd038b6b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.4 MB (386398006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364ed57fa965a34d8e2b567b009d421c57d3e8d90ae551fdc17a054d22c74e4b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 12 Jun 2023 19:20:12 GMT
COPY dir:fcef1a58ca6f7120ef8bf5af7158a168707c721bb2ebb75f4483ac8ec6174c3f in / 
# Mon, 12 Jun 2023 19:20:13 GMT
CMD ["/bin/bash"]
# Mon, 12 Jun 2023 19:41:51 GMT
ARG version=20.0.1.9-1
# Mon, 12 Jun 2023 19:42:18 GMT
# ARGS: version=20.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 12 Jun 2023 19:42:18 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jun 2023 19:42:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
# Tue, 16 May 2023 11:35:55 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 16 May 2023 11:35:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 16 May 2023 11:35:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 16 May 2023 11:35:55 GMT
ARG MAVEN_VERSION=3.9.2
# Tue, 16 May 2023 11:35:55 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 May 2023 11:35:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 May 2023 11:35:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 May 2023 11:35:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8c8d630364ddfad51ca27951f43586450b97e006740d3139ac1c7fc1fa1a48ab`  
		Last Modified: Wed, 07 Jun 2023 18:46:43 GMT  
		Size: 62.5 MB (62493283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f4ed3d4d0eb7d73c0959e9ffc09d21d9096ba38bd73921c68ed7745cd383c6`  
		Last Modified: Mon, 12 Jun 2023 19:47:31 GMT  
		Size: 160.8 MB (160763510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef30371af82f04a49a541bcca42d66922d6587cd197bbddfa97aa2bab9683d5`  
		Last Modified: Mon, 12 Jun 2023 20:57:29 GMT  
		Size: 153.8 MB (153825429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4dc5cdf3eb527fe5d126aa807e7d3db96e88196b22dd09dc251c75c2e7fe75`  
		Last Modified: Mon, 12 Jun 2023 20:57:17 GMT  
		Size: 9.3 MB (9314404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d86ef01951297d6dba08c8a5f69b5f77658111a86bfcd18fd1c313398f7ffc`  
		Last Modified: Mon, 12 Jun 2023 20:57:16 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1924b655b4c3c3cb6550109b5b91cdb7c905b2677a5f40a9da13b7aa711a3ada`  
		Last Modified: Mon, 12 Jun 2023 20:57:16 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f14dd1d45f4efa53c50e57318dd9f0fee084b49cfda3600281818b4f72ade7`  
		Last Modified: Mon, 12 Jun 2023 20:57:16 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-20` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:4dbfbe2079a1068798b4b2b298cf9a6b5035ca7422f272e056fd3d5a0075eaae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350953355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b6a80125ec4642e01d15dd09d29106404d2ba5b1cde07adda52ac36eb1147d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 12 Jun 2023 19:39:41 GMT
COPY dir:51df2295aa01017be94f36c53673ecd4aa152aa99ad3c20338f5409440ff57f7 in / 
# Mon, 12 Jun 2023 19:39:42 GMT
CMD ["/bin/bash"]
# Mon, 12 Jun 2023 19:59:11 GMT
ARG version=20.0.1.9-1
# Mon, 12 Jun 2023 19:59:33 GMT
# ARGS: version=20.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 12 Jun 2023 19:59:35 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jun 2023 19:59:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
# Tue, 16 May 2023 11:35:55 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 16 May 2023 11:35:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 16 May 2023 11:35:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 16 May 2023 11:35:55 GMT
ARG MAVEN_VERSION=3.9.2
# Tue, 16 May 2023 11:35:55 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 May 2023 11:35:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 May 2023 11:35:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 May 2023 11:35:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7943399bb3e529e35dfa651db084f8cbc0868d64a866e4cc4c88d2f0043943a8`  
		Last Modified: Wed, 07 Jun 2023 18:37:02 GMT  
		Size: 64.1 MB (64139660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371c45046361446db5da0f6ce4e2e9d5ed459efdb264a7c4ee89145a89c33456`  
		Last Modified: Mon, 12 Jun 2023 20:04:09 GMT  
		Size: 158.8 MB (158785683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0584c6b3848eb3cea521346b5361b787958fc217cfbbc447f8cf2279b9cfa2`  
		Last Modified: Mon, 12 Jun 2023 20:49:24 GMT  
		Size: 118.7 MB (118712214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c21975db3f885b7d128ce84ca1efbe43b2f2b2a11d5392189d958d24f110c31`  
		Last Modified: Mon, 12 Jun 2023 20:49:16 GMT  
		Size: 9.3 MB (9314413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f39a1ba7d1c975916225a30ba86642e97a3451c4f6bd3df850827080fe1ec7`  
		Last Modified: Mon, 12 Jun 2023 20:49:16 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda77d578ce0bf5845dfacabe2a06e3bed25b2ceb2cbe58d7fdbb3a95bb2fbf7`  
		Last Modified: Mon, 12 Jun 2023 20:49:15 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654f88b96a45668e1c89329251304dabac9e6a7aba932637fe7a2f95c10924b3`  
		Last Modified: Mon, 12 Jun 2023 20:49:16 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
