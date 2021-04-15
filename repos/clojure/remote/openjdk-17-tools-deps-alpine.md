## `clojure:openjdk-17-tools-deps-alpine`

```console
$ docker pull clojure@sha256:26357b6d0066dbe3c4be1e252ee1730c05f588ea76943daa4ddb75f94f7c2756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-17-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:79067c16f465a94e21ed3f40e6f7c3e8f9786696a5c8dabba775244d6bf91983
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208948137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f309d11d881786de5cf9d7e445884e55c65177b2523322b5800e335344e6a2`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

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
# Thu, 15 Apr 2021 10:07:32 GMT
ENV CLOJURE_VERSION=1.10.3.822
# Thu, 15 Apr 2021 10:07:32 GMT
WORKDIR /tmp
# Thu, 15 Apr 2021 10:07:39 GMT
RUN apk add --update --no-cache curl bash make && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ebc820fe0e74de4bd77e6d5bd7db4a262ec1902efdf4d0553309485afcd75abf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Thu, 15 Apr 2021 10:07:39 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
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
	-	`sha256:179c22e86c1d475622a600efc334952132f13b4c9eaa72fb212ac77a48d87d42`  
		Last Modified: Thu, 15 Apr 2021 10:11:13 GMT  
		Size: 18.4 MB (18409440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
