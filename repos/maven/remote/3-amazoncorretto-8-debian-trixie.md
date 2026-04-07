## `maven:3-amazoncorretto-8-debian-trixie`

```console
$ docker pull maven@sha256:074d8f7aa6039b59fb5cd7d55980bf3e2bd5d411fecb483e46b51c2b7bc0eec1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:f66538a8f1402f8f65da35b5eb958be3f2f4438d2ec786fd7a7080f729f54067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164734351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db92ed426db047f89dab1ca83f06ecb8cc5b710153d13f7f032d824009814774`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:10:07 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:10:07 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 05:10:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Tue, 07 Apr 2026 05:10:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 05:10:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:10:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:10:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 05:10:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 05:10:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 05:10:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:10:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 05:10:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 05:10:07 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 05:10:07 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 05:10:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 05:10:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 05:10:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b32e314833d1eb99fa640f90d07df73d33d25fbc6e0bb14691dca00715178a7`  
		Last Modified: Tue, 07 Apr 2026 05:10:25 GMT  
		Size: 125.6 MB (125646489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4007b6e18847493ab8f2f2838a93a69013dc012e07811cb4cd360aa9efc7ec`  
		Last Modified: Tue, 07 Apr 2026 05:10:23 GMT  
		Size: 9.3 MB (9311188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9eff51b26629952a52d10f7a2b01f57cb77ee54cc16fed5b5121446706e5565`  
		Last Modified: Tue, 07 Apr 2026 05:10:22 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d909eec3e27a4f64db877c9462365fc96f8028daa41207ab8230b38735fe97`  
		Last Modified: Tue, 07 Apr 2026 05:10:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:42709f64af468f3b8c774c5535afb9bcdd4bc813ad7a2e9d4e522daf1368ee29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3001305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2686b7fe6c5926fc780ca5e3b39673e185ca7ed2b23953105b60e02b6284db`

```dockerfile
```

-	Layers:
	-	`sha256:1148d65cded58ac0b7e9a76f40aa2ce67ad940802bdcc103e1d229d7a6b7069b`  
		Last Modified: Tue, 07 Apr 2026 05:10:22 GMT  
		Size: 3.0 MB (2982093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1299d07434295fb813852b5b54e7857cc186060a92ac7a1b5b057ad09c384d98`  
		Last Modified: Tue, 07 Apr 2026 05:10:22 GMT  
		Size: 19.2 KB (19212 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:e10810b0702c513bd96f391911c2127dd8ce92b2c3952252d7fdce81f3b825af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148822835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405c5becb61b990cf4687e7b2225b95fd492ea53260fd6f2eda01884d1fa42e4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:17:00 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:17:00 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 05:17:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Tue, 07 Apr 2026 05:17:00 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 05:17:00 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:17:00 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:17:00 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 05:17:00 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 05:17:00 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 05:17:00 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:17:00 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 05:17:00 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 05:17:00 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 05:17:00 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 05:17:00 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 05:17:00 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 05:17:00 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d3e8097063f046e4978a10ceb0c57283a495beed11ee3e547da4401fe7130e`  
		Last Modified: Tue, 07 Apr 2026 05:17:17 GMT  
		Size: 109.4 MB (109372053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be571040fedfeb0366b1481eecc6997988d9906a875368fdb88f1236138ed76d`  
		Last Modified: Tue, 07 Apr 2026 05:17:15 GMT  
		Size: 9.3 MB (9311197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a427bd3d0ea47562ecd510c7ccc804d545ecaaf799f40cdcfa4f48cf442d2f1c`  
		Last Modified: Tue, 07 Apr 2026 05:17:14 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519152558bd4bfe66bf76f61609b4f11511d56dcb18136b679b0e69f2c93a746`  
		Last Modified: Tue, 07 Apr 2026 05:17:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:9e37a417550d0bda9bac337be9a639cfcef0c7a8fe0cbe46973dcf1f4a809835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c4eb6685b6e9707c7154be9c418b6b3e03677b66a7b61d0784ab70abc865a6`

```dockerfile
```

-	Layers:
	-	`sha256:e0d112220d94d987799683461ae293aa2c13458358992542c6907e9329a1a534`  
		Last Modified: Tue, 07 Apr 2026 05:17:15 GMT  
		Size: 3.0 MB (2964914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d93ed2e2208dbfb21d6aa6fe8d809db9aa1b24343023965524b6b9d6dfd43ce2`  
		Last Modified: Tue, 07 Apr 2026 05:17:14 GMT  
		Size: 19.4 KB (19380 bytes)  
		MIME: application/vnd.in-toto+json
