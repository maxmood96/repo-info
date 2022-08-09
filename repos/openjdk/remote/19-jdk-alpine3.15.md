## `openjdk:19-jdk-alpine3.15`

```console
$ docker pull openjdk@sha256:00b9080d669d1997313721aa3ed907ab1cac2df3019e5781a4682c9511d08bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:19-jdk-alpine3.15` - linux; amd64

```console
$ docker pull openjdk@sha256:cbdb435d9b47bdc7fd573a013fbe14ccbdd26af529974df5833141eca2731f54
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194354142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910fb474f1ecde1bdfb12364ba6aa16a6fb2db11221b4fde46af3641a6cd5ce2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 21:10:37 GMT
RUN apk add --no-cache java-cacerts
# Tue, 09 Aug 2022 21:10:37 GMT
ENV JAVA_HOME=/opt/openjdk-19
# Tue, 09 Aug 2022 21:10:37 GMT
ENV PATH=/opt/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 21:10:37 GMT
ENV JAVA_VERSION=19-ea+5
# Tue, 09 Aug 2022 21:10:48 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/5/binaries/openjdk-19-ea+5_linux-x64-musl_bin.tar.gz'; 			downloadSha256='0ee67a41fe97341f131bd4f065ed6092d55c15de5f00f8ba1e57d21eefb2c787'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 09 Aug 2022 21:10:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc550899027618975a3a4e9a37341517d3e717cc6784cc2b745a43f8a8959726`  
		Last Modified: Tue, 09 Aug 2022 21:17:43 GMT  
		Size: 937.9 KB (937925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ff0d8f4379710530e1488163d9ae4878f96eee4295313d069017605b4564c1`  
		Last Modified: Tue, 09 Aug 2022 21:17:57 GMT  
		Size: 190.6 MB (190592705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
