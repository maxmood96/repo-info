## `maven:3-amazoncorretto-17-debian`

```console
$ docker pull maven@sha256:123bf5d6bb6f835247a86552c2945e2f23e1a6c67dc20a44ac2cf6692c2ce24a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-debian` - linux; amd64

```console
$ docker pull maven@sha256:d6c9479da554234a4ca73436e08132735a28e6903ffb43598161a45abb03373f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240506674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad289fb61a917779222051608c637b8b6dfe519245c24337f85722de5f5df3b1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:34:35 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:34:35 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 04:34:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 04 Nov 2025 04:34:35 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 04 Nov 2025 04:34:35 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 04 Nov 2025 04:34:35 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 04 Nov 2025 04:34:35 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 04 Nov 2025 04:34:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 04 Nov 2025 04:34:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 04 Nov 2025 04:34:35 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 04 Nov 2025 04:34:35 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 04 Nov 2025 04:34:35 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 04 Nov 2025 04:34:35 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 04 Nov 2025 04:34:35 GMT
ARG USER_HOME_DIR=/root
# Tue, 04 Nov 2025 04:34:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 04 Nov 2025 04:34:35 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 04 Nov 2025 04:34:35 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a029e1426928c3ed6ee783282ac2aba3b853840d4b1dab0a2b6c77f3f050581c`  
		Last Modified: Tue, 04 Nov 2025 09:29:36 GMT  
		Size: 201.5 MB (201484946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f581dd2e114584e7310f1ba18b71c0d91fa7f2d954f142c776169ec1b8de0bd`  
		Last Modified: Tue, 04 Nov 2025 04:35:03 GMT  
		Size: 9.2 MB (9242586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8192e00814057cf607a54d143a0859f0089f8f6f80a1a3005a69517c0425c2`  
		Last Modified: Tue, 04 Nov 2025 04:35:02 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ac1c71cee5d287f65aa7c18a8976af94ede8c2275312eacce50ffe1a79a289`  
		Last Modified: Tue, 04 Nov 2025 04:35:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian` - unknown; unknown

```console
$ docker pull maven@sha256:906e2bf345faf90cd83484e6badbb76d2ca5fbd2beb67005888878b245dc6f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3123167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f92456fe204ed7d50720e12b6b7d40d720e5746fcfa575bb945a0923da60a1`

```dockerfile
```

-	Layers:
	-	`sha256:aba413b76e642cbedf7e072e626b5125b4afd92e30c1d35a40c4ffb4433925e6`  
		Last Modified: Tue, 04 Nov 2025 09:28:30 GMT  
		Size: 3.1 MB (3103968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38540afa19abb980a46c0339b164f82f1acda652b48d9edb041c1714e4ed7729`  
		Last Modified: Tue, 04 Nov 2025 09:28:30 GMT  
		Size: 19.2 KB (19199 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:525301e69c75e7600aa271a1eaf0ef513324c75a927308a219ca5a79e496582a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.7 MB (238697242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59591c67eb2d73304eda9f5254b532a92c37cbdd0e092e2c761c11418f082420`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 17 Sep 2025 20:58:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 17 Sep 2025 20:58:48 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 20:58:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 17 Sep 2025 20:58:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Sep 2025 20:58:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Sep 2025 20:58:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Sep 2025 20:58:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Sep 2025 20:58:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Sep 2025 20:58:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 17 Sep 2025 20:58:48 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Sep 2025 20:58:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Sep 2025 20:58:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Sep 2025 20:58:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a225b68a3c7b7c4c2546043ddbf17397f2ddfdb77843d5e18d583f9dca2c17f9`  
		Last Modified: Tue, 21 Oct 2025 09:52:16 GMT  
		Size: 199.3 MB (199311489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b949509c44592e3324debf31c16f5f2c1759600e0f02b857dd8e10205cb54f21`  
		Last Modified: Tue, 21 Oct 2025 02:30:32 GMT  
		Size: 9.2 MB (9242591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d36f9282a2da6e8967e744c3b76043e4dd18e46cf84ada19b791d6a88f8c227`  
		Last Modified: Tue, 21 Oct 2025 02:30:31 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0be865ff650e541cf7041b3ee52ff9253bc3d06cf9b3b513fa7d6e18c7e075`  
		Last Modified: Tue, 21 Oct 2025 02:30:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian` - unknown; unknown

```console
$ docker pull maven@sha256:c7bfc302611b5b568e8f065814207ecc9bb8914841563cde05d089f2b8037dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f21a4b608a1d50f7e7c88a52a95049cb3cc94850ead35a9776ae7fbfd77f60`

```dockerfile
```

-	Layers:
	-	`sha256:5247984f24279c84a2f5a1ff9db6d5daa5f5b7894e90754b3ccb9b726f58a839`  
		Last Modified: Tue, 21 Oct 2025 08:27:38 GMT  
		Size: 3.1 MB (3101074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:065aaa78f197c4ee224ec42cc1d3c8fc5cb61101bb4539b19023cfc1070d3ad5`  
		Last Modified: Tue, 21 Oct 2025 08:27:39 GMT  
		Size: 19.4 KB (19410 bytes)  
		MIME: application/vnd.in-toto+json
