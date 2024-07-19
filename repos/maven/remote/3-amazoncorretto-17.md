## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:2a48f4c4d48f67d4c93aa0d4f72bc3be9b3e3c22255dd1d2a9bfa8eedd6555f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:991eff06bd8c16530b34ffb347466a3ac8ca21386fa900ab983c73a7fee63bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.3 MB (369340448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f921698c73d05cd7ac98fb6f20ed9f24c91f40fafd45d617bc1c00ecff19963b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY dir:15f372c0d55f5152b222fa508a1a8c382d0621d72fdef0d2b746557a14bc0dd9 in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ARG version=17.0.12.7-1
# Thu, 27 Jun 2024 09:17:07 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
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
	-	`sha256:1e5e0347739e5468c65eed56d50fba90128674d8aae6fa196a8c01eeea145da9`  
		Last Modified: Thu, 18 Jul 2024 21:20:18 GMT  
		Size: 62.6 MB (62647926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271ace304f61b3183937996bd46b9b87cbdf03510ee0b37f9ee56441f2cc0376`  
		Last Modified: Thu, 18 Jul 2024 21:49:20 GMT  
		Size: 152.2 MB (152214346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7451b99d4b12e90aa2a3b9994edfae456e1824adf9ec5a7795e9b84e618dcac`  
		Last Modified: Fri, 19 Jul 2024 02:15:54 GMT  
		Size: 145.3 MB (145315319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f3ef51f4148316cf648d063084d7b3850c2c851905c886ab501279080b3ce4`  
		Last Modified: Fri, 19 Jul 2024 02:15:53 GMT  
		Size: 9.2 MB (9161816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e011f6cc5ce9b399df41bc28dc51b7dc1055944e635f9a7396ce6aed1afa8b85`  
		Last Modified: Fri, 19 Jul 2024 02:15:51 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e24834fb8d3799544e96813014101d2c81dfe2a8bf374bf155d9dc8dba51184`  
		Last Modified: Fri, 19 Jul 2024 02:15:51 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:b4886494bf051b5d102f6e02ed241d549881e8c7d87a24438b6bdab3c511a3d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5658215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5afd86668912f2adbe2ea7537b00f750f8690eaddf7c190c46a566653537912`

```dockerfile
```

-	Layers:
	-	`sha256:fb4dcdbfec49b62367fb70811435e7bcbacaf60455844332c58e65c7764a5bad`  
		Last Modified: Fri, 19 Jul 2024 02:15:51 GMT  
		Size: 5.6 MB (5641932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7024674cfce023c4eeab2af87e0964b1bc25cccad1c4eeffa4fd0fd7b6ca4339`  
		Last Modified: Fri, 19 Jul 2024 02:15:51 GMT  
		Size: 16.3 KB (16283 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:77911e72d370cdeac55f14c86b16f1b4f9d7f4187f5c0ed854f257a20ec73bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.0 MB (345973016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7a02f431d87739ae453503540bd48a178728adfcfe450923a4d6296ad9a1e0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY dir:cdeeb89e10fdbe3f38b9e5f6d359ee1afb9caaa1018fdd71fd6c0374dc592a5f in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ARG version=17.0.12.7-1
# Thu, 27 Jun 2024 09:17:07 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
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
	-	`sha256:4ba2ef523fa6e28aa5a068ecb9167a3b9efa29481c3ecc6d34fab1c350b98b6d`  
		Last Modified: Thu, 18 Jul 2024 21:40:02 GMT  
		Size: 64.6 MB (64575311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7670e0f13dba13cacf8a72508b2840f1c1d5b318edb811accb584aab4d61a118`  
		Last Modified: Thu, 18 Jul 2024 22:55:17 GMT  
		Size: 150.9 MB (150866532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb4b92b4d777faf76b1adc794d85cf6655cf6eb1f62721fbd50bbd00937c980`  
		Last Modified: Fri, 19 Jul 2024 00:02:24 GMT  
		Size: 121.4 MB (121368347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf26af4fd471eca66ef4822c593266b7c52904b610e64dafe7a25234cbbbc40`  
		Last Modified: Fri, 19 Jul 2024 00:02:22 GMT  
		Size: 9.2 MB (9161783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985acbb30ad207918ef8e86055967bde2f338b4309ac202141123048805df553`  
		Last Modified: Fri, 19 Jul 2024 00:02:22 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075e247c819f86e52056107ebc22190b6257c82dd7f1cc95fcb4d553fefc4f1a`  
		Last Modified: Fri, 19 Jul 2024 00:02:22 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:4cde29e72bf1966f9adbd83cacbcc07e4ca6d4205339b136b91b2e83e41ab750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5657603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1463b366265e6455b1c0f02d2180307ca8c8d937654e6e10be115924ed741a49`

```dockerfile
```

-	Layers:
	-	`sha256:aef68991832b81d45f66a8fcb03ede7269dad788af76eb942330ed689a84f42d`  
		Last Modified: Fri, 19 Jul 2024 00:02:22 GMT  
		Size: 5.6 MB (5640559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46eb8b3c7ba88162ae6e5aa4c7b34a8bb3155e3b8aeec913cb8bf71f818ee707`  
		Last Modified: Fri, 19 Jul 2024 00:02:21 GMT  
		Size: 17.0 KB (17044 bytes)  
		MIME: application/vnd.in-toto+json
