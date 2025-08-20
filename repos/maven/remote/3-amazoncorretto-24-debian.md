## `maven:3-amazoncorretto-24-debian`

```console
$ docker pull maven@sha256:691c4b93374b5e81e1ae61e44898582c225afcefc9fa25c03725d63fa50ae0f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-24-debian` - linux; amd64

```console
$ docker pull maven@sha256:2eee786feabf0e92f8bbd65e3fdb1dfb69bdaf242c5c746a8d15c485fe560d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272516850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62be9af7a39021904c3ae7931925ea4e6e743802fd11b4398d08bc7a8cba589`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Tue, 19 Aug 2025 14:41:45 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-24-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 14:41:45 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 14:41:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
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
	-	`sha256:560599b519742f68147f7e59189ba5a765a9f2e1def6da584c11adb7dc5bb1af`  
		Last Modified: Wed, 20 Aug 2025 21:32:10 GMT  
		Size: 233.5 MB (233499941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a2386a0554cec9ae0292ea85b4020c67d9aedf6d36e59caa2c6f8a57ec836c`  
		Last Modified: Wed, 20 Aug 2025 18:39:47 GMT  
		Size: 9.2 MB (9242585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8147a041a15103e1e3d93d914fa960e9dd215c1f880251af16575a5f743c929`  
		Last Modified: Wed, 20 Aug 2025 18:39:45 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba51215ce555031d86ccffa2850c0f7926d600674edf7c36fbc24731e835dc2f`  
		Last Modified: Wed, 20 Aug 2025 18:39:46 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-24-debian` - unknown; unknown

```console
$ docker pull maven@sha256:4419db8bc0834310752d48773263f6260259ae320db7a6a7d05fc9c3d0c5628e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228afdc861ca4b5279abc9cd70752b81f185a4ea966e918757d03ce8570beef1`

```dockerfile
```

-	Layers:
	-	`sha256:c5e66452e3f575e3f76066b6574a8e90f850f394870083a4d9336423ef9438b8`  
		Last Modified: Wed, 20 Aug 2025 20:27:55 GMT  
		Size: 3.1 MB (3109502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54d0df460401a16a1e1c3e36536b70ab2e3b8a7fc7736d1170f067d792651412`  
		Last Modified: Wed, 20 Aug 2025 20:27:56 GMT  
		Size: 19.2 KB (19243 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-24-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:bd9679ff637f5403d34477e0a90a6cf6e405419d54a528bb384eda7b166553ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270744324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d533e22e235a80e438f5e93131bfa96c71f0f2f82e8aeb631439d291c4f2ed03`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Tue, 19 Aug 2025 14:41:45 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-24-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 14:41:45 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 14:41:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
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
	-	`sha256:b2a3c903fb6c92cb76be2e0a80e5337a47e87bf3097f9073d23e2cee8c480ba7`  
		Last Modified: Wed, 20 Aug 2025 21:33:42 GMT  
		Size: 231.4 MB (231364652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ecab6511953c6d334c287ab2b2df4aa21e2d991e0ec6e49941de52896d87b3`  
		Last Modified: Wed, 20 Aug 2025 18:42:00 GMT  
		Size: 9.2 MB (9242588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0ff80f49969fdb4cc92c37aa5fdb6f7f27930f1e65a87282f88c4bcbc4e3ac`  
		Last Modified: Wed, 20 Aug 2025 18:42:00 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fd98886bc016388fe9ffeb33001573444b0fc8dab506f33d5309619688219a`  
		Last Modified: Wed, 20 Aug 2025 18:42:00 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-24-debian` - unknown; unknown

```console
$ docker pull maven@sha256:e7b6015cfddb610a6f99ade41cf5bb303c2aff09583a7b97ca3c5be4e9e2acd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235e40f3a6e84f5393ea27ae36e9e33b12ee6f41aca2592d38dbc79b3905dca7`

```dockerfile
```

-	Layers:
	-	`sha256:f268896d0f62dbdfa86cd6a1f4b966265bebded6d49bbd7f6b603c0fa7856c90`  
		Last Modified: Wed, 20 Aug 2025 20:28:00 GMT  
		Size: 3.1 MB (3109162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f1e9c76ac8d484cf2470c1853aa8e127dd8ff02912c9a26b6178f1a22a89f61`  
		Last Modified: Wed, 20 Aug 2025 20:28:01 GMT  
		Size: 19.4 KB (19411 bytes)  
		MIME: application/vnd.in-toto+json
