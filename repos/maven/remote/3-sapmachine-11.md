## `maven:3-sapmachine-11`

```console
$ docker pull maven@sha256:e886edde157b0d3400d7120246c2fd5412608704936d84f221a5548289b0e8ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-sapmachine-11` - linux; amd64

```console
$ docker pull maven@sha256:6ab321c44fb50ac20a92b05d3862e14e004dfb28802795f13c9d85881ea01c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.4 MB (265388576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d9af0c908ec48a3efbc634ce10e2fe3f3aff7158b8d3c40e8431d484ceaa99`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:44 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:44 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:44 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.27 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["jshell"]
# Sun, 22 Jun 2025 10:21:55 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ARG MAVEN_VERSION=3.9.10
# Sun, 22 Jun 2025 10:21:55 GMT
ARG USER_HOME_DIR=/root
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 22 Jun 2025 10:21:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 22 Jun 2025 10:21:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307e551b77ecfd4b71a36e426a2a6dadee446efadbec07ad80dee913ea3fa684`  
		Last Modified: Tue, 03 Jun 2025 15:24:50 GMT  
		Size: 201.3 MB (201260265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea520d894fc9939cc0b047abaf1969aa6f682d682a3611722f4b33fed1d099b`  
		Last Modified: Mon, 23 Jun 2025 17:31:17 GMT  
		Size: 25.5 MB (25458532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635efe2f01a4cfe8f8a1bc9abb472662f91cd778f8d95d0472de490a79970631`  
		Last Modified: Mon, 23 Jun 2025 17:31:09 GMT  
		Size: 9.0 MB (8953405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1ed9a9926943ef9c99098d13a8d9160da6341b17a30c43970ade469e1a8d4a`  
		Last Modified: Mon, 23 Jun 2025 17:31:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d53ce326404792a8ccb977c6753d1f0871a1f9766c30f64193683ab6b0c02a`  
		Last Modified: Mon, 23 Jun 2025 17:31:08 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-11` - unknown; unknown

```console
$ docker pull maven@sha256:c315c0c2d8fde6c5a6d3322424cfcfa91900ab1b482bcd8ac687d9e842686f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4344790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab6317284adb6e608e535ef1a9806b495d2e5e0afaff07d4d300dc3f9fbb2a8`

```dockerfile
```

-	Layers:
	-	`sha256:55e395d281b75d75703d08b018fac08e262d37b03b8b65689999f71efe660018`  
		Last Modified: Mon, 23 Jun 2025 20:34:07 GMT  
		Size: 4.3 MB (4328245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40ebb296110e1ef9b0ff0ea76da664b83e98e9f89898721c932126f6eeaa01b2`  
		Last Modified: Mon, 23 Jun 2025 20:34:08 GMT  
		Size: 16.5 KB (16545 bytes)  
		MIME: application/vnd.in-toto+json
