## `maven:3-eclipse-temurin-24-alpine`

```console
$ docker pull maven@sha256:99ff7d4ea2083b629b788d5a7a14c1671a0273aff6a339d62f184963d88ffffc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-eclipse-temurin-24-alpine` - linux; amd64

```console
$ docker pull maven@sha256:bfc4661999fcd6abcfc58c461a80408e19295aa867d74d2c87b9cd9b0ae487ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127238080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a64853ba789a5f77a516c1f920294f21b016efc0e2923fe5438b5949e87f16`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Mar 2025 16:03:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 16:03:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 27 Mar 2025 16:03:48 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Thu, 27 Mar 2025 16:03:48 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='97b14f9c2f7e7ba4d4a958bba6835a23353b5fd858725031fc42af4f40a5a4ad';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_aarch64_alpine-linux_hotspot_24.0.1_9.tar.gz';          ;;        x86_64)          ESUM='74627af4084a9eb65cc5bad3bb5723b89f1ffb5eaec9afbd696ec5bf684ed79a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_alpine-linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["jshell"]
# Thu, 27 Mar 2025 16:03:48 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ARG MAVEN_VERSION=3.9.9
# Thu, 27 Mar 2025 16:03:48 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89fa3206805da3f39f3d33e513000c7fe732767469d033fea6cf0c47b9c3a6b`  
		Last Modified: Wed, 23 Apr 2025 16:32:08 GMT  
		Size: 21.0 MB (20951357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e10588850906e608ba2d19a979d66a3c3231deab14453e4c96f0f145218c2f`  
		Last Modified: Wed, 23 Apr 2025 16:32:09 GMT  
		Size: 90.1 MB (90081657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f971aa3d7e1c0f663d0194507c129d747c8c22bd5a54388471f73fd984c2bb`  
		Last Modified: Wed, 23 Apr 2025 16:32:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883498cd171d42da42c278599e117d11db9885fbea522558e72b6f1740e5567d`  
		Last Modified: Wed, 23 Apr 2025 16:32:07 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783e55fef1cd0dc40d1c1036ff349b3937880986631c4a3489cbd33536c895f7`  
		Last Modified: Mon, 05 May 2025 17:11:43 GMT  
		Size: 3.4 MB (3388930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d24783834ac41d56fd8c8a3c604b65551b81befa8d32484b9f606ce695e493`  
		Last Modified: Mon, 05 May 2025 17:11:43 GMT  
		Size: 9.2 MB (9170438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfee9596f9743897d8c489752ab5503a656ccc76ebcc92aa549e84b42927576`  
		Last Modified: Mon, 05 May 2025 17:11:43 GMT  
		Size: 859.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10b22d5170fddde6619199a9465c36005525639bbb76f22f08b3918131a5bca`  
		Last Modified: Mon, 05 May 2025 17:11:43 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-24-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:e2053eaa4693a4b90239f5360d347d25b8c34bca324313aeca38a741fa9e681e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1193600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a851c03ebf68c8613480fa12068e7c9cc2fb60b3f6c824b226bd128929b4efd`

```dockerfile
```

-	Layers:
	-	`sha256:a4d61b83fd072ac5c250bcf47c31ef1ee6c10341ad71e2d8c06760e68bb22e8d`  
		Last Modified: Mon, 05 May 2025 17:11:43 GMT  
		Size: 1.2 MB (1174226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5399cbd627622ef959b0b377776291c5117b0fd84b64560952063f5bd1a614a9`  
		Last Modified: Mon, 05 May 2025 17:11:43 GMT  
		Size: 19.4 KB (19374 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-24-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:e63a0a92c90f28868b063278e853620a960e8e5504f0ea73f46577128403aac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126686509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48cb70badc75457f7bd7c161376cb84f918d59c49c84d4cdcd466d202931168`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Mar 2025 16:03:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 16:03:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 27 Mar 2025 16:03:48 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Thu, 27 Mar 2025 16:03:48 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='97b14f9c2f7e7ba4d4a958bba6835a23353b5fd858725031fc42af4f40a5a4ad';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_aarch64_alpine-linux_hotspot_24.0.1_9.tar.gz';          ;;        x86_64)          ESUM='74627af4084a9eb65cc5bad3bb5723b89f1ffb5eaec9afbd696ec5bf684ed79a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_alpine-linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["jshell"]
# Thu, 27 Mar 2025 16:03:48 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ARG MAVEN_VERSION=3.9.9
# Thu, 27 Mar 2025 16:03:48 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4dc4c8e3ac1404ce7eb282c94493325536d142e577ef37ec27bcf3edd09f4b`  
		Last Modified: Wed, 23 Apr 2025 16:40:20 GMT  
		Size: 21.0 MB (21006028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b587585b41566074b337300ac392de9b4d45b1d80418a53a9682dc5dc5cfa792`  
		Last Modified: Wed, 23 Apr 2025 16:46:10 GMT  
		Size: 89.1 MB (89067358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de1aae9586f9d6276f2cc85c43560b6c4303b29fadb32b3998b60ca44ac6f4e`  
		Last Modified: Wed, 23 Apr 2025 16:46:07 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eef6807030255660c0fed6484392bae8ed8ca964c95eaf49f68b4b768b6af50`  
		Last Modified: Wed, 23 Apr 2025 16:46:08 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637f29368a5510e8096a2a471575cb9d129ef6c377bd1cb8a32e0dd42d36bfd7`  
		Last Modified: Wed, 23 Apr 2025 20:54:13 GMT  
		Size: 3.4 MB (3446210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fde7ac2374f50ea6c058329391fa2f117a3b88d01cb1db39dceae094b286f1`  
		Last Modified: Wed, 23 Apr 2025 20:54:13 GMT  
		Size: 9.2 MB (9170430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8162f25892bcb01c20399ca6e31e4bb40942e8a0da7c05418f3045af1f7d73`  
		Last Modified: Wed, 23 Apr 2025 20:54:13 GMT  
		Size: 858.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cb58fa3a7ac790f30582098b468971a9da4a47e3e4806705d75caa4f2dcfcf`  
		Last Modified: Wed, 23 Apr 2025 20:54:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-24-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:fd65246a5eab70c8087558fb045275e61a6af58425f81daedbe3ceb0eff798d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1343733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440d4dc661668695a9c19fa9816ad3f18daede030b540016c3411a589574ea20`

```dockerfile
```

-	Layers:
	-	`sha256:00237241897d7f28941f8e95f157314c7f349d6d6005c56bb4e78c90e0aba98b`  
		Last Modified: Wed, 23 Apr 2025 20:54:13 GMT  
		Size: 1.3 MB (1324225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:905bd06104be6cd01374be330dbb2b67fd318ef2cf24bfcb41e7a86bff7b7bbe`  
		Last Modified: Wed, 23 Apr 2025 20:54:13 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.in-toto+json
