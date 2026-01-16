## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:0a6a02e36bb3b3a189baf6ceb87ed121f413bd5e41ef99eede03e56b27217464
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:f75054ea99e2aa248dd36dc2e612128a8d820f66c77ff40e932c45f9e70e199b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.0 MB (423991286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab960cdbb2b59876ba24d1b502b6b3009e1187f11a159908b95310f46caa72ee`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:16 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:16 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:18 GMT
ARG version=11.0.29.7-1
# Thu, 15 Jan 2026 22:07:18 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 15 Jan 2026 22:07:18 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:07:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 16 Jan 2026 02:43:45 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 16 Jan 2026 02:43:54 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 16 Jan 2026 02:43:54 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 02:43:54 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:43:54 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:43:54 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 02:43:54 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 02:43:54 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 02:43:54 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 02:43:54 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 02:43:54 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 02:43:54 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 02:43:54 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 02:43:54 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 02:43:54 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 02:43:54 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:89d3b5863331d6bb79d550bf0acce60aeac36e2c065470bf6d6f8d76c9cb6f4f`  
		Last Modified: Wed, 14 Jan 2026 13:23:48 GMT  
		Size: 62.9 MB (62940156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f9521458adcf521dd7a9c6b42b4e553ccd70b13a33dc1ad4265a9df22b4de0`  
		Last Modified: Thu, 15 Jan 2026 22:08:26 GMT  
		Size: 148.1 MB (148064451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13993cf514f9bfa397083e4b2bf7416b17b56e28b9b037f1f114835db5c373b9`  
		Last Modified: Fri, 16 Jan 2026 02:44:26 GMT  
		Size: 173.6 MB (173599716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbde4eb37d15a71bd2ac105a60a0f059a86bc09976ff209b9fce878443bef148`  
		Last Modified: Fri, 16 Jan 2026 02:44:41 GMT  
		Size: 30.1 MB (30073676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe6bcfa8aead58b3b48b3ffcf091fa09dbba707068925a6712a8261090a0571`  
		Last Modified: Fri, 16 Jan 2026 02:44:34 GMT  
		Size: 9.3 MB (9312246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69c69befb8168a7694a0154675dfd60902a234083849dfb97c95530dce5b8c4`  
		Last Modified: Fri, 16 Jan 2026 02:44:32 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784da088a1ec5c16dfc2a373c6df1d3a9363d2b1b0240e6db9fdc6fda9d61356`  
		Last Modified: Fri, 16 Jan 2026 02:44:32 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:5dbf3325446cdf3e4b9c675d3de175bf8a53363fdd2ad73224e4b73bc3b9e062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6957760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290b567d7f9e06574a9e9d0c3ae1026719267ff6780f06974106340d5c568deb`

```dockerfile
```

-	Layers:
	-	`sha256:6f71830db8b17c8862257e09b0bfb4441fd70191f1839b76976c81cab2f8330a`  
		Last Modified: Fri, 16 Jan 2026 03:28:26 GMT  
		Size: 6.9 MB (6939566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5187f88f93e56fa28c4a6bfaf9355947d75b1357cacc19076afca06d8e95ffd7`  
		Last Modified: Fri, 16 Jan 2026 03:28:27 GMT  
		Size: 18.2 KB (18194 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:e6f89830c6845a2c17adf768f220c956f76d01df275620703f2a4e1b4c2a64e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.5 MB (399524021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e80ca5565618484c2fbb189ff0235d301d4603a8ce2cbfda3d10ef07f51aaa`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:41 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:41 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:25:22 GMT
ARG version=11.0.29.7-1
# Thu, 18 Dec 2025 01:25:22 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 18 Dec 2025 01:25:22 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:25:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 18 Dec 2025 02:22:17 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Thu, 18 Dec 2025 02:22:24 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 18 Dec 2025 02:22:24 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 18 Dec 2025 02:22:24 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 18 Dec 2025 02:22:24 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 18 Dec 2025 02:22:24 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 18 Dec 2025 02:22:24 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 18 Dec 2025 02:22:24 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 18 Dec 2025 02:22:24 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 18 Dec 2025 02:22:25 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 18 Dec 2025 02:22:25 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 18 Dec 2025 02:22:25 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 18 Dec 2025 02:22:25 GMT
ARG USER_HOME_DIR=/root
# Thu, 18 Dec 2025 02:22:25 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 18 Dec 2025 02:22:25 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 18 Dec 2025 02:22:25 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5109e3d25f889e8daddd5fe4018cff5eb742c43e4eebb8d37a493f68a4628ad6`  
		Last Modified: Thu, 18 Dec 2025 02:20:42 GMT  
		Size: 145.1 MB (145144730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e17a21cc7fa7bf7d9476b5db22ef9443df8b89d08bfed6296e9212cdc74842`  
		Last Modified: Thu, 18 Dec 2025 04:04:15 GMT  
		Size: 149.1 MB (149074929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0aa231ccc5fa2bc98effe9acefb522c5332dfbc2907dce0b164d4cdfb47bae`  
		Last Modified: Thu, 18 Dec 2025 02:23:05 GMT  
		Size: 31.2 MB (31195318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158181429a05a90be3d4620513f5b6f33e8c61b81f47fefc518c1336a8a1397d`  
		Last Modified: Thu, 18 Dec 2025 02:22:59 GMT  
		Size: 9.3 MB (9312247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585b67bd6b18d58b62f4719795a5afded240d40166b58647d9b2d4a6d5853ab4`  
		Last Modified: Thu, 18 Dec 2025 02:22:59 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec09d8277decebe81d7d281823e4e3f8238e7777382650b68fc1edcd8b98825c`  
		Last Modified: Thu, 18 Dec 2025 02:22:58 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:4ef49f69f80bface0012f50bf69bc28600697d663945af69e63293053ad3e19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6956112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5e2c3e432fc0623f3bd851ff70349abcc85d6a334f1c65e4eb0d7e010724ce`

```dockerfile
```

-	Layers:
	-	`sha256:a3281622de77566f586a51de90aeb901d195e9b3a7eba427e9579485a4423f87`  
		Last Modified: Thu, 18 Dec 2025 03:27:45 GMT  
		Size: 6.9 MB (6937770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:855475f214ccad1cf6647bf18d8c9598d1eb2f4d3af4498926ca037ad10d03ef`  
		Last Modified: Thu, 18 Dec 2025 02:22:47 GMT  
		Size: 18.3 KB (18342 bytes)  
		MIME: application/vnd.in-toto+json
