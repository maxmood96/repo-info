## `maven:amazoncorretto`

```console
$ docker pull maven@sha256:b6a2cfa6d49103944f7e1e52c5087469900bdf57db64ae966001f35985cda03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:efd7c0d265ffa5e9f8f9303a5cf1e890f312a64d5cb78045b93130a82de5c479
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221656815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3ee95d57615640f65c1c73d7077890a36334a52af8c7c0233b3a75da717d88`
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
# Wed, 04 May 2022 00:25:00 GMT
ARG MAVEN_VERSION=3.8.5
# Wed, 04 May 2022 00:25:00 GMT
ARG USER_HOME_DIR=/root
# Wed, 04 May 2022 00:25:00 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Wed, 04 May 2022 00:25:00 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Wed, 04 May 2022 00:25:06 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 04 May 2022 00:25:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 04 May 2022 00:25:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 04 May 2022 00:25:07 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 04 May 2022 00:25:07 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 04 May 2022 00:25:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 04 May 2022 00:25:07 GMT
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
	-	`sha256:6f784f4b70bf4806720d7fdd6379bf58bc3274e0010a1ba37ed89f311bea4764`  
		Last Modified: Wed, 04 May 2022 00:27:45 GMT  
		Size: 8.7 MB (8736386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83865dfe1c716138c640819f727adbcaf325b07b40a55c83a5d35c1cb6ba4c6d`  
		Last Modified: Wed, 04 May 2022 00:27:45 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b944e48b435f2544b655d7887973e4b0178195e2f646ced6a8558d5911f4b9`  
		Last Modified: Wed, 04 May 2022 00:27:45 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:ea04cf031d2a63b839a359d4db5b50816929bd2795c166568b6de5e7fa39b4ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220475154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d61b26eb277a2387c320589cf1d7cc5dbf3dfc40d88eb48b255d344d7be80b7`
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
# Wed, 04 May 2022 00:42:09 GMT
ARG MAVEN_VERSION=3.8.5
# Wed, 04 May 2022 00:42:10 GMT
ARG USER_HOME_DIR=/root
# Wed, 04 May 2022 00:42:11 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Wed, 04 May 2022 00:42:12 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Wed, 04 May 2022 00:42:20 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 04 May 2022 00:42:21 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 04 May 2022 00:42:22 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 04 May 2022 00:42:24 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 04 May 2022 00:42:25 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 04 May 2022 00:42:25 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 04 May 2022 00:42:26 GMT
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
	-	`sha256:9f03a9657dd42b040e1f57a7251772c5d42e6f4827edc36660a41476147e2472`  
		Last Modified: Wed, 04 May 2022 00:46:09 GMT  
		Size: 8.7 MB (8736339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29bad8e1920b9a1bd68cd5d28ce0c0c33cc565655f49280616f39348575d498`  
		Last Modified: Wed, 04 May 2022 00:46:09 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2601dcd704e45a12e7d08efdbd78b2c2aef76036f9b20c3450854730a7a665df`  
		Last Modified: Wed, 04 May 2022 00:46:08 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
