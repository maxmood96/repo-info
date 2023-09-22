## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:1024d9c451cf1b23d3bc510b1b51f39e8bc5c2b12d9e1537efe08b92e828eea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:e2c6854d4944eb0b97594a5a00191c61e92b859cd1080d8660ce205cb14287d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.2 MB (376214804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ce199e70ea86dbd20fa0dfb45dacd9a559e0da4174d56afaae7d0149f13a0f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 29 Aug 2023 18:29:22 GMT
COPY dir:591ada5c2fb65633b614a3ff732e6d83dcd91fe9ae925844fe9ba3323311bf74 in / 
# Tue, 29 Aug 2023 18:29:23 GMT
CMD ["/bin/bash"]
# Fri, 22 Sep 2023 00:21:15 GMT
ARG version=21.0.0.35-1
# Fri, 22 Sep 2023 00:21:52 GMT
# ARGS: version=21.0.0.35-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 22 Sep 2023 00:21:53 GMT
ENV LANG=C.UTF-8
# Fri, 22 Sep 2023 00:21:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 22 Sep 2023 09:11:50 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 22 Sep 2023 09:11:50 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 22 Sep 2023 09:11:50 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 22 Sep 2023 09:11:50 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 22 Sep 2023 09:11:50 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 22 Sep 2023 09:11:50 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 22 Sep 2023 09:11:50 GMT
ARG MAVEN_VERSION=3.9.4
# Fri, 22 Sep 2023 09:11:50 GMT
ARG USER_HOME_DIR=/root
# Fri, 22 Sep 2023 09:11:50 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 22 Sep 2023 09:11:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 22 Sep 2023 09:11:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8be3d01330d7e2e197495d440aa60d14ac366aad5e8d105d86e384876aefec18`  
		Last Modified: Fri, 25 Aug 2023 08:53:43 GMT  
		Size: 62.5 MB (62477278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431d68e139e72b927b43c4d934ed4d14137aead2ddddfb7a1e713391aa90a0cf`  
		Last Modified: Fri, 22 Sep 2023 00:26:52 GMT  
		Size: 165.4 MB (165433736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb119251e7ac3b5dfc69016d0d066425372b032b35001f7a130bffc2bcc72fef`  
		Last Modified: Fri, 22 Sep 2023 19:24:16 GMT  
		Size: 138.9 MB (138895992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3166abe53b87004d22dd6f6fde70526e30b181ec03ffc5a9331a631ace327086`  
		Last Modified: Fri, 22 Sep 2023 19:24:00 GMT  
		Size: 9.4 MB (9406411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41bb2c3dc2923871f0d8bc3bc2bb884466df1f81169040e57deca7e8e1a78b6`  
		Last Modified: Fri, 22 Sep 2023 19:23:59 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1382eda787f19158bbe7eaf890fd2539ec13b8cbedf89958531b0119fae922c1`  
		Last Modified: Fri, 22 Sep 2023 19:23:59 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0671b5b62ddcb44177a08a074eba625a240af5f84a21f091fa8e70f2c1cbb8a4`  
		Last Modified: Fri, 22 Sep 2023 19:23:59 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
