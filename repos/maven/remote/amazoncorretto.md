## `maven:amazoncorretto`

```console
$ docker pull maven@sha256:b038f33bcfb9ccdc5708102eae3e52019da3e44267380e342fa9a5b6bcb645ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:b320135a10f2ab1723d60a7160314305be10933d1554fff3657407f7a53f57b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.8 MB (411829621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6906d70abab337049e4741a87c4b4ec5da7923d40129e4215179b89808e87cb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=17.0.15.6-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=17.0.15.6-1
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
	-	`sha256:68b5eef1eb563a36e20df422ee1592c70689019fdd12cc4fdc4e4b24c31c1c77`  
		Last Modified: Thu, 27 Mar 2025 19:19:22 GMT  
		Size: 62.8 MB (62752889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3b5771a528b1220f7f687181fc0cec216aed88a7fd109a223e795a33dcb1dd`  
		Last Modified: Tue, 15 Apr 2025 23:55:59 GMT  
		Size: 151.8 MB (151750643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2effdd83a98e69051a2b0c1f25e3d45612eff80be36926fc9a4bd162a947b79`  
		Last Modified: Wed, 16 Apr 2025 00:08:47 GMT  
		Size: 158.1 MB (158080964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3793bc761f126d1eb271fe42a23a2d681203f30f6ee83185cc4ac3786e136db6`  
		Last Modified: Wed, 16 Apr 2025 00:08:45 GMT  
		Size: 30.1 MB (30073640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f26aad95391a6f0d2f3a987e6cf02aeb520de2fbeb60a58c8495d5d1a5897b`  
		Last Modified: Wed, 16 Apr 2025 00:08:45 GMT  
		Size: 9.2 MB (9170441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e312c4787a10f5507ace880c23704f48e3aa33c74b05dc0973e13d3d122fb779`  
		Last Modified: Wed, 16 Apr 2025 00:08:44 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccea63d597c9857fb03574e2b3eb1a99b0aff9ef504001a4fc800f50822dbf1`  
		Last Modified: Wed, 16 Apr 2025 00:08:45 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:ef537ec44d8e6e289897b71e44c53afd5c402b51f8a1cbc4c2a0a2b3ee45a40f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6927977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f728841891f5bbecdc1e48e2b0201e4c36290dd909e8fce3617e37f74db1503`

```dockerfile
```

-	Layers:
	-	`sha256:db002bce553f338308d708c187bd0fd003e4dca5fac246e3d7406c5e2079002f`  
		Last Modified: Wed, 16 Apr 2025 00:08:44 GMT  
		Size: 6.9 MB (6908475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:995982d6c683478fa2607913a9b5e96b434039c7023100c9c2ca05c9922825aa`  
		Last Modified: Wed, 16 Apr 2025 00:08:44 GMT  
		Size: 19.5 KB (19502 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:882621b837faca112c9b3e37eb7459694453b2fcf27141369bcf679eab50ef4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.4 MB (389389362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e6bc79314c4675a732b380515efc449dfce49884c487dd0f4c3eeadb8d73dc1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=17.0.15.6-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=17.0.15.6-1
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
	-	`sha256:bf0d47d55e313b24603bbdfcf71df5fce9b23e8a6af770024f7d7c0282dd1e60`  
		Last Modified: Thu, 27 Mar 2025 19:19:37 GMT  
		Size: 64.6 MB (64565822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc78a794204205caf229722289ea3beec64dfead5533793f7446dc927d5a3ea`  
		Last Modified: Wed, 16 Apr 2025 00:08:14 GMT  
		Size: 150.4 MB (150384110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b014cb79c9d8cf78f2ec7ec7db39a854f8be24831b3fac0d7032dce2869769`  
		Last Modified: Wed, 16 Apr 2025 01:25:44 GMT  
		Size: 134.1 MB (134080324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd30db2c653eceea3a757b034ec398ebca647dd243257f5dcfb0374429339d9`  
		Last Modified: Wed, 16 Apr 2025 01:25:41 GMT  
		Size: 31.2 MB (31187628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e9403d1c45c894d5f1d673675a6dd1e5d7971d88141f5b80a5663d43b65605`  
		Last Modified: Wed, 16 Apr 2025 01:25:41 GMT  
		Size: 9.2 MB (9170435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd234ab56d8fe2ccb625168371a75ca160348856310da3d71270ed16bc98afd`  
		Last Modified: Wed, 16 Apr 2025 01:25:40 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b6ed511d59e221fb1356a4ecd1a538d6945d09c4c690f95a27a50cc3208469`  
		Last Modified: Wed, 16 Apr 2025 01:25:42 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:8efa85b74971d3d1dbf6e128462f5f5008bb963ea65ab5726da4baf1dc0d18eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6925620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905c907c92f7739dd80c93b215a95e7fd19d0fb3b75a80038bfac7a632333ac1`

```dockerfile
```

-	Layers:
	-	`sha256:c0a8d82c130b7d30664b828ce85f381fe42a9bf4f6bf76b5771e4a0e17bd9d88`  
		Last Modified: Wed, 16 Apr 2025 01:25:41 GMT  
		Size: 6.9 MB (6905922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:800baedb8e00320a6b431c0d8a74bde0d58dd9078187908e9c155a408aee8031`  
		Last Modified: Wed, 16 Apr 2025 01:25:40 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json
