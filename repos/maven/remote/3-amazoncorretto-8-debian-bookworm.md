## `maven:3-amazoncorretto-8-debian-bookworm`

```console
$ docker pull maven@sha256:6dd183e3215ffa24ec20e2471c6247b971daa22a6ff2f9665cc600d4f6da5308
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-debian-bookworm` - linux; amd64

```console
$ docker pull maven@sha256:66a2c5d85e017d228cddea23942fe6e4093ab887c349c06926bf818182d2c6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164466104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e11f5de70b42645b5e29d19a30b76ce40fc070a9ae309752d595765766fa2ebb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60fd0d1825006fd738319cebb1aed7c509a848301806ab66bc10c452ac6d9057`  
		Last Modified: Sat, 12 Oct 2024 01:56:38 GMT  
		Size: 126.2 MB (126168359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10ba3c7f538ada4889f311cda8ae2283da2219d8f1b3fabe467306921e9c64e`  
		Last Modified: Sat, 12 Oct 2024 01:56:37 GMT  
		Size: 9.2 MB (9170432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735eda0dd2fe4eee88b97a5157d0e74da2c9d444b06baf30ddffa623b213399e`  
		Last Modified: Sat, 12 Oct 2024 01:56:37 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4489c943ac2f0943981d4aa9db3154ef0a9829fad8be59ee2503826c305b7a0`  
		Last Modified: Sat, 12 Oct 2024 01:56:37 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:12476a60fc3ad74e78edbd5f674fd6f4064400be146d8a036d1e247761951256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2877816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eccf46496e022a078a8080a7dbf484dd81aa285416dfab081fab020e6d7ab186`

```dockerfile
```

-	Layers:
	-	`sha256:ff955adc88007f060ebbf3e4f1f055a0175d562028ecf9093fc5a7cf6e6dd7a7`  
		Last Modified: Sat, 12 Oct 2024 01:56:37 GMT  
		Size: 2.9 MB (2859318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0151e92049d7e6bf601bced740f870e2e343606927ef7b6830652d7205ed9dcb`  
		Last Modified: Sat, 12 Oct 2024 01:56:37 GMT  
		Size: 18.5 KB (18498 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-debian-bookworm` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:7368ea1e6d4880d591ab58ffee09340ff464b1bfdadedbcf39c186558a387077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148260744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b83b9eb11fd5b2921600050ac2685f53bf8f760ad7e90a99f8ea63db08c09a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e8c215cd31bfc9a8dc34b5e778ffc925b1a3aa775f18c04003720bfa9498b0`  
		Last Modified: Wed, 02 Oct 2024 07:12:33 GMT  
		Size: 109.9 MB (109932902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9053726f77de71a0a8b3ca80ab5714fbc35c98f59e1392086c00767edc32e1`  
		Last Modified: Wed, 02 Oct 2024 07:12:30 GMT  
		Size: 9.2 MB (9170437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae6f18889f86a3bf6373a88ab8b12bb83985d0c4712fb748ba9515772fbe160`  
		Last Modified: Wed, 02 Oct 2024 07:12:30 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f1b543837b84d70d69372f51b0b31cf445250e9a26372d93ff970e1f82b99b`  
		Last Modified: Wed, 02 Oct 2024 07:12:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:f6c579eaa2440ce76be0e705769dc1d4098e19166cbb03871e96d442b6ef2f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2860858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08cece1f402a38cdddd7da4b0deb5361ef3ec3bdea7462aa866aa41e04f6dbf`

```dockerfile
```

-	Layers:
	-	`sha256:ae8cbc921d50add96c600355b5e400cec94140c8aec151d12ca4722753b51935`  
		Last Modified: Wed, 02 Oct 2024 07:12:30 GMT  
		Size: 2.8 MB (2842164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02a1bfb075266b215690253c1b5088e8f04ff90c173e2bb7280a2e19d2e28cb6`  
		Last Modified: Wed, 02 Oct 2024 07:12:30 GMT  
		Size: 18.7 KB (18694 bytes)  
		MIME: application/vnd.in-toto+json
