## `maven:3-amazoncorretto-21-debian`

```console
$ docker pull maven@sha256:6458758c89ea859e0fcbfba63fd9969f9304ef2447b52f0768e01507917fa93c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-debian` - linux; amd64

```console
$ docker pull maven@sha256:f471a9f73cb1a9fc9601ed046b902f1f8d13bdcc03ad7dde608f5a3783116fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.2 MB (255225445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec65f54d86d29fd60505019cf0abf333088a345722e6cf33de1e266ae0af5d1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0c8268832ab563752bf82537b21f916b61e13c7361bc3f152ac101a85d2bf5`  
		Last Modified: Thu, 24 Oct 2024 02:56:09 GMT  
		Size: 216.9 MB (216927675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2512f9da23fed72b2fb0846788e4f52c3d758ce95342d08a524a925aa3a298e4`  
		Last Modified: Thu, 24 Oct 2024 02:56:01 GMT  
		Size: 9.2 MB (9170446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789861e233aa3e8daf90ed98933e9a195e0a1db23e49e5a1d0afbf79c1a230b8`  
		Last Modified: Thu, 24 Oct 2024 02:56:01 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd453c4669e99eaaf1db9697d0f55b3810eed1af4237b69ed65afa644f7e011d`  
		Last Modified: Thu, 24 Oct 2024 02:56:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian` - unknown; unknown

```console
$ docker pull maven@sha256:d1dba6d4edfb707bb98d6820382407a10c3f4330306de3bfb63ec5a6ed78680a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3019030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72036d4a2b47d95c9cffb596b14704bdb1da3d5a883c6c594ca4a9ab167ccf7f`

```dockerfile
```

-	Layers:
	-	`sha256:781682e73950cb47d512d31f6ab1d5aac1e524d5c5161511e76a93684fe25302`  
		Last Modified: Thu, 24 Oct 2024 02:56:06 GMT  
		Size: 3.0 MB (3000545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:368dec69ad48ed8b93c88acc2669d85afa96fe5f1ee7c7e15f6d8198a9b45c55`  
		Last Modified: Thu, 24 Oct 2024 02:56:06 GMT  
		Size: 18.5 KB (18485 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:4c0740d1bfceae5357f9eb57b803ff0928ae1e647a6ba2bac6dcfd110391b8ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252991500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3bc494fda9252e857a5187a2ada9740377379c07008c4b63e22eaccd9ab1bb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:02043084621ff842ae4213f878cb58bfe7e0846b07b91d20eab0eb7ca4031daf`  
		Last Modified: Thu, 24 Oct 2024 13:26:59 GMT  
		Size: 214.7 MB (214663680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62019676ec05140e3081e365604867d49b81985f80075508281b734a2ecf1420`  
		Last Modified: Thu, 24 Oct 2024 13:26:54 GMT  
		Size: 9.2 MB (9170444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b24e858ca8df597d3a5acce5c91a52856ae3a4e837627e597cae4da8cd2618`  
		Last Modified: Thu, 24 Oct 2024 13:26:53 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4deb8168bd1bd58eaf8aaa9e3e5eb46a6dd8e80e7c281e958fe7fe49a3e0115`  
		Last Modified: Thu, 24 Oct 2024 13:26:54 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian` - unknown; unknown

```console
$ docker pull maven@sha256:3ba9da9dc19b722af9665c780bae7299e9137e4d8105dc1a16dbe32e00322191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3018887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5574ca71b3f8cd097a01ad6bea5ee0bb70a2387da2b1a061362a00728f446879`

```dockerfile
```

-	Layers:
	-	`sha256:e7fd1d08f148858cc9e3e3b438a5ad4442e947d2e2b60de44922d6a98fb7f211`  
		Last Modified: Thu, 24 Oct 2024 13:26:54 GMT  
		Size: 3.0 MB (3000203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2d276077c3c4bc220e3b41ce723017496c670ff2b5996226ed1c06226aa0b35`  
		Last Modified: Thu, 24 Oct 2024 13:26:53 GMT  
		Size: 18.7 KB (18684 bytes)  
		MIME: application/vnd.in-toto+json
