## `maven:3-amazoncorretto-11-debian-bookworm`

```console
$ docker pull maven@sha256:7891565833dd40fe121e620f4387e4aa55162987d803d01f4dc48ca964a6d99a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-debian-bookworm` - linux; amd64

```console
$ docker pull maven@sha256:ef930de8decb784d07548c38fc94f5ec48c272c52e057cd08807c23179ee0019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241194039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4224357e1cd363cc97a3564b8f69fe4d87ceaaa49fe835f84a1551045b66fcb1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Sat, 25 Jan 2025 20:08:38 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 25 Jan 2025 20:08:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ARG MAVEN_VERSION=3.9.9
# Sat, 25 Jan 2025 20:08:38 GMT
ARG USER_HOME_DIR=/root
# Sat, 25 Jan 2025 20:08:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 25 Jan 2025 20:08:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 25 Jan 2025 20:08:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e96e01626142171a2a42deeb7a4ced17dcbf43b953e305a64b6b966f9e02b`  
		Last Modified: Fri, 31 Jan 2025 03:13:52 GMT  
		Size: 203.8 MB (203810154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634fdab4d2e5f008e4fa3e02b6be74e3f00a5f346ef2d9db7ac63cc873bd63a1`  
		Last Modified: Fri, 31 Jan 2025 03:13:48 GMT  
		Size: 9.2 MB (9170435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e856cf952543d606be8dfba9d3ba12fb35f067f5b09afcb14b9fa9ed0d0b0857`  
		Last Modified: Fri, 31 Jan 2025 03:13:48 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919caa8515f65adba3d5cb0cf1552a3c36901db754daabc0483287ff007b8066`  
		Last Modified: Fri, 31 Jan 2025 03:13:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:4ab058f622810305c9aff9bac665d6e299c01da929095f4165bace49e9e1a827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3020167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4169336c979fa70faee9a64179b871495dd84d5af54f7580980d43cbfb34320`

```dockerfile
```

-	Layers:
	-	`sha256:ed078e3c4ed437b955d4ff3d4f21aaf551024fb64c395497edf57ad0ff7b058c`  
		Last Modified: Fri, 31 Jan 2025 03:13:48 GMT  
		Size: 3.0 MB (3000954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c0d10097c277a2967c1046ad0c7e4405e65e59609f49f30d2e046e4ec4dfb12`  
		Last Modified: Fri, 31 Jan 2025 03:13:48 GMT  
		Size: 19.2 KB (19213 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-debian-bookworm` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6d6ee6f927e901e5161655ed117cd110469b06caf77c4419bcd044f1cade6d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 MB (237812643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845e03c5a497b076e5940a69c972446257719e9c5728b39a2feecedc80077347`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Sat, 25 Jan 2025 20:08:38 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 25 Jan 2025 20:08:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ARG MAVEN_VERSION=3.9.9
# Sat, 25 Jan 2025 20:08:38 GMT
ARG USER_HOME_DIR=/root
# Sat, 25 Jan 2025 20:08:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 25 Jan 2025 20:08:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 25 Jan 2025 20:08:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1af813797d2fe8002f62d6f9738568b99948fedf770e37f3d9ccf2b1f03e19`  
		Last Modified: Mon, 27 Jan 2025 20:20:14 GMT  
		Size: 200.6 MB (200600137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e1689929fb0d3bf9caec3fac69414519de43490b20389829417184bbb3bed0`  
		Last Modified: Mon, 27 Jan 2025 20:20:10 GMT  
		Size: 9.2 MB (9170437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c310599dd09abba8718606785acfb02f63187967c42ee37eb2a938668b12ba`  
		Last Modified: Mon, 27 Jan 2025 20:20:09 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c354217dd0885729efcf486c1fa0d8770182a1a1ab09c9edc70e6a56b444caf`  
		Last Modified: Mon, 27 Jan 2025 20:20:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:f7a120dd5013be89a151f245508f724c975ac1d43f711575c77e5e6074d9a392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3020631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe72be95492c3e54a3e32e271d2b951b77f3a25f2029423da3652dd057f1d1d6`

```dockerfile
```

-	Layers:
	-	`sha256:2e9952d91298bbd1eb7da2e3cf62f7e1cb36881b4b38a6776721a57658972750`  
		Last Modified: Fri, 31 Jan 2025 06:38:40 GMT  
		Size: 3.0 MB (3001251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9303b7add0b036fc47ac13e57a79e9edc6aa835a60d63e72c851354230ac553a`  
		Last Modified: Fri, 31 Jan 2025 06:38:40 GMT  
		Size: 19.4 KB (19380 bytes)  
		MIME: application/vnd.in-toto+json
