## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:9f606bb2d4cc4ccba6c4950384992e786c969b70a201be5ce9f36783a2fe8388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:3549ece93128874684b8d243d11aee458a6b3a70c0787febad1ecf8ea95c6c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.5 MB (375470883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f91c3c67622f067aaecf8cd44ae164c7aa8fe3d40400df7a37bef9a95cdcf0`
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
# Mon, 11 Dec 2023 11:12:11 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 11 Dec 2023 11:12:11 GMT
ARG USER_HOME_DIR=/root
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 11 Dec 2023 11:12:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 11 Dec 2023 11:12:11 GMT
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
$ docker pull maven@sha256:948112e3fa9d8d01a637a549100917f3d94b89a3f2c2879f13af91e871bad316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.0 MB (346959992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c480dcffbd9162d5cc98a93bc08b605eff131db6a3a5a509c62e0379776bbe39`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 16 Mar 2024 00:06:05 GMT
COPY dir:60a98a70510e647cb179bdf64e415936867e1b536f6e2209b88df6cf5ebf8753 in / 
# Sat, 16 Mar 2024 00:06:06 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 03:42:36 GMT
ARG version=17.0.10.7-1
# Sat, 16 Mar 2024 03:42:58 GMT
# ARGS: version=17.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 16 Mar 2024 03:43:00 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 03:43:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 11 Dec 2023 11:12:11 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 11 Dec 2023 11:12:11 GMT
ARG USER_HOME_DIR=/root
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 11 Dec 2023 11:12:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 11 Dec 2023 11:12:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1210c2cda2cd148732bb93623044ab07d9ead686e335afc95ffa891e3032d56b`  
		Last Modified: Mon, 11 Mar 2024 22:40:31 GMT  
		Size: 64.6 MB (64576374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4641ad01ddd7cf9c3d3dce5b975ebb8d924676122c84c72bfc20624f51c0037e`  
		Last Modified: Sat, 16 Mar 2024 03:56:53 GMT  
		Size: 150.6 MB (150578210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705b6ff9bbf208a7d2bf64ec9c19233c721648c18ec379b1f7806f58acd17e4b`  
		Last Modified: Sat, 16 Mar 2024 13:04:06 GMT  
		Size: 122.3 MB (122324096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814bc94c672a13951d2c73f8d4ab77207d5fc7858b6f8d7ffa67f6c9e4edb692`  
		Last Modified: Sat, 16 Mar 2024 13:03:57 GMT  
		Size: 9.5 MB (9479932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330700e51a6ce20477dc882fcc0dd9da78058e4c419b9b9a3dbce826e97b11ad`  
		Last Modified: Sat, 16 Mar 2024 13:03:56 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0faae141de04a62eaf0914cfdf6662e58c6e29c3d63b8f3c985c087cdfeea6d8`  
		Last Modified: Sat, 16 Mar 2024 13:03:57 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd2e2775cbc5adefe22ecff59d5740e558aa94ff144c8fc6c60d0faa641657a`  
		Last Modified: Sat, 16 Mar 2024 13:03:56 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
