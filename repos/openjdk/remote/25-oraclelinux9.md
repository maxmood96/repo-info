## `openjdk:25-oraclelinux9`

```console
$ docker pull openjdk@sha256:b2ccbae7410c957a7affc7a985adb58ba637a37d3242ebd7e22de773d8a5e5c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:25-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:176782a307f7ce50697a5b92d9f5e6a0185c4121b606acbd266aa97e147a8311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 MB (310724176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec00b6a1c73624f0d39f7ed76e625491149b2fc6ac1d5b0ee7bcd0e1e0142b0b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 05:52:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Mon, 09 Dec 2024 05:52:24 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 05:52:24 GMT
ENV LANG=C.UTF-8
# Mon, 09 Dec 2024 05:52:24 GMT
ENV JAVA_VERSION=25-ea+1
# Mon, 09 Dec 2024 05:52:24 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='b2c1c3716a21ae204e31e0f37782552ffef0f6e0d9850ba16fb57cd0fa98d84c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='76761c3ad2bebc865c5ed4ce08a7c5f89eb4f51d3f471d76f650e0556d79daa3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e5b1df7e6678619152ca0b4b1694bb07a547b66ace8461d2532c57140d1e6f`  
		Last Modified: Mon, 09 Dec 2024 23:31:01 GMT  
		Size: 48.8 MB (48764981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60adf24fd38e139d4c6dbab4c7d0f0c61d7a47637e28a92ae590d45795ab2ac`  
		Last Modified: Mon, 09 Dec 2024 23:31:03 GMT  
		Size: 212.9 MB (212860493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:bf8c9c060a38838190d3cc5a3aca72dd32af551ed28cbe268e0062636121f544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4937365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0ea8f37c2af40eda347ad105c6c925a501ad817847595c895de536f339e20c`

```dockerfile
```

-	Layers:
	-	`sha256:6718ba1288415d851be9ac25e9a3380f66b801b50684bf2c1cd5e3fd11057dd3`  
		Last Modified: Mon, 09 Dec 2024 23:31:00 GMT  
		Size: 4.9 MB (4917646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8881f02f01bae8409dc96589d160bf8cd66234b4cadd51420a8409c7dff6196a`  
		Last Modified: Mon, 09 Dec 2024 23:30:59 GMT  
		Size: 19.7 KB (19719 bytes)  
		MIME: application/vnd.in-toto+json
