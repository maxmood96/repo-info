## `maven:3-amazoncorretto-23-debian`

```console
$ docker pull maven@sha256:d62ab01007a7474c8f0b00de62da6a95f4dc8dfdb6af9dab55cf18d11722ab98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-23-debian` - linux; amd64

```console
$ docker pull maven@sha256:b654e142c5f2aca5edb62f645f75473b0dcac218f184c3d02cd68e68d51bff77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.9 MB (261859981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e762acb229bf99f8a17b403ff607a20edac6e0e0321321a58b06f69223844fd5`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 25 Jan 2025 20:08:38 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Sat, 25 Jan 2025 20:08:38 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-23-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 25 Jan 2025 20:08:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ARG MAVEN_VERSION=3.9.9
# Sat, 25 Jan 2025 20:08:38 GMT
ARG USER_HOME_DIR=/root
# Sat, 25 Jan 2025 20:08:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 25 Jan 2025 20:08:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 25 Jan 2025 20:08:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f04174d2f1d64cfd8db62a9d6c9789415a7652dd33d9ce6050bfeb9c68061fd`  
		Last Modified: Tue, 25 Feb 2025 02:36:15 GMT  
		Size: 224.5 MB (224469207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d280923930760845232dd18e7089d7a55183ce0feed9ea1da2e859bc44bd05b`  
		Last Modified: Tue, 25 Feb 2025 02:36:10 GMT  
		Size: 9.2 MB (9170435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28289f2c2a09b08bac9c9d85b21ac79edea63e2e30043fb930f2a37a2ad16e`  
		Last Modified: Tue, 25 Feb 2025 02:36:10 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f085031765c1365418b76841769a04af8af9c5132d0a9476f036d691d99e6b0e`  
		Last Modified: Tue, 25 Feb 2025 02:36:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-debian` - unknown; unknown

```console
$ docker pull maven@sha256:0af768f95100e07dd32dd0543db454692ed60826a68703425cc6d2de3e3745c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3016238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ed28a256295cd4bc8cafa60048b2e553a67abaea1459e1a3966147a295a1a5`

```dockerfile
```

-	Layers:
	-	`sha256:4b94fe6914aaf70613a02672bbb9eac1a6ad1b927d75d1ce3ba729c25ee3c931`  
		Last Modified: Tue, 25 Feb 2025 02:36:10 GMT  
		Size: 3.0 MB (2997025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6236ca276e953ff9c623bc30e2e08e04e5033243cef3825ff3ad36a3b7c57db`  
		Last Modified: Tue, 25 Feb 2025 02:36:10 GMT  
		Size: 19.2 KB (19213 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-23-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:330b1f5b3e269d01b7d2be18dba4759c72e6ef7087a9879ebea0534f8f76426b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.3 MB (259272246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acae42ad6f92f7d77420cae41c6a72fe1284b099d3cfa68e96132b428b9e3638`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 25 Jan 2025 20:08:38 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Sat, 25 Jan 2025 20:08:38 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-23-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 25 Jan 2025 20:08:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ARG MAVEN_VERSION=3.9.9
# Sat, 25 Jan 2025 20:08:38 GMT
ARG USER_HOME_DIR=/root
# Sat, 25 Jan 2025 20:08:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 25 Jan 2025 20:08:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 25 Jan 2025 20:08:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c602973971936d89d2f931f9f173929bdd5cc85aee9aec21af31adf1ec5a03`  
		Last Modified: Wed, 05 Feb 2025 14:47:56 GMT  
		Size: 222.1 MB (222059893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858d2270f7f56ba0eb7f676970171bbdb7f2f506ff7fc8a627d80f7266bccdbe`  
		Last Modified: Wed, 05 Feb 2025 14:47:52 GMT  
		Size: 9.2 MB (9170437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e62a181b7e2643af2942781c3d94e76aeb1fd2f1b3ff4765fb938f173c751d4`  
		Last Modified: Wed, 05 Feb 2025 14:47:51 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1267d0621fa2f3bbde22d8730aa40f3b2293295ad04def4ff8b2b6cb6882e969`  
		Last Modified: Wed, 05 Feb 2025 14:47:51 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-debian` - unknown; unknown

```console
$ docker pull maven@sha256:e228180043e67e941bc012c5761dfef546b6516e1e8a8fa5189171ed1015d07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2344be8117ab63a11a7c24fc1cc4f403102aeb2e27b630f7b1490f8ca171ce0`

```dockerfile
```

-	Layers:
	-	`sha256:5ed8743384d13b0d9f49c61418a75144f3abc18bc18f50a70ba0e13a22f81933`  
		Last Modified: Wed, 05 Feb 2025 14:47:51 GMT  
		Size: 3.0 MB (2996027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72f935b274ebaa7be097b94004066d30d7ced8a274afc33412605616ade16e7b`  
		Last Modified: Wed, 05 Feb 2025 14:47:51 GMT  
		Size: 19.4 KB (19382 bytes)  
		MIME: application/vnd.in-toto+json
