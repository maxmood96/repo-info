## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:64f0286fe84911627e35769b01077e130c029f663403ff56da9f609089baeed6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:d0afa2bc92f55badec752e6e548cd1f1bf45f3a364134247876a38768409e9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.3 MB (425263019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108e0e43bd05c0392941ca4c9ed2796abe0d4c40700047ba5d4873a5b503ed80`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:03 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:06:40 GMT
ARG version=11.0.30.7-1
# Wed, 28 Jan 2026 04:06:40 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 28 Jan 2026 04:06:40 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:06:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 05 Feb 2026 23:29:27 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Thu, 05 Feb 2026 23:29:36 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 05 Feb 2026 23:29:36 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 05 Feb 2026 23:29:36 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:29:36 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:29:36 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 05 Feb 2026 23:29:36 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 05 Feb 2026 23:29:36 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 05 Feb 2026 23:29:36 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 23:29:36 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 05 Feb 2026 23:29:36 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 05 Feb 2026 23:29:36 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 05 Feb 2026 23:29:36 GMT
ARG USER_HOME_DIR=/root
# Thu, 05 Feb 2026 23:29:36 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 05 Feb 2026 23:29:36 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 05 Feb 2026 23:29:36 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340cef2339d12ec141de515488553d7e4c289a0b47b24df9b035a69e2a865b72`  
		Last Modified: Wed, 28 Jan 2026 04:07:00 GMT  
		Size: 148.1 MB (148131156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b765990ff913936fa77aabc8e03be4b6b2cd6a5a960ea323ba730815b68c13f`  
		Last Modified: Thu, 05 Feb 2026 23:30:08 GMT  
		Size: 174.8 MB (174776705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ebf148babfe2de41f51b3340808c3ea9aab0658da300e8183340e2c6a06260`  
		Last Modified: Thu, 05 Feb 2026 23:30:03 GMT  
		Size: 30.1 MB (30078168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b840e170841eb4605cdbaff560cb8b3fd6cff4e9c7f6d316e2886a8f9f48721`  
		Last Modified: Thu, 05 Feb 2026 23:30:02 GMT  
		Size: 9.3 MB (9312239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76aecaf9620179fb5bfa2a001844f6867fa98a36ba75f36063df63df57b90b9e`  
		Last Modified: Thu, 05 Feb 2026 23:30:01 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f21a2ddb95bdb434b8dc0d6fc934f7716412cac787c65be62851073c3811a6`  
		Last Modified: Thu, 05 Feb 2026 23:30:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:66d84604d35bfd8d019f71122c105afee9c5238a72a365e3d4468a0fac8035d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6957759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3862e96ae6fc6661fcaca9e5041f3b1a8df6d1e51ba70ec3dabed37545bc2ccb`

```dockerfile
```

-	Layers:
	-	`sha256:92f8f67fa24207c832a24dd4e71242c829dcfb0a585546949dcc508cf0b67a8b`  
		Last Modified: Thu, 05 Feb 2026 23:30:02 GMT  
		Size: 6.9 MB (6939566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df66b1207fb8dd5373646d7a99d5b22ac7c5f776f83e23b94bb5116f4ffc530e`  
		Last Modified: Thu, 05 Feb 2026 23:30:01 GMT  
		Size: 18.2 KB (18193 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:9ba5b4f2902d0c93f08352615e67ad9be6e3b49f0078ca849fb6a7c300c406df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.0 MB (400955967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d045aa8fb5038f09cbb953988e2e5e6a679d3ed60e88c31808975c66fc2302c5`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:05 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:27:08 GMT
ARG version=11.0.30.7-1
# Wed, 28 Jan 2026 04:27:08 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 28 Jan 2026 04:27:08 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:27:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 05 Feb 2026 23:40:20 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Thu, 05 Feb 2026 23:40:29 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 05 Feb 2026 23:40:29 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 05 Feb 2026 23:40:29 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:40:29 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:40:29 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 05 Feb 2026 23:40:29 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 05 Feb 2026 23:40:29 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 05 Feb 2026 23:40:29 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 23:40:29 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 05 Feb 2026 23:40:29 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 05 Feb 2026 23:40:29 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 05 Feb 2026 23:40:29 GMT
ARG USER_HOME_DIR=/root
# Thu, 05 Feb 2026 23:40:29 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 05 Feb 2026 23:40:29 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 05 Feb 2026 23:40:29 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c848e8ff28e37232003d119f3814367e3bd0c965552f4ce08dfd6f5d55ede073`  
		Last Modified: Wed, 28 Jan 2026 04:27:29 GMT  
		Size: 145.2 MB (145224227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975461052011cb5d9b209806888f8b27eda8e1b34dac1d53ab744276ac7d6855`  
		Last Modified: Thu, 05 Feb 2026 23:40:56 GMT  
		Size: 150.4 MB (150416491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d324c63fd9f001798d9de944e8eb8e5931e2c625a46f6fd816abb53ebdb38d4`  
		Last Modified: Thu, 05 Feb 2026 23:40:54 GMT  
		Size: 31.2 MB (31203069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7761cfd9999ec6f5b3d885d1b30c35296d3e92865b1efd06549816e31e7b5ab4`  
		Last Modified: Thu, 05 Feb 2026 23:40:54 GMT  
		Size: 9.3 MB (9312251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed106c08a6213db8138d025767ee79e596e6966f274b9728c100d412f9137595`  
		Last Modified: Thu, 05 Feb 2026 23:40:53 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59df3bd5dde8776810c178c95e80d2677e0fdb5d6eb4f7c1c9f7e10cb59b877`  
		Last Modified: Thu, 05 Feb 2026 23:40:54 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:391c782147536ccaf3a815822803696f4a183bc7bdbc318be67c43731b01987c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6956112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce8706e7286e08d8f9a84aab8d30e3dcdfd3e21b5cc9f547221a753684f76fe`

```dockerfile
```

-	Layers:
	-	`sha256:7a3f60321b8d524497c3174f131caf7ba651a20d59f7220ef651ab6fb922adef`  
		Last Modified: Thu, 05 Feb 2026 23:40:53 GMT  
		Size: 6.9 MB (6937770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fe6b929d8b4143ba8e30e9245cc44f2c0d9c4f16bf1952219e48b6919221365`  
		Last Modified: Thu, 05 Feb 2026 23:40:52 GMT  
		Size: 18.3 KB (18342 bytes)  
		MIME: application/vnd.in-toto+json
