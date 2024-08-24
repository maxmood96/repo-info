## `clojure:temurin-21-alpine`

```console
$ docker pull clojure@sha256:7ac4cab92e19bf47abcc9712b72215db4b590c0203080e96c6d5a63855c2beef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-21-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:058e6ba36f6e79b019fc7c26dd82fc0ba539faf6499a8edd24f364a8379b689d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 MB (201811664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63fac0bdbd872711f1b58d8b2723c4066d022231c1adfa6346bd7d87e999bd44`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='849c6d5a62a1f3dc2a3d2d7be07ffda089d35b862f6160b2a288c0408c2d8be8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='8fa232fc9de5a861c1a6b0cbdc861d0b0a2bdbdd27da53d991802a460a7f0973';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["jshell"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apk add --no-cache curl bash make git && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
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
	-	`sha256:cf4e44e3ea2cb8913609a6cdac111f101c4e181da4d2d872cc22c856078f0b88`  
		Last Modified: Thu, 25 Jul 2024 17:31:10 GMT  
		Size: 158.8 MB (158815391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238c673ab2bbd210a166189cde9795dce4799e4c34f357d90ba8c00ccf6a2172`  
		Last Modified: Thu, 25 Jul 2024 17:30:57 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b419905a3aad54d3952b04520433835e067c485a4162207785f187aea8578d9`  
		Last Modified: Fri, 23 Aug 2024 19:28:14 GMT  
		Size: 2.1 KB (2105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6823dbe37060569b232161e51acf97b2f4daf47e3412e13890ee6814d69edf0`  
		Last Modified: Fri, 23 Aug 2024 20:04:06 GMT  
		Size: 25.3 MB (25330929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8f0d2f5cd78c9b231f16cb7acf6d650bd3c2fa016f0e649f476785c288d6c1`  
		Last Modified: Fri, 23 Aug 2024 20:04:05 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da105b16a25faca2ca849d84ae0880d40d6093387b99c4b5ce7274e2cd2d33e`  
		Last Modified: Fri, 23 Aug 2024 20:04:05 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:9a804bcd77a419e92239d63d081715f177d36a402846a00e5bc925dfdba01f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1014156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf986fc0f7168308706cf41c650f7d0bd5e6bca94faa6ebf81eece82de3e8bd`

```dockerfile
```

-	Layers:
	-	`sha256:245da26123fd28e5e755151504b1ec406722d98d10ef6a79e96d53d8fe679c61`  
		Last Modified: Fri, 23 Aug 2024 20:04:05 GMT  
		Size: 998.8 KB (998751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a43fa7a0cc90d67c2d745a99080a739b67186e9d25009bf45a8cb1cb8e2915ee`  
		Last Modified: Fri, 23 Aug 2024 20:04:05 GMT  
		Size: 15.4 KB (15405 bytes)  
		MIME: application/vnd.in-toto+json
