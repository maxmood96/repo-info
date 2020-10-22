## `clojure:openjdk-16-tools-deps-1.10.1.716-alpine`

```console
$ docker pull clojure@sha256:a56083972de0c4423f0a221dc9a66dd22c41c9c226ec10a0c27a93fa7265c12c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-16-tools-deps-1.10.1.716-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:9298ebefd73554d4d1fa5424b99ce48299a00ccc8485b8773fe62a4fe36dcf12
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223936258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9275c73739aaf64de6d0fed7d44d9bf76dce11ed375659625447e99fb83054a6`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

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
# Thu, 22 Oct 2020 08:34:26 GMT
ENV CLOJURE_VERSION=1.10.1.716
# Thu, 22 Oct 2020 08:34:26 GMT
WORKDIR /tmp
# Thu, 22 Oct 2020 08:34:35 GMT
RUN apk add --update --no-cache curl bash make && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "6900337e2210895130394bb93248465f7fb9a427fec46638636398bbe82842e3 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Thu, 22 Oct 2020 08:34:35 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
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
	-	`sha256:da8803574cd4a263b97410e0b60dc8c7e9e1bb4486c522fdf885580e4ac8022e`  
		Last Modified: Thu, 22 Oct 2020 08:36:22 GMT  
		Size: 22.5 MB (22543716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
