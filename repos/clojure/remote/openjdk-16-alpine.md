## `clojure:openjdk-16-alpine`

```console
$ docker pull clojure@sha256:dd2787273f0ab871bb7d013349bc355083a337de2cd9e3e20f9af5f5cadf386d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-16-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:16f7ee523b54a3bfe85f54678300d34550279657c0062f68eb3e374390572f31
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.2 MB (206214047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3d3d4f581735b4a6fe67e0c676cda843672df66c9c20d597c0cc9ee6567366`
-	Default Command: `["lein","repl"]`

```dockerfile
# Thu, 28 Jan 2021 23:19:38 GMT
ADD file:0e2d487cd80773e947c8aae6daad3d565b7bb019a954af2b8bff188681c00d81 in / 
# Thu, 28 Jan 2021 23:19:38 GMT
CMD ["/bin/sh"]
# Mon, 01 Feb 2021 19:46:23 GMT
RUN apk add --no-cache java-cacerts
# Mon, 01 Feb 2021 19:49:51 GMT
ENV JAVA_HOME=/opt/openjdk-16
# Mon, 01 Feb 2021 19:49:51 GMT
ENV PATH=/opt/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:49:52 GMT
ENV JAVA_VERSION=16-ea+32
# Mon, 01 Feb 2021 19:50:18 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/32/binaries/openjdk-16-ea+32_linux-x64-musl_bin.tar.gz'; 			downloadSha256='f9ec3071fdea08ca5be7b149d6c2f2689814e3ee86ee15b7981f5eed76280985'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Feb 2021 19:50:19 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 20:48:15 GMT
ENV LEIN_VERSION=2.9.5
# Mon, 01 Feb 2021 20:48:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 01 Feb 2021 20:48:16 GMT
WORKDIR /tmp
# Mon, 01 Feb 2021 20:48:20 GMT
RUN apk add --update --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "3601d55c4b5ac5c654e4ebd0d75abf7ad683f48cba8a7af1a8730b6590187b8a *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver keys.openpgp.org --recv-key 20242BACBBE95ADA22D0AFD7808A33D379C806C3 && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.zip.asc leiningen-$LEIN_VERSION-standalone.zip && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg
# Mon, 01 Feb 2021 20:48:20 GMT
ENV PATH=/opt/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 01 Feb 2021 20:48:20 GMT
ENV LEIN_ROOT=1
# Mon, 01 Feb 2021 20:48:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.1"]])' > project.clj   && lein deps && rm project.clj
# Mon, 01 Feb 2021 20:48:25 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:4c0d98bf9879488e0407f897d9dd4bf758555a78e39675e72b5124ccf12c2580`  
		Last Modified: Thu, 28 Jan 2021 23:20:08 GMT  
		Size: 2.8 MB (2811321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1834e342ac63f74ab268f59b78219089f04f37c6c39e469afc0292192b9c2d`  
		Last Modified: Mon, 01 Feb 2021 20:02:23 GMT  
		Size: 928.2 KB (928244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f4563ac5cfaa5b85c77a78809e4a4d118e39ea769eff648554e6b66d21ad3f`  
		Last Modified: Mon, 01 Feb 2021 20:05:18 GMT  
		Size: 186.0 MB (185958372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7aa6f3a9991e67c50875a99d305a5cac3152a61e0289b1ab1bb0968130b6f0`  
		Last Modified: Mon, 01 Feb 2021 20:54:33 GMT  
		Size: 12.3 MB (12335866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34619f168e6e91b785086a69d015f0c5ee8c1dc6e0f1b924fd0e8af1a5fe8793`  
		Last Modified: Mon, 01 Feb 2021 20:54:32 GMT  
		Size: 4.2 MB (4180244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
