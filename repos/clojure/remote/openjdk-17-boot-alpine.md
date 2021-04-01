## `clojure:openjdk-17-boot-alpine`

```console
$ docker pull clojure@sha256:facc15446a9fc75db6a4e6850bf4beb7c0d5fdbb41febe45c15c7fcd49fb5e00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-17-boot-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:5dd01a69f29f2c8ad3f4d1673bfd39859dd4633f3d9274275b4fd40a8ce1c0f7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250187022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d518c4b987c161893a99bd101aff272db75ba4b37699404e02ea0a44c90a64`
-	Default Command: `["boot","repl"]`

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
# Thu, 01 Apr 2021 01:52:59 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 01 Apr 2021 01:53:00 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 01 Apr 2021 01:53:00 GMT
WORKDIR /tmp
# Thu, 01 Apr 2021 01:53:02 GMT
RUN apk add --update --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Thu, 01 Apr 2021 01:53:02 GMT
ENV PATH=/opt/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Apr 2021 01:53:02 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 01 Apr 2021 01:53:34 GMT
RUN boot
# Thu, 01 Apr 2021 01:53:35 GMT
CMD ["boot" "repl"]
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
	-	`sha256:7f4a96b9f294d2016d8340bc4192971522653a18bf66fc6c4c795500fb803ac8`  
		Last Modified: Thu, 01 Apr 2021 02:09:16 GMT  
		Size: 828.4 KB (828422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8985d022b587c95f8a7425c7103e7e10d638d9bb31d0898ac5275ec312e428`  
		Last Modified: Thu, 01 Apr 2021 02:09:20 GMT  
		Size: 58.8 MB (58820571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
