## `maven:3-amazoncorretto-21-debian-trixie`

```console
$ docker pull maven@sha256:72ddb90f5840f2e4e8a235b3e454c761738b7b73b55c28c0b66a729d6e206b31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:6a7fd877420abc63da7a0c549b9b89c8e0faeab8c21a5304be0b09f61f9b32a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.6 MB (255623169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b81df9a871a77d564a05999049b8cc2eb8853b0e89cfa125dd8e878881f0f1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 01:42:22 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:42:22 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 01:42:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 14 Nov 2025 01:42:22 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 01:42:22 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:42:22 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:42:22 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 01:42:22 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 01:42:22 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 01:42:22 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:42:22 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 01:42:22 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 01:42:22 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 01:42:22 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 01:42:22 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 01:42:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 01:42:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ec9cedbd8ab29d8ed331a8a417510eb2693b02befabe413011cba28d74baa7`  
		Last Modified: Fri, 14 Nov 2025 03:41:02 GMT  
		Size: 216.6 MB (216601448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d321f7eb2b08bdae0c33aba555c0f4700f2dbae54a312819d5c8d0d0cef1f5f`  
		Last Modified: Fri, 14 Nov 2025 01:42:54 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e54a55c293942d6ca9d477ac094cb3755289c41eb6e0d5bfe73bbfa4e69c98`  
		Last Modified: Fri, 14 Nov 2025 01:42:53 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b98baa82a99e25609ef625aaf4e8ef898cf6e9e2860e6a6bcb158b45af0c283`  
		Last Modified: Fri, 14 Nov 2025 01:42:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:4e00f4d2e7818e09387524480aeaeffa8f375dd3ffb45dd8cd2f403521dd5738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3123067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc00210a87ffe7b9041c598a5cb854eb663f326b3c11ad50512ecfb5c48c608`

```dockerfile
```

-	Layers:
	-	`sha256:037a52a04b7cd77b09250b7c976010fe7c60dbab2225cc48fa318fdeb111a300`  
		Last Modified: Fri, 14 Nov 2025 03:28:34 GMT  
		Size: 3.1 MB (3103867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b36aa6bf5efea66c70e4c2a4ee78510d7d4efea70d8cc8b7b3201bb3f7db5ac`  
		Last Modified: Fri, 14 Nov 2025 03:28:35 GMT  
		Size: 19.2 KB (19200 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:7f8da75916cd7269ea407c2de312acfa179b85dc26382fafe90a3ffc89d63c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253937543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d02f13b87faa9e90fad7d8f894e9ba54eec8e5f8a37d61e4089ff0eb39721ae`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:19:26 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:19:26 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:19:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 18 Nov 2025 05:19:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 18 Nov 2025 05:19:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 18 Nov 2025 05:19:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 18 Nov 2025 05:19:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 18 Nov 2025 05:19:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 18 Nov 2025 05:19:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 18 Nov 2025 05:19:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 18 Nov 2025 05:19:26 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 18 Nov 2025 05:19:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 18 Nov 2025 05:19:26 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 18 Nov 2025 05:19:26 GMT
ARG USER_HOME_DIR=/root
# Tue, 18 Nov 2025 05:19:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 18 Nov 2025 05:19:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 18 Nov 2025 05:19:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1833ca47eecf2eba86e5db679913b120d30cd04b05d1bb4b3ea0ad0fc162f69d`  
		Last Modified: Tue, 18 Nov 2025 06:43:38 GMT  
		Size: 214.6 MB (214555302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd7e0497a65b5350b2cdaf258d649c2deeb8d374610dec7ac91c1850bc8cb82`  
		Last Modified: Tue, 18 Nov 2025 05:19:58 GMT  
		Size: 9.2 MB (9242595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb192418d371baa3123f61419858e6f6ef668a7b92d3e473819bb4ba64f7161`  
		Last Modified: Tue, 18 Nov 2025 05:19:57 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0371a83b8f3023f2826730ac08cc84f39ce6fa0b5b8739ee32a39a94eb227210`  
		Last Modified: Tue, 18 Nov 2025 05:19:57 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:3aec602683d81f0065684c68b72f4ac0e4437db04d5c2dfe635559826f844866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea815ee3755d0a42ee412df55cac6a0797ba6bbaf720ac2554d9db827edd7ef`

```dockerfile
```

-	Layers:
	-	`sha256:7b517d2fa8a120ec7aa9b3efb902b19001274fbbb96935fa8f054d05c562a0dc`  
		Last Modified: Tue, 18 Nov 2025 06:29:15 GMT  
		Size: 3.1 MB (3103524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fe8d5698ea57132cbadff0b56d774eb2e213a6c5ece1f0bef2dba0c6fa07b59`  
		Last Modified: Tue, 18 Nov 2025 06:29:16 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json
