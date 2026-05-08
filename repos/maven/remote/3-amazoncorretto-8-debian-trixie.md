## `maven:3-amazoncorretto-8-debian-trixie`

```console
$ docker pull maven@sha256:a67f2dd750c2605e843da28ec6f6499670ad6a8e9eee97afe229b45eefdd26ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:c40a5b2211b8772f74186dc14df1c52cd7981225ba03abf6f4de1d8b2a5981a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164741283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f2ae7a864ae4d143516bfc95d8832f2f354753c8c61664d5ca8878f760d3e3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:21:44 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:21:45 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 20:21:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Fri, 08 May 2026 20:21:45 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 08 May 2026 20:21:45 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 20:21:45 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 20:21:45 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 08 May 2026 20:21:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 08 May 2026 20:21:45 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 08 May 2026 20:21:45 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 08 May 2026 20:21:45 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 08 May 2026 20:21:45 GMT
ARG USER_HOME_DIR=/root
# Fri, 08 May 2026 20:21:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 08 May 2026 20:21:45 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 08 May 2026 20:21:45 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1ccaae35ddb686ce70f144cfc7f9e3d3e3cf83b2ff9fe87577130baaf05bcc`  
		Last Modified: Fri, 08 May 2026 20:22:01 GMT  
		Size: 125.6 MB (125647814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cec901efac9fe984cf4705d614c24c60ff9e6d33f6667b6ae7bf4b9610226d2`  
		Last Modified: Fri, 08 May 2026 20:21:59 GMT  
		Size: 9.3 MB (9312237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e008079bd4c468a8a223dbbe764f39744a053311936a8d123ca7defa87e1288`  
		Last Modified: Fri, 08 May 2026 20:21:58 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd32132d0f3a6de746aa2a4b6a473a4e55c7c0271cb3fa0cba74e42a3314ec84`  
		Last Modified: Fri, 08 May 2026 20:21:58 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:c11e8f370b297ff82de011d0daf6ce298e4c4b802a665c4af41e218ae12bcb1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2999780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfff4c5481a693b000c78e93e6105025795c94cff36f8d3a9ede483d909cd91`

```dockerfile
```

-	Layers:
	-	`sha256:d37014528050c99fb459fab0bc33d8c760632e3a67f32e79e9125a7d5b1b8675`  
		Last Modified: Fri, 08 May 2026 20:21:58 GMT  
		Size: 3.0 MB (2982093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd3baac244dee3749f9efe0d2cc44debffd9b65db25e678194485c208f83ef4e`  
		Last Modified: Fri, 08 May 2026 20:21:58 GMT  
		Size: 17.7 KB (17687 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:4b0b9a188d2ebf52ac228cd233f3b1f78b89a141039c914bd5e5f981d2585c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148821173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91487d33cff7f13c4124f82ca797c59bdc6f68e8206c8f90f6a371b390f91d78`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:26:27 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:26:27 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 20:26:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Fri, 08 May 2026 20:26:27 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 08 May 2026 20:26:27 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 20:26:27 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 20:26:27 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 08 May 2026 20:26:27 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 08 May 2026 20:26:27 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 08 May 2026 20:26:27 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 08 May 2026 20:26:27 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 08 May 2026 20:26:27 GMT
ARG USER_HOME_DIR=/root
# Fri, 08 May 2026 20:26:27 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 08 May 2026 20:26:27 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 08 May 2026 20:26:27 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b77f56760f971d310ef9a30effc9b8ef8616749b7893d09e6db2fc9feb4cee`  
		Last Modified: Fri, 08 May 2026 20:26:51 GMT  
		Size: 109.4 MB (109364267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c740da963a719734cfee4633447c88750f14c816f92a51cdee85c2fb0f54d7`  
		Last Modified: Fri, 08 May 2026 20:26:44 GMT  
		Size: 9.3 MB (9312258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4639cd8962799f64230da83b2f40d05f03c1b582286f97cc53094b7472fd9b`  
		Last Modified: Fri, 08 May 2026 20:26:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee057ec794bf4a27afd901307c504448ffa022719500d38a5c1bf88143e7627d`  
		Last Modified: Fri, 08 May 2026 20:26:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:77f87ad10106e33fa07f24daba07f5c23873fe63603ea705bf4da366c3552dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008cf7f1f9a5227c2adfa36d3ca50848cf63a9c7bd091ca16e3f812886825d25`

```dockerfile
```

-	Layers:
	-	`sha256:66d1c269bda0a327587c6c505e4544363a432400cef0a282c0dd58b2963f7751`  
		Last Modified: Fri, 08 May 2026 20:26:42 GMT  
		Size: 3.0 MB (2964914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:029d72f3a39e94faeef7d73179179a5d91b8461d42036fd9119d142bd2221ab9`  
		Last Modified: Fri, 08 May 2026 20:26:42 GMT  
		Size: 17.9 KB (17856 bytes)  
		MIME: application/vnd.in-toto+json
