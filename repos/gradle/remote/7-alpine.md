## `gradle:7-alpine`

```console
$ docker pull gradle@sha256:8ea10ea875e89d578515f6c87d4e18ba7cc4be4a2660679ddd91756f31d437b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gradle:7-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:041e5ec1cb6f3515e35e53b3a81932bbab3c53a1536a5fa2452959ad3a7e0b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.9 MB (317861235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762018a19fbda7c5b15d9ad370a13a503f7e55b9b96c8cf3f829156478fb9cf0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 05 Feb 2024 22:05:50 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["/bin/sh"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 05 Feb 2024 22:05:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Feb 2024 22:05:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='6d274a292a717a6f8d00a3ed0695497405c5c634c27fec1692dd13784f6ff6fa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["jshell"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["gradle"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 05 Feb 2024 22:05:50 GMT
WORKDIR /home/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_VERSION=7.6.4
# Mon, 05 Feb 2024 22:05:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER gradle
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER root
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479e64820c602a6421582ff22341d66b5c6938bee2115d203f3d03147a89505e`  
		Last Modified: Thu, 25 Jul 2024 17:29:26 GMT  
		Size: 14.0 MB (14039136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e384a19a9b0cde9f53fc5c79a581f80b1606cb9b0c477b8019b1716ffe026fe`  
		Last Modified: Thu, 25 Jul 2024 17:29:36 GMT  
		Size: 144.4 MB (144394552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed71e81fa34c6c2e7902182aaf9da971d499b0e58d2dfcc2c789535bc6768e0`  
		Last Modified: Thu, 25 Jul 2024 17:29:24 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7beb93379603195c1cd0e0fa2dfd4b31ab5a9580ed4dd4cc301f4ca12c31c1ff`  
		Last Modified: Fri, 23 Aug 2024 19:26:45 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d04e6e9122ee5c66f948abfd22af8b1f861c6c80febc68c48526e2e7b67ca8`  
		Last Modified: Fri, 23 Aug 2024 20:02:46 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7238b27cf664bc3f58463ce3fd5d1bfdcdb9cfa30b1f85a8142bc5136bda9692`  
		Last Modified: Fri, 23 Aug 2024 20:02:50 GMT  
		Size: 33.0 MB (33015924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8e4c98d9997c94601ff828d3df1c766d03333ea5264b214af08d9f5fe2eb11`  
		Last Modified: Fri, 23 Aug 2024 20:02:52 GMT  
		Size: 122.7 MB (122730501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc3e6cbd27623b148ea87fbcdfeeafcc8e5057a3266a345d680cd196d0cb76a`  
		Last Modified: Fri, 23 Aug 2024 20:02:49 GMT  
		Size: 54.9 KB (54909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:1359bf5e23a01d283c7d728aaeb40868703bee24d0f00e05279bb0eca4fb3276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3019101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac786c3f2687db0be9094d156e110f7fd46294f91e150215cc2dc68226cb9b0`

```dockerfile
```

-	Layers:
	-	`sha256:1ad2cfca05e332a530b71a7bfbb5f5d5fdb7b65a70f958662037e1656226cca9`  
		Last Modified: Fri, 23 Aug 2024 20:02:49 GMT  
		Size: 3.0 MB (2996664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:375875d77b650df81b94cadd6f1571fff106c9aa5d960ba1776ecf3d702ef458`  
		Last Modified: Fri, 23 Aug 2024 20:02:48 GMT  
		Size: 22.4 KB (22437 bytes)  
		MIME: application/vnd.in-toto+json
