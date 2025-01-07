## `maven:3-amazoncorretto-8-debian-bookworm`

```console
$ docker pull maven@sha256:aec89d19a28025b6e256735ee6dff194e07a8a823e49259718512b2f6fa20179
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-debian-bookworm` - linux; amd64

```console
$ docker pull maven@sha256:b32f0dc07c01477a0a446ab34bb23b9a71668800507d3948c2b8e864a1e796f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163395397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae3c5fa017a4d739fb345728c7cde669a2e90de8dcfc158764f7025c2b16723`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 07 Dec 2024 17:04:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Sat, 07 Dec 2024 17:04:44 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '18bbe2461ff5acb1212f95f3e41034c503460532de21c24f5f935359b2303586 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Sat, 07 Dec 2024 17:04:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 07 Dec 2024 17:04:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 07 Dec 2024 17:04:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 07 Dec 2024 17:04:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 07 Dec 2024 17:04:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 07 Dec 2024 17:04:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
ARG MAVEN_VERSION=3.9.9
# Sat, 07 Dec 2024 17:04:44 GMT
ARG USER_HOME_DIR=/root
# Sat, 07 Dec 2024 17:04:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 07 Dec 2024 17:04:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 07 Dec 2024 17:04:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea57055d233b707639b0b1ae98c2dffd98425e4051a5c77239ab8f66dbd3de6d`  
		Last Modified: Tue, 24 Dec 2024 22:39:11 GMT  
		Size: 126.0 MB (125992335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b1a07cb35708098a508c04492611903e5ec8decbecd5674f3c13a06d7f51b8`  
		Size: 9.2 MB (9170444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ec3a517dcd5b2e7290f3e0749a19baf21bb362ca0c3575e45c37c4ddb70c1d`  
		Last Modified: Tue, 24 Dec 2024 22:39:08 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703c0f7be71cd3a179bb8ed6755fae97aaa70d204845c37e46cf9db83e4096d2`  
		Last Modified: Tue, 24 Dec 2024 22:39:09 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:ae4aab22c63b01e772ef8c72f2be1b4c415b3aa26dd070ced1c4b777b52d635c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2893027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd603ca7c03d5304e87855ee0112eef5a744567a6beb59ecbaa358cebaec8585`

```dockerfile
```

-	Layers:
	-	`sha256:c1db1c26a39bbdb6f34f92c8bb2f708d833543cafc66fa9a111bb2ff56a3d711`  
		Last Modified: Tue, 24 Dec 2024 22:39:09 GMT  
		Size: 2.9 MB (2873803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3899e195f16b6908c2163f975956903f7c5b8c0025ae84b3bc76132379aa5ae`  
		Last Modified: Tue, 24 Dec 2024 22:39:08 GMT  
		Size: 19.2 KB (19224 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-debian-bookworm` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:3f937dc244d00e8ba232d5c7ecfd972cef6b1a3d05f5ea67281bedca42e7a03f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.0 MB (146989295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2556ce27029abdd83aadc8c7cdd8deb87ca39af1a10dea0ba6ae494984ac2b80`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 07 Dec 2024 17:04:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Sat, 07 Dec 2024 17:04:44 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '18bbe2461ff5acb1212f95f3e41034c503460532de21c24f5f935359b2303586 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Sat, 07 Dec 2024 17:04:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 07 Dec 2024 17:04:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 07 Dec 2024 17:04:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 07 Dec 2024 17:04:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 07 Dec 2024 17:04:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 07 Dec 2024 17:04:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
ARG MAVEN_VERSION=3.9.9
# Sat, 07 Dec 2024 17:04:44 GMT
ARG USER_HOME_DIR=/root
# Sat, 07 Dec 2024 17:04:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 07 Dec 2024 17:04:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 07 Dec 2024 17:04:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb98469ebb204fee7bd8a5e73c7698cf537896a3dc8344040ec68331ff78093`  
		Last Modified: Wed, 25 Dec 2024 07:47:11 GMT  
		Size: 109.8 MB (109759105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b0fbead17b87172ee0762b52b37c96df90648200a14e8a4678aa465784f807`  
		Last Modified: Wed, 25 Dec 2024 07:47:09 GMT  
		Size: 9.2 MB (9170429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3656c88111960666dfca000d2e1c9bcb52eb031970d8cebc87b35801f7c9c9a1`  
		Last Modified: Wed, 25 Dec 2024 07:47:08 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b1614c934698b682661c85d73dc6a26f1707c56b8998d8b613884c93e4bd96`  
		Last Modified: Wed, 25 Dec 2024 07:47:08 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:7eb8adac46c8a7144e9a735f3e086c38823f6bfab16107da32916750621a9e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2876015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d091ecfa586ab6c562e8682464ae28bf47ad9fe1cb84ea21b84a67daec163fd7`

```dockerfile
```

-	Layers:
	-	`sha256:b58052a25f279ea77b9da238d31d46bb1c47867336db2e37124b99f5002dee00`  
		Last Modified: Wed, 25 Dec 2024 07:47:09 GMT  
		Size: 2.9 MB (2856621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47ac551eae0332e7008085994d6fde439a038b5fcfef8ebd9ab9309096017098`  
		Last Modified: Wed, 25 Dec 2024 07:47:08 GMT  
		Size: 19.4 KB (19394 bytes)  
		MIME: application/vnd.in-toto+json
