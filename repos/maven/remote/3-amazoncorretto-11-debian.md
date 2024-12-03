## `maven:3-amazoncorretto-11-debian`

```console
$ docker pull maven@sha256:ea30d45680500ea86054bf56a26a4974fa5f5fcf6c25e8d419063565a6354d61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-debian` - linux; amd64

```console
$ docker pull maven@sha256:2f851bcefe204fc6ce87ca25d614252c71820ebb8f6c6329eeabb467864e85d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241039190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489599b80cdb3b621861910b50402bb982d72fbfe323a9265e17b4b0b96c6960`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e11debf78de43968ae31d1b37ae6b0aac2fbed6faaf7ecc7b3cb72c9bce8f2`  
		Last Modified: Tue, 03 Dec 2024 04:33:40 GMT  
		Size: 203.6 MB (203636145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3854c6892d8a38ac6ba68519824320389e71c64564de7c6a27ceca70031d986`  
		Last Modified: Tue, 03 Dec 2024 04:33:38 GMT  
		Size: 9.2 MB (9170429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3f9a3de807d624741f84add53cdae924106f5538366aef061e14f3c0fd5d59`  
		Last Modified: Tue, 03 Dec 2024 04:33:37 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af203b7d08c7cf5f91edef156cf381d5c2e798553d56421bdde1e5714df0dd28`  
		Last Modified: Tue, 03 Dec 2024 04:33:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian` - unknown; unknown

```console
$ docker pull maven@sha256:bda9d80857955009e820e88ecf9739b7199140cd4f2ade0cafeb2a1edfe0236b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3023879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815f0b97bcf0143feda0141ccb8522b1df88908950259cb7bf551c2c9653b008`

```dockerfile
```

-	Layers:
	-	`sha256:f0f19fc29cc02b9f902155dea497ea603ba8f704d5059a9eef2de714006fd827`  
		Last Modified: Tue, 03 Dec 2024 04:33:37 GMT  
		Size: 3.0 MB (3005198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf59fa4299883f8c1e1975ba231d1b4cc693ff3ee67215cf3601236d5463a7f`  
		Last Modified: Tue, 03 Dec 2024 04:33:37 GMT  
		Size: 18.7 KB (18681 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:e34ddae0108044b993d78773b42a5390989a595011dac23553e65ae5fcc78676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238928314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9dc6903ec0f56dc83201bd9451e1632aa4d0c3af741b4532fb24c9230b6075`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ae32073da5bb68a4d7bd392a247372ec74859050d71c38c816eaecd8e25d80`  
		Last Modified: Sat, 16 Nov 2024 07:44:59 GMT  
		Size: 200.6 MB (200599491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0ea49961f3d0d89186d53f21df609967a13ba25445be7d8767c97ffd98a1b5`  
		Last Modified: Sat, 16 Nov 2024 07:44:55 GMT  
		Size: 9.2 MB (9170432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dba31097ae033810e31ff36e8da4a796db16251caa179f7963ceea6446824b`  
		Last Modified: Sat, 16 Nov 2024 07:44:55 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04fafebebef88287196dd263e933ba859536ca3073d34d82a0ee8bdf345d4a9`  
		Last Modified: Sat, 16 Nov 2024 07:44:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian` - unknown; unknown

```console
$ docker pull maven@sha256:bdb7836444f6f3dc890844cf86f35685fcd416586b4c90931e7fef1d354a82cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3025593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5916e0b2c80d78b47e3d2ed007337b263ae1c654cdb4910197d3ac0dbf4422e5`

```dockerfile
```

-	Layers:
	-	`sha256:0884f996eb50d05eaa8c2ee3a812cd2e2cd42a90e18c8ff9d36dbe655d83b89b`  
		Last Modified: Sat, 16 Nov 2024 07:44:55 GMT  
		Size: 3.0 MB (3006742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07a90b3f1bffcee010849a80e9fd5bd367da2c849494e853993cfa8b5880a638`  
		Last Modified: Sat, 16 Nov 2024 07:44:55 GMT  
		Size: 18.9 KB (18851 bytes)  
		MIME: application/vnd.in-toto+json
