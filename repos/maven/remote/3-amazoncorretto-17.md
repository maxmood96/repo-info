## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:182bbd82522256af79c4b8fee88ac10bf72ba70de960219c5e99f275af97323b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:3a872436b3081ad4b888a4ad02ab847139ceb5445b59d224a3207f3964fd45f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.5 MB (375470883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ef87c4d17489a8d0c35a2296f7ffccd7b053fe7aa2649d80d20f2d02226c78`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 16 Mar 2024 07:59:14 GMT
COPY dir:40a794c5e13cc08a029a91ecc5d045abb1bd5b12f20c10640fe8595ecfefa662 in / 
# Sat, 16 Mar 2024 07:59:14 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 13:37:31 GMT
ARG version=17.0.10.7-1
# Sat, 16 Mar 2024 13:37:54 GMT
# ARGS: version=17.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 16 Mar 2024 13:37:55 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 13:37:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 18 Dec 2023 19:11:15 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 18 Dec 2023 19:11:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 Dec 2023 19:11:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fbbe555f6365629780fee590c2a87f84df704cf88725f26d12c40efd06a20308`  
		Last Modified: Mon, 11 Mar 2024 23:51:11 GMT  
		Size: 62.7 MB (62650553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72cc11b9b4b6209b53518f84b8c4e064b2b3be8d5eeceec97b28e8cffc40b37d`  
		Last Modified: Sat, 16 Mar 2024 13:48:30 GMT  
		Size: 151.9 MB (151944057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8362f0f621c404e60a6f0cd0e6afa6d220cfb1e3f577021a43684d2d857d231`  
		Last Modified: Sat, 16 Mar 2024 15:04:16 GMT  
		Size: 151.4 MB (151394943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfd6567336ea86de6215b740132a0fbd29cc7e5477fc653f1a8939d12dffdd8`  
		Last Modified: Sat, 16 Mar 2024 15:04:04 GMT  
		Size: 9.5 MB (9479945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097bf3c752f439dd25996a421dbd94348a0cc7ba464b8ef364befaa32954052f`  
		Last Modified: Sat, 16 Mar 2024 15:04:03 GMT  
		Size: 860.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54432d406ec619bcafadcd85e78e4c79cbde852b98207df0a0d1a1a5c20f81d1`  
		Last Modified: Sat, 16 Mar 2024 15:04:03 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc7a2f8b0f238efb0ffc22441b9de0ee16b9d0626002c90d8fddb2dd17df413`  
		Last Modified: Sat, 16 Mar 2024 15:04:03 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:52568b8271acbf9a3d06e223bf7af40afe72fe454412f7975304716e0eab202c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.9 MB (348895285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df80b6422f769b7af52659e1cdfa4ec44e16ee6c06fa1dbef174f0feb04db46`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 05 Apr 2024 18:07:30 GMT
COPY dir:5c5e76fbf44d4b5d5bbd02274337780df6faf67a7b224750d628854242527355 in / 
# Fri, 05 Apr 2024 18:07:31 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 18:47:30 GMT
ARG version=17.0.10.7-1
# Fri, 05 Apr 2024 18:47:51 GMT
# ARGS: version=17.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 05 Apr 2024 18:47:53 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 18:47:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 18 Dec 2023 19:11:15 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 18 Dec 2023 19:11:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 Dec 2023 19:11:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1e9d4daaed12ccc925403048e4968011b475e192de72d80e36180798aac508fa`  
		Last Modified: Wed, 03 Apr 2024 01:52:31 GMT  
		Size: 64.6 MB (64560609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07c5a38cf733c789b5a6260fff0d81dedc82aa35425ac61c276c1665f3f7cac`  
		Last Modified: Fri, 05 Apr 2024 18:58:50 GMT  
		Size: 150.6 MB (150572609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1b33874d9d9333e9b32fd68ef792dcf3ea1582098f5538c25c76e6629c114a`  
		Last Modified: Fri, 05 Apr 2024 19:40:43 GMT  
		Size: 124.3 MB (124280715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8a4bf29d874ea45973ca5a6af4fe0cf5b84c0a6ec5b08c14e91a94d445f2cd`  
		Last Modified: Fri, 05 Apr 2024 19:40:29 GMT  
		Size: 9.5 MB (9479968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59782180be1c2b85f6289746221d364f72c2c78d0e46d58d47bdb8b47b5c73d2`  
		Last Modified: Fri, 05 Apr 2024 19:40:28 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8f3f79879b678977dd0dc9f048983c2bccfb9347b754dcb1105152d4d5ce7f`  
		Last Modified: Fri, 05 Apr 2024 19:40:28 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f17d58453b50c01527d7953fa839526e6fbd2ee2fdc86ed499ef09df03e16a`  
		Last Modified: Fri, 05 Apr 2024 19:40:28 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
