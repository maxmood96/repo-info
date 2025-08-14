## `maven:3-amazoncorretto-17-debian`

```console
$ docker pull maven@sha256:bce13f8851c0171738c8ae0d5f0cca7683a5cc6ac675fda3d75728cbba15e2d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-debian` - linux; amd64

```console
$ docker pull maven@sha256:6481eee15b64b0b4fc0455daaac2cadc7490ec26f43b9fab700e88dc940db540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239429318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f545c719f908b3f4f36ac10dd459b467b053d442ea35ef2db5acce4b52c4557`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 07:27:41 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 16 Jul 2025 07:27:41 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Jul 2025 07:27:41 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 07:27:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 16 Jul 2025 07:27:41 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 07:27:41 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 07:27:41 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 07:27:41 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 07:27:41 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 07:27:41 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 07:27:41 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 07:27:41 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 07:27:41 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 07:27:41 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 07:27:41 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 07:27:41 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 07:27:41 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 07:27:41 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07a1676f39ad613c3beb917bf40e929e8271fb33c86355d966f244dbd3f60e4`  
		Last Modified: Wed, 13 Aug 2025 00:04:48 GMT  
		Size: 202.0 MB (201955446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60f1ff97b4c8810b908be414a0922cbef54c5ca425f6c6ce72c56eb89048a24`  
		Last Modified: Tue, 12 Aug 2025 22:29:02 GMT  
		Size: 9.2 MB (9242583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de4fcf00bcb7de940af7c6b31ac91e6b6f66df66ff95d3e50ea54877083001f`  
		Last Modified: Tue, 12 Aug 2025 22:28:59 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a62bfe9ea94bcfdc001beffcdf41603789429d7aaf3d7ed878d757c95e07fb5`  
		Last Modified: Tue, 12 Aug 2025 22:28:58 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian` - unknown; unknown

```console
$ docker pull maven@sha256:8e9a71bd19b4e03e9ad64058e1dc85322918ca2652ddb9a4db13d423272c5ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0422a379203ac60a51d67a1cacbd8d59464d37feaf98b2e1210272676cda73`

```dockerfile
```

-	Layers:
	-	`sha256:547f2251bf6232387c33b805834ada09071a56f3ee2d90626d8e135e0a7321cd`  
		Last Modified: Tue, 12 Aug 2025 23:27:29 GMT  
		Size: 3.1 MB (3130411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:371d5c1bc97fdc6b406e42936c1e172087f799235e8b2349d394d78ff615b54a`  
		Last Modified: Tue, 12 Aug 2025 23:27:30 GMT  
		Size: 19.3 KB (19265 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:84d5427b32ff58a398cdeec8b6b524c524c27c3a230dcc2d5759fc76fc497bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237550294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae5978f3cc2e6e9fd392206c9d6736f41bf3f93989c945da33763dd4ddd9d0b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 07:27:41 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 16 Jul 2025 07:27:41 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Jul 2025 07:27:41 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 07:27:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 16 Jul 2025 07:27:41 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 07:27:41 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 07:27:41 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 07:27:41 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 07:27:41 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 07:27:41 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 07:27:41 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 07:27:41 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 07:27:41 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 07:27:41 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 07:27:41 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 07:27:41 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 07:27:41 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 07:27:41 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9cb9fbca4f781d13aad7df34a76f08637e03e085f35977e704b83b8251b711`  
		Last Modified: Wed, 13 Aug 2025 21:21:16 GMT  
		Size: 200.2 MB (200224665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc6a4ec8c348da4cd7ee0a3ec1c8463814a260fd91cf9f84f2da839e0ec6fca`  
		Last Modified: Wed, 13 Aug 2025 20:03:27 GMT  
		Size: 9.2 MB (9242590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8823e25cc5f20c2e4dcddf5b7cfccddac34c9bdadc138540ffbede0e9d176462`  
		Last Modified: Wed, 13 Aug 2025 20:03:26 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d6d59f889c20381a3150a31892c91c64cb35b0cc74e18c36a231e1bfd1d1d4`  
		Last Modified: Wed, 13 Aug 2025 20:03:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian` - unknown; unknown

```console
$ docker pull maven@sha256:1c798940a3fef062de7c0d2117f184635ae87ffb1cea9d9c8594c45e2c36856d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597c47ec5248de4dd06ef9cb4655ac7535e8a40c64c8fd51a704471632f64fb9`

```dockerfile
```

-	Layers:
	-	`sha256:af3b28486fbd410f1ce0da0d294f3aec60da635795c1ccbaedaa841cd3173743`  
		Last Modified: Wed, 13 Aug 2025 20:27:56 GMT  
		Size: 3.1 MB (3130071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab76bcd46f4e5672c91095eb197aa481efe48349454fc1c29746b50b2cf95720`  
		Last Modified: Wed, 13 Aug 2025 20:27:57 GMT  
		Size: 19.4 KB (19433 bytes)  
		MIME: application/vnd.in-toto+json
