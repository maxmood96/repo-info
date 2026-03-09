## `maven:3-amazoncorretto-8-debian-trixie`

```console
$ docker pull maven@sha256:0dd62af6338e527cdfb9798ffa79552218aefbbcc8b4962d02fc24db5d427346
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:cd5d61efaa2b1e58916007f6e8f48f132933b649f5832b6a61fce6d705513a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.1 MB (165123778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2ecfd7aa55f084a7b92836afa8e1b5d9ca49454cabeff5974f7b7077645f1b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 19:15:04 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Mar 2026 19:15:04 GMT
ENV LANG=C.UTF-8
# Mon, 09 Mar 2026 19:15:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Mon, 09 Mar 2026 19:15:04 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Mar 2026 19:15:04 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:15:04 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:15:04 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Mar 2026 19:15:04 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Mar 2026 19:15:04 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Mar 2026 19:15:04 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Mar 2026 19:15:04 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Mar 2026 19:15:04 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Mar 2026 19:15:04 GMT
ARG MAVEN_VERSION=3.9.13
# Mon, 09 Mar 2026 19:15:04 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Mar 2026 19:15:04 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Mar 2026 19:15:04 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Mar 2026 19:15:04 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b4f111e0e85af9a821c51feedd6cb800e8ebd1de72b19cf9fa10e3534ecb7c`  
		Last Modified: Mon, 09 Mar 2026 19:15:22 GMT  
		Size: 125.6 MB (125646597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d66c6140cd7f912ce7495b7669990f98d48a02764e56936fa9f1a049162e55`  
		Last Modified: Mon, 09 Mar 2026 19:15:19 GMT  
		Size: 9.7 MB (9697513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e3ef179f98e5d94d2e50e948154bb99a1c045564c54745a74f28f41593812d`  
		Last Modified: Mon, 09 Mar 2026 19:15:19 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5f53232df4bdc3b0385178cc8f2fc6009e22198be875cdbec47bfe71ce270e`  
		Last Modified: Mon, 09 Mar 2026 19:15:19 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:42ea008445dd66fd0fc15a23b6efbce945e9eec01e3319e95eccb024de066b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3007720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87cd83f117928f19485b48e884531cd4ecb0c308c67c3e61e1567c1e84f3bde`

```dockerfile
```

-	Layers:
	-	`sha256:b42343173d6675917ef3bbc22b24b7a7b3f88ea2cf3e09fd9981a7ff43f87217`  
		Last Modified: Mon, 09 Mar 2026 19:15:19 GMT  
		Size: 3.0 MB (2988508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69ef6c6ab1f42c0445ec38980885f8a29218eea78fb26189fff072241c23b847`  
		Last Modified: Mon, 09 Mar 2026 19:15:19 GMT  
		Size: 19.2 KB (19212 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6a1437ec07d1d0e6c7fa43d8c48c6f5816ea97c5fe51c3042ffd2e6c123f1550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149210489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b6ba0b3cc09e995fcc0522e6379bf7bf1b81adae9988bb5ee6627bc9c6f044`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 19:14:48 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Mar 2026 19:14:49 GMT
ENV LANG=C.UTF-8
# Mon, 09 Mar 2026 19:14:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Mon, 09 Mar 2026 19:14:49 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Mar 2026 19:14:49 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:14:49 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:14:49 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Mar 2026 19:14:49 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Mar 2026 19:14:49 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Mar 2026 19:14:49 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Mar 2026 19:14:49 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Mar 2026 19:14:49 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Mar 2026 19:14:49 GMT
ARG MAVEN_VERSION=3.9.13
# Mon, 09 Mar 2026 19:14:49 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Mar 2026 19:14:49 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Mar 2026 19:14:49 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Mar 2026 19:14:49 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eddc0224a7429b54d3ac0d765a049a4f4dd1a5b5cbcbe2f28bbe081f59d2927`  
		Last Modified: Mon, 09 Mar 2026 19:15:05 GMT  
		Size: 109.4 MB (109371823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de35b1d6a859950ffc105d07fa162c571232cf71758dce7b34628bec64ccee1`  
		Last Modified: Mon, 09 Mar 2026 19:15:03 GMT  
		Size: 9.7 MB (9697532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff5702ce32f18d6d8b98e8cba3964595487545271e514f79f7e73c191806c9d`  
		Last Modified: Mon, 09 Mar 2026 19:15:03 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2456c0b4c263051ee4f8770ccb8dc02ddc9f7fc71d3af5c6cdbf94115cd67642`  
		Last Modified: Mon, 09 Mar 2026 19:15:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:7fd4f48f7326dbbde689178fc056234dfeee2f0d56fb0a254bb22e4795b6d0a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2990710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a504ce2c0fa3764699c1170fa9d84cb3d9223329a395ab333205adc5ed5c12`

```dockerfile
```

-	Layers:
	-	`sha256:e767838840d58454a11c66eac8e20a74d8a8f4a60773b01e028d154c94e16f25`  
		Last Modified: Mon, 09 Mar 2026 19:15:03 GMT  
		Size: 3.0 MB (2971329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2d46be6ec7a9e55a067d45847c1ef8e7b25c9180a84e66dd98dae756652a008`  
		Last Modified: Mon, 09 Mar 2026 19:15:02 GMT  
		Size: 19.4 KB (19381 bytes)  
		MIME: application/vnd.in-toto+json
