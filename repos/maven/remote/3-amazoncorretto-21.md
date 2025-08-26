## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:20fa64ab8abe5a6e20f6077c884bfe88b625cf09cc582595d48c65b913c59f59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:ce2692ba15e2e1ed85cd1458eba2df074f6d10ccc5766f437729381527574f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.5 MB (433520721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d7352b86de32499451c3fb461243626b193b667ef9ef1dad2f17a9f65f2343b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=21.0.8.9-1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=21.0.8.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:f21a9c156d2ab29af4b5e451610a197ca56345598aa7ad950a22561b52bd146d`  
		Last Modified: Fri, 22 Aug 2025 17:34:29 GMT  
		Size: 63.0 MB (62978125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6d1fa18a34a0c0fc45e16116451d99d67634c7c4fc2b5fce27a221d8d5d90f`  
		Last Modified: Mon, 25 Aug 2025 20:55:08 GMT  
		Size: 165.1 MB (165092101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bb3be7a57c1e5561d2e47030ed2b839ce1f2c999be6206c17dad004c43e4d5`  
		Last Modified: Mon, 25 Aug 2025 23:28:29 GMT  
		Size: 166.1 MB (166099724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311dc4abe49ee86be7056aae5b3ab4e2aae311ba40613acba4359604b1c483e3`  
		Last Modified: Mon, 25 Aug 2025 20:56:20 GMT  
		Size: 30.1 MB (30107142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e571f65d2b165722f891e0b43884ee89d20c15dc58c55911320ba5482210fa2e`  
		Last Modified: Mon, 25 Aug 2025 20:56:20 GMT  
		Size: 9.2 MB (9242585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9a3df7c918a0ff916e42604b67bfbd1d2b652090faaf06895098b37a65f6cf`  
		Last Modified: Mon, 25 Aug 2025 20:56:20 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b40d47870456366fe769817be8e7739187b691367bade083ba8ae35a062d132`  
		Last Modified: Mon, 25 Aug 2025 20:56:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:91f9fb7c3f3ebe26781339ffffdc023b4fc7e8ba908a4d911708b7223b7a8a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6947161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f951da4634d0249998beb3d822b32b843e1e19dd794cf675d885486e6a11e6d`

```dockerfile
```

-	Layers:
	-	`sha256:db5acc2173abc8ea31c32d190192bb188500b4c92b52007ec906abc1b16e2dc4`  
		Last Modified: Mon, 25 Aug 2025 23:27:48 GMT  
		Size: 6.9 MB (6928924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f63ad22972abe9be67391e142c80a78749900a42e1983e02f77b36b6daae4c9`  
		Last Modified: Mon, 25 Aug 2025 23:27:49 GMT  
		Size: 18.2 KB (18237 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6c8a33034fdd31ff65517c2092f45d5c91a9ca11f2d51cff2b6518b3e9d197b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.4 MB (410418806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c87fb6b586e987e5547ea38eef529818ad4258af353f89e4828e498cc9da06`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=21.0.8.9-1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=21.0.8.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:a3bec375112fa06818025bf7b6ee4b903edf4e301e27d2464f104b8aabf964f3`  
		Last Modified: Fri, 22 Aug 2025 17:35:51 GMT  
		Size: 64.8 MB (64801350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da42fd9574b5784d709e992e3af3d845e89cc8404fd9babadbb440e560a6f91a`  
		Last Modified: Tue, 26 Aug 2025 00:50:27 GMT  
		Size: 163.1 MB (163120082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a323a45f09888f2814d96e2e557932e77119607edca89f65600ed9fd6d415ace`  
		Last Modified: Tue, 26 Aug 2025 02:32:15 GMT  
		Size: 142.1 MB (142052902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b5cf7d82bffee02d1a35fdb9ba0e30d10959e77f1680c771dc7bc3e21526f3`  
		Last Modified: Mon, 25 Aug 2025 23:38:53 GMT  
		Size: 31.2 MB (31200842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae99834bfd43d0f1b5a15b62ea769ededac891a0df80a337c7553c9725094bbd`  
		Last Modified: Mon, 25 Aug 2025 23:38:52 GMT  
		Size: 9.2 MB (9242586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c809cda9aa7253147cf5d7641d3e4381063190affd69405389d1c23a6caeaf4`  
		Last Modified: Mon, 25 Aug 2025 23:38:52 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938631617d3ac441e1dacb337d4d6daa868eef122bb86759a9c272d2ab843724`  
		Last Modified: Mon, 25 Aug 2025 23:38:52 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:6746ece900541462b84b3426da84998cc01a09d8d970d29e043a08b751c6e63c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6944708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8c3f095d3770a4b56593898ccd8fba7b39bef066d5f50f78e122b9fb20a454`

```dockerfile
```

-	Layers:
	-	`sha256:a4d43a850733db0d1b1313bbce6e630b8aab06ab2818b6f83a278a29ac41ac62`  
		Last Modified: Tue, 26 Aug 2025 02:27:51 GMT  
		Size: 6.9 MB (6926323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f714a2b497026860bfc8dbea101cf712f52031a12bf5d18d4386a4f8ab1492b2`  
		Last Modified: Tue, 26 Aug 2025 02:27:52 GMT  
		Size: 18.4 KB (18385 bytes)  
		MIME: application/vnd.in-toto+json
