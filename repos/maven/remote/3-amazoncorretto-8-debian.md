## `maven:3-amazoncorretto-8-debian`

```console
$ docker pull maven@sha256:91bc0b07e3549ae867a97b9bedb98cb1508deb214b562810ff377e411d0d8b95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-debian` - linux; amd64

```console
$ docker pull maven@sha256:0f4a05b5ffd18f1cb1a77a5e35723a710366f404596a7537e39cc3b8e08e0e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.2 MB (164175214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0e18cdc423addcaf2e2e93ac953ad5e933c2d9298ca51d802dfa3ab7cd6917`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Wed, 17 Sep 2025 20:58:48 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 20:58:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
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
	-	`sha256:a6888f3ca32f1904414732653c3a14dbd5179d256d5e0a64d0784060a83dcb02`  
		Last Modified: Thu, 18 Sep 2025 21:44:22 GMT  
		Size: 125.2 MB (125158105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3675df5aeaf21e80cda7c69221ffc3e29f43927ce88aea094529d70d7df79a2f`  
		Last Modified: Thu, 18 Sep 2025 21:44:06 GMT  
		Size: 9.2 MB (9242575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9745c3d01f44192d6f9b7e98322ef2d8a120a71c75566d2beaf19d4d3384f1`  
		Last Modified: Thu, 18 Sep 2025 21:44:06 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc54e654f80c9b6e8c8da10ab000c5e10368a8e0d4c181b8b634d09e4dc296e`  
		Last Modified: Thu, 18 Sep 2025 21:44:06 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian` - unknown; unknown

```console
$ docker pull maven@sha256:505cd1f155ccd7b44f6ddda6dd6dd9aa0d699865a4827a319971b3bb5438c158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2999254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c9fbbf59966e60ad3444448a978d45008bf6b54fa3690b8a1edc59b7159991`

```dockerfile
```

-	Layers:
	-	`sha256:cbce7e28cd9ed624acd215208410ffd038a77b05017cf1d431c047032fb338b3`  
		Last Modified: Thu, 18 Sep 2025 23:28:12 GMT  
		Size: 3.0 MB (2979999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf8e5b482a92f534ddc983d75ede71e53e3c79b72dd05ce8fda66f39e1f66476`  
		Last Modified: Thu, 18 Sep 2025 23:28:12 GMT  
		Size: 19.3 KB (19255 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:39ee154a8a45b1ac94a4b925061805c7b5fab130d1ecae526ada1ce20afb3c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148482750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67fc94a37434662e98f844f7dcca46614453ef0db9abd39c8328f74603b01e80`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Wed, 17 Sep 2025 20:58:48 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 20:58:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
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
	-	`sha256:3adeec2a4a5eced56eaf7191c6dc2baeb4669f702524746bc3ccecd56d96835f`  
		Last Modified: Thu, 18 Sep 2025 21:43:58 GMT  
		Size: 109.1 MB (109102499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11a76cffa519c67f5a1d530e8b6ee1fba90cbd3723c2294afd684a6d8dfaec0`  
		Last Modified: Thu, 18 Sep 2025 21:43:48 GMT  
		Size: 9.2 MB (9242580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0d3aac026b86ec03106b17e6bb97e8ae01dfe8bfde53048aba84a121dfe3b5`  
		Last Modified: Thu, 18 Sep 2025 21:43:47 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819ab38661d2a6eeb4a008c42a3e313e57999b3766ef262d85f1959e4936c970`  
		Last Modified: Thu, 18 Sep 2025 21:43:47 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian` - unknown; unknown

```console
$ docker pull maven@sha256:70acca86193bbc84e1416d5b678de8f6430f2fe15c10b2e8568d691d35b518c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245b2ae6b6c8a24b5c142d3193bf96025b1e5f320aad88114ac4e0ea6da9e30f`

```dockerfile
```

-	Layers:
	-	`sha256:801193b5961983750d89989096bf071eff0eb20c4d798bb5dbb5e61474e8d449`  
		Last Modified: Thu, 18 Sep 2025 23:28:16 GMT  
		Size: 3.0 MB (2962820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:444a85e5d1c8a34b2f12637c0d40f5c0892410d86e7af6b6baf5adf7f85fde44`  
		Last Modified: Thu, 18 Sep 2025 23:28:17 GMT  
		Size: 19.4 KB (19424 bytes)  
		MIME: application/vnd.in-toto+json
