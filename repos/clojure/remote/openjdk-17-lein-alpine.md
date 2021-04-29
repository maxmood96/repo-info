## `clojure:openjdk-17-lein-alpine`

```console
$ docker pull clojure@sha256:393c07155282ca9a3b9a1f951cdf456d1a4ae7bc8ee9a27dc30c4c846e0e6f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-17-lein-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:9a6a662aea2fd0d1f467ebe36a80b4cd9ea111dcb5da29c7203e144c82eb982e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.1 MB (207083397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b965cad1e7efd8520812a756af558621fa7d6929737edaaea3ef01826f8a7b2`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:36:27 GMT
RUN apk add --no-cache java-cacerts
# Wed, 14 Apr 2021 23:36:27 GMT
ENV JAVA_HOME=/opt/openjdk-17
# Wed, 14 Apr 2021 23:36:27 GMT
ENV PATH=/opt/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 23:36:28 GMT
ENV JAVA_VERSION=17-ea+14
# Wed, 14 Apr 2021 23:36:39 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/14/binaries/openjdk-17-ea+14_linux-x64-musl_bin.tar.gz'; 			downloadSha256='f07a1ac921333dafac1cd886ad49600ce143be7efebd32e1a02599a8a0829dd4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 14 Apr 2021 23:36:40 GMT
CMD ["jshell"]
# Thu, 29 Apr 2021 17:23:23 GMT
ENV LEIN_VERSION=2.9.6
# Thu, 29 Apr 2021 17:23:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 29 Apr 2021 17:23:23 GMT
WORKDIR /tmp
# Thu, 29 Apr 2021 17:23:28 GMT
RUN apk add --update --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "094b58e2b13b42156aaf7d443ed5f6665aee27529d9512f8d7282baa3cc01429 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver keys.openpgp.org --recv-key 20242BACBBE95ADA22D0AFD7808A33D379C806C3 && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.zip.asc leiningen-$LEIN_VERSION-standalone.zip && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg
# Thu, 29 Apr 2021 17:23:28 GMT
ENV PATH=/opt/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 29 Apr 2021 17:23:29 GMT
ENV LEIN_ROOT=1
# Thu, 29 Apr 2021 17:23:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Thu, 29 Apr 2021 17:23:32 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59807c90332abccc99cec67ac7e54a6f2030704f47653b41ca8d4d82301dcbd`  
		Last Modified: Wed, 14 Apr 2021 23:42:06 GMT  
		Size: 928.4 KB (928421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f4673b4883008024de99185a0fa8b4c418c4208a54a723b50b7244eeaec203`  
		Last Modified: Wed, 14 Apr 2021 23:42:21 GMT  
		Size: 186.8 MB (186798307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad245801c636968e035eb89fdebbf7bd036a7d6e423fd47fec7ccf5c52617aa`  
		Last Modified: Thu, 29 Apr 2021 17:28:43 GMT  
		Size: 12.3 MB (12340965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd15b9f1abd2d3f0e85ea46fe1181defbb337373545453073fa060386ad9023`  
		Last Modified: Thu, 29 Apr 2021 17:28:43 GMT  
		Size: 4.2 MB (4203735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
