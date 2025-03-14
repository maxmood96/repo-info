## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:86dcfb7c8f1b8543be356ccd14990fd091b1a50df961c079441fc04779af5264
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:7ed06ce2d232c20e82a3480a9c91bb74fdaacb14add3b0ddf40b1026fe44f0d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.0 MB (423967383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7512bec9755e522955bad56a9411fe163a5be050311d00a801bafe109878a17e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=21.0.6.7-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=21.0.6.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f3dc83dc2e4e000fd189efee126db80e38a079b47b8e5229a794a0a6148bfec6`  
		Last Modified: Sat, 08 Mar 2025 04:13:59 GMT  
		Size: 62.8 MB (62772838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d780df9adcbd4f85fae763ecd2a7c4d99ab147a0e44e15e0f45784ba50fa4a`  
		Last Modified: Thu, 13 Mar 2025 22:53:06 GMT  
		Size: 164.8 MB (164818822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb7a1ad65a3498de68e19e919b214f67290f33b4bf4dadd849e88a76b2ecfcc`  
		Last Modified: Thu, 13 Mar 2025 23:09:47 GMT  
		Size: 157.1 MB (157110609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa099e45dae72413660b5b053ce07c040f8e48368a79f43c3711584e745e2d0d`  
		Last Modified: Thu, 13 Mar 2025 23:09:45 GMT  
		Size: 30.1 MB (30093637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bcbedf140bdfb4cb0558545339187b8a27cb8151c3372f50c7a4885139d60c`  
		Last Modified: Thu, 13 Mar 2025 23:09:44 GMT  
		Size: 9.2 MB (9170435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446b57288c8a77e9a87ece84fcdfa8e8b4997f1606a59e0d9afc5db15da5db12`  
		Last Modified: Thu, 13 Mar 2025 23:09:44 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f9f5138ddef4eac0a260a742e5cd02ea744912b763e85b54aedae614d1804e`  
		Last Modified: Thu, 13 Mar 2025 23:09:44 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:684796b4fdf95bd73a8027590cde9d79641649692d5186cf82dd11a1a06026ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6925290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713e00248013dca9df11c1fbd65fa00852044086f49cc279d51961e3a45b1408`

```dockerfile
```

-	Layers:
	-	`sha256:f5abdc3bc4ff89caa127fa71fe36e87f807d084a92dfcaa090314f20cc7e2f85`  
		Last Modified: Thu, 13 Mar 2025 23:09:44 GMT  
		Size: 6.9 MB (6907062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30b84e3ee4f9a1b85c63dd0b26b9f443835a129772e6791c4816331a08e04af7`  
		Last Modified: Thu, 13 Mar 2025 23:09:44 GMT  
		Size: 18.2 KB (18228 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:08813a4e15eb7a746089adad7917d5491f10480b36e0f3718bd30bfc551f73b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.7 MB (399703625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a739bad9296a8b54a954dac54d13260b4ba7c1bb37fd782ca7b74ba4610b1e7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=21.0.6.7-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=21.0.6.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5270c35d4d9446d8a0ab2f41ab0020c11889bd8617236093cc9c87563d120b9e`  
		Last Modified: Wed, 26 Feb 2025 15:57:39 GMT  
		Size: 64.5 MB (64521208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9033b51658d3a3d4c550c89424db4382b2da4dfd6525286c8e303377d9c05bce`  
		Last Modified: Thu, 27 Feb 2025 21:21:38 GMT  
		Size: 162.8 MB (162810700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3a44bddd419e06b1db1fa19b8839eed493283a686acf2a1c8fdf2e6c7cc024`  
		Last Modified: Thu, 27 Feb 2025 22:39:08 GMT  
		Size: 132.0 MB (132037207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85017afd88153dea117db99e2fe31e3f472379790b1db7926bd101c86f3ff3ef`  
		Last Modified: Thu, 27 Feb 2025 22:39:06 GMT  
		Size: 31.2 MB (31163036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fcdce7cd2a155f4b970a5da7638fbbc6b1bc436b7387818ffb8a9e48eab8b6`  
		Last Modified: Thu, 27 Feb 2025 22:39:05 GMT  
		Size: 9.2 MB (9170433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768b0ae1e5e5e6e347c965ba60f4487778d27c86ccc441a05e38e610e6aaa63a`  
		Last Modified: Thu, 27 Feb 2025 22:39:05 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ba6440c92bf852bca7fcb79a4daff70163af197e4e5281449df2f1d4e9c3bc`  
		Last Modified: Thu, 27 Feb 2025 22:39:06 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:ca6b16b170ef9b395f778a5d6a3ff3acbc224660f9eaeab694dd26329a9cfa27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6922838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dace4c43c8137c05af37afc60dea3ecbf188466334e43d85f45c7b2465845c2`

```dockerfile
```

-	Layers:
	-	`sha256:79d397d9d78e671a40c235e7f2b58cd070d784e9db4f5a3bf998ddf3a083865b`  
		Last Modified: Thu, 27 Feb 2025 22:39:05 GMT  
		Size: 6.9 MB (6904461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe7eeca138205601d40cc618fa56ed0c9bea156f2affb301b4161a05b1c8cd6`  
		Last Modified: Thu, 27 Feb 2025 22:39:05 GMT  
		Size: 18.4 KB (18377 bytes)  
		MIME: application/vnd.in-toto+json
