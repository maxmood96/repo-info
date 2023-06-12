## `maven:amazoncorretto`

```console
$ docker pull maven@sha256:3a4610cd9cc930707e829c835df60335954bc94bf5b2093b6a93dfaa0bbe2e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:f2df128b2961f99922392fc796df9d253fc3930782734528ca834b888105c0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.4 MB (373416382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22440afb8989cc22843adebd72f90ddf299a6755353c42e2299db3da218fec0f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 12 Jun 2023 19:20:12 GMT
COPY dir:fcef1a58ca6f7120ef8bf5af7158a168707c721bb2ebb75f4483ac8ec6174c3f in / 
# Mon, 12 Jun 2023 19:20:13 GMT
CMD ["/bin/bash"]
# Mon, 12 Jun 2023 19:38:41 GMT
ARG version=11.0.19.7-1
# Mon, 12 Jun 2023 19:39:05 GMT
# ARGS: version=11.0.19.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 12 Jun 2023 19:39:06 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jun 2023 19:39:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:480bf58f72b4bbe5678732504474d092d31d21283abd2db6fb6640d698c4b2ab`  
		Last Modified: Mon, 12 Jun 2023 19:44:39 GMT  
		Size: 147.8 MB (147786810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1899e8e37745eb41aade791371104eecea45156918ced242cd0e55f73be0e288`  
		Last Modified: Mon, 12 Jun 2023 20:56:33 GMT  
		Size: 153.8 MB (153820499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1e67e393aa37ef86e1e8851144dbcdb142e7ed7a7ab380af6695ce959e87f0`  
		Last Modified: Mon, 12 Jun 2023 20:56:21 GMT  
		Size: 9.3 MB (9314408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f037b2f51e9b2e08001e497d2afc0cccaeaff4ba63bf233abb7408d72ebe105`  
		Last Modified: Mon, 12 Jun 2023 20:56:20 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd0d4c22ec20845edc35fa02619832f8dd773fc507b108ac7c1226ec78e4d75`  
		Last Modified: Mon, 12 Jun 2023 20:56:20 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d101f4b5f68a571963f22d38e4627cce4b9a3858fc6338e20d9b19bfd7a0ee2`  
		Last Modified: Mon, 12 Jun 2023 20:56:20 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:674e347e04bb2630cc873800ff5e999af5d6af18cdfa5d88713d890acd175df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337125511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f88adc8175e54275720adb9919e0affaa234d868767da7eec7b2acd4f7c74b1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 12 Jun 2023 19:39:41 GMT
COPY dir:51df2295aa01017be94f36c53673ecd4aa152aa99ad3c20338f5409440ff57f7 in / 
# Mon, 12 Jun 2023 19:39:42 GMT
CMD ["/bin/bash"]
# Mon, 12 Jun 2023 19:56:22 GMT
ARG version=11.0.19.7-1
# Mon, 12 Jun 2023 19:56:43 GMT
# ARGS: version=11.0.19.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 12 Jun 2023 19:56:45 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jun 2023 19:56:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:d230810294aeb4c5e07869834731892493ac7269c38f064f575c4543fb500e6e`  
		Last Modified: Mon, 12 Jun 2023 20:01:30 GMT  
		Size: 144.9 MB (144941516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8ba1397211b0d2dd16b79316c0371a33a1e8a1c95b0c3d8c23da23d0a6b425`  
		Last Modified: Mon, 12 Jun 2023 20:48:34 GMT  
		Size: 118.7 MB (118728540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8629af114b1c2afb03c68ca547d27877a06d217fe2ace1af3e1f8ed200b823a9`  
		Last Modified: Mon, 12 Jun 2023 20:48:27 GMT  
		Size: 9.3 MB (9314410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9975d3b9947e40db958e01e141f1684ef70a29acdbdd1b3b9e7e62798ab120bc`  
		Last Modified: Mon, 12 Jun 2023 20:48:26 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcfb5ac84d08bd59aa1e64f55219331091464fc144bc30341d25b03e7b17b6e3`  
		Last Modified: Mon, 12 Jun 2023 20:48:26 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c5d0c120bf00b2cd920da36cd295da15d431ad9b2ecb72e9f67c411f8e8b5e`  
		Last Modified: Mon, 12 Jun 2023 20:48:26 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
