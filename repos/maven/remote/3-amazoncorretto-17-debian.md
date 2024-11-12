## `maven:3-amazoncorretto-17-debian`

```console
$ docker pull maven@sha256:f952de7b40e28d9b310804db3f5788b72bb6c94333b44ef805e411cdd8bb8249
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-debian` - linux; amd64

```console
$ docker pull maven@sha256:f6d427378f240a23c061f3333586c18694c566deb6d18fa6551b0d757c9c5bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (240012578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37bfd7b7cd0396f9847bff92c0402c514fac1040f8f964ddaff601e1d3e82a49`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf43ca87cd126a9ff7d9e7c1ed07cb3f2d8f61eb97030ba532c027125728ec9`  
		Last Modified: Tue, 12 Nov 2024 02:51:14 GMT  
		Size: 201.7 MB (201713123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7593837df5d3e1d21345be56865ba081dc01cfac6a5942c2a31938b53c715f7b`  
		Last Modified: Tue, 12 Nov 2024 02:51:10 GMT  
		Size: 9.2 MB (9170424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a1a9d323ca14d52adcbea9a26e4076fb1e8fa2c1f30e881887b6a0610ffeae`  
		Last Modified: Tue, 12 Nov 2024 02:51:09 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d0a47756fdc6ca0a53d3b47db0d648a5b9315d01c4c967bea605e520f43375`  
		Last Modified: Tue, 12 Nov 2024 02:51:09 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian` - unknown; unknown

```console
$ docker pull maven@sha256:5a7608cd6c38c148fe838b73af7dc59e15f83b3a8de6e29ac9e603ad7f8619cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3019328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd1ff2c406b9585178efc5d2f37ef87b19019ecc8043a8ab1df44b578474d5f`

```dockerfile
```

-	Layers:
	-	`sha256:d576619a1ae1336042064520d69cef7154c99b62d0a2bc872ae6f65c2f036df5`  
		Last Modified: Tue, 12 Nov 2024 02:51:09 GMT  
		Size: 3.0 MB (3000646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aefa708c2fedfb22b314bdec429738e9a5dbe2f7000fd4e70428850e064b1576`  
		Last Modified: Tue, 12 Nov 2024 02:51:09 GMT  
		Size: 18.7 KB (18682 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:414bd2a04057e546ba1d77de3ff5acc926435ecb1917cb3543858fcb321fba1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238341052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65f960946d6b54bebbc9c9cde329cab0cc61eda0145d9c04d0c4d4846b2f61c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c487667db4f9024e18dbdb5afacb0d3f76993b084bcd7a076d61f1dd500f381`  
		Last Modified: Thu, 24 Oct 2024 13:22:28 GMT  
		Size: 200.0 MB (200013240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e46d338696aa5f5118b22349e37ffe1e97f66a482c2ecbb2084b25eab3c8c6`  
		Last Modified: Thu, 24 Oct 2024 13:22:24 GMT  
		Size: 9.2 MB (9170436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ba424a494818ef230e9a0c6639185b0876e980cc9254267cabf553c98f6ec9`  
		Last Modified: Thu, 24 Oct 2024 13:22:24 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f58826a581e0877244362d56999a972dbd9c0eff7dee3648707434e1100c256`  
		Last Modified: Thu, 24 Oct 2024 13:22:24 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian` - unknown; unknown

```console
$ docker pull maven@sha256:1cba5e19ac02d8ca821dc7e101edd4c566e4c033a2bff3ce34c302f8df277d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3018989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df331882a394043e5b38029ef2f29bb6330affa6912e16f0b95b3dd2e7b9eb4`

```dockerfile
```

-	Layers:
	-	`sha256:a2693425d97c9d31fcb894d2f42125923b8dfbb2f3a63c60a33fd9faf67dce9c`  
		Last Modified: Thu, 24 Oct 2024 13:22:24 GMT  
		Size: 3.0 MB (3000304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:815fa04c52cdbdad31966c98d9387048c1525386d953ebb229746e09b03551e0`  
		Last Modified: Thu, 24 Oct 2024 13:22:23 GMT  
		Size: 18.7 KB (18685 bytes)  
		MIME: application/vnd.in-toto+json
