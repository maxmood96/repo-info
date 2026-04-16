## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:da4a275df2bf1422693e373d998a4226e03cc0c97d4cb86beb6c09a3d26d9b71
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:4a77d1e4f3971fb4df289a3abb0608808c25f6fee8ed585e64d2e9b2867d298d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.0 MB (427036595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3bd70de6f91415a2bcf680560ea52bd47e9aaf511a512c59a9f215a077538f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:21 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:21 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:24:12 GMT
ARG version=11.0.30.7-1
# Wed, 15 Apr 2026 21:24:12 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 15 Apr 2026 21:24:12 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:24:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 15 Apr 2026 22:50:12 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 15 Apr 2026 22:50:21 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 15 Apr 2026 22:50:21 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 15 Apr 2026 22:50:21 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:50:21 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:50:21 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 15 Apr 2026 22:50:21 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Apr 2026 22:50:21 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 15 Apr 2026 22:50:21 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 22:50:21 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 15 Apr 2026 22:50:21 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 15 Apr 2026 22:50:21 GMT
ARG MAVEN_VERSION=3.9.14
# Wed, 15 Apr 2026 22:50:21 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Apr 2026 22:50:21 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Apr 2026 22:50:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Apr 2026 22:50:21 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5a3a1a219789b0285ea1d6a41ad03e6fab76f369592968c458dbfffd408719dd`  
		Last Modified: Thu, 09 Apr 2026 08:25:08 GMT  
		Size: 63.0 MB (62955266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f889f80a08d9942d941775fa5fbd5062ab478854872f8451cf918fafd8783a`  
		Last Modified: Wed, 15 Apr 2026 21:24:32 GMT  
		Size: 148.1 MB (148118425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830dcf062c64183ddb372c039e9ac1f268fd8a6e3a91c0b0ecf38920438454ed`  
		Last Modified: Wed, 15 Apr 2026 22:50:55 GMT  
		Size: 176.6 MB (176574965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cd150fb0ba8842caf364f15486afa8fc42329c33b77d3cdc838f5ce7450546`  
		Last Modified: Wed, 15 Apr 2026 22:50:51 GMT  
		Size: 30.1 MB (30075710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52daeca357234217db07973a8c9d59a05038df3112c7a221f0e2b7193f298cd4`  
		Last Modified: Wed, 15 Apr 2026 22:50:50 GMT  
		Size: 9.3 MB (9311189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a883b9d12b8637b368065fc0043d159752284320f021ae557462bc349e6613d5`  
		Last Modified: Wed, 15 Apr 2026 22:50:49 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5326b8d1c2d91be387b97274f4eee206dfaa2199f68d01f6443ce8de19502e95`  
		Last Modified: Wed, 15 Apr 2026 22:50:51 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:17897361e0b2f1490fdf80847fcbeba4c7339a29a561fafffc9137915d6d9b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6957845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87edf98b1cf49c70a2d5d7eef8aa90d827622af6c1e1842a1cea19e5b9651ab6`

```dockerfile
```

-	Layers:
	-	`sha256:9907de90a5fcf58127bb7d11adada2eb50f3f1a44c0cf932d3bb1c571a61763f`  
		Last Modified: Wed, 15 Apr 2026 22:50:49 GMT  
		Size: 6.9 MB (6939651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4452e774e3bff5cb89751fe01310c9499e3945a113fc672a64bb5530183d6a1f`  
		Last Modified: Wed, 15 Apr 2026 22:50:49 GMT  
		Size: 18.2 KB (18194 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6bdd4d2a99b2d98a507d5e716390c865224d39b712bc9d8e3ee9ac4b00bb06e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.6 MB (402641641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f895f51518b37f260d6f4d0af7b78ee6b78cf926ec1771fb90fdc47218479c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:35 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:35 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:38:14 GMT
ARG version=11.0.30.7-1
# Wed, 15 Apr 2026 21:38:14 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 15 Apr 2026 21:38:14 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:38:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 15 Apr 2026 23:16:33 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 15 Apr 2026 23:16:40 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 15 Apr 2026 23:16:40 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 15 Apr 2026 23:16:40 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 23:16:40 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 23:16:40 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 15 Apr 2026 23:16:40 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Apr 2026 23:16:40 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 15 Apr 2026 23:16:40 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 23:16:40 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 15 Apr 2026 23:16:41 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 15 Apr 2026 23:16:41 GMT
ARG MAVEN_VERSION=3.9.14
# Wed, 15 Apr 2026 23:16:41 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Apr 2026 23:16:41 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Apr 2026 23:16:41 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Apr 2026 23:16:41 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f1f2697b3535de3cb27d338e724d6283baf064a258669349257ede7e5670fff3`  
		Last Modified: Thu, 09 Apr 2026 08:25:15 GMT  
		Size: 64.8 MB (64802975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc41dd512eba15547765998d4e676ad13bd0561b820ba3e5ed260f3d81ec292`  
		Last Modified: Wed, 15 Apr 2026 21:38:34 GMT  
		Size: 145.2 MB (145219095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5049e6dcaf3970d0188c49922e4fe594e7d2fd27f99ac289d2c93f1f9b984db`  
		Last Modified: Wed, 15 Apr 2026 23:17:08 GMT  
		Size: 152.1 MB (152098807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6d39e52ed81bc5dd763a793c342ca76cef47c272495d76bd342c605908cedb`  
		Last Modified: Wed, 15 Apr 2026 23:17:06 GMT  
		Size: 31.2 MB (31208527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf1f2c8015c293ed69cd0f7dec794e5c5b782791052307c7dc7de0c5103b4f4`  
		Last Modified: Wed, 15 Apr 2026 23:17:05 GMT  
		Size: 9.3 MB (9311196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c343ca4fea05de3343e938e198059ac5104b42f176a17f38c4d735aca5d61b6a`  
		Last Modified: Wed, 15 Apr 2026 23:17:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c40dd8a26aeb9371b269c21f5f425aef49c7fcf4c1e165a68978a255b651c71`  
		Last Modified: Wed, 15 Apr 2026 23:17:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:d9c55d7547ec01d1f6b034d4bab145e6a683c1e7f00fc695e91cab28f8634d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6956197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832fff9cd1e96a318bcb4e0905e4b244254edf97040da93d2fba570715e17c79`

```dockerfile
```

-	Layers:
	-	`sha256:3ddee24d2ee7692f4d169ec9db6cbb6143b06b9405ae9fe6520fbc732828ef6d`  
		Last Modified: Wed, 15 Apr 2026 23:17:05 GMT  
		Size: 6.9 MB (6937855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e567e97966117772aeb8cc9d875b9c3475eb76c68fe48d31966b5b9eeeea492`  
		Last Modified: Wed, 15 Apr 2026 23:17:04 GMT  
		Size: 18.3 KB (18342 bytes)  
		MIME: application/vnd.in-toto+json
