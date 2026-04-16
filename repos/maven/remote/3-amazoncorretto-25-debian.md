## `maven:3-amazoncorretto-25-debian`

```console
$ docker pull maven@sha256:4461c0a0e701b4f1eab684b132a89dcb943ca05e04be2641bd843e0ee70e1173
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-debian` - linux; amd64

```console
$ docker pull maven@sha256:ea6913959561758ccc00ade6c808621ff6b54e45016a51fed219cd7dde70a6c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277326527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312fabf6f98652d63b04c35f901b2952eea06929a780e1e22b906f9eb2972888`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:52:16 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:52:17 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 22:52:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 15 Apr 2026 22:52:17 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 15 Apr 2026 22:52:17 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:52:17 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:52:17 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 15 Apr 2026 22:52:17 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Apr 2026 22:52:17 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 15 Apr 2026 22:52:17 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 22:52:17 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 15 Apr 2026 22:52:17 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 15 Apr 2026 22:52:17 GMT
ARG MAVEN_VERSION=3.9.14
# Wed, 15 Apr 2026 22:52:17 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Apr 2026 22:52:17 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Apr 2026 22:52:17 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Apr 2026 22:52:17 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e900490f81b7389e7886273b69e6d2e04bba52636275c12f71b01bb1535b254c`  
		Last Modified: Wed, 15 Apr 2026 22:52:44 GMT  
		Size: 238.2 MB (238238655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0581614ffc7f1b726e904e72e5747758b64c044c2178f636eb6d36274ebba9cc`  
		Last Modified: Wed, 15 Apr 2026 22:52:40 GMT  
		Size: 9.3 MB (9311195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb5a324a391d01ad132813106202a1f8081956e2e49b99d18435105d70446a5`  
		Last Modified: Wed, 15 Apr 2026 22:52:39 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d8c9a512982a9bdada91825330ba1860380a1db8ef3f51032628b4dfb3cc1e`  
		Last Modified: Wed, 15 Apr 2026 22:52:39 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian` - unknown; unknown

```console
$ docker pull maven@sha256:d4acd3cb317c6506142f96a61d9d0b615ab78ad172c432eef005ce12eb9ddabd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3132290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a3e71d7069bde79095aa424c23939ab1200b863358bf4ff881202a270db50a`

```dockerfile
```

-	Layers:
	-	`sha256:180649503a0591ea76d057f36a8d836d5d1ce09da9468b79cb227fd776d128a5`  
		Last Modified: Wed, 15 Apr 2026 22:52:39 GMT  
		Size: 3.1 MB (3113090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1729e661e31a92414dca637056018b326074ca373fd591a40590b1585eb1aa`  
		Last Modified: Wed, 15 Apr 2026 22:52:39 GMT  
		Size: 19.2 KB (19200 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:776ea99e42af0eb977a983a381b97320573cda921a6259da7f21b89e6e11bfac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.8 MB (275804659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db57b4587e2b93ee24f7a38ac1874aa336bbaa2340b7e8f0b4c640eef2ab1f14`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 23:18:34 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:18:34 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 23:18:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 15 Apr 2026 23:18:34 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 15 Apr 2026 23:18:34 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 23:18:34 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 23:18:34 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 15 Apr 2026 23:18:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Apr 2026 23:18:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 15 Apr 2026 23:18:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 23:18:34 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 15 Apr 2026 23:18:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 15 Apr 2026 23:18:34 GMT
ARG MAVEN_VERSION=3.9.14
# Wed, 15 Apr 2026 23:18:34 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Apr 2026 23:18:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Apr 2026 23:18:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Apr 2026 23:18:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc55e58816eab72781f7c69573eca6164f6b6a997a719b18fd73578a5b4286d`  
		Last Modified: Wed, 15 Apr 2026 23:19:01 GMT  
		Size: 236.4 MB (236353876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f40b2c04d20c97fdd2270b3275d4d36b8c2ef51400c27671d7d4e4b90e5266`  
		Last Modified: Wed, 15 Apr 2026 23:18:57 GMT  
		Size: 9.3 MB (9311193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0918ed6746db426304a375e39e0031becec756e02b1796418d57674027ae6306`  
		Last Modified: Wed, 15 Apr 2026 23:18:56 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d849ec9eae9de8d6be529c280b02534386f90d01e70a87dade8c196980bab6`  
		Last Modified: Wed, 15 Apr 2026 23:18:57 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian` - unknown; unknown

```console
$ docker pull maven@sha256:a0dc193d68781c6a258d35eb86a3936177833a989cfcdd1e0a4122c31b011cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3132119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e183a5ec747abaa532d48f6e0d2e4bdf69c68f70fd2c9ff0cfa8f9f45ad6d05`

```dockerfile
```

-	Layers:
	-	`sha256:8a784c600543fdb631bc9a50c67bcad31c2cba5a4b0cc246d9d2b2f21744e580`  
		Last Modified: Wed, 15 Apr 2026 23:18:57 GMT  
		Size: 3.1 MB (3112750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccb18a7f08895ae1276b5b458e77df2ed5ac3f38ab02293e179e41090cb694e3`  
		Last Modified: Wed, 15 Apr 2026 23:18:57 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json
