## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:4e032073ff62f7b35211ebe4546aa9f93916de3ee2a9a4832b510b6e081bfcb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:c131e52266020dd9a3a8de284bbcf36bb1322beb887bfb379125e2cc3427060e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.7 MB (424716014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9881327e5281100a0b8058b04df49af1eb6037509a9fbfcfc743def4c9b699aa`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=21.0.6.7-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=21.0.6.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:df4e5b00f72c04406d50eed4e27aff00b665ec05fda916e7c0dbd80e3726202c`  
		Last Modified: Thu, 27 Mar 2025 23:58:46 GMT  
		Size: 164.8 MB (164801153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bc2e8da521659ad1ab35c9826473a1cabc2490e6903cf076e1f93dc27d8a60`  
		Last Modified: Fri, 28 Mar 2025 00:08:46 GMT  
		Size: 157.9 MB (157920106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d8de559f72f827ab5178722e692a1d83b32988d274c3c1f5426d240ad83f12`  
		Last Modified: Fri, 28 Mar 2025 00:08:44 GMT  
		Size: 30.1 MB (30070386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d95ea9571d93ff48298613379256070d9320c5b557eb423b6e21f297fa7e98`  
		Last Modified: Fri, 28 Mar 2025 00:08:43 GMT  
		Size: 9.2 MB (9170437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f1f28384dccf9e8434f409d307c7948e86a8fbd6741243b7cf718f8d4174da`  
		Last Modified: Fri, 28 Mar 2025 00:08:43 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca93d95088ff0e3ec7a23de0354fae61ffe07fcc56ec1d4fda38df51a7b816f3`  
		Last Modified: Fri, 28 Mar 2025 00:08:44 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:e72decdd737b240152785309ad5b9b83ccf3bb0b4adad95c28ad65769edd1538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6925290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d0623b7534b0de505511fb910f2e0b97d255bec2ef57569c365362ae656185`

```dockerfile
```

-	Layers:
	-	`sha256:43f8dde2cfe4c1466bd27d2cbfdb1b06b4609ef39eb9f03e3649a6cddf284277`  
		Last Modified: Fri, 28 Mar 2025 00:08:43 GMT  
		Size: 6.9 MB (6907062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd9fb4d6f78d903efb1ca318f6485422416bd9528a186179ef3ed9624ce72099`  
		Last Modified: Fri, 28 Mar 2025 00:08:43 GMT  
		Size: 18.2 KB (18228 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f3ac7c4e8359f3bc0892d01c431970dce6920965e2068089bf45230e6a634aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.7 MB (401720613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b58436ba5c69ed86d436164105927f09bbe97db5d7bf7038334b58650fe69f5`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=21.0.6.7-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=21.0.6.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:c02c8c8bc977637eecad4ad82b0d7f078cd804f97adf048597fe2186066e830e`  
		Last Modified: Fri, 28 Mar 2025 00:19:35 GMT  
		Size: 162.9 MB (162868002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ff3e50332d509d7597e23c32b0c556fb85f815cd88ae51150b581bf6d2a3c7`  
		Last Modified: Fri, 28 Mar 2025 01:44:13 GMT  
		Size: 133.9 MB (133931680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471d8ddb6c5684e970da776816796e18a058618f726548a39c9ffc31654ef3ca`  
		Last Modified: Fri, 28 Mar 2025 01:44:10 GMT  
		Size: 31.2 MB (31183638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bccfa27231cb44f2a16525b7d4bd62c03c1639886250e29797b418628052ef`  
		Last Modified: Fri, 28 Mar 2025 01:44:09 GMT  
		Size: 9.2 MB (9170432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb6fd579bcb7c3e48b2463ce1095692d44af64b2647bf47bdadb1289e988df1`  
		Last Modified: Fri, 28 Mar 2025 01:44:09 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ef73f8d2fb6f6fef7990615f0946f3031c18abd40062b1bc92c2b661d6cded`  
		Last Modified: Fri, 28 Mar 2025 01:44:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:9ad8ecef57ead9af29850b3b739cb334bf9d05d9dbbb8847b35c51dd30969d6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6922838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea153bb630a189333d52c2912eb29279a0731c3633f5d53c28ae15385db2b72`

```dockerfile
```

-	Layers:
	-	`sha256:ca29c66f7a411be4070e5f7fc9d8b8a5cc36150b5c81e46e9504e423b949fd78`  
		Last Modified: Fri, 28 Mar 2025 01:44:09 GMT  
		Size: 6.9 MB (6904461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc4e64a5945cef15273f089a50f136cea93f3fbb25fcc0b95e63bed3f8ed326f`  
		Last Modified: Fri, 28 Mar 2025 01:44:09 GMT  
		Size: 18.4 KB (18377 bytes)  
		MIME: application/vnd.in-toto+json
