## `maven:3-amazoncorretto-21-debian-trixie`

```console
$ docker pull maven@sha256:a4e2604c77adaa8ecb0cb9d63046efec33007732397922ff3a53879bd84dff8d
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
$ docker pull maven@sha256:adb579262a9a6e2c3d3e91a8e4879fb61d40b98dd8cc6644698e702df9212ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257387632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4baed75e230aae891476ce7286862150d7a236ead979cd647bbafd572d4b1f3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 21 Apr 2026 18:12:16 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 18:12:16 GMT
ENV LANG=C.UTF-8
# Tue, 21 Apr 2026 18:12:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 21 Apr 2026 18:12:16 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:12:16 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:16 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:16 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:12:16 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:12:16 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:12:16 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:12:16 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:12:16 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:12:16 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:12:16 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:12:16 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de0b23b1317da82e80298e438777bd11d2d481f06c64cf19a79b31bd29fc4f9`  
		Last Modified: Tue, 21 Apr 2026 18:12:43 GMT  
		Size: 217.9 MB (217935840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2654f8ae99676f922459add0d878e2821dafce467209e21506872cac8516930f`  
		Last Modified: Tue, 21 Apr 2026 18:12:37 GMT  
		Size: 9.3 MB (9312238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729e0d51c32bbaa06520ecf202dbf2d4830199dd810a554a93ff9b66fc99da01`  
		Last Modified: Tue, 21 Apr 2026 18:12:36 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1382ca67b8bab3e53d1b50bada7457ee104505e9d8830eb969f2a658baf45ed2`  
		Last Modified: Tue, 21 Apr 2026 18:12:37 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:f23805e20a12f6dd274391d234847be6b83377003fc0eecaa54b2d27ad27b624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3121347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2427c00f5f193ab01da87ada9e43071ed028d7a6adf6fbfe1f712de7e007adfe`

```dockerfile
```

-	Layers:
	-	`sha256:3a81d4bdabfc980c9a47e1c5156ebbeb366f8a231afb92432161157511c25af7`  
		Last Modified: Tue, 21 Apr 2026 18:12:37 GMT  
		Size: 3.1 MB (3103653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddc47f4322f25bc0d59b5bdd7f124afedb7b838c58980d85c0d05a78281a4b71`  
		Last Modified: Tue, 21 Apr 2026 18:12:36 GMT  
		Size: 17.7 KB (17694 bytes)  
		MIME: application/vnd.in-toto+json
