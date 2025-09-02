## `maven:3-amazoncorretto-8-debian-trixie`

```console
$ docker pull maven@sha256:b162ffb83690fcbf19b07e3a500fe5fbc86af92121cae6da66878aa3beb48cb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:58037319d45aa741e6a08b78b36c9e23e926646f78ef8dc20023d174c74e7f19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.2 MB (164174663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4598dc54d86035b66d307f33a2a650b1ca01b05b12ef4b908782db3a76a714f6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Tue, 19 Aug 2025 14:41:45 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 14:41:45 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 14:41:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Tue, 19 Aug 2025 14:41:45 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 19 Aug 2025 14:41:45 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 19 Aug 2025 14:41:45 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 19 Aug 2025 14:41:45 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 19 Aug 2025 14:41:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 19 Aug 2025 14:41:45 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 19 Aug 2025 14:41:45 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 19 Aug 2025 14:41:45 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 19 Aug 2025 14:41:45 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 19 Aug 2025 14:41:45 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 19 Aug 2025 14:41:45 GMT
ARG USER_HOME_DIR=/root
# Tue, 19 Aug 2025 14:41:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 19 Aug 2025 14:41:45 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 19 Aug 2025 14:41:45 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebddc5d52918f27ae389f868825aa8be15168957edd1970462f06ccf7e9d2ca3`  
		Last Modified: Tue, 02 Sep 2025 01:14:22 GMT  
		Size: 125.2 MB (125157766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabce5dd023cccd8fdf4c1b17a27a33a45f6f61e282d4a8660439a8334183cb3`  
		Last Modified: Tue, 02 Sep 2025 01:14:08 GMT  
		Size: 9.2 MB (9242575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ec227f5d91b10cb6f8af01a9e72e961fc5b77b8302cffde4ccd470107c6190`  
		Last Modified: Tue, 02 Sep 2025 01:14:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab27da25d8c9a2cd5d8c26288071aa6e2d46be44baaa092aa1ec621ce553d34`  
		Last Modified: Tue, 02 Sep 2025 01:14:08 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:a81e8dcfca6883b64f9d78954caec09e7ea9cf3db548b55a0f18655454eee4cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2998406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d72a038ffb484f4813e84adf0c1328e8e7ace7230446640edd6f06e6f1b1c4e`

```dockerfile
```

-	Layers:
	-	`sha256:8daf85a346368e07a81f7da3614dfff2f9a82026ee568c868ff005fdc6de2792`  
		Last Modified: Tue, 02 Sep 2025 02:29:01 GMT  
		Size: 3.0 MB (2979151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a921f844797c8ff2370b229be32ba0f02aab93988552aa58264a0a7e2280db`  
		Last Modified: Tue, 02 Sep 2025 02:29:02 GMT  
		Size: 19.3 KB (19255 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:3161060da8423d8a88590120fa08d212174045d5658b79a0c03bf398207775af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148482105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd9b3cafd1b58ff7327920c89486ed12527980e1f9bba24f51633d3dc6abcbe`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Tue, 19 Aug 2025 14:41:45 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 14:41:45 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 14:41:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Tue, 19 Aug 2025 14:41:45 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 19 Aug 2025 14:41:45 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 19 Aug 2025 14:41:45 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 19 Aug 2025 14:41:45 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 19 Aug 2025 14:41:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 19 Aug 2025 14:41:45 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 19 Aug 2025 14:41:45 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 19 Aug 2025 14:41:45 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 19 Aug 2025 14:41:45 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 19 Aug 2025 14:41:45 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 19 Aug 2025 14:41:45 GMT
ARG USER_HOME_DIR=/root
# Tue, 19 Aug 2025 14:41:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 19 Aug 2025 14:41:45 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 19 Aug 2025 14:41:45 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71df21dc85fa9db47a8c04826b623b3628154c0911dd05b9a3930ef12c94f688`  
		Last Modified: Wed, 20 Aug 2025 21:31:24 GMT  
		Size: 109.1 MB (109102434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3701320fbe24cf892aa4dc83d492b550e4f88a7d25889f5e388e29caaf2f63c1`  
		Last Modified: Wed, 20 Aug 2025 18:42:53 GMT  
		Size: 9.2 MB (9242588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecf365c151a7ffd11edaca6cb2d1bb8937127bfec88abf9f67d0a209a9621a3`  
		Last Modified: Wed, 20 Aug 2025 18:42:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0008733fbab23f6a4e633d1043f0b2df2a4cc3c60539db68f583ffe03ba59c18`  
		Last Modified: Wed, 20 Aug 2025 18:42:52 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:83333fe46c98f24d8241c01eafec8120d9a6b5d7c258657767e736c68d759a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9cdeef9ceb0f409ee945f88fc0005f485f9e8a119f11bb6e4098bdf3e34330b`

```dockerfile
```

-	Layers:
	-	`sha256:cc262bddbbfb2821b94ed736637a695eded52c18dd73b49a6429a11304120dd1`  
		Last Modified: Wed, 20 Aug 2025 20:28:11 GMT  
		Size: 3.0 MB (2961972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b58b10af168ffbe1ae3d8b906092686f8de190d130a41afe6a36195a52098788`  
		Last Modified: Wed, 20 Aug 2025 20:28:12 GMT  
		Size: 19.4 KB (19424 bytes)  
		MIME: application/vnd.in-toto+json
