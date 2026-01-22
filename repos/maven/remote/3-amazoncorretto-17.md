## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:54de5fbf7ac7bc455dea17ca0dfcd30dbf4155e43a067e72242f31d1213cce4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:3d613c104ffc363ef1542a7118a0e289669352a73e69711b6f21e087e86b05e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.4 MB (428402941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1ac6fb5d5c85fa6689407f1129d2c03a0131dd9b9f98d236c5af9bb05d27a6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:16 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:16 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:00:15 GMT
ARG version=17.0.18.8-1
# Wed, 21 Jan 2026 19:00:15 GMT
# ARGS: version=17.0.18.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 21 Jan 2026 19:00:15 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 21 Jan 2026 19:21:24 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 21 Jan 2026 19:21:32 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 21 Jan 2026 19:21:32 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 21 Jan 2026 19:21:32 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:21:32 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:21:32 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 21 Jan 2026 19:21:32 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 21 Jan 2026 19:21:32 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 21 Jan 2026 19:21:32 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 21 Jan 2026 19:21:33 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 21 Jan 2026 19:21:33 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 21 Jan 2026 19:21:33 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 21 Jan 2026 19:21:33 GMT
ARG USER_HOME_DIR=/root
# Wed, 21 Jan 2026 19:21:33 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 21 Jan 2026 19:21:33 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 21 Jan 2026 19:21:33 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:89d3b5863331d6bb79d550bf0acce60aeac36e2c065470bf6d6f8d76c9cb6f4f`  
		Last Modified: Wed, 14 Jan 2026 13:13:55 GMT  
		Size: 62.9 MB (62940156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d09c36562c02e291fec0cd8d510ab0c206591e85dce9cebfe7fe6bd12f6006`  
		Last Modified: Wed, 21 Jan 2026 19:00:36 GMT  
		Size: 152.5 MB (152462935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3d4affbbc6ba2dd64190a0cf7936a335f24d78cdd3303ce807c4ed76404fcb`  
		Last Modified: Wed, 21 Jan 2026 19:21:59 GMT  
		Size: 173.6 MB (173614725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f23b3febd5fd9e21be18d451761624259bcdd7bd8c85ffd7359c5a2a5e6d77`  
		Last Modified: Wed, 21 Jan 2026 19:21:56 GMT  
		Size: 30.1 MB (30071830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6f6fdf154bbd0ade48d14689f70c086f070686b7008fe019c71a530bf1bc0e`  
		Last Modified: Wed, 21 Jan 2026 21:24:24 GMT  
		Size: 9.3 MB (9312251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f432dd758cde3a636c5e011c735240e77cf3c4404421141217cc2dced76e4e7`  
		Last Modified: Wed, 21 Jan 2026 21:26:22 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a0d7d3ec49d372f7d4c6f4290459b411075e0ba85e289d15d83015ef054710`  
		Last Modified: Wed, 21 Jan 2026 19:22:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:4ff8282506cb39ed32602d7682e61420f2f52a3ca446786182e1213baccea991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6950455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03eff40bae2a9897de982122120a7b955435f12fa7c3cae96ac25c595383b26c`

```dockerfile
```

-	Layers:
	-	`sha256:82a559877b029d934c828204133003356eecd3605ca3b3766e2c4476486eda90`  
		Last Modified: Wed, 21 Jan 2026 19:21:55 GMT  
		Size: 6.9 MB (6932261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67b3239934ee27a75a0edd46e809856e623260c1957dca898241a9622b3635c5`  
		Last Modified: Wed, 21 Jan 2026 21:28:26 GMT  
		Size: 18.2 KB (18194 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d49aface71c0a7e93383ea10f5a5b4134ea4e0c5ea736538fd7cf76f8b193dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.7 MB (405691852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9304e1f17e9687c4cab4bcae3bcc9a29fe36b74163930a8bba20a09d5520214f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:03 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:03 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:00:16 GMT
ARG version=17.0.18.8-1
# Wed, 21 Jan 2026 19:00:16 GMT
# ARGS: version=17.0.18.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 21 Jan 2026 19:00:16 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 21 Jan 2026 19:17:01 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 21 Jan 2026 19:17:09 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 21 Jan 2026 19:17:09 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 21 Jan 2026 19:17:09 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:17:09 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:17:09 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 21 Jan 2026 19:17:09 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 21 Jan 2026 19:17:09 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 21 Jan 2026 19:17:09 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 21 Jan 2026 19:17:09 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 21 Jan 2026 19:17:09 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 21 Jan 2026 19:17:09 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 21 Jan 2026 19:17:09 GMT
ARG USER_HOME_DIR=/root
# Wed, 21 Jan 2026 19:17:09 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 21 Jan 2026 19:17:09 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 21 Jan 2026 19:17:09 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:afb133ffe3cfc9458fcd28fa75abd002d894e187faa842d48d3c35c676633646`  
		Last Modified: Thu, 15 Jan 2026 07:47:55 GMT  
		Size: 64.8 MB (64770434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da03988e890a2734422b08930678b55aacec1ee085bede5e1b18f8c3f898b33e`  
		Last Modified: Wed, 21 Jan 2026 19:18:28 GMT  
		Size: 151.0 MB (150985142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371d21c8f64c8070c26b5920e78091e333e23e85b9188cb0547c04a28241b016`  
		Last Modified: Wed, 21 Jan 2026 22:13:24 GMT  
		Size: 149.4 MB (149420957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d0426887ed60cf7d66f021a5f461847fb193452c68bc7200524b12b47e3e5a`  
		Last Modified: Wed, 21 Jan 2026 22:13:19 GMT  
		Size: 31.2 MB (31202037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86170cef3bf0c3f02b496c41ccecdaf951831485b88f3d61fd4f413a80c5ea1c`  
		Last Modified: Wed, 21 Jan 2026 19:17:32 GMT  
		Size: 9.3 MB (9312243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e571ea5c9c936db78a46d86b0e1292e87a7ff37acaf223c1bf36de4a1734a527`  
		Last Modified: Wed, 21 Jan 2026 19:17:32 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc93880cbb22a9b5514a9abc9bb583d21ee2a154e5f5b4fdf6d27a58e579aa0`  
		Last Modified: Wed, 21 Jan 2026 19:17:33 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:055121661812f2a9f73e1d483fe7df6415350aff78c06766e07641a92643e33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6948002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6d6eac5f4cf38aaa4d51f2e85bf1395970674c8c8cb304df70d42a9f0c3ace`

```dockerfile
```

-	Layers:
	-	`sha256:c20d6078938dca671ef7be3faf58dbf1925a378d7ad48d41ad005dcd851dc39e`  
		Last Modified: Wed, 21 Jan 2026 21:28:03 GMT  
		Size: 6.9 MB (6929660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1279e6cf17f9591b494fcef10bde4bcb3d36a249c13ffcd962840411216804cb`  
		Last Modified: Wed, 21 Jan 2026 19:17:31 GMT  
		Size: 18.3 KB (18342 bytes)  
		MIME: application/vnd.in-toto+json
