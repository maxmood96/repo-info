## `clojure:openjdk-16-lein-alpine`

```console
$ docker pull clojure@sha256:ad787d32d66941fb7826041f8f97f77f69c3f9000baa10001be37810e37f6530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-16-lein-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:4c3928e52e48806057f33ccfa1ba4999ef06dd17f367ee14422230acaaf8e224
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.5 MB (219527490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166fabc2399df2810bba5d714c5f71d03b8f3c3f91344f07801e695c2a31d26c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:36:52 GMT
RUN apk add --no-cache java-cacerts
# Thu, 22 Oct 2020 02:36:52 GMT
ENV JAVA_HOME=/opt/openjdk-16
# Thu, 22 Oct 2020 02:36:52 GMT
ENV PATH=/opt/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Oct 2020 02:36:52 GMT
ENV JAVA_VERSION=16-ea+14
# Thu, 22 Oct 2020 02:37:35 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64) 			downloadUrl=https://download.java.net/java/early_access/alpine/14/binaries/openjdk-16-ea+14_linux-x64-musl_bin.tar.gz; 			downloadSha256=6d6943f9c350ca20fd2892e024c363e538ab4a2c1aeaceeab4450a47cbaca54c; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 22 Oct 2020 02:37:36 GMT
CMD ["jshell"]
# Thu, 22 Oct 2020 08:33:46 GMT
ENV LEIN_VERSION=2.9.3
# Thu, 22 Oct 2020 08:33:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 22 Oct 2020 08:33:47 GMT
WORKDIR /tmp
# Thu, 22 Oct 2020 08:33:50 GMT
RUN apk add --update --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "42e18e8a833b863ddfba1c5565bd5d78b54bcee661ec86e94a8bdc67b1733e63 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver keys.openpgp.org --recv-key 20242BACBBE95ADA22D0AFD7808A33D379C806C3 && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.zip.asc leiningen-$LEIN_VERSION-standalone.zip && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg
# Thu, 22 Oct 2020 08:33:50 GMT
ENV PATH=/opt/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 22 Oct 2020 08:33:51 GMT
ENV LEIN_ROOT=1
# Thu, 22 Oct 2020 08:33:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 22 Oct 2020 08:33:55 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90d4961e1b84bb83aca8e1aadcad45ff59be8b1b7e2040c1004a1a4e4dd330b`  
		Last Modified: Thu, 22 Oct 2020 02:46:10 GMT  
		Size: 926.4 KB (926394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746e2d2217623d0a52653391881289717c3b58886a6dd0e0c2c74933de18c3c9`  
		Last Modified: Thu, 22 Oct 2020 02:46:35 GMT  
		Size: 197.7 MB (197669288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56070a9ecf8d4e86e521ff7ab17d2a03665c40660ee01dfa301ca13b4a54d8d7`  
		Last Modified: Thu, 22 Oct 2020 08:36:06 GMT  
		Size: 14.0 MB (13966811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca5451a9d019c2884fb9820baafb0ee014f6065b7c1650e4499af7198e70c40`  
		Last Modified: Thu, 22 Oct 2020 08:36:05 GMT  
		Size: 4.2 MB (4168137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
