## `clojure:openjdk-14-tools-deps-alpine`

```console
$ docker pull clojure@sha256:5874f17f654e23172962a93e5b74638375af996c3f8deb4b4b8fdd8b8b18d36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-14-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:1c3a20b3c7c77f060d850a895a6c0cd1399c88f7e301818188168de9e026f9e5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226080695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d493106d4c7e1643b6e6374efa48745a1a22053d29e686be1a3222f90c7ae9d7`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

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
# Tue, 28 Jan 2020 02:31:32 GMT
ENV CLOJURE_VERSION=1.10.1.502
# Tue, 28 Jan 2020 02:31:33 GMT
WORKDIR /tmp
# Tue, 28 Jan 2020 02:31:41 GMT
RUN apk add --update --no-cache curl bash make && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Tue, 28 Jan 2020 02:31:41 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
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
	-	`sha256:0703dacb21a8837971f39fc3beea0a6c17c58c13664828d6d4c087cec9e07a0f`  
		Last Modified: Tue, 28 Jan 2020 02:32:49 GMT  
		Size: 22.9 MB (22937863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
