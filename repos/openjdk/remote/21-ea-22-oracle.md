## `openjdk:21-ea-22-oracle`

```console
$ docker pull openjdk@sha256:6545510099d090fc2044f02b52405a4cb1715e932bbf80e12d4376a6395e1aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:21-ea-22-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:9dc558d41a1acd6b97136ce2ebbfb9b5194c401904675fedbc977116295d8e33
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.7 MB (261736825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00162fe5c935ca27514e6dd116f506533fde96e11273b9ac1cd3068fc4827f3`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 06 Apr 2023 18:20:31 GMT
ADD file:61a2085af5116916e7b117c2e7ad7116bdc0282d8fa9ce76191c4101f5e866ff in / 
# Thu, 06 Apr 2023 18:20:32 GMT
CMD ["/bin/bash"]
# Thu, 06 Apr 2023 18:37:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 06 Apr 2023 18:37:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Thu, 06 Apr 2023 18:37:15 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Apr 2023 18:37:16 GMT
ENV LANG=C.UTF-8
# Thu, 11 May 2023 23:01:38 GMT
ENV JAVA_VERSION=21-ea+22
# Thu, 11 May 2023 23:01:56 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/22/GPL/openjdk-21-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='6ae3958a32809960b925b0fc4fae2236b5640c92b015274035fe3fb3ceb94f98'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/22/GPL/openjdk-21-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='c9afb1a0be1b35ed1e61bab79d5fec466f7e5c42b65bd8a65595d6699d0e77cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 11 May 2023 23:01:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:328ba678bf27575937f8b9dfbf5b5f39b21941af068f8e5960de8131e289da85`  
		Last Modified: Thu, 06 Apr 2023 18:21:19 GMT  
		Size: 44.6 MB (44563902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55560f49b1cd4515e5c12b0a190ca11492533ca3757e761c254daf809031bdc5`  
		Last Modified: Thu, 06 Apr 2023 18:38:00 GMT  
		Size: 15.0 MB (15002954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cae0e92f0cac6ebd681120532cd5c08e603197ae51005af632b0dbee9495e0`  
		Last Modified: Thu, 11 May 2023 23:04:15 GMT  
		Size: 202.2 MB (202169969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
