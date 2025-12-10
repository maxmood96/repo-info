## `maven:3-amazoncorretto-11-debian-trixie`

```console
$ docker pull maven@sha256:d225408ad01dc2fe4c8847716cfd872224d1e9f2592fc8d9deb989f6aec8773e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:0f0ee9840c51a074226dc4f7f0906c8c71375f3e16a33fb5e171113fb30123f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.6 MB (241609102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f08ff2fbc2aefbfdb0c640dea64d3d40b3a98d084f3a9f59aab32e81411ef0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:58:02 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:58:02 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 23:58:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 08 Dec 2025 23:58:02 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 08 Dec 2025 23:58:02 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 08 Dec 2025 23:58:02 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 08 Dec 2025 23:58:02 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 08 Dec 2025 23:58:02 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 08 Dec 2025 23:58:02 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 08 Dec 2025 23:58:03 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:58:03 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 08 Dec 2025 23:58:03 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 08 Dec 2025 23:58:03 GMT
ARG MAVEN_VERSION=3.9.11
# Mon, 08 Dec 2025 23:58:03 GMT
ARG USER_HOME_DIR=/root
# Mon, 08 Dec 2025 23:58:03 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 08 Dec 2025 23:58:03 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 08 Dec 2025 23:58:03 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b195f935088aa541a111ddae11bc3ba28fa7f74f77025ea8a55f994a03af4acf`  
		Last Modified: Tue, 09 Dec 2025 01:50:52 GMT  
		Size: 202.6 MB (202588998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9793f2abeb78167c3c0f94e5b17555e5a9b63e7a28d721d3aca778257b3dbe`  
		Last Modified: Mon, 08 Dec 2025 23:58:29 GMT  
		Size: 9.2 MB (9242572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3daf5c078717449bff5569514ff62f784e93a6561df7aa2dd533ad06d43cf554`  
		Last Modified: Mon, 08 Dec 2025 23:58:28 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed41296c3c8c12fe31ee414e55a38f56ac34d5e1d4dede847a48564348e06c8`  
		Last Modified: Mon, 08 Dec 2025 23:58:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:e5f0be6054621f009a73e0f8760fbfa1b99a5ad5f08e88cbf5d46f5faecacedf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd47e72db821e4331ec0a1fd9dcdf60f3f64a0d5bef16b32625653b75e8c2a77`

```dockerfile
```

-	Layers:
	-	`sha256:86e892bc15894bd5446f5666958f5f0ae9f006850d5670db12f8aec74ca6a2a8`  
		Last Modified: Tue, 09 Dec 2025 03:27:53 GMT  
		Size: 3.1 MB (3109753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6d0dbbf8d06881345851625ad393146756acd0af1cf550344ba97c8d1bd7b1b`  
		Last Modified: Tue, 09 Dec 2025 03:27:54 GMT  
		Size: 19.2 KB (19199 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f3bac1d97fd441a5baa32a76386c90d9bf290cd043f52772cdaedb3054e62c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238948343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7eaa526e48aa01c635f88bbe60eeefa20c350b108772feb72c5caea82cdc93a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:04:22 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:04:23 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 00:04:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 09 Dec 2025 00:04:23 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 09 Dec 2025 00:04:23 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 09 Dec 2025 00:04:23 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 09 Dec 2025 00:04:23 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 09 Dec 2025 00:04:23 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 09 Dec 2025 00:04:23 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 09 Dec 2025 00:04:23 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:04:23 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 09 Dec 2025 00:04:23 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 09 Dec 2025 00:04:23 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 09 Dec 2025 00:04:23 GMT
ARG USER_HOME_DIR=/root
# Tue, 09 Dec 2025 00:04:23 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 09 Dec 2025 00:04:23 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 09 Dec 2025 00:04:23 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5888d2b0f94c184c409032a71e90d1e27f65fe51dd8958cad9737c8924843ac`  
		Last Modified: Tue, 09 Dec 2025 00:05:06 GMT  
		Size: 199.6 MB (199566107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b66234626d16f68ca800fd366fbe51177a517b766c7b0ad28e38b82b03ff3a1`  
		Last Modified: Tue, 09 Dec 2025 00:04:53 GMT  
		Size: 9.2 MB (9242570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705cee6dc4b9e1f9c85326be47880a1b898349b3ede8a772777d589c6027659`  
		Last Modified: Tue, 09 Dec 2025 00:04:52 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ec2304dd25e0252756ed1c79b933a656db00913e3b651eb6d4032e602417ba`  
		Last Modified: Tue, 09 Dec 2025 00:04:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:d6a35a021ba79363b280911d1bf890c278fae4500cdb53781190f3e59654f63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4109ec294defee3d6402e84c43b1658a61a21ec509a3a682325baa0cb1eff485`

```dockerfile
```

-	Layers:
	-	`sha256:4d98449512f4e70be3435f2e5a7fa1b629a5ca39f53793e5e064b3bda8d3f6fa`  
		Last Modified: Tue, 09 Dec 2025 03:27:59 GMT  
		Size: 3.1 MB (3110053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98a3de92e49234dd3f668e984061faa98787324c96998601b00d58b41e49e165`  
		Last Modified: Tue, 09 Dec 2025 03:27:59 GMT  
		Size: 19.4 KB (19368 bytes)  
		MIME: application/vnd.in-toto+json
