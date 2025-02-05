## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:8cf258b669129504e217caa1cb689848b2cf435834fb2ef84a397318c7f5d602
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:638b6dd52c5d681236ecdb74a23cbb1c8fe5dd7d36da63158a6e60d4bfdf10d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.2 MB (404210397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47149387604c5d52f8fb70e06279ea639fbe253caf46d541419879c2e9f30780`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=11.0.26.4-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:b6252bf1f0f9b41e2a8f6374a8a252f1ae25a67239bcc02d43af3b859d1b4c3d`  
		Last Modified: Sat, 25 Jan 2025 04:14:29 GMT  
		Size: 62.7 MB (62669455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a915f6a9013dcc7d789628238b94f837415410b738bac0f918a7f1dfa8e86be`  
		Last Modified: Sat, 01 Feb 2025 01:08:39 GMT  
		Size: 148.2 MB (148181339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf227ea59db7ff774b47824ddda3620e8a66e8081e0cc40db150c22f5fb2c4d`  
		Last Modified: Tue, 04 Feb 2025 06:15:33 GMT  
		Size: 154.1 MB (154121305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf83f37d2ebcd05a3dcb57e69a0889f4e7376f9f502e8dd8d7cbc3d052c53c6a`  
		Last Modified: Tue, 04 Feb 2025 06:15:32 GMT  
		Size: 30.1 MB (30066820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fc93c650392059818ad6acdf3001b247a5167ef27727117326e5146d3cd879`  
		Last Modified: Tue, 04 Feb 2025 06:15:31 GMT  
		Size: 9.2 MB (9170434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1361217a1bdb9b20af009d625a91c2987978df11200e136960e97d06d9a69e1a`  
		Last Modified: Tue, 04 Feb 2025 06:15:31 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6966b198cc8e429194e002327ea71cdd5649064b984be9faf41812f6479093e4`  
		Last Modified: Tue, 04 Feb 2025 06:15:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:4579d49da85ec4df72c57a836fe36610b51f3028f1cf46671e18e1c232e3b137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6932696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebc28fbe6a43c84e84e13659e8a4ec0a103eaf504bf50b703af2c0319d1024e`

```dockerfile
```

-	Layers:
	-	`sha256:df9fb66838009228301c3e976748f19870f11ec60e57dcf0e00135014a459485`  
		Last Modified: Tue, 04 Feb 2025 06:15:31 GMT  
		Size: 6.9 MB (6914466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad807ad901b420644fb23efad92ae90a86b7d79e837c1e8271ce9b2e192d030f`  
		Last Modified: Tue, 04 Feb 2025 06:15:31 GMT  
		Size: 18.2 KB (18230 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:98fdf38662990b7aedb4836edcb6f36cc4ee6ceb198dff6283c3d9d6af9b9f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.3 MB (381323602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70cae78706eda3c3e8999a799d54ef8a84bed2dc040119eb5ecc4ea30db9369b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=11.0.26.4-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:e694aca9e8d5c223f3e2469e032276879ab4b403abc21549d4277f4463b2974b`  
		Last Modified: Mon, 27 Jan 2025 15:17:25 GMT  
		Size: 64.6 MB (64578423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e8904a985d69287eab1fab568d78d1bb01a93fa4abef3da47a0d9d5d2d39b6`  
		Last Modified: Sat, 01 Feb 2025 02:11:11 GMT  
		Size: 145.3 MB (145288456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945d290d6bcc4ed8913fa9a088c0a56d16b94bc2f996fceef4c5bba41a53413d`  
		Last Modified: Wed, 05 Feb 2025 14:15:01 GMT  
		Size: 131.1 MB (131107285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e819741f062e7224dfec5934a9f590303b63e4a104130df40cf3379d029de228`  
		Last Modified: Wed, 05 Feb 2025 14:14:59 GMT  
		Size: 31.2 MB (31177966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5372fc9192c573f407971f24eb121e442a25cefb96a133163937dea4c7426f7`  
		Last Modified: Wed, 05 Feb 2025 14:14:58 GMT  
		Size: 9.2 MB (9170430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3351c6d5fcd8e4e660414aa45c1cc0d8b5ad3b3cac34de1f3a84e3469a79bb35`  
		Last Modified: Wed, 05 Feb 2025 14:14:58 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6397f3d83edcd303c1da382f606677eb55fb4ac8b3c1f00e0535ce10570a7c`  
		Last Modified: Wed, 05 Feb 2025 14:14:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:c3547cd8e52dc24b0b51fec82b8856653827f00fb691b35b1e0784b99aecf271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6931048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91bc48e703dc2d621b818f3626153776841a088cc8a41854b57befa765c3cfd4`

```dockerfile
```

-	Layers:
	-	`sha256:f35ac936644f922036045bb4e1253042049176814b7f9d0f60ecae9dad664eac`  
		Last Modified: Wed, 05 Feb 2025 14:14:58 GMT  
		Size: 6.9 MB (6912670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a649fb771a7f71397488036b624e57f55cbc08f4990df2ed17089b89f54874e`  
		Last Modified: Wed, 05 Feb 2025 14:14:57 GMT  
		Size: 18.4 KB (18378 bytes)  
		MIME: application/vnd.in-toto+json
