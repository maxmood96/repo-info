## `maven:3-amazoncorretto`

```console
$ docker pull maven@sha256:ff8ec9fd8449d63695dd3a0ca206aeb87047b83b19fd6d2569884eb773b9f5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:1c85d03f7dc373c5ee6f4d21b96972ae88fc3f5c2062998127ae4106ebacf9e3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221659928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d39ffaec09fb6a2099d6321bcba4982ec355d4ee5eab12913cece72e214330`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 03 May 2022 23:19:31 GMT
ADD file:386c34c6960464ef8f88891333fb091aef731602a28a185a9d6db27726fbe504 in / 
# Tue, 03 May 2022 23:19:32 GMT
CMD ["/bin/bash"]
# Wed, 04 May 2022 00:02:46 GMT
ARG version=11.0.15.9-1
# Wed, 04 May 2022 00:03:11 GMT
# ARGS: version=11.0.15.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 04 May 2022 00:03:11 GMT
ENV LANG=C.UTF-8
# Wed, 04 May 2022 00:03:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 04 May 2022 00:25:00 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Wed, 15 Jun 2022 18:22:52 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 15 Jun 2022 18:22:52 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Jun 2022 18:22:52 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 15 Jun 2022 18:22:52 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 15 Jun 2022 18:22:58 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 15 Jun 2022 18:22:58 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Jun 2022 18:22:58 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Jun 2022 18:22:59 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 15 Jun 2022 18:22:59 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 15 Jun 2022 18:22:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Jun 2022 18:22:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8de5b65bd171294b1e04e0df439f4ea11ce923b642eddf3b3d76d297bfd2670c`  
		Last Modified: Mon, 02 May 2022 22:06:03 GMT  
		Size: 62.3 MB (62291142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d24904f7237b09e359fd66273bf3d4c42b1e1eb74b99cb8c17e79d58caee9a1`  
		Last Modified: Wed, 04 May 2022 00:07:01 GMT  
		Size: 147.0 MB (146985840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49b4182752c0ee8bcbf69ebf2791339aea19bb3e1bb86bf83a382631f9bdadf`  
		Last Modified: Wed, 04 May 2022 00:27:45 GMT  
		Size: 3.6 MB (3642235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcdc3418dec3e29d8a49c95f33ea1005e86ee2f3861496701d7ae6ffb4193a2`  
		Last Modified: Wed, 15 Jun 2022 18:30:54 GMT  
		Size: 8.7 MB (8739496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954ada8bf87787809a6b168011e9f7299dca68548caeec347f847f47d06f4515`  
		Last Modified: Wed, 15 Jun 2022 18:30:53 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c452a5915e50bdbc9b7b9ff3c7930a151282ea64b8486cb5cfe17bfd232522a`  
		Last Modified: Wed, 15 Jun 2022 18:30:53 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:4fdf9e6f3f0c886fe5004417c12c8800128b92f08b92466a674be8faa20a8831
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220478271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ae76b588acc8c70357f0a54a79a4ab37ff4cd5fd4aca70c365fb82d1b09c1c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 03 May 2022 22:39:32 GMT
ADD file:c351a8c80719ef38e02c26849f50bb7d79c24a6347cc2a72ae1a0768964bd113 in / 
# Tue, 03 May 2022 22:39:34 GMT
CMD ["/bin/bash"]
# Wed, 04 May 2022 00:21:16 GMT
ARG version=11.0.15.9-1
# Wed, 04 May 2022 00:21:28 GMT
# ARGS: version=11.0.15.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 04 May 2022 00:21:28 GMT
ENV LANG=C.UTF-8
# Wed, 04 May 2022 00:21:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 04 May 2022 00:42:08 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Wed, 15 Jun 2022 18:45:44 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 15 Jun 2022 18:45:45 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Jun 2022 18:45:46 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 15 Jun 2022 18:45:47 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 15 Jun 2022 18:45:50 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 15 Jun 2022 18:45:51 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Jun 2022 18:45:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Jun 2022 18:45:54 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 15 Jun 2022 18:45:55 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 15 Jun 2022 18:45:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Jun 2022 18:45:56 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ec3b4c26678b188d3874bed5e14dd278311fc05c81e418d5f0da36ec38d9f488`  
		Last Modified: Tue, 03 May 2022 03:07:52 GMT  
		Size: 63.9 MB (63902179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cf0ac4dd2e460d5683fed0b58f5db05785fe85b42c71b6bed852c21865e22f`  
		Last Modified: Wed, 04 May 2022 00:23:51 GMT  
		Size: 144.2 MB (144209078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a703e1691205e898b0699041d5767bce5df5f7c92f10b2f25ea84b26580617`  
		Last Modified: Wed, 04 May 2022 00:46:09 GMT  
		Size: 3.6 MB (3626344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e40ec64b1d8579694d8a0e3c7d3f8bb18298c3b8fb7d421d70de002088aaa41`  
		Last Modified: Wed, 15 Jun 2022 18:54:21 GMT  
		Size: 8.7 MB (8739457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce6b2c3d8ec8f90eb4f0cb41b9a593bc1732ac9c1fe84430bd945acdea3a713`  
		Last Modified: Wed, 15 Jun 2022 18:54:20 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bcce18922d13eec3762e382e08580f4babba2f574cba120e5cbdb1ba376a77`  
		Last Modified: Wed, 15 Jun 2022 18:54:20 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
