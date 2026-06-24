## `maven:3-amazoncorretto-11-debian-trixie`

```console
$ docker pull maven@sha256:949a4312c288ae62e40f939b0f175912ad3f03bf4319ad0570063ce7fa99b45a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:3a2506a5604793da7feb42be34f27d9bc50da72183fd26a47d6a6087098b1e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241896508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:135cfd39afb39c51069d3cbbc833b592be3817daa8b0aa1281260e658d2731a5`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:24:27 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:24:27 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 02:24:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 24 Jun 2026 02:24:27 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 24 Jun 2026 02:24:27 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 24 Jun 2026 02:24:27 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 24 Jun 2026 02:24:27 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 24 Jun 2026 02:24:27 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 24 Jun 2026 02:24:27 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 24 Jun 2026 02:24:27 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 24 Jun 2026 02:24:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 24 Jun 2026 02:24:28 GMT
ARG USER_HOME_DIR=/root
# Wed, 24 Jun 2026 02:24:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 24 Jun 2026 02:24:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 24 Jun 2026 02:24:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e106d4835ce675e7c706a3e7852ff710b788c273c68c3fe9d9a940bd1fc95e`  
		Last Modified: Wed, 24 Jun 2026 02:24:50 GMT  
		Size: 202.8 MB (202750113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c9dd13c3069b01bd18cbaeb7e0b49d5ae6eb432327e5491dd9d8f20111f1df`  
		Last Modified: Wed, 24 Jun 2026 02:24:45 GMT  
		Size: 9.4 MB (9359971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9972cfd53c8fe09fcbfe9cdec4585f0a3579f636cf9112a19f81ac5d521325`  
		Last Modified: Wed, 24 Jun 2026 02:24:45 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d692185fee667b40cd8dc8d4c0161b8b02657d979950fb63390ea651d867d1`  
		Last Modified: Wed, 24 Jun 2026 02:24:44 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:333edc0ab4f4936765a781c554aa2ba48fedc3a8503b20fa64eddd53e121d883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f9cb0e6135dd49f5c977efffd93cb6e88013e667a3748575e13ab1e8452241`

```dockerfile
```

-	Layers:
	-	`sha256:278be692ff52a5845624b10e9a1dcd6d0f26b898fd6a907f08b9b7ab9b5b5127`  
		Last Modified: Wed, 24 Jun 2026 02:24:45 GMT  
		Size: 3.1 MB (3110035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81e4233dadc4f3d58e47ca27ab75c102cd16fa6349f99a1a87a825385bd2a5b6`  
		Last Modified: Wed, 24 Jun 2026 02:24:45 GMT  
		Size: 17.5 KB (17525 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b13fc2b0cfe0e8a3b4227672574720108162d1160a65f85cee5ae20ba8197289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.3 MB (239327876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567caac43c112c7478dafff83e830ff245778f13da38ec2732e7ae2501cd3eb4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:30:58 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:30:58 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 02:30:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 24 Jun 2026 02:30:58 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 24 Jun 2026 02:30:58 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 24 Jun 2026 02:30:58 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 24 Jun 2026 02:30:58 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 24 Jun 2026 02:30:58 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 24 Jun 2026 02:30:58 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 24 Jun 2026 02:30:58 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 24 Jun 2026 02:30:58 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 24 Jun 2026 02:30:58 GMT
ARG USER_HOME_DIR=/root
# Wed, 24 Jun 2026 02:30:58 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 24 Jun 2026 02:30:58 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 24 Jun 2026 02:30:58 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee4d5543c5312840b4b0009e53dcd540c6a7943cdc4d8981a0ac83444895b5e`  
		Last Modified: Wed, 24 Jun 2026 02:31:21 GMT  
		Size: 199.8 MB (199818352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fadbdd58791b4d97d09d91f60ada2b7bf6601174330b710e1fb66840977be18`  
		Last Modified: Wed, 24 Jun 2026 02:31:17 GMT  
		Size: 9.4 MB (9359967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d06a99d9413a1f476b81fbfaff87fd6914ea1c0a2495c9324a2078e65f69ee5`  
		Last Modified: Wed, 24 Jun 2026 02:31:17 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ec3d5c80bdae14c36b5b6fbfbee2cd5adc5c79e65e54a51db7d52a20e4f1ec`  
		Last Modified: Wed, 24 Jun 2026 02:31:17 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:406ff384a350131515f64b5ef3821b171d07a6af3f0b75ad0c81b23adc7601f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa31b6f360040d3372e5e070cc773269f50ec1c10e516a21097106f88509077c`

```dockerfile
```

-	Layers:
	-	`sha256:e22399e466e84933d3195b4f4ee4b8dd21414cf88f1cf346e9a6fc5fbe547360`  
		Last Modified: Wed, 24 Jun 2026 02:31:17 GMT  
		Size: 3.1 MB (3110327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fde35b71757559be6b5fe4694d920a72fd98b104a18fa139f03be8a8a46bbdea`  
		Last Modified: Wed, 24 Jun 2026 02:31:17 GMT  
		Size: 17.7 KB (17694 bytes)  
		MIME: application/vnd.in-toto+json
