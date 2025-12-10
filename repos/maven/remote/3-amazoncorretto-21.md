## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:d6055d8b69717759ea3723a38bcd3305ca7740e75265b883fc8784bd3ffdfd6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:ea315ce97340f134ac0e181604064d9a04d5c3f3c255e1ad531c9fbddfc59e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.9 MB (439878540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75383c02754867857a0ba50f8b0907ec9a09914e6683b7274854f128588f7dcd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:30 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:30 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:23:21 GMT
ARG version=21.0.9.11-1
# Wed, 03 Dec 2025 20:23:21 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 03 Dec 2025 20:23:21 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:23:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 03 Dec 2025 21:15:03 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 03 Dec 2025 21:15:12 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Wed, 03 Dec 2025 21:15:12 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 03 Dec 2025 21:15:12 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 03 Dec 2025 21:15:12 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 03 Dec 2025 21:15:12 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 03 Dec 2025 21:15:12 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 03 Dec 2025 21:15:12 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 03 Dec 2025 21:15:12 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 03 Dec 2025 21:15:12 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 03 Dec 2025 21:15:12 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 03 Dec 2025 21:15:12 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 03 Dec 2025 21:15:12 GMT
ARG USER_HOME_DIR=/root
# Wed, 03 Dec 2025 21:15:12 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 03 Dec 2025 21:15:12 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 03 Dec 2025 21:15:12 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbb2013f839dc1b3c014b823b3aac80d0e6d67fac06ba1b5ce16eef96069369`  
		Last Modified: Wed, 03 Dec 2025 21:11:38 GMT  
		Size: 165.5 MB (165496684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362143223f6536c18919ff6a416c1a3ce6de2a5dc44a1ab2df5d201b3babbd73`  
		Last Modified: Thu, 04 Dec 2025 00:30:35 GMT  
		Size: 172.2 MB (172157686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4592fd7b17dbe3ea2da062d3a64e3f7d1e7ac4851efb9df36a594d7972f40bb7`  
		Last Modified: Wed, 03 Dec 2025 21:15:52 GMT  
		Size: 30.0 MB (30049977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83375fb19aa241b5f20a3b1144f82f76178824d94461e626ee495e7732ebcf12`  
		Last Modified: Wed, 03 Dec 2025 21:15:48 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bfaba5ebcb4482a479f7fb5007ee0cc18016640acef2c45cd2095a785a4f2a`  
		Last Modified: Wed, 03 Dec 2025 21:15:47 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37dc6379587fe7c8111e676c5318a2c9f396040762da9603d31774da3b8abaf8`  
		Last Modified: Wed, 03 Dec 2025 21:15:47 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:9294106d845f259692b4f55bda86ac15978517bc04d5892171d6469399df35c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6950375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1509c98bcc87621eda32b3b75f969c25a75a107f249bd3591e3452a79fd2a80b`

```dockerfile
```

-	Layers:
	-	`sha256:a78c1dc03b6071b6c070033e7cfb5a252398360a35d5e141452f5a5b873cd794`  
		Last Modified: Thu, 04 Dec 2025 00:28:07 GMT  
		Size: 6.9 MB (6932159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e476d2adfe4daf16a5d1891fde8cbbe21beec34db74c70d3ab144b3f6ed5399`  
		Last Modified: Thu, 04 Dec 2025 00:28:07 GMT  
		Size: 18.2 KB (18216 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c2c60b2a9e2f1cd6d51691bddd2e436a9b91fe91f33571d1d0a2d799a70baf60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.8 MB (416842158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbbfe972a8599d95dd1f46317d25a1d74d955ef4d631f2de71565ead3abea26f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 03 Dec 2025 20:03:07 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:03:07 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:27:26 GMT
ARG version=21.0.9.11-1
# Wed, 03 Dec 2025 20:27:26 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 03 Dec 2025 20:27:26 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:27:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 03 Dec 2025 21:15:30 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 03 Dec 2025 21:15:38 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Wed, 03 Dec 2025 21:15:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 03 Dec 2025 21:15:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 03 Dec 2025 21:15:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 03 Dec 2025 21:15:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 03 Dec 2025 21:15:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 03 Dec 2025 21:15:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 03 Dec 2025 21:15:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 03 Dec 2025 21:15:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 03 Dec 2025 21:15:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 03 Dec 2025 21:15:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 03 Dec 2025 21:15:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 03 Dec 2025 21:15:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 03 Dec 2025 21:15:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 03 Dec 2025 21:15:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ba2b3f44053754feffb2ec7cfa45b66127e117d0d28e5607dbc6e1b6044b97`  
		Last Modified: Wed, 03 Dec 2025 21:41:24 GMT  
		Size: 163.6 MB (163582881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a77fda297d83898a544fd36578087b0825d52adbd2cf31ed0d1809ab214a1b9`  
		Last Modified: Thu, 04 Dec 2025 00:28:38 GMT  
		Size: 148.0 MB (148031509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d990d38037b855065dae79360df8b04436ea76edcd97d48dd369695e37b233e2`  
		Last Modified: Wed, 03 Dec 2025 21:16:20 GMT  
		Size: 31.2 MB (31191345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f73e58e01a34e0e86ca29a42f3969387ccb45d80d800dc86f419ec18b90b9c`  
		Last Modified: Wed, 03 Dec 2025 21:16:14 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22cc5d2568fb3f3c9f22fb98b4d9a1a997a47e51cdcc2f7ef41dccfe20fc718`  
		Last Modified: Wed, 03 Dec 2025 21:16:12 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4941245379ff7d89409efd1ba0cfda709c88a37fa48f06af72f65df3a7b154c`  
		Last Modified: Wed, 03 Dec 2025 21:16:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:542e9caf94316c4d4b5484fc0ddc1763b428203a3934396a734e634b48d08cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6947922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9c09b54585e0fe08f4f6607dbd0083891c7716cc98665535973164ecc5988e`

```dockerfile
```

-	Layers:
	-	`sha256:7bf7052ae5b6fec30c9b553652eb3d7174204b9df95457f536b3acc5d1591c11`  
		Last Modified: Thu, 04 Dec 2025 00:28:12 GMT  
		Size: 6.9 MB (6929558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fc74aa67b9252cfbad5e8cc69339ef3cdc1c8f61f30d5cd861baad8a5946bca`  
		Last Modified: Thu, 04 Dec 2025 00:28:13 GMT  
		Size: 18.4 KB (18364 bytes)  
		MIME: application/vnd.in-toto+json
