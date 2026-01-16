## `maven:3-amazoncorretto-17-debian`

```console
$ docker pull maven@sha256:bd351a7111c045a87d89654b1413e1b23f3328aee78255ac987266995cc7a878
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-debian` - linux; amd64

```console
$ docker pull maven@sha256:014d132a849a0c9e963aabc94f2999f70b6c3f286f58d86d812bdef5cb6a46aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240572246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf6338199ea37960d183d1aeb6c3ae8691b3aacaa0fc286970f7f596d5c5f12`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 02:44:58 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:44:58 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jan 2026 02:44:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 16 Jan 2026 02:44:58 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 02:44:58 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:44:58 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:44:58 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 02:44:58 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 02:44:58 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 02:44:58 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 02:44:58 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 02:44:58 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 02:44:58 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 02:44:58 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 02:44:58 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 02:44:58 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 02:44:58 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735c75d2ff16af9fc4d9b8ad049c2e0eceea85c00cf3e8fc767cce6313221993`  
		Last Modified: Fri, 16 Jan 2026 02:45:21 GMT  
		Size: 201.5 MB (201485280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4c0b0c12a339e0407f1be0d33af9a2357cc8a3b1d14ecf31243792871cd705`  
		Last Modified: Fri, 16 Jan 2026 02:45:27 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f3849acca03dab23bb028a3806794ae362ccf634cbd3296a3dfea3f79ad017`  
		Last Modified: Fri, 16 Jan 2026 02:45:26 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2ccea0cb12f9c02f387f4060b467e3351038c6ca0488b8fa29a84d6a74a4c0`  
		Last Modified: Fri, 16 Jan 2026 02:45:26 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian` - unknown; unknown

```console
$ docker pull maven@sha256:8f427bc696702060317968a095071c3a0c5ef2f40959562bcfbd7b964ad25543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3123225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:679b3a2231ef4c5e416317731a4352f6a22e0cc786ff23b658f86e851249c678`

```dockerfile
```

-	Layers:
	-	`sha256:0edfcb75e953fa2547c0453a071142827c4b093eb522b7c1a641a87d165d1d93`  
		Last Modified: Fri, 16 Jan 2026 03:29:03 GMT  
		Size: 3.1 MB (3104027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:548b34c70493a662767cec47cd906289ba78f1b8e25b47041ff7cc801a559f45`  
		Last Modified: Fri, 16 Jan 2026 03:29:04 GMT  
		Size: 19.2 KB (19198 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6975fd3e551c8d40c87c3a6d1ca8484af18140f2335874b3f796c84734dbe315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239372867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eacca54420e2deda05291c290dfb105e4b763f53959c176d0b151b6f22ec20fd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:45:07 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:45:07 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:45:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 13 Jan 2026 03:45:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 13 Jan 2026 03:45:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 13 Jan 2026 03:45:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 13 Jan 2026 03:45:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 13 Jan 2026 03:45:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 13 Jan 2026 03:45:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 13 Jan 2026 03:45:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 13 Jan 2026 03:45:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 13 Jan 2026 03:45:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 13 Jan 2026 03:45:08 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 13 Jan 2026 03:45:08 GMT
ARG USER_HOME_DIR=/root
# Tue, 13 Jan 2026 03:45:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 13 Jan 2026 03:45:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 13 Jan 2026 03:45:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091f7ef37ea048177b909dc56a3e2ff3256004775e7d5181b5e065576a569a28`  
		Last Modified: Tue, 13 Jan 2026 06:38:25 GMT  
		Size: 199.9 MB (199925538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e530b6bebd9c6c85a9bf9e56919c2fd5f9440ed4f6503091b0ab4abb51c15290`  
		Last Modified: Tue, 13 Jan 2026 03:45:38 GMT  
		Size: 9.3 MB (9312249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7143453ae398d0dc3e432b60cd880d1617a14c6f630e47cf43851ec986e59a0`  
		Last Modified: Tue, 13 Jan 2026 03:45:37 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2006bee65378d87a72a1ec47f765c8bb7d2bed30561be23d38b4753f716404`  
		Last Modified: Tue, 13 Jan 2026 03:45:37 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian` - unknown; unknown

```console
$ docker pull maven@sha256:5babb45d508ff0afaf2e6fa3eaab6d1d52e6be321fc7160aeeaa8afe00c312e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3123057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da98c3e85bb034ba11f602d6891b432782fefd37c833784c7d7994c508d032fe`

```dockerfile
```

-	Layers:
	-	`sha256:19c03aa92f3b3e9fe2a488bbcf6c6f06199aea82f2deb11226d155bc23743c09`  
		Last Modified: Tue, 13 Jan 2026 06:29:55 GMT  
		Size: 3.1 MB (3103690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da7608e960d3f29a28f53c1601e74109c80e33a5fb636413607b2a141dfd0de4`  
		Last Modified: Tue, 13 Jan 2026 06:29:56 GMT  
		Size: 19.4 KB (19367 bytes)  
		MIME: application/vnd.in-toto+json
