## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:beaa74bc548683b0008a9635322f3d98922e8c63755f4c0ded95dc9e25ccd080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:45714a68a876bf56be8078c57f56d2fe9b4b47828418b80e492c6e86f15e550c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.3 MB (150301801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeedd4a2fef5999bac4527858037048dc2d2d69b85cea66f5406ee9f3cb1e47d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 01 Oct 2021 21:20:20 GMT
ADD file:21dc1ad70daefae1cf0e1b3e78fab06decda5cb9bc958d8a178adb3eddd1fb32 in / 
# Fri, 01 Oct 2021 21:20:20 GMT
CMD ["/bin/bash"]
# Fri, 01 Oct 2021 21:39:00 GMT
ARG version=1.8.0_302.b08-1
# Fri, 01 Oct 2021 21:39:20 GMT
# ARGS: version=1.8.0_302.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 01 Oct 2021 21:39:20 GMT
ENV LANG=C.UTF-8
# Fri, 01 Oct 2021 21:39:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 01 Oct 2021 22:20:48 GMT
ARG MAVEN_VERSION=3.8.2
# Fri, 01 Oct 2021 22:20:49 GMT
ARG USER_HOME_DIR=/root
# Fri, 01 Oct 2021 22:20:49 GMT
ARG SHA=b0bf39460348b2d8eae1c861ced6c3e8a077b6e761fb3d4669be5de09490521a74db294cf031b0775b2dfcd57bd82246e42ce10904063ef8e3806222e686f222
# Fri, 01 Oct 2021 22:20:49 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.2/binaries
# Fri, 01 Oct 2021 22:20:58 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.2/binaries MAVEN_VERSION=3.8.2 SHA=b0bf39460348b2d8eae1c861ced6c3e8a077b6e761fb3d4669be5de09490521a74db294cf031b0775b2dfcd57bd82246e42ce10904063ef8e3806222e686f222 USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Fri, 01 Oct 2021 22:21:07 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.2/binaries MAVEN_VERSION=3.8.2 SHA=b0bf39460348b2d8eae1c861ced6c3e8a077b6e761fb3d4669be5de09490521a74db294cf031b0775b2dfcd57bd82246e42ce10904063ef8e3806222e686f222 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 01 Oct 2021 22:21:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 01 Oct 2021 22:21:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 01 Oct 2021 22:21:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 01 Oct 2021 22:21:08 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 01 Oct 2021 22:21:08 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 01 Oct 2021 22:21:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 01 Oct 2021 22:21:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0728ce74490afacced1ac863ee989913071f97c52ab996e46cdd6b5369a2d63a`  
		Last Modified: Fri, 01 Oct 2021 10:54:14 GMT  
		Size: 62.0 MB (61952638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4427fc41f60de7402bd4220fcc04d95ec47eca25a9d36918efdf2beae74a0bdd`  
		Last Modified: Fri, 01 Oct 2021 21:41:47 GMT  
		Size: 75.3 MB (75341685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d1846c6a085fd809481d1abac169e9be91cac931a322fb70f2dc02c8396842`  
		Last Modified: Fri, 01 Oct 2021 22:24:31 GMT  
		Size: 3.6 MB (3600811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274d949672bdaa087826111d227b8cf3e484fa1c769066733c1d075af8be843c`  
		Last Modified: Fri, 01 Oct 2021 22:24:31 GMT  
		Size: 9.4 MB (9405458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b226d11d41a3c3f7332c9b4f98fe24c18d31498369d0dbd7bb620bebb499a03d`  
		Last Modified: Fri, 01 Oct 2021 22:24:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a61e4d9ac7acdabc3d6084e6a75d0818800bc887d2c8288b691fcce3dd8e68`  
		Last Modified: Fri, 01 Oct 2021 22:24:30 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:bee69e0a9c6e7e24fec04f8e31e9f7aa2bebc9cd08bfca98e72493643d429707
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135967438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1a7c4378ea15448213025f34cec8b2223f36833ad2e92137dfb366140f63a6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 01 Oct 2021 21:39:54 GMT
ADD file:1d2ae2bfc4c1f83dc53f48b42503812d345622ab95d8fc84536216ef3d53d807 in / 
# Fri, 01 Oct 2021 21:39:55 GMT
CMD ["/bin/bash"]
# Fri, 01 Oct 2021 21:57:32 GMT
ARG version=1.8.0_302.b08-1
# Fri, 01 Oct 2021 21:57:50 GMT
# ARGS: version=1.8.0_302.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 01 Oct 2021 21:57:50 GMT
ENV LANG=C.UTF-8
# Fri, 01 Oct 2021 21:57:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 01 Oct 2021 22:21:07 GMT
ARG MAVEN_VERSION=3.8.2
# Fri, 01 Oct 2021 22:21:08 GMT
ARG USER_HOME_DIR=/root
# Fri, 01 Oct 2021 22:21:08 GMT
ARG SHA=b0bf39460348b2d8eae1c861ced6c3e8a077b6e761fb3d4669be5de09490521a74db294cf031b0775b2dfcd57bd82246e42ce10904063ef8e3806222e686f222
# Fri, 01 Oct 2021 22:21:08 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.2/binaries
# Fri, 01 Oct 2021 22:21:16 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.2/binaries MAVEN_VERSION=3.8.2 SHA=b0bf39460348b2d8eae1c861ced6c3e8a077b6e761fb3d4669be5de09490521a74db294cf031b0775b2dfcd57bd82246e42ce10904063ef8e3806222e686f222 USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Fri, 01 Oct 2021 22:21:24 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.2/binaries MAVEN_VERSION=3.8.2 SHA=b0bf39460348b2d8eae1c861ced6c3e8a077b6e761fb3d4669be5de09490521a74db294cf031b0775b2dfcd57bd82246e42ce10904063ef8e3806222e686f222 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 01 Oct 2021 22:21:24 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 01 Oct 2021 22:21:24 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 01 Oct 2021 22:21:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 01 Oct 2021 22:21:25 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 01 Oct 2021 22:21:25 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 01 Oct 2021 22:21:25 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 01 Oct 2021 22:21:25 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5aa4871be3ec1bcadf7a5257231adc7740edac9a612749884f03ab14b4b2d4ec`  
		Last Modified: Fri, 01 Oct 2021 16:32:04 GMT  
		Size: 63.6 MB (63581978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59aa11c1c46065f0e96c13fcd24b5d373b0d7152e74ec2eaa61aa3c0582ede4`  
		Last Modified: Fri, 01 Oct 2021 22:00:20 GMT  
		Size: 59.4 MB (59393641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b7167b5855f6d4a6ffdb28bf1b893b169e0c32c0660989229907d9c32664e7`  
		Last Modified: Fri, 01 Oct 2021 22:26:40 GMT  
		Size: 3.6 MB (3585138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d994c0570696b67f8ce1612b816d703253ca9a758ac3bb71ead81aef25a300`  
		Last Modified: Fri, 01 Oct 2021 22:26:41 GMT  
		Size: 9.4 MB (9405469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52efb95c5f6ee5270ffb89863e5d52dcf1314544103cbb7f496564f0318af1b`  
		Last Modified: Fri, 01 Oct 2021 22:26:40 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01888509edfe7ce066c86f80bdd2fe21aebff6d8be88451dd5be705c03e54e37`  
		Last Modified: Fri, 01 Oct 2021 22:26:40 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
