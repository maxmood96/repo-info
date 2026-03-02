## `clojure:temurin-11-tools-deps-alpine`

```console
$ docker pull clojure@sha256:6a64084ad9ae4e244e138787205c0cc78f2e482ea7913bce6ea2943aac58c566
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:08dfcfeb9a0476dbf3f59e3209e715ad19ca490aa1954fb53ebb5da21a0b03d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187053737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c882050f4d188894a4551022f47a3024d915c6ea89a210e50202bf732d4a0a6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:13:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:13:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:13:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:13:12 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:13:12 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Thu, 05 Feb 2026 22:15:19 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='b55a38b75ba99d86f4adb47552ee5306b9589e2026861a3b8f030993c42aedc7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:15:20 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:15:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:15:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:15:20 GMT
CMD ["jshell"]
# Mon, 02 Mar 2026 19:45:30 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:30 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:45:33 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Mon, 02 Mar 2026 19:45:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:45:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba30a9b9fbd57b01a8081d96f19cccf9befdb10d3a054b012d5419c813f251a`  
		Last Modified: Thu, 05 Feb 2026 22:13:27 GMT  
		Size: 16.8 MB (16839871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e03198ce1bcff72d14da682b57422ca0339a46a5a480a429fb7dfc1584cf098`  
		Last Modified: Thu, 05 Feb 2026 22:15:37 GMT  
		Size: 140.9 MB (140916724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ec050240a37b134eae130d1c8a581f8dc3f6a1812c89605de53cbc4807a7c8`  
		Last Modified: Thu, 05 Feb 2026 22:15:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b685f9f516a02949ff913848fd8f5097682da3f014f7f123cd6d47c1c03e35fa`  
		Last Modified: Thu, 05 Feb 2026 22:15:34 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ac82b9616ac07b67a076949778202060f4c7593fd387421b68e9eae611e019`  
		Last Modified: Mon, 02 Mar 2026 19:45:43 GMT  
		Size: 25.4 MB (25432260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e6dc407d77d714f4965d290c3d299766fe675e9690ec0ef243d063760f04f9`  
		Last Modified: Mon, 02 Mar 2026 19:45:42 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:3c134ce90d72deaaa2bf7cb712d86886191a967a7ea92efa1eeae5ed0138d4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1227754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389946e4c6293a9fb97b5dc9035d32eb1d9192b6166df83e0216bccdde671a81`

```dockerfile
```

-	Layers:
	-	`sha256:3bfcb01ddab071a666dddf4720639fff631554827de0e831e20239eb80ccb5ea`  
		Last Modified: Mon, 02 Mar 2026 19:45:43 GMT  
		Size: 1.2 MB (1214359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c316ce2483f163926793483878eada37ede46b5dcbcc740a5fe8f0cf906f0e9a`  
		Last Modified: Mon, 02 Mar 2026 19:45:42 GMT  
		Size: 13.4 KB (13395 bytes)  
		MIME: application/vnd.in-toto+json
