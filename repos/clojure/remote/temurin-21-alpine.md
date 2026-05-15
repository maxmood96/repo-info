## `clojure:temurin-21-alpine`

```console
$ docker pull clojure@sha256:50416402d2a7a8ef1f09572ada91700736577438d3e7ff562ac19e475ff6f46d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:b4accab0ae47e8590a63b3f5d79061d813f5f09c562298d40ae17fc787dc49cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.0 MB (208995475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25415b22f23d8144aa1326dca000d6548cfe0b9d8a7b90948f1ff6ae68c7e380`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 23:58:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:58:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:58:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:58:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 07 May 2026 23:58:34 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Thu, 07 May 2026 23:59:37 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='c8d63598d1dc0a656033515ed258bd6db37506a05407d9f65cd23b95c21027b5';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='38bfdcef1e4b45de2ec222047ac79c76bea75d4d7406a310e26cfa236763f05f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 07 May 2026 23:59:39 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:59:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:59:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 07 May 2026 23:59:39 GMT
CMD ["jshell"]
# Thu, 14 May 2026 23:35:19 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:19 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:35:22 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Thu, 14 May 2026 23:35:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:35:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:35:22 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:35:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b50ae58d435408a9b026fe52e1670bc1fa8333eabfe9bf8732808b503921e21`  
		Last Modified: Thu, 07 May 2026 23:58:58 GMT  
		Size: 21.3 MB (21336223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcaabbcdfa248e8282ff1b8185b085013c4acad8c1d745f6bc6c254ca2c91cb`  
		Last Modified: Thu, 07 May 2026 23:59:56 GMT  
		Size: 158.4 MB (158396777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b89d263afc40ec784ccb9f91009ff3a1331571314d0a8213a083c9035f3155`  
		Last Modified: Thu, 07 May 2026 23:59:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4011cd827d707fc4492dbd50182b9de9e9d695532577a6760b7fa8a6b093e0`  
		Last Modified: Thu, 07 May 2026 23:59:54 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e06c5f905fc4e0860b4d8d99c324cce4ff3eb3df08722acddeb403f9779d62`  
		Last Modified: Thu, 14 May 2026 23:35:32 GMT  
		Size: 25.4 MB (25394825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af56e0028613545560e4f64e27bc8f3d5283b34153a03a9d7d82b6a932a36f74`  
		Last Modified: Thu, 14 May 2026 23:35:31 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2be364db091c5b1e265cc7d7e533726bf35126459eae2a0fe25d85c858c3c8c`  
		Last Modified: Thu, 14 May 2026 23:35:31 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:cccdd81bd7b94d384b7e124d8317b279ca30157ce224b7e74bb7e438bf617b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12dfc1a3695b324ca672df376691f8fc7af0c81c10ba53d3fc5fafc6184a634`

```dockerfile
```

-	Layers:
	-	`sha256:3fe650a27629e7a65ebfa7e4baafa56bf507b08c6be7ef48e0d495dd137810c2`  
		Last Modified: Thu, 14 May 2026 23:35:31 GMT  
		Size: 1.3 MB (1310575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f89544069684fb456e661e542eb0259337836e982150059457107cc047665483`  
		Last Modified: Thu, 14 May 2026 23:35:31 GMT  
		Size: 15.4 KB (15430 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:04d80b7c3dab42f80518ed27bf5fe93be1fdf0ce1137d13f4967cf664db7084a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.5 MB (207473416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53132905d93223822589f7e853cb1dc4ae3509a970ea18b076edb28635681d25`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 23:58:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:58:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:58:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:58:58 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 07 May 2026 23:58:58 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Thu, 07 May 2026 23:59:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='c8d63598d1dc0a656033515ed258bd6db37506a05407d9f65cd23b95c21027b5';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='38bfdcef1e4b45de2ec222047ac79c76bea75d4d7406a310e26cfa236763f05f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 07 May 2026 23:59:07 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:59:07 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:59:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 07 May 2026 23:59:07 GMT
CMD ["jshell"]
# Thu, 14 May 2026 23:35:14 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:14 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:35:18 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Thu, 14 May 2026 23:35:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:35:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:35:18 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:35:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a9f60e46e53646ef0910131cad063b4c547e8b484db8a7f43c06e8c8d8ee11`  
		Last Modified: Thu, 07 May 2026 23:59:24 GMT  
		Size: 21.3 MB (21321387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e7335552e625aa4d940009043b9ade8114a61f7445ad089dd0699e9c2cbd02`  
		Last Modified: Thu, 07 May 2026 23:59:27 GMT  
		Size: 156.4 MB (156402365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbe5c3db0c5dad3a2183ba5e385ef243c43b6847fa16af1db10346a47fb9e86`  
		Last Modified: Thu, 07 May 2026 23:59:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319e0f520245ecdfe248ad69c9025626cdb9a8a435ccd3b9a19da574bc33023`  
		Last Modified: Thu, 07 May 2026 23:59:23 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3d2a322668d29c624990a9a9e075855a732fe4d9d1bc46b7fab2a558d9aa38`  
		Last Modified: Thu, 14 May 2026 23:35:28 GMT  
		Size: 25.5 MB (25546336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f116c7268305dc5ca2d1364254ab00abdf72d360f3a79d4a5d782281d5aaf7`  
		Last Modified: Thu, 14 May 2026 23:35:27 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5505109a8459221c78012e78b226a4cae0a1a5332620f9aa6f52a1f79f2fa2eb`  
		Last Modified: Thu, 14 May 2026 23:35:27 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:e9ba45616eda0e11a8498039e94514903c4eed19ad24843e4bbf9599a750b8e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 MB (1475451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff8f1044a016dc36aa253123095f0450cf7301944e194347a2a888dbb572c3b`

```dockerfile
```

-	Layers:
	-	`sha256:dcb71573f9a4b8a54e5b2126c037e5439c159411546b50f4f8fcfc10144bfbd6`  
		Last Modified: Thu, 14 May 2026 23:35:27 GMT  
		Size: 1.5 MB (1459927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4ad688500c38b2ae86121a261f67a5d5d4af4764c8320af03935aa5d71ef1aa`  
		Last Modified: Thu, 14 May 2026 23:35:27 GMT  
		Size: 15.5 KB (15524 bytes)  
		MIME: application/vnd.in-toto+json
