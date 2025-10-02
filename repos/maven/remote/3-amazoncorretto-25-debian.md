## `maven:3-amazoncorretto-25-debian`

```console
$ docker pull maven@sha256:20866633ad6cf6475c9f6032fb4191523e7a8ff13501ef976ffbb278fb82ad94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-debian` - linux; amd64

```console
$ docker pull maven@sha256:273a9ba84bf35cb0ccd9300b2a77a85dd734c4dbf61a41116a2af672830e79ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.8 MB (273775266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9e31db8d5c2f32903b1a4491b7bf861fe7e7b0ac006576be5d280605189694`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 19 Sep 2025 20:50:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 19 Sep 2025 20:50:17 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Sep 2025 20:50:17 GMT
ENV LANG=C.UTF-8
# Fri, 19 Sep 2025 20:50:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 19 Sep 2025 20:50:17 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 19 Sep 2025 20:50:17 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 20:50:17 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 20:50:17 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 19 Sep 2025 20:50:17 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 19 Sep 2025 20:50:17 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 19 Sep 2025 20:50:17 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 20:50:17 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 19 Sep 2025 20:50:17 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 19 Sep 2025 20:50:17 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 19 Sep 2025 20:50:17 GMT
ARG USER_HOME_DIR=/root
# Fri, 19 Sep 2025 20:50:17 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 19 Sep 2025 20:50:17 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 19 Sep 2025 20:50:17 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e07cdd15d4a5fce067b6848b05295375af79dd23fa2e03da5f31df90e5ab7c`  
		Last Modified: Wed, 01 Oct 2025 14:42:13 GMT  
		Size: 234.8 MB (234753897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86dae8666a1da14b084385b34964b7d45e3b6eb4a86c00d84dee57b7c050d685`  
		Last Modified: Tue, 30 Sep 2025 00:58:29 GMT  
		Size: 9.2 MB (9242568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90241165c737a8564a761e1d129ea1a4e9ccfc51981379512ba1c25874c3e3dc`  
		Last Modified: Tue, 30 Sep 2025 00:58:29 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f157df299c2df63299461031f8bb50e32d8fc1fb22fac820fea8a44be13a84dc`  
		Last Modified: Tue, 30 Sep 2025 00:58:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian` - unknown; unknown

```console
$ docker pull maven@sha256:eec6194e5dec9365154aad0dd6863513ee0b534e5e1631267db2e89d57f00057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be90223913da573eed00ec25fd080b5bb04ee3398cdf61adf95750a17ca17863`

```dockerfile
```

-	Layers:
	-	`sha256:48e75e2555c37cf6145d7ffbebfad99f3a4f01bc47462909067f1766d4ed7c37`  
		Last Modified: Wed, 01 Oct 2025 14:27:47 GMT  
		Size: 3.1 MB (3110352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd30ef87e1edf05b541a9730d63aaabf6cc10e514073a298fdad19a2560232c3`  
		Last Modified: Wed, 01 Oct 2025 14:27:47 GMT  
		Size: 19.2 KB (19241 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:e44daad51ce4b9725afc56934067bd68c8950cf4cc77b85cc73c7c699b2485dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275159431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d5259d1819a72b8b6a1fbfef975ff97cb694bf365d15df0ec287ce7511eaf9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 19 Sep 2025 20:50:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 19 Sep 2025 20:50:17 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Sep 2025 20:50:17 GMT
ENV LANG=C.UTF-8
# Fri, 19 Sep 2025 20:50:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 19 Sep 2025 20:50:17 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 19 Sep 2025 20:50:17 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 20:50:17 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 20:50:17 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 19 Sep 2025 20:50:17 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 19 Sep 2025 20:50:17 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 19 Sep 2025 20:50:17 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 20:50:17 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 19 Sep 2025 20:50:17 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 19 Sep 2025 20:50:17 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 19 Sep 2025 20:50:17 GMT
ARG USER_HOME_DIR=/root
# Fri, 19 Sep 2025 20:50:17 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 19 Sep 2025 20:50:17 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 19 Sep 2025 20:50:17 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b83288cbd32df3c29b0a03697dbc4758c703e3d6d2b94f76750d47d6ab9e92`  
		Last Modified: Thu, 02 Oct 2025 05:43:37 GMT  
		Size: 235.8 MB (235774979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9ce084a0058cf094336e78115b8f47ec7146b6c8545fca6fcb18349d3ed783`  
		Last Modified: Thu, 02 Oct 2025 05:11:20 GMT  
		Size: 9.2 MB (9242575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85571637431fedad4513c74366d3d604d20e67695d51431988669732dff9304`  
		Last Modified: Thu, 02 Oct 2025 05:09:16 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed34836621e0421aa178b9423c9fb2f5f5529441e53bbc5a791f893204a0230`  
		Last Modified: Thu, 02 Oct 2025 05:09:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian` - unknown; unknown

```console
$ docker pull maven@sha256:8a99bd618515e8b1ac56f8a22b744ca03278bcaae005678ec91d5c5e57adbbef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb319238d0a2611030fe74f448f58120a69b3eb51f7707103e3537b9c8d303ee`

```dockerfile
```

-	Layers:
	-	`sha256:31080153023f2e2d2a4feda47697e19809d1b05178efa3131c3d056e62fb0970`  
		Last Modified: Thu, 02 Oct 2025 05:29:23 GMT  
		Size: 3.1 MB (3110066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3b8f14ff847b3df37e90940d9b12ea1e6e5f4be70e17ef5be6b426ab711a043`  
		Last Modified: Thu, 02 Oct 2025 05:29:24 GMT  
		Size: 19.4 KB (19411 bytes)  
		MIME: application/vnd.in-toto+json
