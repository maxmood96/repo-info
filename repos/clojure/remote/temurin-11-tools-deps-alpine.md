## `clojure:temurin-11-tools-deps-alpine`

```console
$ docker pull clojure@sha256:0ce0fc75bdd31723b54e89b0aafab083a7621eff93abca779ec97f4818079af6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:a0a77928b7483ef2fe35536257da14fa5b97725c78924e716d83f13a847014fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.7 MB (185728073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc6f1c8c915d77d43c8c84fa1e497eff33bf3e6e7637d5e1f85b4e72aa7cdf8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Jan 2025 01:19:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 01:19:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='0a431310ccccc36c85b1274b5d31e368fdc8cf62cb7c2ed98d7b59eb5a13dc82';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Jan 2025 01:19:15 GMT
CMD ["jshell"]
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apk add --no-cache curl bash make git && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173d2d9b0a8b46032d314316667cd35f83981b340801b2eee2e4b2f5a9e1551a`  
		Last Modified: Wed, 22 Jan 2025 18:27:50 GMT  
		Size: 16.1 MB (16135215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57e5d440f7c1441b7d1825ea8f76a92995b27246ce624f8a62a09b758d92aee`  
		Last Modified: Wed, 22 Jan 2025 18:27:54 GMT  
		Size: 140.8 MB (140775205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2a28f11eac8e07ee789aec0651a007ebf7347f6b67af05c483b2a842c93310`  
		Last Modified: Wed, 22 Jan 2025 18:27:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eec7655b90e61e589217af43d5e02f51e095291b9cedf34c5739d3c5bac5f9`  
		Last Modified: Wed, 22 Jan 2025 18:27:49 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b2e6e08ee93cf4f9d4eece75a701ae4a799fcb1ce3c51c786e8645f701e4f8`  
		Last Modified: Wed, 29 Jan 2025 20:27:23 GMT  
		Size: 25.2 MB (25172876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d009216970d67338a02c836cb9025dece9dda5b7e350856921c83968a7f27aa`  
		Last Modified: Wed, 29 Jan 2025 20:27:22 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:baddca250b558af9b458951481da50d6e5813be2a2e4f3997a39b27615933c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c32278a0b4eed158afcaf643a547660e28b38ec37569f31be9ec5dfffec7432`

```dockerfile
```

-	Layers:
	-	`sha256:d35d57c77ddf6e451490aba280f2ccb3c5c611da28879675a62f3df9da72d112`  
		Last Modified: Wed, 29 Jan 2025 20:27:22 GMT  
		Size: 1.2 MB (1151179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c687645f953a3815a08f8300db04fdac55d8b45c85e39bd3d88fded3e48706c0`  
		Last Modified: Wed, 29 Jan 2025 20:27:22 GMT  
		Size: 13.4 KB (13423 bytes)  
		MIME: application/vnd.in-toto+json
