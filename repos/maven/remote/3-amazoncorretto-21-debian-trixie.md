## `maven:3-amazoncorretto-21-debian-trixie`

```console
$ docker pull maven@sha256:1cd311bf4e4f418a640fda170bb8c1eba838fd1daf2b87eab2c4158425382856
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:099f503288ed7dd6974ccc0ad37ca6ceb91a5c1453fe9f30425b616c493c2024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258698256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f33e32147374042644e7230b3a8c738751d984824a393702ad9464ebc80bc58`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 21 Apr 2026 18:12:25 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 18:12:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Apr 2026 18:12:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 21 Apr 2026 18:12:25 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:12:25 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:25 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:25 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:12:25 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:12:25 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:12:25 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:12:25 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:12:25 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:12:25 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:12:25 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:12:25 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a82280236e824c64f7aad555a993d6cfcb8561538a06b604f632b725cdd7d4`  
		Last Modified: Tue, 21 Apr 2026 18:12:51 GMT  
		Size: 219.6 MB (219609414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d26d8bf9bb9912e3b2fbdfd8aa523d92b7e4347b552eeb615c757f12730e7e4`  
		Last Modified: Tue, 21 Apr 2026 18:12:47 GMT  
		Size: 9.3 MB (9312197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27813abcb005504f41e55b9078a46067dc65bf62030a3bbaecd3c0ccd412702`  
		Last Modified: Tue, 21 Apr 2026 18:12:45 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511245866157a23a9b7b3f0d964ac2a2b2662bb7f4f647aba40bdff1dc0c9b0a`  
		Last Modified: Tue, 21 Apr 2026 18:12:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:e049bcf0d16d27fd1c60fd0f54cc719c3e1ead6507b0639c25ccb2221cdec05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3121514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f51b1df832fc3eadbeec0daac11713d85328bb64626866ae1aa78f1f80e28fc`

```dockerfile
```

-	Layers:
	-	`sha256:603c752b5762c5141d01ff04421e8e9f64d3b13e959bb390abb998e6c21f7d2b`  
		Last Modified: Tue, 21 Apr 2026 18:12:46 GMT  
		Size: 3.1 MB (3103990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9771f0b5789b781bdd7dff5cadbac44883ccce818b1135136a9e1995b7a54c52`  
		Last Modified: Tue, 21 Apr 2026 18:12:46 GMT  
		Size: 17.5 KB (17524 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:2b52d3266b907e708c76dae87f0e09445ec4e5543b1821388ff76838b27573f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 MB (254383461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcad92aa5ed26a28ff02672e70fb9ff621a08cb1606bbbc3591497eec4ccb4f1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:26:06 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:26:06 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 02:26:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 22 Apr 2026 02:26:06 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 22 Apr 2026 02:26:06 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 02:26:06 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 02:26:06 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 22 Apr 2026 02:26:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 22 Apr 2026 02:26:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 22 Apr 2026 02:26:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:26:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 22 Apr 2026 02:26:06 GMT
ARG USER_HOME_DIR=/root
# Wed, 22 Apr 2026 02:26:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 22 Apr 2026 02:26:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 22 Apr 2026 02:26:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6635bfe95bb45da17004a9c22cba4a976923e72c3199e6361085d9eeb8a051c2`  
		Last Modified: Wed, 22 Apr 2026 02:26:31 GMT  
		Size: 214.9 MB (214926598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7cf939c78fcc94ce3ce785fa3bb286c360508130b73e9923fd0c036316a243`  
		Last Modified: Wed, 22 Apr 2026 02:26:26 GMT  
		Size: 9.3 MB (9312255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380635f34eda643a2dfd295aea65ebaf3065256ced3002c9e370d45853845b2e`  
		Last Modified: Wed, 22 Apr 2026 02:26:25 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c661a821d79e81225e2de74381dfc0fc5b1cee8d93e7b00cf92b5bd6e5f3ca`  
		Last Modified: Wed, 22 Apr 2026 02:26:26 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:21b28e49df4bad8a62c1e3d96afac145515c4e7f962d385c7140708579e944cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3121993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550df84a8e4f6579b49b7c41e7419993dd0bc12bbc41d72e40cad603d6fa9241`

```dockerfile
```

-	Layers:
	-	`sha256:733f45b2244eeb79559b028c7faf1070c21199df8a37da3d627e7847ea64d66d`  
		Last Modified: Wed, 22 Apr 2026 02:26:26 GMT  
		Size: 3.1 MB (3104299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fff0e301b3a11f3d422acc0f868414f0f6d2e58afc875e489993781eb7fdb01`  
		Last Modified: Wed, 22 Apr 2026 02:26:26 GMT  
		Size: 17.7 KB (17694 bytes)  
		MIME: application/vnd.in-toto+json
