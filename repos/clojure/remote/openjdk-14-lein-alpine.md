## `clojure:openjdk-14-lein-alpine`

```console
$ docker pull clojure@sha256:5750f851e44e42c58e3befbd5c76742323bb597a7d286f5cb515eff3726b65f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-14-lein-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:139651621b1dbf34e8f52edbee4dda0abac22e3c2e19018c8986cdc5b404953b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221658625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa5a6a36afe4119f1b51603424552086451dfb299283a83bbec1c86a43618f1`
-	Default Command: `["lein","repl"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 22:15:00 GMT
ENV JAVA_HOME=/opt/openjdk-14
# Thu, 23 Jan 2020 22:15:00 GMT
ENV PATH=/opt/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 01:03:57 GMT
ENV JAVA_VERSION=14-ea+33
# Tue, 28 Jan 2020 01:03:57 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/alpine/33/binaries/openjdk-14-ea+33_linux-x64-musl_bin.tar.gz
# Tue, 28 Jan 2020 01:03:58 GMT
ENV JAVA_SHA256=25344fdf7438d05166fb3471a591aacf72e5fc7ca334b59b3f90ff34ee3b27e5
# Tue, 28 Jan 2020 01:05:39 GMT
RUN set -eux; 		wget -O /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		java -Xshare:dump; 		java --version; 	javac --version
# Tue, 28 Jan 2020 01:05:39 GMT
CMD ["jshell"]
# Tue, 28 Jan 2020 02:30:06 GMT
ENV LEIN_VERSION=2.9.1
# Tue, 28 Jan 2020 02:30:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 Jan 2020 02:30:06 GMT
WORKDIR /tmp
# Tue, 28 Jan 2020 02:30:09 GMT
RUN apk add --update --no-cache bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha1sum lein-pkg && echo "93be2c23ab4ff2fc4fcf531d7510ca4069b8d24a *lein-pkg" | sha1sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver pool.sks-keyservers.net --recv-key 2B72BF956E23DE5E830D50F6002AF007D1A7CC18 && echo "Verifying Jar file signature ..." && gpg --verify leiningen-$LEIN_VERSION-standalone.zip.asc && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del tar openssl gnupg
# Tue, 28 Jan 2020 02:30:09 GMT
ENV PATH=/opt/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 Jan 2020 02:30:10 GMT
ENV LEIN_ROOT=1
# Tue, 28 Jan 2020 02:30:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 28 Jan 2020 02:30:14 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345cf19c142c73b4673b7f5195d90723d77f452a902206b91c63c6ddca4e6bb7`  
		Last Modified: Tue, 28 Jan 2020 01:09:10 GMT  
		Size: 200.4 MB (200355870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d27bb1938563fb80ac536b2ed756d6d0cc1c65e6bbd459a6df32647a91e6341`  
		Last Modified: Tue, 28 Jan 2020 02:32:34 GMT  
		Size: 14.3 MB (14347612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bfcd5c78aede02b54efdbec96f6fbda7b5bdc9c7912baf74536604db089e54`  
		Last Modified: Tue, 28 Jan 2020 02:32:34 GMT  
		Size: 4.2 MB (4168181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
