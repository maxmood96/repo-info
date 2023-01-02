## `maven:3-amazoncorretto-19`

```console
$ docker pull maven@sha256:48674c3ffffc1d838843045fe6abcf2a1b63e9525ed6bcf13ab0c3ca87fed1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-19` - linux; amd64

```console
$ docker pull maven@sha256:d814743587fa323d5f9de119eede2a3ddf35b0e49b65e8988887b74e56deee24
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233689801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a89f6982e6c96fa9d0675529e1978e2761f77cbddba29404dd507a3369ef2f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 16 Dec 2022 01:19:49 GMT
ADD file:a69ca7a5499bcd9d6e4317fdbd7256e93be44364bb746f5da10b4268c090bda0 in / 
# Fri, 16 Dec 2022 01:19:50 GMT
CMD ["/bin/bash"]
# Fri, 16 Dec 2022 02:18:05 GMT
ARG version=19.0.1.10-1
# Fri, 16 Dec 2022 02:18:44 GMT
# ARGS: version=19.0.1.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-19-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-19-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 16 Dec 2022 02:18:45 GMT
ENV LANG=C.UTF-8
# Fri, 16 Dec 2022 02:18:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-19-amazon-corretto
# Fri, 16 Dec 2022 03:12:28 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Mon, 02 Jan 2023 18:41:49 GMT
ARG MAVEN_VERSION=3.8.7
# Mon, 02 Jan 2023 18:41:49 GMT
ARG USER_HOME_DIR=/root
# Mon, 02 Jan 2023 18:41:50 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Mon, 02 Jan 2023 18:41:50 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Mon, 02 Jan 2023 18:41:56 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 02 Jan 2023 18:41:56 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 02 Jan 2023 18:41:56 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 02 Jan 2023 18:41:56 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 02 Jan 2023 18:41:56 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 02 Jan 2023 18:41:56 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 02 Jan 2023 18:41:56 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5b4a36b5b78f93a5f470cf722b313bb32cddb0f8e0fa0db348059b5c0881b04f`  
		Last Modified: Thu, 15 Dec 2022 23:08:20 GMT  
		Size: 62.3 MB (62328625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748d50c9408cb82ead9c2f065bb30e9e65b3d4c842cd46e5842d6adc2f1e4a6c`  
		Last Modified: Fri, 16 Dec 2022 02:25:18 GMT  
		Size: 159.4 MB (159380735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b24b88f7ab8f45bc72761ad4e15311d73d47bb60be61ed5ea1922dd495c4da`  
		Last Modified: Fri, 16 Dec 2022 03:15:21 GMT  
		Size: 3.6 MB (3628075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca300ef28833c7b560e0687111e4a4855fd8a08af7982a4a91b89aaa5033e6b6`  
		Last Modified: Mon, 02 Jan 2023 18:47:53 GMT  
		Size: 8.4 MB (8351150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ecd3a7a9c6e0733e308f9048fa56844e967bf55b11b67eb4bd376910f89c3d`  
		Last Modified: Mon, 02 Jan 2023 18:47:52 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce99fba65de2847a690589c472a2325f57e6cabfc6ae10d12fdf7a8ec8cfcb4`  
		Last Modified: Mon, 02 Jan 2023 18:47:52 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-19` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:fd99f23a621a11ecb4668c9912f262b27963e958c516331dc96c3f6a44f78bbf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233795523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3151e77b54c22e20236bbfad8fd1d23f462d3e23736e253b852b81472919676`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 16 Dec 2022 00:41:05 GMT
ADD file:26a6bf75c84c408d289e5569f13b1c65206966f875cdfc53ded0670cb85e35bf in / 
# Fri, 16 Dec 2022 00:41:07 GMT
CMD ["/bin/bash"]
# Fri, 16 Dec 2022 01:01:40 GMT
ARG version=19.0.1.10-1
# Fri, 16 Dec 2022 01:01:59 GMT
# ARGS: version=19.0.1.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-19-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-19-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 16 Dec 2022 01:02:01 GMT
ENV LANG=C.UTF-8
# Fri, 16 Dec 2022 01:02:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-19-amazon-corretto
# Fri, 16 Dec 2022 01:22:52 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Mon, 02 Jan 2023 18:14:06 GMT
ARG MAVEN_VERSION=3.8.7
# Mon, 02 Jan 2023 18:14:06 GMT
ARG USER_HOME_DIR=/root
# Mon, 02 Jan 2023 18:14:06 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Mon, 02 Jan 2023 18:14:06 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Mon, 02 Jan 2023 18:14:09 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 02 Jan 2023 18:14:09 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 02 Jan 2023 18:14:09 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 02 Jan 2023 18:14:09 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 02 Jan 2023 18:14:09 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 02 Jan 2023 18:14:10 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 02 Jan 2023 18:14:10 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6cbfee25f0741b3d3f4d2474d904a200cd8404a01aa17813bf3fc3d4ebb551a4`  
		Last Modified: Thu, 15 Dec 2022 23:08:20 GMT  
		Size: 64.0 MB (63964214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a522d703ce658eafb2884db6606c458357c76578aa4a908df5bfdeab0f214a97`  
		Last Modified: Fri, 16 Dec 2022 01:06:12 GMT  
		Size: 157.8 MB (157832709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e542c6b0d8f59679f781e6ee666378e6eb4dd770aa2529d2157146c8917d7cca`  
		Last Modified: Fri, 16 Dec 2022 01:25:10 GMT  
		Size: 3.6 MB (3646238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6d4de3feee1b01bda5acfd604b612d050e83b221312eff923c08b08821b1cc`  
		Last Modified: Mon, 02 Jan 2023 18:18:31 GMT  
		Size: 8.4 MB (8351151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b7e9d442f4d5024d13b1a696b39ace3254c04c6fa141b53899e263b959d6fa`  
		Last Modified: Mon, 02 Jan 2023 18:18:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32e7f9743c9ccb6065a0362700b0799cd8bf5373ccab08c89091b7053d5ef4e`  
		Last Modified: Mon, 02 Jan 2023 18:18:30 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
