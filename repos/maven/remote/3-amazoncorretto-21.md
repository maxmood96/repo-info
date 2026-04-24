## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:3a86e2ab499d09e7e45133dcd4418fbc56be44ab2eb85237e5e16e606056e489
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:26f93c5dffa367c6d24cb33c69571c54fb20d68dd513b2a7781d1d20b1bc6b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.7 MB (444718044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9e064e8f4c5b023d1ca09f5188af1f5f2260f9d42aea117c5de27bdefe6b58`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 24 Apr 2026 00:03:09 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:03:09 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:13:20 GMT
ARG version=21.0.11.10-1
# Fri, 24 Apr 2026 00:13:20 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Apr 2026 00:13:20 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:13:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 24 Apr 2026 01:14:19 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 24 Apr 2026 01:14:29 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 24 Apr 2026 01:14:30 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 24 Apr 2026 01:14:30 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 24 Apr 2026 01:14:30 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 24 Apr 2026 01:14:30 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 24 Apr 2026 01:14:30 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 24 Apr 2026 01:14:30 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 24 Apr 2026 01:14:30 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 24 Apr 2026 01:14:30 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 24 Apr 2026 01:14:30 GMT
ARG USER_HOME_DIR=/root
# Fri, 24 Apr 2026 01:14:30 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 24 Apr 2026 01:14:30 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 24 Apr 2026 01:14:30 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e31bc602eae80620b93a07bcadec78ad83d112fa08abc35008da53ebf7ca3693`  
		Last Modified: Wed, 15 Apr 2026 10:04:45 GMT  
		Size: 63.0 MB (62952183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec9fac6410c3c9ac2657fbeb0d603472d8240308a45a2c1714d1ca951ee5f45`  
		Last Modified: Fri, 24 Apr 2026 00:13:43 GMT  
		Size: 165.8 MB (165776055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3559e4be9e3ae57fe964400d46fb91c0e4c57964f14e848af3d2a21a58399023`  
		Last Modified: Fri, 24 Apr 2026 01:14:59 GMT  
		Size: 176.6 MB (176593825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee14980ec00ee9390d03b67daa4759cdcead42c06f06a55c61604717af9d791e`  
		Last Modified: Fri, 24 Apr 2026 01:14:56 GMT  
		Size: 30.1 MB (30082771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad943eeaf24b26eb2ded085f637fc389ca4e26d3b1bf1182181fa2a1e17cabb`  
		Last Modified: Fri, 24 Apr 2026 01:14:55 GMT  
		Size: 9.3 MB (9312199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ae85d0fee21aa4ab246350a2a85047eae39d661401ee7c06b2295c2df6c77f`  
		Last Modified: Fri, 24 Apr 2026 01:14:54 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d78ce99617285f0a1086c76634cffe917e980867edb16e6398cc5bfddd86c3f`  
		Last Modified: Fri, 24 Apr 2026 01:14:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:3f324c610e924ae09ec8081f52163eed02fac7d079db78f2f2cd44764f4cb34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6949283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44381e6e43b64aae6325e4b54169d4054b0002e516e08616faf381ad8e7e340`

```dockerfile
```

-	Layers:
	-	`sha256:46c03a5f3e6b4f020b2883a756ba6d9659d496e5788632341bdc93e741df7cf3`  
		Last Modified: Fri, 24 Apr 2026 01:14:55 GMT  
		Size: 6.9 MB (6933065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d112ef1cb1c86efd7353563df3337f2d4417d08cb4117856e745dd3d1a31869`  
		Last Modified: Fri, 24 Apr 2026 01:14:54 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6687c7dbfbb0a12aa22f1b191f7dbe1a4e0769aa0e390e7c15f9f8be2039700e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.3 MB (421310479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a79bdeb816ad26d1f99cf49366be591e1b47eee576508926143fff6221f2b514`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:35 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:35 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:13:24 GMT
ARG version=21.0.11.10-1
# Fri, 24 Apr 2026 00:13:24 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Apr 2026 00:13:24 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:13:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 24 Apr 2026 01:14:12 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 24 Apr 2026 01:14:20 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 24 Apr 2026 01:14:20 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 24 Apr 2026 01:14:20 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 24 Apr 2026 01:14:20 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 24 Apr 2026 01:14:20 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 24 Apr 2026 01:14:20 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 24 Apr 2026 01:14:20 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 24 Apr 2026 01:14:20 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 24 Apr 2026 01:14:20 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 24 Apr 2026 01:14:20 GMT
ARG USER_HOME_DIR=/root
# Fri, 24 Apr 2026 01:14:20 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 24 Apr 2026 01:14:20 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 24 Apr 2026 01:14:20 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0089d862b3b6e84c40891727df0dc5639dc509aa2f4dc6079056a5a3f8b526e1`  
		Last Modified: Wed, 15 Apr 2026 10:04:56 GMT  
		Size: 64.8 MB (64798783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4172a5721cede5f9312e166024bf95d5415d09c1db340145ae3aae91bfcc30`  
		Last Modified: Fri, 24 Apr 2026 00:13:51 GMT  
		Size: 163.9 MB (163893165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9fbf00140d5d48156a4e33a0ca83bb05dfc06301ff1dcca2727c082583a3a49`  
		Last Modified: Fri, 24 Apr 2026 01:14:49 GMT  
		Size: 152.1 MB (152101994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831f00a188888bc0ecd8f698b1fcffb6f289a669e0a426f99c94bf9bf1f1f55e`  
		Last Modified: Fri, 24 Apr 2026 01:14:46 GMT  
		Size: 31.2 MB (31203275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a32630ec9aa5cc70d52355046c7ff08d05e720083df4dc48308e0ce38227b9`  
		Last Modified: Fri, 24 Apr 2026 01:14:45 GMT  
		Size: 9.3 MB (9312251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f8afddb568abf862e8d79df907f09d5c18daf99163304cd72259b4bd77efe2`  
		Last Modified: Fri, 24 Apr 2026 01:14:45 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633b0793444c809645258383cbf93be7729ad1b02b4e0285698971f2edc1f254`  
		Last Modified: Fri, 24 Apr 2026 01:14:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:5a797391fd9873f886d12acec79fb7ae382650dcbe77df46d69b8e15648e90a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6946830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1972d8b222383283a936c987ad7fbbb770933fd2ba44f7e7e3c53c4b8272aa95`

```dockerfile
```

-	Layers:
	-	`sha256:5b35bb186ae835029aa3bf223fb2cca42784753acacbb7ed6ac2698343772340`  
		Last Modified: Fri, 24 Apr 2026 01:14:45 GMT  
		Size: 6.9 MB (6930464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b679041c58a6594b2e8520fc766e2eb01df5cab1e612abf3e16b2fb40dbf06cc`  
		Last Modified: Fri, 24 Apr 2026 01:14:44 GMT  
		Size: 16.4 KB (16366 bytes)  
		MIME: application/vnd.in-toto+json
