## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:8c89cef5a5358217f65ab4de204c4539444421b601116fd0be659babb31a656e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:f561dbae251fec073ab78391fb98080898efac68d480211989335518d6526f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.4 MB (368410475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0925218863f5ec3735c4f771b5c000675112cf95ef81edc7ce69ab03678b0fd0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY dir:db8dc48874881c2542c8e2120173f53413158e7da7526edf07aa742f426b8c16 in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ARG version=17.0.11.9-1
# Thu, 27 Jun 2024 09:17:07 GMT
# ARGS: version=17.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=C.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 27 Jun 2024 09:17:07 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2a5dc0ac7266321476902a4277a4723285b608c065fcb80cacdb3ed43a7c29fe`  
		Last Modified: Fri, 28 Jun 2024 00:20:37 GMT  
		Size: 62.6 MB (62646638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e034acdf66e3297a49cf63d7d0b9ab75bbc1b44c38ab12befb2dd66d3c21de5`  
		Last Modified: Fri, 28 Jun 2024 01:23:30 GMT  
		Size: 152.1 MB (152144884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa41d67f4aafef322200eddda08f67df72b4f5199635bc7c95767c122167803`  
		Last Modified: Tue, 02 Jul 2024 09:09:45 GMT  
		Size: 144.5 MB (144456096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda078f3c40c79489061125e1ab6b4dbcc62b8fd35b5f33ab00de42faa5f09d1`  
		Last Modified: Tue, 02 Jul 2024 09:09:41 GMT  
		Size: 9.2 MB (9161815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae974c39edb94fe61e493c566331d9168d47e505d48884ce3b6d49578dff8ff5`  
		Last Modified: Tue, 02 Jul 2024 09:09:41 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daed87562fdd631a7e6296efa090c94308a47d3b27c97eb8e12548221bf06b04`  
		Last Modified: Tue, 02 Jul 2024 09:09:41 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:95bdfda3610b6d712142bd3dc55115a71e2165b18a6b6b6345904a6027dc2ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f353690e19dc2830cf85568a608e98738a8abe8ff855767722dda0b5f18da5`

```dockerfile
```

-	Layers:
	-	`sha256:bbc7a275e03302f3e9d02f969832e4e26890e159a6efdfda89f3c003dd76c9a4`  
		Last Modified: Tue, 02 Jul 2024 09:09:41 GMT  
		Size: 5.6 MB (5612573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97ea1a79071f5d72ba1ffabb8914c68d34f22151027b130387feb1dd4884e6b1`  
		Last Modified: Tue, 02 Jul 2024 09:09:41 GMT  
		Size: 16.1 KB (16150 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d2382146a92cad8aa97212ed9ce6569a24358f10f5f6d0c5afd854a632fc867c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.0 MB (345009168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d52d7719f4f4694be562ce80cb2151597b4646879a763400c49d5ae04ce891`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY dir:36542351efcfebe46f7ccbf0def8f62c4d1fc618b41a02b6d9df97e06c5cf74a in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ARG version=17.0.11.9-1
# Thu, 27 Jun 2024 09:17:07 GMT
# ARGS: version=17.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=C.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 27 Jun 2024 09:17:07 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2936210a619ec662b53521cc3dd41798a491971a48e14f14ebb594e81dc798b0`  
		Last Modified: Fri, 28 Jun 2024 00:40:34 GMT  
		Size: 64.6 MB (64568765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a5400ea07504e79bc0fc093c0447820e98babd760b87a6024f8b58349c8a68`  
		Last Modified: Fri, 28 Jun 2024 01:28:50 GMT  
		Size: 150.8 MB (150790193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633b5644f8796d27f55652af6c5155ef5ed799983d500ddfe0327699fde417e5`  
		Last Modified: Fri, 28 Jun 2024 02:06:42 GMT  
		Size: 120.5 MB (120487354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2fd3016e96c0bf61d54da0ab17717c1544b5e3e5c6b5e2b681928b9a3af0be`  
		Last Modified: Fri, 28 Jun 2024 02:06:39 GMT  
		Size: 9.2 MB (9161808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49ddbe96e6df39a2fff647e0151af3b8c583d3ad5a46eed3ef17bbe438a88d7`  
		Last Modified: Fri, 28 Jun 2024 02:06:39 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13b66ec86722dcca4c413d31b7fa665ad8f2db79efa5b35d4d669503dc38e39`  
		Last Modified: Fri, 28 Jun 2024 02:06:40 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:2582186e6b0e3b6a10726711e392449df5e59a6f3c9c0411a460f2718cd1df63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5627996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe6f800f7bbdb2398f065dde4c8809e88e77c93572499d045d80ca59a30522a`

```dockerfile
```

-	Layers:
	-	`sha256:1c5d1869b8c9923b6330d691739ec82ad8974ce4756a19a0646a2a1e2b2e5bff`  
		Last Modified: Fri, 28 Jun 2024 02:06:39 GMT  
		Size: 5.6 MB (5611200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:feeffb45ddd3ebfd6572f70290f55c6e5ea8661f6829274cdbd140052288635c`  
		Last Modified: Fri, 28 Jun 2024 02:06:39 GMT  
		Size: 16.8 KB (16796 bytes)  
		MIME: application/vnd.in-toto+json
