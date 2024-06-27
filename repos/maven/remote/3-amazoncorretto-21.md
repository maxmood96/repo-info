## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:f4b056ec50d6252ac65f9bed39c4527ca743fbce722c149ec639b95adc9601e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:1230cdb7f077cc4370b0717a3d0705ba141394ccfad742725d8bf326552601bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.6 MB (381587810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df1f27ce2d00cf73b1a06455e4decf5944a357b72e8bc234db547e694b5258e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 27 May 2024 15:57:48 GMT
COPY dir:4184bb78726a0c9ceccafb2f51aa4c1f9147f3cd1379888561d889de0d9e48af in / 
# Mon, 27 May 2024 15:57:48 GMT
CMD ["/bin/bash"]
# Mon, 27 May 2024 15:57:48 GMT
ARG version=21.0.3.9-1
# Mon, 27 May 2024 15:57:48 GMT
# ARGS: version=21.0.3.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 27 May 2024 15:57:48 GMT
ENV LANG=C.UTF-8
# Mon, 27 May 2024 15:57:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:6587bf502e0fddfa3d71e42fc5be22a5dada226ab4e30f31f4c34ed43581b965`  
		Last Modified: Thu, 20 Jun 2024 18:23:58 GMT  
		Size: 165.7 MB (165682272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d3ed75213bab1fc0c2c0e6d58165ca67a82471d87322c499ae3af11e38f4fd`  
		Last Modified: Fri, 21 Jun 2024 02:01:53 GMT  
		Size: 143.6 MB (143610460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8ea93bd134c0462a8e81c8e2951c0b4ce82831cfc0a6afa9749ac70805f387`  
		Last Modified: Fri, 21 Jun 2024 02:01:50 GMT  
		Size: 9.6 MB (9647582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa0c27804aa80de79c5aeef8177026810971d0a0bd6249ec59b77999bf6730c`  
		Last Modified: Fri, 21 Jun 2024 02:01:49 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328bbd393b88407eec5ada1fb386550dc701897180e5b90a0f0bfaaeb42f29ad`  
		Last Modified: Fri, 21 Jun 2024 02:01:50 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:923446ea1d8d5ba934459d81b12a7b5aaef7dc4fdb3da9ded28581e4e2d07b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5629486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b2f3d78fc56957cdfe7215bd68a5119eda2f5b7091a16d93cb40e5be7bb46f`

```dockerfile
```

-	Layers:
	-	`sha256:2d15282170510f71bccff270bcac445776211d8008b823ee01e128a9fbb266d5`  
		Last Modified: Fri, 21 Jun 2024 02:01:50 GMT  
		Size: 5.6 MB (5613336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb00b570ab2221f9770d8ea7206cb05bf56e85559d9402cc4d334c7100ec8464`  
		Last Modified: Fri, 21 Jun 2024 02:01:49 GMT  
		Size: 16.1 KB (16150 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d0aa2949d9bdbd2f568e5349cf7e676bf63185759694d6f2637a39a86c545281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.4 MB (358445235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a972c2dcfe73fa47e7dc3d2d95a86341064a994dabc8633289618fa6dd7e7250`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 27 May 2024 15:57:48 GMT
COPY dir:23934f7f3a9c4ad2c0f7afe64c708fe8194f94cafce3bfbba33d3cd60b2fc65e in / 
# Mon, 27 May 2024 15:57:48 GMT
CMD ["/bin/bash"]
# Mon, 27 May 2024 15:57:48 GMT
ARG version=21.0.3.9-1
# Mon, 27 May 2024 15:57:48 GMT
# ARGS: version=21.0.3.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 27 May 2024 15:57:48 GMT
ENV LANG=C.UTF-8
# Mon, 27 May 2024 15:57:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:385a0ab3ae31a54931e74a64c95205fed2b9ef2e2b72157455064e05fd1fd523`  
		Last Modified: Wed, 26 Jun 2024 16:52:41 GMT  
		Size: 163.7 MB (163740143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3af05b946deb55876596e9f067f9ee7bb4b3062ecb5a1f24a98df430565105`  
		Last Modified: Wed, 26 Jun 2024 19:01:04 GMT  
		Size: 120.5 MB (120487720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a85d135de19ca3706f2dcc0a967307e3c3e11fc90e73cfe4fe309471014cbf`  
		Last Modified: Wed, 26 Jun 2024 19:01:02 GMT  
		Size: 9.6 MB (9647617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79d0051b393a43bf41413b3ca161317273f95cb2cd280ab4a1688fbbe45c942`  
		Last Modified: Wed, 26 Jun 2024 19:01:02 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bcf87e71d01eada3acf7ebbcecfaa01060d680c2cb595e211f080dbe566117`  
		Last Modified: Wed, 26 Jun 2024 19:01:03 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:d6e265bbf26804805848af71e5f55213bf9c443fd000aac6d0d967386b63a967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c419b016639d0df091a1054912d97b36416819885feb271a4cb1b6aff18011eb`

```dockerfile
```

-	Layers:
	-	`sha256:d7ccc41127902e5536b766701c13ff4fb1bbac3395cdef59097c18b2cf975a38`  
		Last Modified: Wed, 26 Jun 2024 19:01:02 GMT  
		Size: 5.6 MB (5611963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0710a1a4610b540f81550c62a6daf8cd10f97b4f9ff650c4117f57efdda4e442`  
		Last Modified: Wed, 26 Jun 2024 19:01:01 GMT  
		Size: 16.8 KB (16796 bytes)  
		MIME: application/vnd.in-toto+json
