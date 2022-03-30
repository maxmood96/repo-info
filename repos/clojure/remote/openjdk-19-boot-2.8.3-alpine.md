## `clojure:openjdk-19-boot-2.8.3-alpine`

```console
$ docker pull clojure@sha256:9b71a29d6325b70e10786e097a1c92a732a8d3d4dad6ff1ae7851034fcca8117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:openjdk-19-boot-2.8.3-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:56d3d3ca89a4524d92be1ba9b10f6878407feff5c1c7918d6b1b4280694fa7ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (253978103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f21d7f016e8aac91127252c8451ce998a5dab6bb7e6416693705c7262ff481`
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
# Tue, 29 Mar 2022 23:54:05 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 29 Mar 2022 23:54:05 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 29 Mar 2022 23:54:05 GMT
WORKDIR /tmp
# Tue, 29 Mar 2022 23:54:06 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Tue, 29 Mar 2022 23:54:07 GMT
ENV PATH=/opt/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 29 Mar 2022 23:54:07 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 29 Mar 2022 23:54:30 GMT
RUN boot
# Tue, 29 Mar 2022 23:54:30 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 29 Mar 2022 23:54:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 29 Mar 2022 23:54:30 GMT
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
	-	`sha256:8f011ea1ee9820588cd4b1cd2c7d5184b1e89c5192ee7289212d6d1641afffde`  
		Last Modified: Wed, 30 Mar 2022 00:13:49 GMT  
		Size: 831.3 KB (831325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffc0faf058a9923b3faa088a685edd9c81152aac5bac69f73f403cd822ca65b`  
		Last Modified: Wed, 30 Mar 2022 00:13:52 GMT  
		Size: 58.8 MB (58820509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b086de710d42fee5debbee5f924571b76829135ef8b57c4345d7c8339b12d4`  
		Last Modified: Wed, 30 Mar 2022 00:13:49 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
