## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:686f0f72a6dd524c1b449be7beb44bb2b9906ed89b3b88f53e98ab334a256278
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:39ccb833db2e165306d0e16e66b187ae703c21d345a2b1a427a194e8904592e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.8 MB (426796080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3bcaf6102adb16485e3a1e8b5140d8a07942ea1a82affac03c6642a65dba922`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:59 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:59 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:15:47 GMT
ARG version=17.0.17.10-1
# Fri, 14 Nov 2025 02:15:47 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 14 Nov 2025 02:15:47 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:15:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 14 Nov 2025 03:18:12 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 14 Nov 2025 03:18:20 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 14 Nov 2025 03:18:20 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 03:18:20 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 03:18:20 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 03:18:20 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 03:18:20 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 03:18:20 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 03:18:20 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 03:18:20 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 03:18:20 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 03:18:20 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 03:18:20 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 03:18:20 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 03:18:20 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 03:18:20 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2eeedbb6c19345cead693cc54b4ab6b968c029966c1439c8e1b1921ecaed2c`  
		Last Modified: Fri, 14 Nov 2025 03:14:58 GMT  
		Size: 152.4 MB (152415922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6365e26c7ba16ab6e63580cf4e62e1b0f0cd1f048211f78e464bd0a482c00879`  
		Last Modified: Fri, 14 Nov 2025 06:28:11 GMT  
		Size: 172.1 MB (172146050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50f94139ffac2c16f37e142c71a6d472d44fc5d7bd6039507e0b73e97340510`  
		Last Modified: Fri, 14 Nov 2025 03:18:58 GMT  
		Size: 30.1 MB (30059926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16dc55cf4bc0558e23b937742243d91ea1e5a0351a8fd990e66beed932a3eff`  
		Last Modified: Fri, 14 Nov 2025 03:18:55 GMT  
		Size: 9.2 MB (9242570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1606865b283fd54080b9820650084c9b75ba9fbcdd072ee698e2b505ab2e45`  
		Last Modified: Fri, 14 Nov 2025 03:18:54 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b021e63131ccf0804e6000248944d158db62811343f34c8759119b5ac940378`  
		Last Modified: Fri, 14 Nov 2025 03:18:54 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:43dbacae6f9a45055101f1796b93fb4fa60c4f05fa3f4b2c8ca51b12a8305b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6950456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa6cf678bef1e5929b2bfad26a81d8f0f1893f25dc0fd15e68bd8740891cee59`

```dockerfile
```

-	Layers:
	-	`sha256:4e2dcd101d69eb96730221058ee345c33cd540079858ddf615b889f04e108c8a`  
		Last Modified: Fri, 14 Nov 2025 06:27:53 GMT  
		Size: 6.9 MB (6932262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92be807b6b5b4fa42ef718f01994f0c7d27ade14fc33d674deaaa15f9e3cefea`  
		Last Modified: Fri, 14 Nov 2025 06:27:54 GMT  
		Size: 18.2 KB (18194 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b5bc31a499eb5ac716c9e21ce136e049387846a880d990b52c8ad712bb701243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.2 MB (404245559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f2d25a73d1abe41cddfdadc905ace2a475ee9110cbfc9415c1325bf6ef731e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:55 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:55 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:17:17 GMT
ARG version=17.0.17.10-1
# Fri, 14 Nov 2025 02:17:17 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 14 Nov 2025 02:17:17 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:17:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 14 Nov 2025 03:18:17 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 14 Nov 2025 03:18:24 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 14 Nov 2025 03:18:24 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 03:18:24 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 03:18:24 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 03:18:24 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 03:18:24 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 03:18:24 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 03:18:24 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 03:18:24 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 03:18:25 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 03:18:25 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 03:18:25 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 03:18:25 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 03:18:25 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 03:18:25 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b8742846c34daad6dea6d70c9dbb64562941f5ec5c46f8d2eb1e6eb5241816`  
		Last Modified: Fri, 14 Nov 2025 03:15:35 GMT  
		Size: 151.0 MB (150987992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece9e2e6ee44c49e902e212d37e2db208881fd80273ec7037ec02266661025eb`  
		Last Modified: Fri, 14 Nov 2025 03:18:51 GMT  
		Size: 148.0 MB (148024030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f4f4152f96025a7f66c031c09539012306093399d74d763ef73134979deb10`  
		Last Modified: Fri, 14 Nov 2025 03:18:59 GMT  
		Size: 31.2 MB (31197100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21a33f29ac657c0c6d22f2f98534113f4e7ea512d73ab07d943654808f6d1a5`  
		Last Modified: Fri, 14 Nov 2025 03:18:57 GMT  
		Size: 9.2 MB (9242595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d9078c02c266fb58856891ff745c5713e9a014e3b28931c656f01b944c04f2`  
		Last Modified: Fri, 14 Nov 2025 03:18:56 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39154bfa97eea1c98b9aec05077b61e6b4cabd3c78f549dc9709b00883a2223c`  
		Last Modified: Fri, 14 Nov 2025 03:18:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:f618bd9ae41891eb48d87c9188b3fc1f26016bad9af022b60d94f1e4f88e33cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6948003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9394f493e7ce08159beb3e18ae56251d8293a33edda9fc7993fc59ec4539d94`

```dockerfile
```

-	Layers:
	-	`sha256:3462858f8dcacb6f7db6d57015105d1377be7b483e19926ff2a2eb50861cdd78`  
		Last Modified: Fri, 14 Nov 2025 06:28:00 GMT  
		Size: 6.9 MB (6929661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c19d889a6f174f8803dbba0126b94b3bdaaf3df25aab1bb29063e7e088867049`  
		Last Modified: Fri, 14 Nov 2025 06:28:00 GMT  
		Size: 18.3 KB (18342 bytes)  
		MIME: application/vnd.in-toto+json
