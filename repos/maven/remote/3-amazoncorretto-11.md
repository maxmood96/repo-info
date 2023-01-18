## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:52870f789f4d6bbcd442298e6fde342c3022450f6a8bd9dde31ffc7c0dfc4efd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:f07b7d68c7967a5a61f23e5e145da44c0723853bc1c0419c31b63f564dcdfacd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.1 MB (222099464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b99f2966e4adf9bebec35bbb3758c6335677427bf4834b97a0f7f8dc906529`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 16 Dec 2022 01:19:49 GMT
ADD file:a69ca7a5499bcd9d6e4317fdbd7256e93be44364bb746f5da10b4268c090bda0 in / 
# Fri, 16 Dec 2022 01:19:50 GMT
CMD ["/bin/bash"]
# Wed, 18 Jan 2023 20:23:49 GMT
ARG version=11.0.18.10-1
# Wed, 18 Jan 2023 20:24:14 GMT
# ARGS: version=11.0.18.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 18 Jan 2023 20:24:15 GMT
ENV LANG=C.UTF-8
# Wed, 18 Jan 2023 20:24:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 18 Jan 2023 21:00:27 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Wed, 18 Jan 2023 21:00:28 GMT
ARG MAVEN_VERSION=3.8.7
# Wed, 18 Jan 2023 21:00:28 GMT
ARG USER_HOME_DIR=/root
# Wed, 18 Jan 2023 21:00:28 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Wed, 18 Jan 2023 21:00:28 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Wed, 18 Jan 2023 21:00:36 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 18 Jan 2023 21:00:36 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 18 Jan 2023 21:00:36 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 18 Jan 2023 21:00:36 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 18 Jan 2023 21:00:36 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 18 Jan 2023 21:00:36 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 18 Jan 2023 21:00:36 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5b4a36b5b78f93a5f470cf722b313bb32cddb0f8e0fa0db348059b5c0881b04f`  
		Last Modified: Thu, 15 Dec 2022 23:08:20 GMT  
		Size: 62.3 MB (62328625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f55f2021815a051cafaba1ebe12a8234c8d17320223fc81d0409df4084c28fd`  
		Last Modified: Wed, 18 Jan 2023 20:35:12 GMT  
		Size: 147.8 MB (147787288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4404910a6e2efcadad6a75e7adb309bbec31945fb53b54a77f9a4dcfeeb80fe`  
		Last Modified: Wed, 18 Jan 2023 21:04:05 GMT  
		Size: 3.6 MB (3631153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d06d586bc20a61994242a5c5530024098fd1466b0e18ad200e8ad907766a26`  
		Last Modified: Wed, 18 Jan 2023 21:04:05 GMT  
		Size: 8.4 MB (8351182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c67e4eaf810ad6d12c8082e1e2d9ab483732463e943935e4970c23da24c335`  
		Last Modified: Wed, 18 Jan 2023 21:04:04 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d49157100791874ef4b7fbfbd462d5520622ac571f71b3efb9039b32d82038`  
		Last Modified: Wed, 18 Jan 2023 21:04:04 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:4d4b49433a35f1806da47a9334d0701da8edd0975162c93f6c2e87fcc9b60374
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220920509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebbfaaf513fd8dad27015a435afebedc5b9812bd8c58ce12d16906a545bec778`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 16 Dec 2022 00:41:05 GMT
ADD file:26a6bf75c84c408d289e5569f13b1c65206966f875cdfc53ded0670cb85e35bf in / 
# Fri, 16 Dec 2022 00:41:07 GMT
CMD ["/bin/bash"]
# Wed, 18 Jan 2023 20:39:58 GMT
ARG version=11.0.18.10-1
# Wed, 18 Jan 2023 20:40:16 GMT
# ARGS: version=11.0.18.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 18 Jan 2023 20:40:17 GMT
ENV LANG=C.UTF-8
# Wed, 18 Jan 2023 20:40:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 18 Jan 2023 21:03:03 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Wed, 18 Jan 2023 21:03:03 GMT
ARG MAVEN_VERSION=3.8.7
# Wed, 18 Jan 2023 21:03:03 GMT
ARG USER_HOME_DIR=/root
# Wed, 18 Jan 2023 21:03:03 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Wed, 18 Jan 2023 21:03:03 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Wed, 18 Jan 2023 21:03:09 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 18 Jan 2023 21:03:09 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 18 Jan 2023 21:03:09 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 18 Jan 2023 21:03:09 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 18 Jan 2023 21:03:09 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 18 Jan 2023 21:03:09 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 18 Jan 2023 21:03:09 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6cbfee25f0741b3d3f4d2474d904a200cd8404a01aa17813bf3fc3d4ebb551a4`  
		Last Modified: Thu, 15 Dec 2022 23:08:20 GMT  
		Size: 64.0 MB (63964214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec844dce5e3e166143eef9f0213107e39132eeb0a192b134af1c48df884cbd2`  
		Last Modified: Wed, 18 Jan 2023 20:44:28 GMT  
		Size: 145.0 MB (144956175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e270b720b6e9e46fc2a9f8a2fd214cb0b28a55492958b761958665b5f47f70ed`  
		Last Modified: Wed, 18 Jan 2023 21:05:21 GMT  
		Size: 3.6 MB (3647734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543b81bd3ca70b3be3f09b402e5b65689c3356bd1cf6268ffe864eb26234381`  
		Last Modified: Wed, 18 Jan 2023 21:05:21 GMT  
		Size: 8.4 MB (8351169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d625e54ca5ed34abf49cb119234f084e8f338931da27d188e2fb188e858aff09`  
		Last Modified: Wed, 18 Jan 2023 21:05:20 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3adcbf689964d24aa7b9fffa788a0dda791849b53029977b330f42a0b82426`  
		Last Modified: Wed, 18 Jan 2023 21:05:20 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
