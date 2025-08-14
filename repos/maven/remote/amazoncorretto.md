## `maven:amazoncorretto`

```console
$ docker pull maven@sha256:3dd24660b46b562f15f0ff8e774bd7a32ef88da565177fe7e4db6075546ed0ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:0626fd75c9c33861b134bfe9a9186a8c07b7d35e7cd559d53b811cc7592e6747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.3 MB (419268645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7d53ef6e33d68d7b9dcf73441a4fcd06bf45856daef4693774bd6cbdf2e9b2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=17.0.16.8-1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=17.0.16.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:dcefe03e9009da4739e237894f3fe49af6782d53d9e2202e46127bd568617855`  
		Last Modified: Sat, 09 Aug 2025 04:15:21 GMT  
		Size: 63.0 MB (62959372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a0609072df14ca55d332f8e3c224846b0b7eead95460c9ece0cfefd122f064`  
		Last Modified: Wed, 13 Aug 2025 23:11:17 GMT  
		Size: 151.9 MB (151874859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6ab72c9537b80aa84aaa26f7b1767d8d2aaf4ebe376c3a3ade7a85781d9363`  
		Last Modified: Thu, 14 Aug 2025 02:27:33 GMT  
		Size: 165.1 MB (165088817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7739cb1d444b843c6b2321ea5fc76e5a4fe8cd6356d85b86c1de455c00b6d886`  
		Last Modified: Thu, 14 Aug 2025 00:14:41 GMT  
		Size: 30.1 MB (30101969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0201d1232da56f70072e24810749904c8eedb6b562214282f57c34f0290f86`  
		Last Modified: Wed, 13 Aug 2025 23:19:55 GMT  
		Size: 9.2 MB (9242585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3816c4499398ae6a0ca47e7bfadb269f3d08a0c3fff0ac8a9225c2838313c09`  
		Last Modified: Wed, 13 Aug 2025 23:20:03 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa2a2ef46e443099c57c962c5f9df3765915ba11d8567168f405686f61607f`  
		Last Modified: Wed, 13 Aug 2025 23:20:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:4909e6a38143de8b9bcdd94b40f857e1ddc80fb71ef1e1b9958f04268eea250e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6949812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155018991bec7df488caaa01a389f4501da7ad34e6ee28b96c534b71c92361fa`

```dockerfile
```

-	Layers:
	-	`sha256:e205ebd9f1d4ece7eb645c2c2742c7240281e7dbd9f5c7346afea098314b3576`  
		Last Modified: Thu, 14 Aug 2025 02:27:24 GMT  
		Size: 6.9 MB (6930301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4476b3a1e5175afc70cf82709e6ec1b35c5efb3538f17ab06ce5e8d0e3a5c7f0`  
		Last Modified: Thu, 14 Aug 2025 02:27:25 GMT  
		Size: 19.5 KB (19511 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:ec7b4bd9c4466015b6c630742b72d052bb850d911ec0fddc0466b4189164f80d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.7 MB (396701213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f57d9c677bf68620d78d5f3c22be51a4b6b26a953b77c3a9bb6f329aba44264`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=17.0.16.8-1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=17.0.16.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2c5df7aef58ef9598380ed47447cb5a8a274be6648b1015fa328f378b9e2da76`  
		Last Modified: Wed, 13 Aug 2025 22:57:44 GMT  
		Size: 64.8 MB (64794364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cd4aced99c35e8bc24c9f8f76de4c6384d08e38ee655cb9bdcb8b655f87e74`  
		Last Modified: Thu, 14 Aug 2025 09:14:46 GMT  
		Size: 150.4 MB (150397839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c962ca2ac4ebcd2a531a8393ff8ad50e5e2602f6b4f2342f767e137b376abf`  
		Last Modified: Thu, 14 Aug 2025 20:36:54 GMT  
		Size: 141.1 MB (141082893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c87233e8a191c036f6390b752f32373ec0525c9b6691f603b8e98b4cd4f5003`  
		Last Modified: Thu, 14 Aug 2025 18:42:12 GMT  
		Size: 31.2 MB (31182490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c840f6447eb7c05df0d5e11828bf398941bf4bdd38e264861903772a8c6a29`  
		Last Modified: Thu, 14 Aug 2025 18:42:01 GMT  
		Size: 9.2 MB (9242585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4005c5c6543b1f2735c99b0232d4e8963994cf58276736a2e027b4c765b9d42b`  
		Last Modified: Thu, 14 Aug 2025 18:42:00 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941da73b461d5bec43bea2101222561388f975ce51191b95bda7e0d22896ae55`  
		Last Modified: Thu, 14 Aug 2025 18:42:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:b9281af6a543aa42f0c872a6e38a11e95af6fb363919465d4148c3974694c593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6947455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c32c380af72e69572e81eaf64d7c6b051ee84613ab6f1729bfd33f810ba98e05`

```dockerfile
```

-	Layers:
	-	`sha256:f7e9ef8dad9ed3a19cee82fdea756aa56271149edcf63bdbcc208daa28a09e67`  
		Last Modified: Thu, 14 Aug 2025 20:27:26 GMT  
		Size: 6.9 MB (6927748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbaf125d539a227ad1b2912354d5bd91c0bf21de00485e652877841fae8505f5`  
		Last Modified: Thu, 14 Aug 2025 20:27:27 GMT  
		Size: 19.7 KB (19707 bytes)  
		MIME: application/vnd.in-toto+json
