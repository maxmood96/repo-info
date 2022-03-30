## `clojure:openjdk-19-lein-2.9.8-alpine`

```console
$ docker pull clojure@sha256:c02c6b087e8d4a105f84eea36afb668588daa6605129500c9dbff91776594f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:openjdk-19-lein-2.9.8-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:892a2b22f01e3931282ba2c9af7a364ed58fbe02206e676e5941aaaed525510d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210938864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10238bb091b8d1ba1703f90511a53f6bcf552ffa5fe3eeadfa15a1455040d31`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 00:53:12 GMT
RUN apk add --no-cache java-cacerts
# Tue, 29 Mar 2022 00:53:12 GMT
ENV JAVA_HOME=/opt/openjdk-19
# Tue, 29 Mar 2022 00:53:12 GMT
ENV PATH=/opt/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 00:53:12 GMT
ENV JAVA_VERSION=19-ea+5
# Tue, 29 Mar 2022 00:53:23 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/5/binaries/openjdk-19-ea+5_linux-x64-musl_bin.tar.gz'; 			downloadSha256='0ee67a41fe97341f131bd4f065ed6092d55c15de5f00f8ba1e57d21eefb2c787'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 00:53:24 GMT
CMD ["jshell"]
# Tue, 29 Mar 2022 23:53:54 GMT
ENV LEIN_VERSION=2.9.8
# Tue, 29 Mar 2022 23:53:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 29 Mar 2022 23:53:54 GMT
WORKDIR /tmp
# Tue, 29 Mar 2022 23:53:58 GMT
RUN set -eux; apk add --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "9952cba539cc6454c3b7385ebce57577087bf2b9001c3ab5c55d668d0aeff6e9 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg
# Tue, 29 Mar 2022 23:53:58 GMT
ENV PATH=/opt/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 29 Mar 2022 23:53:58 GMT
ENV LEIN_ROOT=1
# Tue, 29 Mar 2022 23:54:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Tue, 29 Mar 2022 23:54:02 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 29 Mar 2022 23:54:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 29 Mar 2022 23:54:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc6d90ffa98debe440e17dff9ae93f8fc2b8065f5e2d7bc0d2261f9651ae35b`  
		Last Modified: Tue, 29 Mar 2022 01:06:31 GMT  
		Size: 918.6 KB (918583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1650a84836207ca17554d4eebd9a03ac64a82705d0b490da64d2094be0481e6`  
		Last Modified: Tue, 29 Mar 2022 01:06:45 GMT  
		Size: 190.6 MB (190592769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed72e1e187f5ff3dd6075f0cc2ef17c35385529580b704eec70d2243ca2c198`  
		Last Modified: Wed, 30 Mar 2022 00:13:39 GMT  
		Size: 12.4 MB (12405403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205be25ed0ce008b289905c6caedf2b12e37e1038eebd904c7abb8ee739ebce1`  
		Last Modified: Wed, 30 Mar 2022 00:13:39 GMT  
		Size: 4.2 MB (4207191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef76e33c8d9e64f94f6c8f247a160532205b5bb610e123c4f4b5352eb8e024fd`  
		Last Modified: Wed, 30 Mar 2022 00:13:39 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
