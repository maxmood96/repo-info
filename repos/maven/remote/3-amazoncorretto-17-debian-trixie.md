## `maven:3-amazoncorretto-17-debian-trixie`

```console
$ docker pull maven@sha256:d90fefbc6f899c588340ad2df5aaf157bf73f67ea1ed3cbc369ee6e381eeaf20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:f06d2366fbefd63b55cdfadfa691cc4054ca765030a1e126e29648e159297554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239904972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794aed0d3d591321e143fbd07b913842c9b2493c9b1ea9ff5667b70a9007c5ed`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 17 Sep 2025 20:58:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 17 Sep 2025 20:58:48 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 20:58:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 17 Sep 2025 20:58:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Sep 2025 20:58:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Sep 2025 20:58:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Sep 2025 20:58:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Sep 2025 20:58:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Sep 2025 20:58:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 17 Sep 2025 20:58:48 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Sep 2025 20:58:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Sep 2025 20:58:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Sep 2025 20:58:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff4bd148c33d3fa54e2b792ecfe803e8e48f11a08365371d5d44db3782219a9`  
		Last Modified: Tue, 30 Sep 2025 21:33:32 GMT  
		Size: 200.9 MB (200883605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047f1bf0e9bbacc5abe6fe86978995d0cef849b81d302e1642ed47ae9b2f01d1`  
		Last Modified: Tue, 30 Sep 2025 01:06:32 GMT  
		Size: 9.2 MB (9242568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a1fa840af79318c0e1925ff4195c77460f19c31981f9a357e78f0b0c198639`  
		Last Modified: Tue, 30 Sep 2025 01:06:37 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f05d2cc861376690d06e0691a68135bf75dcad5f2386789a42d014a09d884d6`  
		Last Modified: Tue, 30 Sep 2025 01:06:41 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:fc9c6baa403d9592706ee1d7b1afdb2ed6c42f29dc5026e81958689d9bd0a74b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebeff726f1799868879f7a63164f880831f3fa56ff67f72dac1a2a0356d3423e`

```dockerfile
```

-	Layers:
	-	`sha256:ea337312f561e8783735d2c00b9c1c27ec4ca082e0d0da70f9c4ff9d781a2c68`  
		Last Modified: Tue, 30 Sep 2025 20:27:25 GMT  
		Size: 3.1 MB (3101357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfc2f78b49b25798868e407136899bf1b9aff666a46f00e4fa9212d808a7f54c`  
		Last Modified: Tue, 30 Sep 2025 20:27:26 GMT  
		Size: 19.2 KB (19242 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:a82244b70347ab11c081e7186d22e9082b7f7eaf9f893cb701036e1b3bbdd3b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.7 MB (238691854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3fd3f6c5941da7149f2d39f84ad7937dc192011a0d333ab453a3cdad586f04`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Wed, 17 Sep 2025 20:58:48 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 20:58:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 17 Sep 2025 20:58:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Sep 2025 20:58:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Sep 2025 20:58:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Sep 2025 20:58:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Sep 2025 20:58:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Sep 2025 20:58:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 17 Sep 2025 20:58:48 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Sep 2025 20:58:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Sep 2025 20:58:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Sep 2025 20:58:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758cd0f67c7e744cf92c7e4b2a9ff0a5934ed17ef6778b7bf129cc214ef836fe`  
		Last Modified: Fri, 19 Sep 2025 01:52:29 GMT  
		Size: 199.3 MB (199311597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdfeb58e814fd0d11fdc084f5a25837aebf6f40e2ed6091aa59a61f9e0dcc1f`  
		Last Modified: Thu, 18 Sep 2025 21:43:12 GMT  
		Size: 9.2 MB (9242588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56059064b973209aa0afc14f83750bd6fafe3585c1c6f6da51a1adbac5aaa3c`  
		Last Modified: Thu, 18 Sep 2025 21:43:10 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49af77a8f0484c5f2d65fbdaebbd437a3878009b09cf6ad1bb28285c1f1126fa`  
		Last Modified: Thu, 18 Sep 2025 21:43:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:7b6476b4f4a9a1b0da6c0e56e54bef2e7c5a19a44e15932a3e0abd194c2d54f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d4ee6d5132436720c0f81ebe64505d1d9676337ffa9b5046123f834f0e6d34`

```dockerfile
```

-	Layers:
	-	`sha256:163dea52d862d43e0f9eb68af4000374e06c2952a13ed3b8fd249ff660d8ee32`  
		Last Modified: Thu, 18 Sep 2025 23:27:43 GMT  
		Size: 3.1 MB (3101020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3f82ca8c5785e258e1f23a0dcc2d69317468d1a9b9e347b69b55f1d141ea730`  
		Last Modified: Thu, 18 Sep 2025 23:27:44 GMT  
		Size: 19.4 KB (19411 bytes)  
		MIME: application/vnd.in-toto+json
