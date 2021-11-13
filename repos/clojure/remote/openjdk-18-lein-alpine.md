## `clojure:openjdk-18-lein-alpine`

```console
$ docker pull clojure@sha256:a6d87bbf12ae162cd4c344cf10e131447da981903834a64308a09570b2fe4ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:openjdk-18-lein-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:e465c41cc84c29651587728915aa43c4bba00fe791d59c5a2821dccb7b2fdab9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.1 MB (209060811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aeced35250696dd57cb58199ffa1a684faf94ca76017af4d1a2a91610f2f8b3`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:32:26 GMT
RUN apk add --no-cache java-cacerts
# Sat, 13 Nov 2021 07:32:27 GMT
ENV JAVA_HOME=/opt/openjdk-18
# Sat, 13 Nov 2021 07:32:27 GMT
ENV PATH=/opt/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 07:32:27 GMT
ENV JAVA_VERSION=18-ea+11
# Sat, 13 Nov 2021 07:32:40 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/11/binaries/openjdk-18-ea+11_linux-x64-musl_bin.tar.gz'; 			downloadSha256='86fad9069587a5e9dd003e7354a69b2f720a05c12706d2f2345a0c8d90e56c47'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 13 Nov 2021 07:32:40 GMT
CMD ["jshell"]
# Sat, 13 Nov 2021 11:55:59 GMT
ENV LEIN_VERSION=2.9.8
# Sat, 13 Nov 2021 11:55:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 13 Nov 2021 11:55:59 GMT
WORKDIR /tmp
# Sat, 13 Nov 2021 11:56:04 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "9952cba539cc6454c3b7385ebce57577087bf2b9001c3ab5c55d668d0aeff6e9 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg
# Sat, 13 Nov 2021 11:56:04 GMT
ENV PATH=/opt/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 13 Nov 2021 11:56:04 GMT
ENV LEIN_ROOT=1
# Sat, 13 Nov 2021 11:56:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Sat, 13 Nov 2021 11:56:09 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad0d0169427449f303a2c6baf5a00c969d2b2b85c2edd07aaa19ce580773a4a`  
		Last Modified: Sat, 13 Nov 2021 07:40:09 GMT  
		Size: 928.2 KB (928186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c40c2a9a506010fe514760d27418dde11f26d48c0ceb564f3e4f2bf468074ba`  
		Last Modified: Sat, 13 Nov 2021 07:40:24 GMT  
		Size: 188.7 MB (188699691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8264a216ca5b01ea95dd2a35dd85cd81f26d034c6bd02a53f2d613513fa2e6d9`  
		Last Modified: Sat, 13 Nov 2021 12:05:39 GMT  
		Size: 12.4 MB (12402721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47b6aa3739c81e8150e9ae447ba6c893c4ab23b997951c795bf8f932340d857`  
		Last Modified: Sat, 13 Nov 2021 12:05:39 GMT  
		Size: 4.2 MB (4207232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
