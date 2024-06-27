## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:ddf52ebe4da6022fffe9e907d6e85f2d54de9293a53ed4a474f0c234d30f9dd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:82532565fed78e01287a1a2b81188c681424b691f99ba6982b23875a5e40270c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.1 MB (368050924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cadf7793db8ab1965bf658f596ac57ad592074a983e0f474600f0d968bae53c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 27 May 2024 15:57:48 GMT
COPY dir:4184bb78726a0c9ceccafb2f51aa4c1f9147f3cd1379888561d889de0d9e48af in / 
# Mon, 27 May 2024 15:57:48 GMT
CMD ["/bin/bash"]
# Mon, 27 May 2024 15:57:48 GMT
ARG version=17.0.11.9-1
# Mon, 27 May 2024 15:57:48 GMT
# ARGS: version=17.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 27 May 2024 15:57:48 GMT
ENV LANG=C.UTF-8
# Mon, 27 May 2024 15:57:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 27 May 2024 15:57:48 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 27 May 2024 15:57:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 27 May 2024 15:57:48 GMT
ARG MAVEN_VERSION=3.9.7
# Mon, 27 May 2024 15:57:48 GMT
ARG USER_HOME_DIR=/root
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 27 May 2024 15:57:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 27 May 2024 15:57:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:492439933c1ff7612b0a83687414326a9f2b12f1ab63e5ac2e42a257e9834145`  
		Last Modified: Thu, 13 Jun 2024 01:57:58 GMT  
		Size: 62.6 MB (62646452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8122220135d78584f57387e7ed3c95af6a688def4b291d8e18a3e77cb35441cd`  
		Last Modified: Thu, 20 Jun 2024 18:21:17 GMT  
		Size: 152.1 MB (152144847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd10868a4e21646ae26c02e74f65b1dd1e7397ae72c2c41833d7718f4a29422`  
		Last Modified: Fri, 21 Jun 2024 02:01:46 GMT  
		Size: 143.6 MB (143610998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751cb296fefcaf279c9a8ab4d701372dfca0202a94ef1aa8cba17473d0b7d8b3`  
		Last Modified: Fri, 21 Jun 2024 02:01:44 GMT  
		Size: 9.6 MB (9647582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed7cef8242a284b0d4d1a47af9a70c5843d6e13a96c32c229955100a5a89917`  
		Last Modified: Fri, 21 Jun 2024 02:01:45 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5b128c8fa86229947542a69d5895370ac71765d00d1aef5e5a41250c26a487`  
		Last Modified: Fri, 21 Jun 2024 02:01:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:24253f18b198c6dd61003e3f062215cd0492aea5161aa123a7b554bac1504a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085c0381665501623195231a0285002b579ca4cb97d45b54b6e1dd179edcc7b1`

```dockerfile
```

-	Layers:
	-	`sha256:70b061cfb50596887c0d327261c55bc2ccc2f3600039e1546c748f579e32fcc1`  
		Last Modified: Fri, 21 Jun 2024 02:01:44 GMT  
		Size: 5.6 MB (5612618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eab5e5b527aaf5afef76a0078796987542263b3a598dc57c27be0b414f70b300`  
		Last Modified: Fri, 21 Jun 2024 02:01:44 GMT  
		Size: 16.1 KB (16150 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:13eebc387ff05e3509df20b54ecdad0f88888997127fe516377de814d6314db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.5 MB (345494676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0538d44e2c88b919c767c3bcafb5a7fd68637059c302388c35ad6ba69bafaa`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 27 May 2024 15:57:48 GMT
COPY dir:23934f7f3a9c4ad2c0f7afe64c708fe8194f94cafce3bfbba33d3cd60b2fc65e in / 
# Mon, 27 May 2024 15:57:48 GMT
CMD ["/bin/bash"]
# Mon, 27 May 2024 15:57:48 GMT
ARG version=17.0.11.9-1
# Mon, 27 May 2024 15:57:48 GMT
# ARGS: version=17.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 27 May 2024 15:57:48 GMT
ENV LANG=C.UTF-8
# Mon, 27 May 2024 15:57:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 27 May 2024 15:57:48 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 27 May 2024 15:57:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 27 May 2024 15:57:48 GMT
ARG MAVEN_VERSION=3.9.7
# Mon, 27 May 2024 15:57:48 GMT
ARG USER_HOME_DIR=/root
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 27 May 2024 15:57:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 27 May 2024 15:57:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6b964e874adca881e086a1062b2772882d2bcb2401e15ce21606f20d7a58e7de`  
		Last Modified: Thu, 13 Jun 2024 01:57:59 GMT  
		Size: 64.6 MB (64568709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d7068a47d0ed30b3b3c624262d1d44e1a48c54bfb60a353b15bc654b9d80cf`  
		Last Modified: Wed, 26 Jun 2024 16:49:16 GMT  
		Size: 150.8 MB (150790006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f661ca8649dd15e91e12d1b2f9b6f0e2619dbd7edb92614cd6c7cb642bf756b`  
		Last Modified: Wed, 26 Jun 2024 18:59:11 GMT  
		Size: 120.5 MB (120487297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d82e39e7cba845bfeab1e04b487fd98f91eb1fab0988fa520ed61c75584fe00`  
		Last Modified: Wed, 26 Jun 2024 18:59:08 GMT  
		Size: 9.6 MB (9647617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28089f3ba0e9c58672be4bebe4b1d68a6b2c1736941d8bb87aa7624118dcf906`  
		Last Modified: Wed, 26 Jun 2024 18:59:08 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ab4f74a022269ae45e61635e4c6c0f0b1824a3c3abbece959e2e9e44ccfa83`  
		Last Modified: Wed, 26 Jun 2024 18:59:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:ef2ff9e76d81dd1ef5a14bc729acba8c98400988f52c283edc2a1e50f128fa52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d192733f1c7508f2684d7de501801d598e522e30d411c87875da058eb2622d3`

```dockerfile
```

-	Layers:
	-	`sha256:de6fd665f444dc420e6317d300fbaa0fa7663fb1ea5b77a4118b95b5711a7844`  
		Last Modified: Wed, 26 Jun 2024 18:59:08 GMT  
		Size: 5.6 MB (5611245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0e929591cf820ec43395136e884f99b12361f8dc02b1d7d72412125e346aba2`  
		Last Modified: Wed, 26 Jun 2024 18:59:07 GMT  
		Size: 16.8 KB (16796 bytes)  
		MIME: application/vnd.in-toto+json
