## `clojure:openjdk-17-lein-2.9.5-alpine`

```console
$ docker pull clojure@sha256:ebf666f1aba034069ccc1f61585a2cfc1e202437664eac960a164fce4326e618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-17-lein-2.9.5-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:4c0ea9cd148740a7b67cf312f488ffcffb622d334cddd89d7207b906babb500d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.1 MB (207077716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6753061f096705b331512c82628a3b4b7eda3ea428464dc5a6f592391037d5e2`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 01:15:06 GMT
RUN apk add --no-cache java-cacerts
# Thu, 01 Apr 2021 01:15:07 GMT
ENV JAVA_HOME=/opt/openjdk-17
# Thu, 01 Apr 2021 01:15:07 GMT
ENV PATH=/opt/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Apr 2021 01:15:07 GMT
ENV JAVA_VERSION=17-ea+14
# Thu, 01 Apr 2021 01:15:19 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/14/binaries/openjdk-17-ea+14_linux-x64-musl_bin.tar.gz'; 			downloadSha256='f07a1ac921333dafac1cd886ad49600ce143be7efebd32e1a02599a8a0829dd4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 01 Apr 2021 01:15:20 GMT
CMD ["jshell"]
# Thu, 01 Apr 2021 01:52:44 GMT
ENV LEIN_VERSION=2.9.5
# Thu, 01 Apr 2021 01:52:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 01 Apr 2021 01:52:45 GMT
WORKDIR /tmp
# Thu, 01 Apr 2021 01:52:51 GMT
RUN apk add --update --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "3601d55c4b5ac5c654e4ebd0d75abf7ad683f48cba8a7af1a8730b6590187b8a *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver keys.openpgp.org --recv-key 20242BACBBE95ADA22D0AFD7808A33D379C806C3 && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.zip.asc leiningen-$LEIN_VERSION-standalone.zip && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg
# Thu, 01 Apr 2021 01:52:52 GMT
ENV PATH=/opt/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Apr 2021 01:52:52 GMT
ENV LEIN_ROOT=1
# Thu, 01 Apr 2021 01:52:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Thu, 01 Apr 2021 01:52:56 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c0977514f1a113de97ffc6f5e9fd1873b8d77fb352205316fdc4d7696aab84`  
		Last Modified: Thu, 01 Apr 2021 01:21:03 GMT  
		Size: 928.4 KB (928397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563752cd6ffc7ae1632f28e21155f16c5b95902be182e29ba84e415f794f40c1`  
		Last Modified: Thu, 01 Apr 2021 01:21:19 GMT  
		Size: 186.8 MB (186797685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6aeba2f7977d9f186dc02d16afce641cab377de97f70a5127b6127071803cf6`  
		Last Modified: Thu, 01 Apr 2021 02:09:01 GMT  
		Size: 12.3 MB (12335957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b93a7166dcd0ddc5a91bf34bf652f020bf1385e772928f92a188aaac6bb8107`  
		Last Modified: Thu, 01 Apr 2021 02:09:00 GMT  
		Size: 4.2 MB (4203730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
