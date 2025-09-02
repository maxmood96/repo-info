## `maven:3-amazoncorretto-21-debian-trixie`

```console
$ docker pull maven@sha256:8e41e92f6e518052a06a80b047f369ead41236e79f13b75703860856e982e6c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:9db4aa6a17593d6767ab29ebb083f27de5ae5e73854ec8cec9f75dafdf39ccf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.2 MB (255159992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19effd548a7baf43587388836ce50adafbdd6fedb16257f8ae77096f092631bb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Tue, 19 Aug 2025 14:41:45 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 14:41:45 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 14:41:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:513c1195652b697372d3216fdd0c7ad81a32942faa93ccb66ee9905a2d81721c`  
		Last Modified: Tue, 02 Sep 2025 02:36:37 GMT  
		Size: 216.1 MB (216143093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7158d3f89fa7a52e2d1ba5b2247128050e1fe043deb7231ecc6d3ea818066575`  
		Last Modified: Tue, 02 Sep 2025 01:14:04 GMT  
		Size: 9.2 MB (9242575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1f7b2075e771ae93a5c2a5eb10705a505557048df5e7074550086d19942573`  
		Last Modified: Tue, 02 Sep 2025 01:14:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c301080fae5372d676a6218f849842fdb8dca63a4956b931b4136ae1f76ca3`  
		Last Modified: Tue, 02 Sep 2025 01:14:03 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:ded3521e5929bf715ec7452f53c10d9970bb9274fab2959951a03e8c248d4fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3119651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8d0b58212e2c58ea26fdc0ea8c2bec4f45030bd948a29bbd8dd655d0d6da11`

```dockerfile
```

-	Layers:
	-	`sha256:3053e0baffb1ef5be1629ce5e7966013f982cd734b4cb1281898fab110ea7f15`  
		Last Modified: Tue, 02 Sep 2025 02:28:26 GMT  
		Size: 3.1 MB (3100408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ec8fe8d42770167d0b7379f81a349bf41847288c15185b540fac61e9b722d72`  
		Last Modified: Tue, 02 Sep 2025 02:28:27 GMT  
		Size: 19.2 KB (19243 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:fb86634d623fd8895653628524dc051d074400c4fb1197cb072407c43538f551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.5 MB (253461556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661b841ca8da17bec0583c369a5bb1615532be68c6f141b61929db98057c1d63`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Tue, 19 Aug 2025 14:41:45 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 14:41:45 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 14:41:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:a73452ee2bfa79891699f700437d890c434b3e3cbd9215135ef0576e4a77a643`  
		Last Modified: Wed, 20 Aug 2025 21:35:36 GMT  
		Size: 214.1 MB (214081885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7925385bf325d92fb997be9b02325d8f2f63638ee28b2c84b755c6581802c075`  
		Last Modified: Wed, 20 Aug 2025 18:40:56 GMT  
		Size: 9.2 MB (9242588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb61cd46fc4fa36e3760226520843424f74024f8d278e0e32a698607a953dcf0`  
		Last Modified: Wed, 20 Aug 2025 18:40:55 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cd328812cd0fdbc3aab5781d3b9f0a037f810fdb7c7082978d358969afd936`  
		Last Modified: Wed, 20 Aug 2025 18:40:55 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:361b8d1b837aeb11acf3a8fbcdfd4ee278952d0df52523aed25f61e0de4a8331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3119483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b57a43ce668287659ebd246ffde7fcebd5ce550a3cd6ad5ea98e75a499e369`

```dockerfile
```

-	Layers:
	-	`sha256:db1a4a88de4f611c0c0f21df4a2bb499fede00ce5f15403483b79e06d5cae7bb`  
		Last Modified: Wed, 20 Aug 2025 20:27:51 GMT  
		Size: 3.1 MB (3100071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cb9c6914cc4ed1e0b63bae6b064d34e768fff02f787f98044d59bf381687d10`  
		Last Modified: Wed, 20 Aug 2025 20:27:51 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json
