## `maven:3-amazoncorretto-25-debian`

```console
$ docker pull maven@sha256:e738c538b74bada7dd8d9ba0226b0a00d97851c25df3762ef24ebc2b3e1bb11f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-debian` - linux; amd64

```console
$ docker pull maven@sha256:b77c6e09df484f6546a5dd335cc756269a3a4dc149f313d3886b8d2cb442c177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274253102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a95199e54957d0d47fe89b4015e29f5f7d22237e504fd94f1aba098a8461bac`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 01:42:40 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:42:41 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 01:42:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 14 Nov 2025 01:42:41 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 01:42:41 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:42:41 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:42:41 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 01:42:41 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 01:42:41 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 01:42:41 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:42:41 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 01:42:41 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 01:42:41 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 01:42:41 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 01:42:41 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 01:42:41 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 01:42:41 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aa264d9f487a50b003f89e7e1270db85a91a22bf4515dee0bc9cf179a5cd25`  
		Last Modified: Fri, 14 Nov 2025 01:43:07 GMT  
		Size: 235.2 MB (235231393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c472c29c15b04387dd68e1f989a7ec4a2d535c14b21a178c1be5c1e34947d6`  
		Last Modified: Fri, 14 Nov 2025 01:43:13 GMT  
		Size: 9.2 MB (9242569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac483c058ea328c639a05d20725b3b48dc45e74c30ff814aef2aa57cd1b4e385`  
		Last Modified: Fri, 14 Nov 2025 01:43:12 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c901cb65c7443c558dfd5ec24232cecfb72accecde32a5c9285fcac0a4bfa2a3`  
		Last Modified: Fri, 14 Nov 2025 01:43:12 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian` - unknown; unknown

```console
$ docker pull maven@sha256:e0101c04379c3581b93c2a51b9505a3cfd9f482bc871cdd2b57893c6fa228e01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3132166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9903dedee192503f3b423ececfbdabfb53f941285b7ae07dffd4af3bf64a9cf3`

```dockerfile
```

-	Layers:
	-	`sha256:547808acd89a2545a149522fcbafba95377020d74b4d67e5339f85a2ede9dfff`  
		Last Modified: Fri, 14 Nov 2025 03:28:54 GMT  
		Size: 3.1 MB (3112967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cca4cec0ca48a6d299932d874577475de8aefe4bb6673896e5d8663e27192d4`  
		Last Modified: Fri, 14 Nov 2025 03:28:55 GMT  
		Size: 19.2 KB (19199 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:a01d8b9d34613d1150baa8328209f5f9dea665d0e9df60058c68760e6ac00b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272353547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a75a6a557ee04ebfa77cf3fe8e5fafe7960cc6892080bf5dfaafdeb254bfde`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 01:59:52 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:59:52 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 01:59:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 14 Nov 2025 01:59:52 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 01:59:52 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:59:52 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:59:52 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 01:59:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 01:59:52 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 01:59:52 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:59:52 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 01:59:52 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 01:59:52 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 01:59:52 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 01:59:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 01:59:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 01:59:52 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696a9888bbef25c4af132de2c2e6b01d2534dd58a305e898cfefe5da5f8c80a0`  
		Last Modified: Fri, 14 Nov 2025 02:00:23 GMT  
		Size: 233.0 MB (232967639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9efed204ae51dd17ff037a81925237888c3374010d1bb7f05e8e50c5960723`  
		Last Modified: Fri, 14 Nov 2025 02:00:32 GMT  
		Size: 9.2 MB (9242571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab37dfc9bec7ad384801ab18f72c761420c497a405ad4ba47bc99f185378aa89`  
		Last Modified: Fri, 14 Nov 2025 02:00:31 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3044c72882298fc1968668523b58df763439f1ff35ef41babec11fd36bdb180`  
		Last Modified: Fri, 14 Nov 2025 02:00:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian` - unknown; unknown

```console
$ docker pull maven@sha256:94ce56e362229a12ccc9218e440706511aed67195b8f88917bc1d7abcb044313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b0abc0a75624d79c02b8961cf3ab02a0c5fd22288e889e3ccc543122855e28`

```dockerfile
```

-	Layers:
	-	`sha256:14590163e60330e3887b235d0a0f6421ec56981064825e2402f012c07b04a957`  
		Last Modified: Fri, 14 Nov 2025 03:28:59 GMT  
		Size: 3.1 MB (3112627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e87b8a892c6896b092b9521ce1209b1e2ea34f0da5cbe6044fbee0ce7521ae1`  
		Last Modified: Fri, 14 Nov 2025 03:29:02 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json
