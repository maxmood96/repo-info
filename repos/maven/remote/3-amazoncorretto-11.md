## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:8f221d17f515626fa131800a34bac76fa41a70a5dccec71a70c3c3cb9cd6d7aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:a34b323e7f70dc173287b902e70f677aff4dcdecc41bfd50ecc9d9305a372158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.6 MB (425635227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8211f67a53c526b413b92e9db119eb80c6f64e6536c5ca851d09280b4e6cc4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 11 Mar 2026 18:22:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:22:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:32:07 GMT
ARG version=11.0.30.7-1
# Wed, 11 Mar 2026 18:32:07 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 11 Mar 2026 18:32:07 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:32:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 12 Mar 2026 20:12:35 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Thu, 12 Mar 2026 20:12:44 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 12 Mar 2026 20:12:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 12 Mar 2026 20:12:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:12:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:12:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 12 Mar 2026 20:12:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 12 Mar 2026 20:12:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 12 Mar 2026 20:12:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 12 Mar 2026 20:12:44 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 12 Mar 2026 20:12:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 12 Mar 2026 20:12:44 GMT
ARG MAVEN_VERSION=3.9.14
# Thu, 12 Mar 2026 20:12:44 GMT
ARG USER_HOME_DIR=/root
# Thu, 12 Mar 2026 20:12:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 12 Mar 2026 20:12:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 12 Mar 2026 20:12:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:94fc983b0f2661f620fb3c97c279be6e7a6a21ff4a004bf4df15272612aed901`  
		Last Modified: Sat, 07 Mar 2026 04:10:35 GMT  
		Size: 63.0 MB (62956510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b20d6ad17bf5a5e6c795a6bafe254f811eb55ef5f45999fe7ad9419d1a2c4a`  
		Last Modified: Wed, 11 Mar 2026 18:32:27 GMT  
		Size: 148.1 MB (148126018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d1c776b775dded44d8be8baec8cdcae13c8e8217b648dd55e5c8538dca1dea`  
		Last Modified: Thu, 12 Mar 2026 20:13:13 GMT  
		Size: 175.2 MB (175156189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ae5af27e3bbc496110821ee2282adef32f9d6fc09f5ea781954d10dc449143`  
		Last Modified: Thu, 12 Mar 2026 20:13:10 GMT  
		Size: 30.1 MB (30084289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b246b3f42fa92f5a49464d0d800115b68da0ad7a5fe726bfcdce8354ee1a2c30`  
		Last Modified: Thu, 12 Mar 2026 20:13:09 GMT  
		Size: 9.3 MB (9311179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e0a81516518e7c747e81f20aeb525b798e91315b4ac640a9cde8c6f3308215`  
		Last Modified: Thu, 12 Mar 2026 20:13:09 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e606636e72c786535ff7801189419c986356d7c98b5b6faa0126106c923d75`  
		Last Modified: Thu, 12 Mar 2026 20:13:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:e1afc5228f927cdfc6f0501e41d668399ef10acadcc4cd19c67b16ee2a087f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6957748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847c4ceb771f3b5c76e311e8735f3d22a5b6cf70acfa831f5ce73f14076a51bc`

```dockerfile
```

-	Layers:
	-	`sha256:8125af308d13cfc713c5ae5b68f2bda2be250c293e7f07eec5295710ec322825`  
		Last Modified: Thu, 12 Mar 2026 20:13:09 GMT  
		Size: 6.9 MB (6939554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b513eab56438709075dffabbec64d963914fe48e1fff14a27a6de96c1da9a49d`  
		Last Modified: Thu, 12 Mar 2026 20:13:08 GMT  
		Size: 18.2 KB (18194 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c9fd0743e583c36c5b2b0e013f6fe80e4d5e84cebe64fef9c191110a0ecf15d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.3 MB (401293573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58489fe2684dfeb41d71296422873075792368bfa49402968fb873771e39260`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:38 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:32:21 GMT
ARG version=11.0.30.7-1
# Wed, 11 Mar 2026 18:32:21 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 11 Mar 2026 18:32:21 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:32:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 12 Mar 2026 20:10:59 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Thu, 12 Mar 2026 20:11:06 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 12 Mar 2026 20:11:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 12 Mar 2026 20:11:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:11:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:11:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 12 Mar 2026 20:11:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 12 Mar 2026 20:11:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 12 Mar 2026 20:11:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 12 Mar 2026 20:11:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 12 Mar 2026 20:11:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 12 Mar 2026 20:11:07 GMT
ARG MAVEN_VERSION=3.9.14
# Thu, 12 Mar 2026 20:11:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 12 Mar 2026 20:11:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 12 Mar 2026 20:11:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 12 Mar 2026 20:11:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1331e22401e9e6f680f618ca7ac295b00616904425c0ac818294801fd11443e3`  
		Last Modified: Mon, 09 Mar 2026 09:10:03 GMT  
		Size: 64.8 MB (64803149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7932995bd594e75f8d5178d3e3fd2c3400b84edd2f1cf6db87ccb7b6cd9e798`  
		Last Modified: Wed, 11 Mar 2026 18:32:47 GMT  
		Size: 145.2 MB (145212347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ef43d7078dd9db0f20d8f56269ac4c0295546b4fd262aff1a67fc311925226`  
		Last Modified: Thu, 12 Mar 2026 20:11:34 GMT  
		Size: 150.8 MB (150767906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d5ac335b75312c0b04756d7543d67dee859a190e6436524a95035f65a7404b`  
		Last Modified: Thu, 12 Mar 2026 20:11:32 GMT  
		Size: 31.2 MB (31197951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4d66f9922a1c550dbff2950fde560c32584e72ba690babff7a7ca8a2cb5179`  
		Last Modified: Thu, 12 Mar 2026 20:11:31 GMT  
		Size: 9.3 MB (9311178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f616a71be4e11a1813f85319ea976c147707200b92bc06c0ff8b1a382dbca6dc`  
		Last Modified: Thu, 12 Mar 2026 20:11:30 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29465d7dac0150646f725d447faa212d02c500e1a7cfa102c883b8f73e426af6`  
		Last Modified: Thu, 12 Mar 2026 20:11:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:3028dd5cfeabd3cbb46f482bb0043196570e6fe4ca493c0f887bcb390450f14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6956100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9858b6e34d6e078caff1734f7d2b57b14a3e5ea0100348ee5ea729d2be6c53`

```dockerfile
```

-	Layers:
	-	`sha256:15c753957919e570efe44b385ea07d639a467bb405d8bb6cc8d30f769dd90513`  
		Last Modified: Thu, 12 Mar 2026 20:11:30 GMT  
		Size: 6.9 MB (6937758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83311a38560a42bad13eb55329ec3de0fa605861fd56ba3201947ea0784167f5`  
		Last Modified: Thu, 12 Mar 2026 20:11:30 GMT  
		Size: 18.3 KB (18342 bytes)  
		MIME: application/vnd.in-toto+json
