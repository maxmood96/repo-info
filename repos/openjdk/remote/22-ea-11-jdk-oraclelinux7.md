## `openjdk:22-ea-11-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:71bb2dc6ec317a95bf82616b5590eac3a949f240000f10700d39772135729e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `openjdk:22-ea-11-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:88bdf16fbe83a20c93512778ee28f89355060cf1771d264bb467c210c37918fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269445749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64799f95089a2c7403f598f9bb45594e98a10ce6bf543037fa93b22f1c73cf85`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Jun 2023 03:45:43 GMT
ADD file:a9ba9c7acb256e802c7248b56f377a6f0ea08b1b61e11e482516633a13f4d686 in / 
# Wed, 14 Jun 2023 03:45:44 GMT
CMD ["/bin/bash"]
# Wed, 14 Jun 2023 04:08:20 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 14 Jun 2023 04:08:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Wed, 14 Jun 2023 04:08:20 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 04:08:20 GMT
ENV LANG=en_US.UTF-8
# Thu, 17 Aug 2023 21:46:45 GMT
ENV JAVA_VERSION=22-ea+11
# Thu, 17 Aug 2023 21:46:57 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/11/GPL/openjdk-22-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='dce8ce5e81ef514ed2faafa3099af148988d8ef1faf5bdd4f7775eff0c3d6179'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/11/GPL/openjdk-22-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='12210754c3958bf625bcd480cc2381c1059dff46c417dcbe71f0baff189f7df0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 17 Aug 2023 21:46:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:52fd87ed40fcddc3fe63b876d1f94f6edae688637a5cc56983dced68a50c953e`  
		Last Modified: Wed, 14 Jun 2023 03:46:28 GMT  
		Size: 51.1 MB (51052081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39aeb39f5d39e6fb51e698f8f5e6416d0689047f9392a9bd3f97f28c4d5d5596`  
		Last Modified: Wed, 14 Jun 2023 04:10:01 GMT  
		Size: 15.2 MB (15238146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c2e3f9353075d6c3903eb2c31ba781a5b83d3564acbf40960757f1cee3395`  
		Last Modified: Thu, 17 Aug 2023 21:49:54 GMT  
		Size: 203.2 MB (203155522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
