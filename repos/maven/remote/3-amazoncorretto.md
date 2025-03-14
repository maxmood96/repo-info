## `maven:3-amazoncorretto`

```console
$ docker pull maven@sha256:7306723439e8f0b7a61916b1305e0a5b20478ea6932d6a1772980e8775ef161e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:a387d8149be063bdaf351c1944dea1ce5d6bed7fafd94acdb1c1795e242442ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.9 MB (410863551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0533768e249475723bf6a4914a4c817552480c196fd98c9560f202d0d7e51569`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=17.0.14.7-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f3dc83dc2e4e000fd189efee126db80e38a079b47b8e5229a794a0a6148bfec6`  
		Last Modified: Sat, 08 Mar 2025 04:13:59 GMT  
		Size: 62.8 MB (62772838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43286579a12ae4b9ab20c4fc9bf5cc0f11f37c50af6d2f23f657c01068d00ac6`  
		Last Modified: Thu, 13 Mar 2025 22:53:03 GMT  
		Size: 151.7 MB (151707304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e92c1dcf58d627582c5236b7495ef7b876b3e98579592191c2e269215d67ed`  
		Last Modified: Thu, 13 Mar 2025 23:09:44 GMT  
		Size: 157.1 MB (157119393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d76b6d037f4eed3681688f03395cb6d3fbfce9ee490730ba6e95093da34cb52`  
		Last Modified: Thu, 13 Mar 2025 23:09:43 GMT  
		Size: 30.1 MB (30092538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d36c7037d0d489b3a06e51a124e276acf459e98081997539525251747b31e1`  
		Last Modified: Thu, 13 Mar 2025 23:09:42 GMT  
		Size: 9.2 MB (9170436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6ab4c1660c703358e80209c72912be04ea06df5a045c431765dd0b58b501b6`  
		Last Modified: Thu, 13 Mar 2025 23:09:42 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105ef78696303fd73cab359bcd803d52b84c000cf10c5dd9e135afee89dc53e3`  
		Last Modified: Thu, 13 Mar 2025 23:09:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:01c48ea20ba2217fcc958005b9716cc808caf33366c74de177c9260be09cd950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6927939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c65276695cd472d539feb1c125bb5c32a4edfe16fad207b8ccada7698ed4e4`

```dockerfile
```

-	Layers:
	-	`sha256:bf5e49cafac933ec92d6709ac620451904f76f7ef754c3184b727119d93e0bb7`  
		Last Modified: Thu, 13 Mar 2025 23:09:42 GMT  
		Size: 6.9 MB (6908437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1a25d07c9d33cda611e4ab8b1de07cf57818c2b044ca9413c23a1d2e2d2c72b`  
		Last Modified: Thu, 13 Mar 2025 23:09:42 GMT  
		Size: 19.5 KB (19502 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:73978b7429a871613a815faae0608983715344c3c5e9e09e290034248fa34e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.3 MB (388300568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8650aff49c3cd59b0d632026ea13a3697d752231ecf1f1a2cffad98113c34a1c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=17.0.14.7-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:37d03ccf62e80c78860df81fce0c2ae4e2349efe1a11714ff404080836c55d45`  
		Last Modified: Mon, 10 Mar 2025 14:33:01 GMT  
		Size: 64.6 MB (64576854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8bf0cdbdc0bf98d70c12f8458c667a38d58b1c554dd6deb1715417d5b3be5d`  
		Last Modified: Fri, 14 Mar 2025 01:16:16 GMT  
		Size: 150.3 MB (150317807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6c1d370932b13db5da5063a873cfe29cfc8be801aa713a0ba2b7dcaf31e9fd`  
		Last Modified: Fri, 14 Mar 2025 17:43:02 GMT  
		Size: 133.0 MB (133048970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a628636156e796039c963535c8700c7bff2569bbe6b310f8e4b0b64b0ae57ddd`  
		Last Modified: Fri, 14 Mar 2025 17:43:00 GMT  
		Size: 31.2 MB (31185462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a301ed630fc351d2e4d994f3c017b09522e76eedd907ad4753d6307ece4fabc2`  
		Last Modified: Fri, 14 Mar 2025 17:42:59 GMT  
		Size: 9.2 MB (9170434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f717a70be5445ca3409ed89ee72953515a7bed2212d0b0f8773696114e761f9e`  
		Last Modified: Fri, 14 Mar 2025 17:42:59 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a42c65e9b0ce3f29adab6f41b1f01bb05e3b2ecd2cfc0803b08dba4d26b7ff6`  
		Last Modified: Fri, 14 Mar 2025 17:43:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:7ae07f6b6664a2d2ada7c5b318c3c93f7f5b765d83dce82dd2bb77e17d773baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6925582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc2437941802f4fe3642ab65f81e126bbcac9a59659d30ba5620180e75f761da`

```dockerfile
```

-	Layers:
	-	`sha256:f6e58f39cbbab201728f67164a87a1e9ddd9bd1180248bbb0c9e7990aa47fd28`  
		Last Modified: Fri, 14 Mar 2025 17:42:59 GMT  
		Size: 6.9 MB (6905884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee2fddf7e269176d77f326878d693c029b9b903e8bd4c05a44e29ded1e835f44`  
		Last Modified: Fri, 14 Mar 2025 17:42:58 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json
