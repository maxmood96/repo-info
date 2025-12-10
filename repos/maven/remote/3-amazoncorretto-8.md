## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:5fb647d19ae93fd05b8f9ccdd330dc121db275f76103b00cb057eb14c59ab831
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:17b210c1179ff8383eeeff7ca1df199dac4889820e06eb7e1d42534d871dc107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.4 MB (350420647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e18eb99a7e75da45e543d32806d9043455e3155106bf75739e6430ba6000bdb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:30 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:30 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:20:39 GMT
ARG version=1.8.0_472.b08-1
# Wed, 03 Dec 2025 20:20:39 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 03 Dec 2025 20:20:39 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:20:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 03 Dec 2025 21:15:37 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 03 Dec 2025 21:15:45 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 03 Dec 2025 21:15:45 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 03 Dec 2025 21:15:45 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 03 Dec 2025 21:15:45 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 03 Dec 2025 21:15:45 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 03 Dec 2025 21:15:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 03 Dec 2025 21:15:45 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 03 Dec 2025 21:15:45 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 03 Dec 2025 21:15:45 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 03 Dec 2025 21:15:45 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 03 Dec 2025 21:15:45 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 03 Dec 2025 21:15:45 GMT
ARG USER_HOME_DIR=/root
# Wed, 03 Dec 2025 21:15:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 03 Dec 2025 21:15:45 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 03 Dec 2025 21:15:45 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b941b2711da4fbb3da23c84124d1934e7fb36712490259252fdc7026b7e44960`  
		Last Modified: Wed, 03 Dec 2025 20:21:07 GMT  
		Size: 76.0 MB (76043199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e1a83df4e3f0c1b6a05f210034f1f945423397c5852d5d49c5d647b42812aa`  
		Last Modified: Thu, 04 Dec 2025 00:30:48 GMT  
		Size: 172.1 MB (172147233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100780f2d8ea1f1451f777ef37d18692d4fb0890cf17b8acbf046ab3ea285ea0`  
		Last Modified: Wed, 03 Dec 2025 21:16:23 GMT  
		Size: 30.1 MB (30056020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09f0f0037eb70f64ddd9361b9cdd4bb131547b527d032e87bb6bfe8aaf1172b`  
		Last Modified: Wed, 03 Dec 2025 21:16:20 GMT  
		Size: 9.2 MB (9242579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fccdad0f2c2f34a16b0eeea1cf432a69410848acf4dc55d7bf4657c3d23dc09`  
		Last Modified: Wed, 03 Dec 2025 21:16:18 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f6798c17f778e0c2ae4e2ce4e3d2411c3831345e720bdbaceb3925f89b8e96`  
		Last Modified: Wed, 03 Dec 2025 21:16:18 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:f42036ba3936af8be0dfc76f0f0180f7498c370e9646399166031239ad89e5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6791800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f046b68d916fc83a85fe07628657489bc7b32e0b5d8b37136965dcf16bbe883`

```dockerfile
```

-	Layers:
	-	`sha256:8784ebb24508e5ae99b16a5a08689efce8a2a75286f03d7a51868bb865d2f6ae`  
		Last Modified: Thu, 04 Dec 2025 00:28:38 GMT  
		Size: 6.8 MB (6773614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07baa8d6dfea580ec12f2551e2af647987f71b2e5c8e54ae9c842591a1cd7427`  
		Last Modified: Thu, 04 Dec 2025 00:28:39 GMT  
		Size: 18.2 KB (18186 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c29b6b53f6f2c2e937b16afe69212cd68f8e132919e5cadf9b156700f5768081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.4 MB (313392276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dfed6cb79eed9d40a3e158daa524e73eb54d58042a6d6e79da1009e8b1f6443`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 03 Dec 2025 20:03:07 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:03:07 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:24:44 GMT
ARG version=1.8.0_472.b08-1
# Wed, 03 Dec 2025 20:24:44 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 03 Dec 2025 20:24:44 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:24:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 03 Dec 2025 21:16:04 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 03 Dec 2025 21:16:12 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 03 Dec 2025 21:16:12 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 03 Dec 2025 21:16:12 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 03 Dec 2025 21:16:12 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 03 Dec 2025 21:16:12 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 03 Dec 2025 21:16:12 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 03 Dec 2025 21:16:12 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 03 Dec 2025 21:16:12 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 03 Dec 2025 21:16:12 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 03 Dec 2025 21:16:12 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 03 Dec 2025 21:16:12 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 03 Dec 2025 21:16:12 GMT
ARG USER_HOME_DIR=/root
# Wed, 03 Dec 2025 21:16:12 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 03 Dec 2025 21:16:12 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 03 Dec 2025 21:16:12 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b9e592d86547093987189c87cb61affd6d9b575595342a3460822d42288e65`  
		Last Modified: Wed, 03 Dec 2025 20:25:13 GMT  
		Size: 60.1 MB (60119087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415eaded1a6899c67742b56d68f709072c968af4a5bd4793bb5b0cfbc3b24fbb`  
		Last Modified: Thu, 04 Dec 2025 00:40:13 GMT  
		Size: 148.0 MB (148028304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67ab4f1bb41f29ccf1aa6e1e0cb02b45485226acac8da71ba4c9889115c2faf`  
		Last Modified: Wed, 03 Dec 2025 21:16:54 GMT  
		Size: 31.2 MB (31208461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ca7b45c831170e0efb17d0f92d7e2fbc85f4e63c0f2660b535b43a620deeae`  
		Last Modified: Wed, 03 Dec 2025 21:16:51 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848c6f6260cf4f8dfb445114db8bdd0e55fb4ea7909e2c93ab665436654ffee4`  
		Last Modified: Wed, 03 Dec 2025 21:16:50 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bddf52618eada93da2fe6f9db770539457df59e4d1cdab01f97949a8d06faa`  
		Last Modified: Wed, 03 Dec 2025 21:16:50 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:6055db05ffa3f7b8343855d74de3e4d060d3c90873478b701b06c3dc422c2fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6769146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a673a66df237dc1c2e1cdd521d2cf5a6687c792c3630bfbc973dfc7f7cca9ab0`

```dockerfile
```

-	Layers:
	-	`sha256:67fd4eb1dd79ac9017d4c943a2e5dd99eeffc852738cb91a689296034cc2c7ff`  
		Last Modified: Thu, 04 Dec 2025 00:28:45 GMT  
		Size: 6.8 MB (6750811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da9d04c42e33460c876a5c30c7c12c3c90438a63fa7c93db50250056730940a8`  
		Last Modified: Thu, 04 Dec 2025 00:28:46 GMT  
		Size: 18.3 KB (18335 bytes)  
		MIME: application/vnd.in-toto+json
