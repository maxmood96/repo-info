## `maven:3-amazoncorretto-23-debian`

```console
$ docker pull maven@sha256:6b3986c4485ba720abe495cffd7e5243d17d09f6083e43c923c8881790c8f3fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-23-debian` - linux; amd64

```console
$ docker pull maven@sha256:29da3d97b320f8cf5abcee06c7540a5b6da123543b411645fe425eaa921cc849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261644045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8722af39cfd7974db197cf3417ae5d5c7c30814161a5d0ed48772a91edb52d56`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Sat, 07 Dec 2024 17:04:44 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '18bbe2461ff5acb1212f95f3e41034c503460532de21c24f5f935359b2303586 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-23-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
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
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79347c5dfb5b7e191a5f422d3bef6a484f6964a75b11ae6c8fb356d5465d8d5`  
		Last Modified: Mon, 09 Dec 2024 20:31:50 GMT  
		Size: 224.2 MB (224240990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6722fe424e3619e348376ffd1cc75b2627be5d1cacfda4366c48ce9b41edad`  
		Last Modified: Mon, 09 Dec 2024 20:31:47 GMT  
		Size: 9.2 MB (9170438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4270152709991d7e116db0878f19955217f0f7d3acd7adc2dd443ec6df179bc`  
		Last Modified: Mon, 09 Dec 2024 20:31:47 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d392805aefd4733a800c2876a2fbff766c1fa6b8e3fccd588787ce4c536b74a4`  
		Last Modified: Mon, 09 Dec 2024 20:31:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-debian` - unknown; unknown

```console
$ docker pull maven@sha256:70bfdeabc81a775e298ac138807ebbfec9463b4ec556669d9805ec567e38acb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3020458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378881e273445887693e7c8b10a3fb204df4301efcc042840e69090b31fd139a`

```dockerfile
```

-	Layers:
	-	`sha256:2cef979391edf0e810f434439a9c0141f9be41648fff58b8d5cf43eb75dab063`  
		Last Modified: Mon, 09 Dec 2024 20:31:47 GMT  
		Size: 3.0 MB (3001245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f3b0757914a1d81b6a17ecdf00f1d421bbdc824bd3ed7b36cabbaea9a560d6`  
		Last Modified: Mon, 09 Dec 2024 20:31:47 GMT  
		Size: 19.2 KB (19213 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-23-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:4913e322a3886a6c531d7fcede01c650ade5b54e8d43138897fda7ae9c2750d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (258989092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99a0f430948d5a45a4ae7036aa644c4805262ad3c94f885eadbb15b5c204908`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Sat, 07 Dec 2024 17:04:44 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '18bbe2461ff5acb1212f95f3e41034c503460532de21c24f5f935359b2303586 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-23-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Dec 2024 17:04:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
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
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06727bb706706d0066c2269bf6ead6565e2f4e3c1a72c999eb669a715f2587a4`  
		Last Modified: Tue, 10 Dec 2024 02:29:13 GMT  
		Size: 221.8 MB (221758808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779b480759d55ef43f0de932ec7061cd3329df9ea634542d63ec5dca1a9205c5`  
		Last Modified: Tue, 10 Dec 2024 02:29:08 GMT  
		Size: 9.2 MB (9170437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443c2cab7c10d9c35466e057a316b34783cb6ff896bea066e5c484f998564e11`  
		Last Modified: Tue, 10 Dec 2024 02:29:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccc83b55bded8d14bcc625de1704f188c6ecee26d7e70e3a591c9274670a13d`  
		Last Modified: Tue, 10 Dec 2024 02:29:08 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-debian` - unknown; unknown

```console
$ docker pull maven@sha256:ee9165c6c0823b7cf109448f997811c80d67f355daf782c0b1f9ebe4e1e039d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3019643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fcd2530426206825426d3462aa743ee33cd7cd2c8b8f2e6ac2efab8174c4541`

```dockerfile
```

-	Layers:
	-	`sha256:18c2e67e9c94b6ac2589920138c2dd31c629de20efe8a896f536e125987e85da`  
		Last Modified: Tue, 10 Dec 2024 02:29:08 GMT  
		Size: 3.0 MB (3000262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82fd51711e8f9048efa15a91626ca8c1834d6d10eab102a8582936123248ccc6`  
		Last Modified: Tue, 10 Dec 2024 02:29:08 GMT  
		Size: 19.4 KB (19381 bytes)  
		MIME: application/vnd.in-toto+json
