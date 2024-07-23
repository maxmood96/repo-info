## `openjdk:24-ea-7-oraclelinux8`

```console
$ docker pull openjdk@sha256:a4d765352345a8d6a9588ff35e8e0bd7b292db99efa7dcf4ffbfb6c9775a92c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-7-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:038945c08f15576a3cd149e80060e2dad9c0a50de5d63f198ff1f55a27912f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.2 MB (278248327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e1e276728612d8b23fcf2fe096d7dce5c5408104b2239db53fb7b39864c52f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 03 Jul 2024 23:20:38 GMT
ADD file:789b4bad3c8ec49deaec755e6ce00146287ec0b8dd5361181f491244ef0c5901 in / 
# Wed, 03 Jul 2024 23:20:38 GMT
CMD ["/bin/bash"]
# Sat, 20 Jul 2024 00:52:05 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 20 Jul 2024 00:52:05 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 20 Jul 2024 00:52:05 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 00:52:05 GMT
ENV LANG=C.UTF-8
# Sat, 20 Jul 2024 00:52:05 GMT
ENV JAVA_VERSION=24-ea+7
# Sat, 20 Jul 2024 00:52:05 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/7/GPL/openjdk-24-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='d175c4cfc7ab8306b42cf88fe0e60b2b827a2106c026ae6d2a3f2e51bbcb60d0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/7/GPL/openjdk-24-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='5df46f7b64a38a7a34e1b283f6c37b57f8238567b81c3db0f127f348f4842977'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 20 Jul 2024 00:52:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46ed4d5ee531c13affa3e9cde2a49eff959d69e21ccfb79df05d6d268512b8b9`  
		Last Modified: Wed, 03 Jul 2024 23:21:44 GMT  
		Size: 51.2 MB (51219624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f9b7fbf404a560bcd8d20188d8a13267df2d1b0219108021aed4deef915dbe`  
		Last Modified: Mon, 22 Jul 2024 21:00:15 GMT  
		Size: 15.0 MB (15036200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0a4a09f2eb4c512b6dc21d8b87c526802721c3be1d9f22bbbc969b9df0c60c`  
		Last Modified: Mon, 22 Jul 2024 21:00:18 GMT  
		Size: 212.0 MB (211992503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-7-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:b9e8ad25676cd33df82d146206999adffcad221f3e874ff205085e8a5ddb8466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68ef9c53fd804c306c5717735fbee40ce2a218565f31d199e6d4fe91c56a663`

```dockerfile
```

-	Layers:
	-	`sha256:334e53007cf853783549daf66defa9793d6ac50d9855a1d7115b5431b9181401`  
		Last Modified: Mon, 22 Jul 2024 21:00:15 GMT  
		Size: 2.3 MB (2287817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f090670c53ea0af20335c7a6b298f91abbe00dc684d33bddd9c46ae4a5ab5a0`  
		Last Modified: Mon, 22 Jul 2024 21:00:15 GMT  
		Size: 15.8 KB (15803 bytes)  
		MIME: application/vnd.in-toto+json
