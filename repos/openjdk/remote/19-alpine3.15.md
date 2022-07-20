## `openjdk:19-alpine3.15`

```console
$ docker pull openjdk@sha256:ea52ef52e02bbb0c56e277a566cee1bb0292d48c753168cb3399326d7226e6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:19-alpine3.15` - linux; amd64

```console
$ docker pull openjdk@sha256:e36f5031752f708c9d6ecd3a7f979c1e522b0e6a3de3ed30c40be5fcbe2952fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 MB (194326003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36cb086678fba619e3f116f0c2edeec5609d7faab723297844926adc2cb388cf`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 03:21:06 GMT
RUN apk add --no-cache java-cacerts
# Wed, 20 Jul 2022 03:21:06 GMT
ENV JAVA_HOME=/opt/openjdk-19
# Wed, 20 Jul 2022 03:21:06 GMT
ENV PATH=/opt/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Jul 2022 03:21:06 GMT
ENV JAVA_VERSION=19-ea+5
# Wed, 20 Jul 2022 03:21:31 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/5/binaries/openjdk-19-ea+5_linux-x64-musl_bin.tar.gz'; 			downloadSha256='0ee67a41fe97341f131bd4f065ed6092d55c15de5f00f8ba1e57d21eefb2c787'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 20 Jul 2022 03:21:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe0a7397a0967e998407117b38468b0119aef452950b50c59982808b2247324`  
		Last Modified: Wed, 20 Jul 2022 03:27:47 GMT  
		Size: 918.6 KB (918577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549fca73ea0136920b0fb6de42311df97f8a8dbec94d10e027bd7611e633aab9`  
		Last Modified: Wed, 20 Jul 2022 03:28:01 GMT  
		Size: 190.6 MB (190592781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
