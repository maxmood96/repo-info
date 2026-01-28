## `maven:3-amazoncorretto-25-alpine`

```console
$ docker pull maven@sha256:90bd1958af93cdd8b916c4819a15b42914b611b749563828fb6c7ed4ded667d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-alpine` - linux; amd64

```console
$ docker pull maven@sha256:7a49ce81cb366976223d9e84c89164a1a6a86dbe3e1d4627b49a1d2996fa737e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196352904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce92788fb72e5436eab80db0475d334127ece6a51e81c504bc3c3cb0e653e28`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:01:45 GMT
ARG version=25.0.2.10.1
# Wed, 21 Jan 2026 19:01:45 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:01:45 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:01:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 21 Jan 2026 19:21:45 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 21 Jan 2026 19:21:45 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 21 Jan 2026 19:21:45 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:21:45 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:21:45 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 21 Jan 2026 19:21:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 21 Jan 2026 19:21:45 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 21 Jan 2026 19:21:45 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 21 Jan 2026 19:21:45 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 21 Jan 2026 19:21:45 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 21 Jan 2026 19:21:45 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 21 Jan 2026 19:21:45 GMT
ARG USER_HOME_DIR=/root
# Wed, 21 Jan 2026 19:21:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 21 Jan 2026 19:21:45 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 21 Jan 2026 19:21:45 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fe0a027d97a838ab13b2e3d57d7525a5569c5db5279b7348af4ebd22438c12`  
		Last Modified: Wed, 21 Jan 2026 19:02:06 GMT  
		Size: 180.8 MB (180759153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdb6bad7ea862f904007724bcf863246744bd244c69ab7b028a1998b6dd3473`  
		Last Modified: Wed, 21 Jan 2026 19:21:52 GMT  
		Size: 2.4 MB (2420360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dc6aa3d294228e1155d478ee22707538e363256f05809d5d31af0c5f4b51bf`  
		Last Modified: Wed, 21 Jan 2026 19:21:52 GMT  
		Size: 9.3 MB (9312247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae38f165b3fd1af42add42b2d071d4068e5c6b36990ceb0ec43b4c8682ae42e`  
		Last Modified: Wed, 21 Jan 2026 19:21:52 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa1a10c72758b85ecd8e449b09597f3b0aa7a86976dc73170286b70cd09c050`  
		Last Modified: Wed, 21 Jan 2026 19:21:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:d36dcbc0e1a961ce8883ce24ae387153839726b546e6e519211762e3d0efda46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **753.1 KB (753089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89919c9c7a50f5a3809163eacbf285f51425a17dba4d932b181dd4d442446c17`

```dockerfile
```

-	Layers:
	-	`sha256:2a800c363483692b1ccf2e2fbb049a42d6d7c5d9f467460d24aec8307977d0e2`  
		Last Modified: Wed, 21 Jan 2026 19:21:52 GMT  
		Size: 736.7 KB (736727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abf2e0b7176171f6f6afe1b5c77e0c21b13af820e3573dcba4efde74b609d877`  
		Last Modified: Wed, 21 Jan 2026 19:21:52 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5547d8f8d72d3ce7d1dfd777e69d8266a811da8cdda8b5f50369f2f8c860e334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194384360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24de594af36996c77573b6f9fb06c050617f4df96e81c65c16ca09960c6bd20c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:54:31 GMT
ARG version=25.0.2.10.1
# Wed, 28 Jan 2026 02:54:31 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:54:31 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:54:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:54:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 28 Jan 2026 04:53:05 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 28 Jan 2026 04:53:05 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 28 Jan 2026 04:53:05 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 04:53:05 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 28 Jan 2026 04:53:05 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 28 Jan 2026 04:53:05 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 28 Jan 2026 04:53:05 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 28 Jan 2026 04:53:05 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 28 Jan 2026 04:53:05 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 28 Jan 2026 04:53:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 28 Jan 2026 04:53:06 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 28 Jan 2026 04:53:06 GMT
ARG USER_HOME_DIR=/root
# Wed, 28 Jan 2026 04:53:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 28 Jan 2026 04:53:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 28 Jan 2026 04:53:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea00285b52f6f6c9e088cd08bc54a41499c353ac64712efcaf2aff682f021f1a`  
		Last Modified: Wed, 28 Jan 2026 02:54:52 GMT  
		Size: 178.4 MB (178412260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad64593ec6f9eec63b6b79757c12ef5ffa6643096803837fc72bf1348a3e9d8`  
		Last Modified: Wed, 28 Jan 2026 04:53:13 GMT  
		Size: 2.5 MB (2461730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9f8c306199a41aa4e76c31c7edd1cfec9578550ed3641fa058681bfc7cba08`  
		Last Modified: Wed, 28 Jan 2026 04:53:13 GMT  
		Size: 9.3 MB (9312241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3661ef5055ccc86ae972a1fc10cc1a04ef4fa579cb98e9e92ad2845d0ff97f9f`  
		Last Modified: Wed, 28 Jan 2026 04:53:13 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92291d29ea3bebf569cdb117b2a61d045a4ae55030ea84d977dd104bda7d2d1c`  
		Last Modified: Wed, 28 Jan 2026 04:53:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:b688a08112e329aa98259e6d7fe08412d42345a5ad49da7c7fdc0e469fc78b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **752.0 KB (751976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98235451bd0a271e1eeaea1b205426538956b401c55feed88384c9edec84750b`

```dockerfile
```

-	Layers:
	-	`sha256:1119bfaafcf1a7e074374488d7e63f41191337a79fb9e61abad38a2f912783c2`  
		Last Modified: Wed, 28 Jan 2026 04:53:13 GMT  
		Size: 735.5 KB (735481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8671f4c43dedf0728e66ea023450a3044ab1498623c8237691a03fa23c40f39d`  
		Last Modified: Wed, 28 Jan 2026 04:53:13 GMT  
		Size: 16.5 KB (16495 bytes)  
		MIME: application/vnd.in-toto+json
