## `openjdk:23-ea-oraclelinux9`

```console
$ docker pull openjdk@sha256:c87f75b8b18870bde32c9137f172ba34de8c72ee3b822d41cd968998f7ae10a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:13ee6eb48c4bd8d73d58bb9db45484e278935d42ddf9886bcac47107c7b0bcb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.6 MB (297560436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82fdd39c5e63c8735a9343b5e0660545e48d95b0d4a53c0d1f79d1ea5a338076`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:04 GMT
ADD file:9bcef05fa351e2fb72a4b6052a0252eeaa2cff794ed089a482670c67961d2e90 in / 
# Fri, 08 Mar 2024 19:21:04 GMT
CMD ["/bin/bash"]
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Thu, 04 Apr 2024 18:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+17
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='e7d451c3caeb76083337f090da37588acb90bb60417bff99ef160a3a8b730bfd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='9ede1afd67be11e1e99e13b78f8b3159c14107cc919920d0e1e30636f67b92b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:972029ff9873af36c6c0fcee05b14acbc57a61ecd0b8bf86b167bdf46f973823`  
		Last Modified: Fri, 08 Mar 2024 19:22:31 GMT  
		Size: 49.0 MB (48978454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f79db7cdc29ebc9132d9674a8ebe3ab1650b04f8332355d709ba3724c0d1a3`  
		Last Modified: Fri, 05 Apr 2024 17:52:39 GMT  
		Size: 37.7 MB (37737131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734aa191b9dfe5279c951699a4a480ca95f4406a97147f2de83b6b8083544a73`  
		Last Modified: Fri, 05 Apr 2024 17:52:43 GMT  
		Size: 210.8 MB (210844851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:530d20b94339952ccec8043b29f52a7360bf149ef9095f9e5c2c405326f95711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3349426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11465c6433a0ac736805aade037255a9977cb3f1e76836af8514e28161feab53`

```dockerfile
```

-	Layers:
	-	`sha256:43949525415390922a9335de10f43e495179a5380ba0237a20bd1614c5582bf2`  
		Last Modified: Fri, 05 Apr 2024 17:52:38 GMT  
		Size: 3.3 MB (3329538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:964fe03502b2698b174f1b154fb46927aff4062e51f26e82c2f564ea876aa945`  
		Last Modified: Fri, 05 Apr 2024 17:52:38 GMT  
		Size: 19.9 KB (19888 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:67d7d255581d4a3fff1e8d38f5a71cd04751f4d024ac0df39212094ed105e2dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294538990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c38096ad04f7a65c6bd82f22c71df3a1656552da2db7740a2538209f4910196`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 08 Mar 2024 19:48:53 GMT
ADD file:71724b501850c3e6cd72efc58b3430394f691a428c2c62755eac0b93c5579f35 in / 
# Fri, 08 Mar 2024 19:48:53 GMT
CMD ["/bin/bash"]
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Thu, 04 Apr 2024 18:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+17
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='e7d451c3caeb76083337f090da37588acb90bb60417bff99ef160a3a8b730bfd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='9ede1afd67be11e1e99e13b78f8b3159c14107cc919920d0e1e30636f67b92b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c53b3bc8702e4b172b3fdde99731082a493b5f5fdd7e9632b3cf7dea02a52b4`  
		Last Modified: Fri, 08 Mar 2024 19:49:57 GMT  
		Size: 47.7 MB (47664888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71597242e3bc84850918d978b72bcf84c5867bfb6441051c67b805dca13e66a`  
		Last Modified: Sat, 16 Mar 2024 15:50:44 GMT  
		Size: 38.1 MB (38140694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaca8e4b43c229d5798a3d44bb80d4f0d0d96c6deb2bb29d044ffcc13603e29a`  
		Last Modified: Fri, 05 Apr 2024 17:56:06 GMT  
		Size: 208.7 MB (208733408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:ceaeecf7d121512679c9dbfe0acec28e25f53405dce223a03521b46f5608c319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3346520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b766374b27eb2682bc21c321147de76ef779c8ce39a0d40a2301cff49a0ce6d0`

```dockerfile
```

-	Layers:
	-	`sha256:4d85b961ce4e2c3d8ca33807155c65c8d754e023d17256d6bef5910b0ba32e89`  
		Last Modified: Fri, 05 Apr 2024 17:56:02 GMT  
		Size: 3.3 MB (3326760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0600f71b9fe3b81a3dbbd14b65c5c6104874ebd602fad95743926f6e237616fe`  
		Last Modified: Fri, 05 Apr 2024 17:56:01 GMT  
		Size: 19.8 KB (19760 bytes)  
		MIME: application/vnd.in-toto+json
