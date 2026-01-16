## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:3c0b481930f4fd463f345c142b7b05be9882a6a1cf6009fe75f214ae1d99962b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:e736023e557fe2bbb0535598cda824af1e51f30604976d986f46598d0c78de39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.5 MB (441456277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69afdee8bdf134590203d0756adc978e1fa7a4bf1fab9a9a28048b90881a50b5`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:16 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:16 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:01 GMT
ARG version=21.0.9.11-1
# Thu, 15 Jan 2026 22:10:01 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 15 Jan 2026 22:10:01 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:10:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 16 Jan 2026 02:45:06 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 16 Jan 2026 02:45:15 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 16 Jan 2026 02:45:15 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 02:45:15 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:45:15 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:45:15 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 02:45:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 02:45:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 02:45:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 02:45:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 02:45:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 02:45:15 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 02:45:15 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 02:45:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 02:45:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 02:45:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:89d3b5863331d6bb79d550bf0acce60aeac36e2c065470bf6d6f8d76c9cb6f4f`  
		Last Modified: Wed, 14 Jan 2026 13:23:48 GMT  
		Size: 62.9 MB (62940156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764343a8a8f79d8c00b1ec06bd8200f0f02fccf18829a21af3210a0530260cfb`  
		Last Modified: Thu, 15 Jan 2026 22:10:49 GMT  
		Size: 165.5 MB (165515480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327a4f189b147c3b49b6913eacd273f3908d4c0f0fb652ce97ae837321b77de7`  
		Last Modified: Fri, 16 Jan 2026 03:30:05 GMT  
		Size: 173.6 MB (173604479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e059ef077dcb04446c3e9fc6264c5f54f625a0bf3d24b45043c5197e8b356a13`  
		Last Modified: Fri, 16 Jan 2026 02:45:56 GMT  
		Size: 30.1 MB (30082879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28878d3c200df778e45f85783026cb87c7d59602a42632ee568ad48b6708250a`  
		Last Modified: Fri, 16 Jan 2026 02:45:55 GMT  
		Size: 9.3 MB (9312242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589568b85916e8a64b41f83ceefa0d059c50196b17e51a02dcae9bd22661cceb`  
		Last Modified: Fri, 16 Jan 2026 02:45:54 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab3361119a21fffd396b80130f820211ae471999d93c2dd5d1bd3f1937071ec`  
		Last Modified: Fri, 16 Jan 2026 02:45:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:d12555703a91b13302419ee900bbaeb81ba2c09665f263226c31d1811ab55d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6950378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b07ad07cd8a3807094b01e1c5ce36daf89d3ba717358999aa927514a66ec07f`

```dockerfile
```

-	Layers:
	-	`sha256:69fd0229340f22e3647e9c23c1f36524135de5379bde1dc0ae591b3166205203`  
		Last Modified: Fri, 16 Jan 2026 03:29:12 GMT  
		Size: 6.9 MB (6932162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcdfd09dd1863198566fd3311c3b6543005b3ba908321f0377686db52a9c2b53`  
		Last Modified: Fri, 16 Jan 2026 03:29:13 GMT  
		Size: 18.2 KB (18216 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5bed9380eedae5e81d693fa2fa97b78606fdda37a5e9d90eb8106380cf5b7997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.0 MB (417966549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd221cb0c323c5265de9829c86cc5eb3a7233465900b099d4060cba0882b2ed1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:41 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:41 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:26:49 GMT
ARG version=21.0.9.11-1
# Thu, 18 Dec 2025 01:26:49 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 18 Dec 2025 01:26:49 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:26:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 18 Dec 2025 02:22:51 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Thu, 18 Dec 2025 02:22:59 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Thu, 18 Dec 2025 02:22:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 18 Dec 2025 02:22:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 18 Dec 2025 02:22:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 18 Dec 2025 02:22:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 18 Dec 2025 02:22:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 18 Dec 2025 02:22:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 18 Dec 2025 02:22:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 18 Dec 2025 02:22:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 18 Dec 2025 02:22:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 18 Dec 2025 02:22:59 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 18 Dec 2025 02:22:59 GMT
ARG USER_HOME_DIR=/root
# Thu, 18 Dec 2025 02:22:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 18 Dec 2025 02:22:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 18 Dec 2025 02:22:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22bdf99b000252028c87652a8573d46452c5cb60b7d624b1036ae366a0cefc4`  
		Last Modified: Thu, 18 Dec 2025 02:20:19 GMT  
		Size: 163.6 MB (163581031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5a590a7a99c3fbf275dc89857ca27e22c7c9727a47ab18af4b424d1b033b22`  
		Last Modified: Thu, 18 Dec 2025 03:31:14 GMT  
		Size: 149.1 MB (149085410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f48d0f087043c5d0057f9e28824bf0736b217002f86eeb9452cd866ac02283`  
		Last Modified: Thu, 18 Dec 2025 02:23:32 GMT  
		Size: 31.2 MB (31191068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a66f20aa35e94172054f814de339eaf0c777f76aa1dd84cf19dc9548b25c5ed`  
		Last Modified: Thu, 18 Dec 2025 02:23:31 GMT  
		Size: 9.3 MB (9312242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3ba0e51a669687861dc2cbfc2b0226e4102f381118c64b93070d871895de59`  
		Last Modified: Thu, 18 Dec 2025 02:23:31 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01fdb8f107e65fc636dc3728ce0508a6580bd1d6d250fdc818eb46063f8e7eaa`  
		Last Modified: Thu, 18 Dec 2025 02:23:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:86908f29aed3f15649f12d37c08e6d3a8ac3eb14d9030354c5fcae4a74b9dc5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6947925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1b64ddcc20a04ec3bba9376d84753310d649da8a27b7ce4046990dca170511`

```dockerfile
```

-	Layers:
	-	`sha256:a098f6eb94d8d6993b1821550edfe062896737e2997b1899549f4af6c4c6ddbc`  
		Last Modified: Thu, 18 Dec 2025 03:28:23 GMT  
		Size: 6.9 MB (6929561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43861cdd7c4ed1ba2dc5922ec3831f6eb99eccd65584e0a02b3aa3d54e8cc6c8`  
		Last Modified: Thu, 18 Dec 2025 03:28:24 GMT  
		Size: 18.4 KB (18364 bytes)  
		MIME: application/vnd.in-toto+json
