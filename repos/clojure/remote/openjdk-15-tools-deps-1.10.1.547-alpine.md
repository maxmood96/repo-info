## `clojure:openjdk-15-tools-deps-1.10.1.547-alpine`

```console
$ docker pull clojure@sha256:8cd75c7deb217cc9c293e69843ccdd0acb71ffcec4750465e90973c65c5e4688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-15-tools-deps-1.10.1.547-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:3c0c6d04ed6fe55ffc2f69c3424ef2b88a8f6a1e683a8199d4a300b9c9896b53
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226108728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940aa48c64cb926fcb9b5df896ec55c0d5381e3753693ebd1408d2b26c78f25a`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2020 20:22:15 GMT
RUN apk add --no-cache java-cacerts
# Mon, 22 Jun 2020 20:22:15 GMT
ENV JAVA_HOME=/opt/openjdk-15
# Mon, 22 Jun 2020 20:22:15 GMT
ENV PATH=/opt/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2020 20:22:16 GMT
ENV JAVA_VERSION=15-ea+10
# Mon, 22 Jun 2020 20:22:16 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/alpine/10/binaries/openjdk-15-ea+10_linux-x64-musl_bin.tar.gz
# Mon, 22 Jun 2020 20:22:16 GMT
ENV JAVA_SHA256=15a5e8002e24ed129b82bfe55ffe4bdbf3cfd0a7e5ad3399879cdd44175bfd06
# Mon, 22 Jun 2020 20:22:57 GMT
RUN set -eux; 		wget -O /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java --version; 	javac --version
# Mon, 22 Jun 2020 20:22:57 GMT
CMD ["jshell"]
# Mon, 06 Jul 2020 19:30:00 GMT
ENV CLOJURE_VERSION=1.10.1.547
# Mon, 06 Jul 2020 19:30:00 GMT
WORKDIR /tmp
# Mon, 06 Jul 2020 19:30:09 GMT
RUN apk add --update --no-cache curl bash make && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "779ce3bd2aea008fa4d7a0569d00b1a1011b88662960355bab54fb86851ae5ad *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Mon, 06 Jul 2020 19:30:10 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0121b9d547c5ad1e5b9845b4a6b9f44a4bb6c15e45cc609316809d19b5d27345`  
		Last Modified: Mon, 22 Jun 2020 20:26:56 GMT  
		Size: 971.8 KB (971778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ae062329c82bbdb09eb9b3ac5a9f754a1a9a4d7ffb87a547ffbefccb4ed628`  
		Last Modified: Mon, 22 Jun 2020 20:27:13 GMT  
		Size: 199.8 MB (199807555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a43deb4abf5847b0ddcefdd2e58be330e006a55ba5a63fe2417b483fbcd6500`  
		Last Modified: Mon, 06 Jul 2020 19:32:17 GMT  
		Size: 22.5 MB (22516079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
