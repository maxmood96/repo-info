## `maven:3-amazoncorretto-24-alpine`

```console
$ docker pull maven@sha256:a4847235907b95e54a38a5a7ea5b12c4fda2f2d6a61e84c4f66e94aa92ae9a61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-24-alpine` - linux; amd64

```console
$ docker pull maven@sha256:b98fa489077e04eea396b0043f6a3f713866fd04397ab0a0dc17896475fb36a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192179400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53e40bb5a55032e025bce54538fed2eae333f16808f22cec203adc0d68d3e781`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=24.0.2.12.1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=24.0.2.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 06:51:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6044ea9c8a1ef640a4f19ab13afda53c68d55374d877a5f49f223648ee77d0`  
		Last Modified: Fri, 18 Jul 2025 20:07:59 GMT  
		Size: 176.8 MB (176770797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee19148c746e3dcdb5cf77cef2d7fb917e9c2fcbf0ea9be5486515ef31c1fbc`  
		Last Modified: Thu, 02 Oct 2025 12:25:01 GMT  
		Size: 2.4 MB (2365285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a649d17232df959e535953f629b760860099bd20acca024af0ae61534834c4ae`  
		Last Modified: Thu, 02 Oct 2025 12:25:01 GMT  
		Size: 9.2 MB (9242589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c52b98761dee36e0993589092f25816c903c2867e378f573c893207ee2bf58`  
		Last Modified: Thu, 02 Oct 2025 12:25:01 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeedf8d9a26a47b03090d69966465502c169c510aaf50fd1d2ffc09beccb1539`  
		Last Modified: Thu, 02 Oct 2025 12:25:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-24-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:b0997b1271f2602549bcf86e20bd1a0bee423d4c4dced0f62c6d4ed03018a861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.6 KB (553635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ec4b72ef33745cb0ddfcfde7a508cec22be3224898f5a8ac62ca060c221d37`

```dockerfile
```

-	Layers:
	-	`sha256:00bf46a7c692645c2d917b16abff27d1e2bfd41b3de7b14542799d7f3be8e80b`  
		Last Modified: Thu, 02 Oct 2025 14:28:56 GMT  
		Size: 537.2 KB (537230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0adf050db19344d7cc36d1df1a8edb95aa1a1e8cca34f8ae3eb3fcf62ee5238`  
		Last Modified: Thu, 02 Oct 2025 14:28:58 GMT  
		Size: 16.4 KB (16405 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-24-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:04d0a86aa94a0ee20ca4787fe461ad30a5211dff6aebf81f5f25155714a1a119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190288566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb11aa41e5ac48e7fb233ba1cac0998dfeb091cd722d615c965ddaa0bdb71ff`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=24.0.2.12.1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=24.0.2.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 06:51:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de9585f1b7564cbcb01d30dbbbf1693f75039bedbf47afb1c24cb8380f5d989`  
		Last Modified: Fri, 18 Jul 2025 22:13:41 GMT  
		Size: 174.5 MB (174517397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb59fb1bd21dbd771b34e02774b211c87fa9185f15770e342af64c68746f9a3`  
		Last Modified: Thu, 02 Oct 2025 03:32:05 GMT  
		Size: 2.4 MB (2396801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53304826e20e0b378047966c91fd13703e1994f020b1261ca7fadf37ac3ddfb8`  
		Last Modified: Thu, 02 Oct 2025 03:32:06 GMT  
		Size: 9.2 MB (9242579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1139c9d541bc2a094c9690b0fa823cc4295d7c4dfc12a1a7772009ea5ff1fbc9`  
		Last Modified: Thu, 02 Oct 2025 03:32:05 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231bc8474d418987f4c850e02730c5894ffbc9e67131736062c194853e88e842`  
		Last Modified: Thu, 02 Oct 2025 03:32:05 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-24-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:f4d11638df442eb2208fa511d1876352051ff757ec9edb74e30328b46b8a3231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.2 KB (553171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b0808180c5d0acae7d2aaab2ca94cfe6ba374d2343a8c71810da4906c5757b`

```dockerfile
```

-	Layers:
	-	`sha256:b0e1ba761e4447f14f44fc270daf3eaece0ac8970d22a43ac7fcf2adbcc9bd37`  
		Last Modified: Thu, 02 Oct 2025 05:28:56 GMT  
		Size: 536.6 KB (536634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bda0b53ea8f5f9ad718140924ebf2600972d2937adc7f3dccbb0fdfe30d142ba`  
		Last Modified: Thu, 02 Oct 2025 05:28:56 GMT  
		Size: 16.5 KB (16537 bytes)  
		MIME: application/vnd.in-toto+json
