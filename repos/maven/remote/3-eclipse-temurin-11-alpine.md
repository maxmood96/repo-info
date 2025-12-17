## `maven:3-eclipse-temurin-11-alpine`

```console
$ docker pull maven@sha256:5573920ba8fcb8e87f0674a404cdccf261d17cf040ad40dbfdac74a7e00fbbaf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-eclipse-temurin-11-alpine` - linux; amd64

```console
$ docker pull maven@sha256:b0a27005193c9c019b539e04f4ca7051f2075e12578d10f22ef47bdeb2773d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173313299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a8cdc541b78e0f38ba2c0cbbcfacedb083392efd2ffbca844be53b63423325`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:57:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:57:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:57:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:57:13 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:57:13 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Sat, 08 Nov 2025 17:57:18 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='c7b58655ffde7b5e6fce4a32fdcd21be5745b3bb64ee2bc723fcf55eae720ebe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 08 Nov 2025 17:57:19 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:57:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:57:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:57:19 GMT
CMD ["jshell"]
# Wed, 17 Dec 2025 20:09:38 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Wed, 17 Dec 2025 20:09:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Dec 2025 20:09:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:09:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:09:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Dec 2025 20:09:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Dec 2025 20:09:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Dec 2025 20:09:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Dec 2025 20:09:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Dec 2025 20:09:39 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Dec 2025 20:09:39 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 17 Dec 2025 20:09:39 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Dec 2025 20:09:39 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Dec 2025 20:09:39 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Dec 2025 20:09:39 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974df0e0eb67fd6fa35aefb5620f2d84f013b3e0b11b4c38737099a86303d60b`  
		Last Modified: Sat, 08 Nov 2025 17:57:42 GMT  
		Size: 16.3 MB (16289652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b829ff2503da3447968682832d5a69ea284ba1d657a4f8e58d4c799c8c348e`  
		Last Modified: Sat, 08 Nov 2025 18:23:46 GMT  
		Size: 140.1 MB (140102363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a217f6eeaed3b8ab583b886e8495c9ca0664bb21717752475480bc1453bb07d2`  
		Last Modified: Sat, 08 Nov 2025 17:57:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea81eccc49bc152ef173ac2d3a5ac97163278251fda36902720deae5aa454418`  
		Last Modified: Sat, 08 Nov 2025 17:57:41 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5988db9c4c12e30d78aed93dcd85a5fa7614a0aae30e8376c6202f886aa6c82`  
		Last Modified: Wed, 17 Dec 2025 20:09:56 GMT  
		Size: 3.8 MB (3803137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ab60cfa8ac68de7e16b0550e7c200bfff905ef328b67e0c0dd9bd4c4d4ee3b`  
		Last Modified: Wed, 17 Dec 2025 20:09:57 GMT  
		Size: 9.3 MB (9312242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce223c1cef7771ed46226e98dc2b088e63e59cc63dc719255401de7ea55fdfa5`  
		Last Modified: Wed, 17 Dec 2025 20:09:57 GMT  
		Size: 859.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df7042ad27c3ecd1a56c5e99dc615ce86052a855e12c54831b4fc96ed33230e`  
		Last Modified: Wed, 17 Dec 2025 20:09:57 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-11-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:8a3f234e1aa88b66db0d98da43dba1cba16e7f9c21dca735b30541dbe3ea8226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1156401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c511f5a46ef49f634043fe05e60c09f1d1cd26038112c1e74d4b5b9dbd1f5161`

```dockerfile
```

-	Layers:
	-	`sha256:1f81173d82cdb254883190dfc6ae294533c09de5d5b43cc4c2b607654e165e23`  
		Last Modified: Wed, 17 Dec 2025 21:31:08 GMT  
		Size: 1.1 MB (1137054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b488d167c30ba6acbc74f3de70f4a71df075832a64a016a00595c22912e2a1d1`  
		Last Modified: Wed, 17 Dec 2025 21:31:09 GMT  
		Size: 19.3 KB (19347 bytes)  
		MIME: application/vnd.in-toto+json
