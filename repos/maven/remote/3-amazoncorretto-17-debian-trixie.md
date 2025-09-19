## `maven:3-amazoncorretto-17-debian-trixie`

```console
$ docker pull maven@sha256:091508922fbfe106f563aae7d09416e6a27f8bdeb169ab29d4ce35fdc76baf07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:4b0e10155d1ca1266360cbfa38b49f8bab767aac2fdfa06f1ba36f22fddf8416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239900674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10cc7409ee6c2f4c3e571b05ee940c18c54d3237fc4b98e21ed7f40e003e52e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf12b329c2de484d3491c2ca234618ba16c1fcd31062eb7f26ea9afddc56173f`  
		Last Modified: Thu, 18 Sep 2025 22:10:17 GMT  
		Size: 200.9 MB (200883572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af6a9fd351c5681c969d39de481301955d8718e335e5fe89ea2fba2301af073`  
		Last Modified: Thu, 18 Sep 2025 21:43:53 GMT  
		Size: 9.2 MB (9242570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61dd54473ab3ec83dde96c4378fe30f3168f9c41b026fabcfe6cc89153b8a6e`  
		Last Modified: Thu, 18 Sep 2025 21:43:53 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277bdd4cdf5e025b38121f0b23016527ba476af25b68af54ea93da9fec27e72b`  
		Last Modified: Thu, 18 Sep 2025 21:43:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:ca60951bd79717b6c0c44a85016d46f1070b2646541ff9ce860e362451ee9107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db5f3a9063f20a15d4ebf92f4c97b3d294f550e2bbdc87f9378d87d30e5eb38`

```dockerfile
```

-	Layers:
	-	`sha256:9d7ba626111f0ed6880ea2f13bee84c0f6e6f734b674cb2777ffe3af2bc354a6`  
		Last Modified: Thu, 18 Sep 2025 23:27:38 GMT  
		Size: 3.1 MB (3101357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b96e40ce3872536cf48a5c1745a03fb6f737d1b89c3e11218b93e2b413fbcbc`  
		Last Modified: Thu, 18 Sep 2025 23:27:39 GMT  
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
