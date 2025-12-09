## `maven:3-amazoncorretto-8-debian-trixie`

```console
$ docker pull maven@sha256:b3143d9b5fd43203e1762cc50b2c7c963881d7f1ab69f896cd6955c13b5f899a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:a8f0347707ba85b85e2be9bbddd13503660eea1d3179c0295d045f828a1f2ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164612280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846b1e3c90abc1b8181b4fa00683879aeda5bf64e8fbbe29e3edcfdd0dc44e59`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:57:50 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:57:51 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 23:57:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Mon, 08 Dec 2025 23:57:51 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 08 Dec 2025 23:57:51 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 08 Dec 2025 23:57:51 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 08 Dec 2025 23:57:51 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 08 Dec 2025 23:57:51 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 08 Dec 2025 23:57:51 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 08 Dec 2025 23:57:51 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:57:51 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 08 Dec 2025 23:57:51 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 08 Dec 2025 23:57:51 GMT
ARG MAVEN_VERSION=3.9.11
# Mon, 08 Dec 2025 23:57:51 GMT
ARG USER_HOME_DIR=/root
# Mon, 08 Dec 2025 23:57:51 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 08 Dec 2025 23:57:51 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 08 Dec 2025 23:57:51 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2058fe79934b211e7cfd7dfcfca8d429d8707b291c2f6775a094f4743bf7fe7`  
		Last Modified: Mon, 08 Dec 2025 23:58:28 GMT  
		Size: 125.6 MB (125592177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82163d316c8e4010e5e632d816aa4d62096764a3d3c3a0a916c1270c3aaa26ee`  
		Last Modified: Mon, 08 Dec 2025 23:58:15 GMT  
		Size: 9.2 MB (9242572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7319b009f01c95cb6a589e5aaccbc179e5462562f5e078ed291885f3639f1ef0`  
		Last Modified: Mon, 08 Dec 2025 23:58:13 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb249083cc1cb187a88e19de4d5bb96b3379f0f49a74a7909880ef5dc01f49cd`  
		Last Modified: Mon, 08 Dec 2025 23:58:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:c533e885afaf56853c4e7d0624f5919cd1b124e40b916eb91e61851ab00bcfc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3001178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be384bcdad211d382b03cac28d57b07d89aca0294e62d8a9fa12a312bd35699a`

```dockerfile
```

-	Layers:
	-	`sha256:8db58870e2eb504f957e8aed7e8cf526efa9afec9bff18aabdbc5f64cfed6b3b`  
		Last Modified: Tue, 09 Dec 2025 03:28:40 GMT  
		Size: 3.0 MB (2981966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea4763e8eee9f51ddf2ff189021a5efa6e021fd002760896d05d0ee86c32c27`  
		Last Modified: Tue, 09 Dec 2025 03:28:41 GMT  
		Size: 19.2 KB (19212 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d0d7839b11a5be2fa216dc66cc688170f5abdb40184e1847ba1bdc6ac102eb89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148948937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c26433fd83500b11e77beae9b4c885707341f51d0a8382ba148ba3118bb08d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:05:25 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:05:25 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 00:05:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Tue, 09 Dec 2025 00:05:25 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 09 Dec 2025 00:05:25 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 09 Dec 2025 00:05:25 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 09 Dec 2025 00:05:25 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 09 Dec 2025 00:05:25 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 09 Dec 2025 00:05:25 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 09 Dec 2025 00:05:25 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:05:25 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 09 Dec 2025 00:05:25 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 09 Dec 2025 00:05:25 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 09 Dec 2025 00:05:25 GMT
ARG USER_HOME_DIR=/root
# Tue, 09 Dec 2025 00:05:25 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 09 Dec 2025 00:05:25 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 09 Dec 2025 00:05:25 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a221b1eea3c17b61c03656d12ab6867add2dca660b59447299363f9dc5b054`  
		Last Modified: Tue, 09 Dec 2025 00:06:06 GMT  
		Size: 109.6 MB (109566703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8a80f24ac5320e390d17dd93f792f43e7d29f67bd1ffd774bfd1a84b49984a`  
		Last Modified: Tue, 09 Dec 2025 00:05:49 GMT  
		Size: 9.2 MB (9242570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5895adae87d47bf4731e11d52c23e8a1fbd65df8888a5b62b043cb2067d8bb`  
		Last Modified: Tue, 09 Dec 2025 00:05:49 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89cd6af392517c4cc35320966009657bbae1b091653b825d3b08a2646c2fff3`  
		Last Modified: Tue, 09 Dec 2025 00:05:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:4407c71373d81b98f8d8da523e90d43d967dd6d917fd00ddb5aef9295288ccca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d372fa84988ec5e6da0c10a727903b237bb684c49d2ff4bb22776591f9682024`

```dockerfile
```

-	Layers:
	-	`sha256:c2151fe524995128545520016a3168b480675f854175bfc4e66394b1328e27b1`  
		Last Modified: Tue, 09 Dec 2025 03:28:45 GMT  
		Size: 3.0 MB (2964787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ddfba65f4fab2707f6d652ce706ac5e2fb068b91f56fc9dd20f310d2a2f306`  
		Last Modified: Tue, 09 Dec 2025 03:28:50 GMT  
		Size: 19.4 KB (19381 bytes)  
		MIME: application/vnd.in-toto+json
