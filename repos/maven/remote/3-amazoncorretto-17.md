## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:eecfc7b13860f6f498484e7d6dbde198d51eb18f910cb3d518edcb1a02b1eeaa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:9c29d34f56dcb979fb5819193abff63246115b21cdfc58287f73708af7a66117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.6 MB (369561079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7438db51180e7097cf25adfa9e36194371d94df28fbff9f678915d2e6fb9bb8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /rootfs/ / # buildkit
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
	-	`sha256:78d6b943ec35657899afc44f3f9b766ee923d9028028da721b7d4e7bc35e184f`  
		Last Modified: Tue, 23 Jul 2024 13:50:25 GMT  
		Size: 62.7 MB (62679166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16d1356ff865ed2ae4a8317d0fc95d8da710d367d04ec8a934e449d8ff736a1`  
		Last Modified: Thu, 25 Jul 2024 21:02:15 GMT  
		Size: 152.2 MB (152247639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a536ec179e1f1ebe3cc99b9a1130d152a40e814f8fe8dc7064f847396d59e41`  
		Last Modified: Thu, 25 Jul 2024 22:00:58 GMT  
		Size: 145.5 MB (145471421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996b38cfc916db2626d02d5dea7a6eab190688b8e44570ce1f8f59cc3a937f96`  
		Last Modified: Thu, 25 Jul 2024 22:00:56 GMT  
		Size: 9.2 MB (9161813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fa76681dc115e0bb85e1f7fe97b7fb5bbcf53cabd29324cc47c6ddc513d62d`  
		Last Modified: Thu, 25 Jul 2024 22:00:56 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0f6b7aac5dba3db5d03d1ab7c16a3c6129489fdd1ee99976af9702b373f7c2`  
		Last Modified: Thu, 25 Jul 2024 22:00:56 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:2bffb719ba0258df81bc6bb15130085e1f9e53175315acb6f6cf47765c7cf784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5658216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bf1f1c830a75228df1d723526affca2fd6e23ddbfe16d7707b8a78e1350e60`

```dockerfile
```

-	Layers:
	-	`sha256:cffed9662ee4cc63e6ae2216ce46480976d049105e60f7345061cab3828f63f2`  
		Last Modified: Thu, 25 Jul 2024 22:00:56 GMT  
		Size: 5.6 MB (5641932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52e95da2dd9cd5a318dcf9341e443558cab9d6ba273d5a13ae630709aa04e0f1`  
		Last Modified: Thu, 25 Jul 2024 22:00:56 GMT  
		Size: 16.3 KB (16284 bytes)  
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
