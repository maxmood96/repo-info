## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:1b77a4d0425011ef5d0a13e0d448e27a5a0181ca73c80fa8710a9fe00fddeae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:9dbb2bd2f629195525e076224750d44048caf06577e37f41c47b8dbe3169b161
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149877503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36f548df1017afe6253f5d8f9484a29ea58e9bee163aa3ac1688818b36de7af`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 16 Dec 2022 01:19:49 GMT
ADD file:a69ca7a5499bcd9d6e4317fdbd7256e93be44364bb746f5da10b4268c090bda0 in / 
# Fri, 16 Dec 2022 01:19:50 GMT
CMD ["/bin/bash"]
# Wed, 18 Jan 2023 20:19:36 GMT
ARG version=1.8.0_362.b08-1
# Wed, 18 Jan 2023 20:19:58 GMT
# ARGS: version=1.8.0_362.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 18 Jan 2023 20:19:58 GMT
ENV LANG=C.UTF-8
# Wed, 18 Jan 2023 20:19:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 18 Jan 2023 21:01:27 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Wed, 18 Jan 2023 21:01:27 GMT
ARG MAVEN_VERSION=3.8.7
# Wed, 18 Jan 2023 21:01:28 GMT
ARG USER_HOME_DIR=/root
# Wed, 18 Jan 2023 21:01:28 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Wed, 18 Jan 2023 21:01:28 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Wed, 18 Jan 2023 21:01:35 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 18 Jan 2023 21:01:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 18 Jan 2023 21:01:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 18 Jan 2023 21:01:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 18 Jan 2023 21:01:36 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 18 Jan 2023 21:01:36 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 18 Jan 2023 21:01:36 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 18 Jan 2023 21:01:36 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5b4a36b5b78f93a5f470cf722b313bb32cddb0f8e0fa0db348059b5c0881b04f`  
		Last Modified: Thu, 15 Dec 2022 23:08:20 GMT  
		Size: 62.3 MB (62328625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828bbbb52f997e482d12d7af1e9d075fcc2b7705cfc2214e96b08e225d4f8a6b`  
		Last Modified: Wed, 18 Jan 2023 20:31:24 GMT  
		Size: 75.6 MB (75568930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775abb90f55916573ad707515f86a4f743492a6521f91dbbca47055cd67588b9`  
		Last Modified: Wed, 18 Jan 2023 21:04:47 GMT  
		Size: 3.6 MB (3627547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3dfd507c953306e0cc7684471508b05f78494d86db76c8fa25c124e8e7a9671`  
		Last Modified: Wed, 18 Jan 2023 21:04:47 GMT  
		Size: 8.4 MB (8351187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e0b040ab5938c1c5845e0204372e4f6e6ed823fae45c590b4e633ccc5817f1`  
		Last Modified: Wed, 18 Jan 2023 21:04:46 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7a399b272ee8d5604dbd253b4f3310ebb187315342f30ba4d982d24e6e648b`  
		Last Modified: Wed, 18 Jan 2023 21:04:46 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:9bb40730151e1e445adc4fddcbe88cedae8bdc7ffd4d9198caba168e3afeaadd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135550480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7317a8feaa9800f724c1cb647975b9645a2ff7fe3e42406ba5110beecdf37cd5`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 16 Dec 2022 00:41:05 GMT
ADD file:26a6bf75c84c408d289e5569f13b1c65206966f875cdfc53ded0670cb85e35bf in / 
# Fri, 16 Dec 2022 00:41:07 GMT
CMD ["/bin/bash"]
# Wed, 18 Jan 2023 20:39:18 GMT
ARG version=1.8.0_362.b08-1
# Wed, 18 Jan 2023 20:39:35 GMT
# ARGS: version=1.8.0_362.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 18 Jan 2023 20:39:36 GMT
ENV LANG=C.UTF-8
# Wed, 18 Jan 2023 20:39:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 18 Jan 2023 21:03:52 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Wed, 18 Jan 2023 21:03:52 GMT
ARG MAVEN_VERSION=3.8.7
# Wed, 18 Jan 2023 21:03:52 GMT
ARG USER_HOME_DIR=/root
# Wed, 18 Jan 2023 21:03:52 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Wed, 18 Jan 2023 21:03:52 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Wed, 18 Jan 2023 21:03:59 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 18 Jan 2023 21:03:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 18 Jan 2023 21:04:00 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 18 Jan 2023 21:04:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 18 Jan 2023 21:04:00 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 18 Jan 2023 21:04:00 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 18 Jan 2023 21:04:00 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 18 Jan 2023 21:04:00 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6cbfee25f0741b3d3f4d2474d904a200cd8404a01aa17813bf3fc3d4ebb551a4`  
		Last Modified: Thu, 15 Dec 2022 23:08:20 GMT  
		Size: 64.0 MB (63964214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112796c846ba50588965e42754a37ac5559197d230cb95d874cc89a8248e789f`  
		Last Modified: Wed, 18 Jan 2023 20:43:37 GMT  
		Size: 59.6 MB (59599868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314b30e87dd5675dae32498a8c3b2bdd12e895e6d5ed3a5e696db6e98aebcdfb`  
		Last Modified: Wed, 18 Jan 2023 21:06:03 GMT  
		Size: 3.6 MB (3634008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ad2fccf39b3bb3ac3b2a3b458ada16edb46497f256021d34b1c7767ba9e5cd`  
		Last Modified: Wed, 18 Jan 2023 21:06:03 GMT  
		Size: 8.4 MB (8351174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca885c9c544569a0106db5e6f4c43d8d01d8c053d3ea62df8e575af0a3e9324`  
		Last Modified: Wed, 18 Jan 2023 21:06:03 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052905b0d95a42dab841a054e7c4e8873ac4d2d8b7935ab5c824cfd76c795623`  
		Last Modified: Wed, 18 Jan 2023 21:06:03 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
