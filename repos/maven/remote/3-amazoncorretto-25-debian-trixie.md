## `maven:3-amazoncorretto-25-debian-trixie`

```console
$ docker pull maven@sha256:cd159bc1d48b300e1bce48f98eeec4bd10ef9ab99fbcfc58d2ddb5b5df342415
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:31d49f557d4c51a8eaf2b6afab6a45845051407b8901762dbb0a7ba4b6fd223e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276732763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a7fb68b08d9b026ab925d55b2de71fedc8f7586ba1d4627c3584828df778b3`
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
	-	`sha256:add9c18f2266e121ddef7b9d4a6a71cdc3b0a4a15346fcf9233a417a105826c0`  
		Last Modified: Thu, 02 Oct 2025 14:42:45 GMT  
		Size: 237.7 MB (237711378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf913faee7db263fcbc22bf3fc31064928f46c00d1be95e7a7d45faa4065ca2`  
		Last Modified: Thu, 02 Oct 2025 13:18:08 GMT  
		Size: 9.2 MB (9242584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50cd470a2d0f19b64609f93526c9a724602358041289ed70cc0ee059f4f11f0`  
		Last Modified: Thu, 02 Oct 2025 13:18:06 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aceadef46ecc0afceeac8076d9b2f6514583732c439c3bbb5af6fc15ba30ef7`  
		Last Modified: Thu, 02 Oct 2025 13:17:33 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:0deebcb22b016902d208e56d5b985d744b43a900a627ddf6a211eacccaf3c90a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670e3aa2ac0218a58213a95345f8841a8a740a149840c29b24a04d6dc81a9f49`

```dockerfile
```

-	Layers:
	-	`sha256:6129f52abd5c22152b2f45bb6f313afc1eb32c6b91a5329c4b27a7db90afb651`  
		Last Modified: Thu, 02 Oct 2025 14:29:21 GMT  
		Size: 3.1 MB (3110406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adbd5016b2937b2374ecae115e2c5051a2234cfb6c3a7d61dd0ba23d2071d919`  
		Last Modified: Thu, 02 Oct 2025 14:29:22 GMT  
		Size: 19.2 KB (19243 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-debian-trixie` - linux; arm64 variant v8

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

### `maven:3-amazoncorretto-25-debian-trixie` - unknown; unknown

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
