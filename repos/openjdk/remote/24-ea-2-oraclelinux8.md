## `openjdk:24-ea-2-oraclelinux8`

```console
$ docker pull openjdk@sha256:7364ff3efad187e8b6aa8c779311dbf23e2d5d488021b3e530a8638464ef627c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-2-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:c77d8b6b1f8c5226cbbc8d56e03053b08001c7e48c6197087ceba32d3cfe373d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278035163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09b274081b894c237f58ff253bf651da7639cad9a1c299c68fb39c4ed861cb8`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:53 GMT
ADD file:6f8c3cf297caf3b2a501a32c94a4fc0d2c7024f63d5e4b2215730b56faa6cdfb in / 
# Fri, 07 Jun 2024 03:48:53 GMT
CMD ["/bin/bash"]
# Thu, 13 Jun 2024 18:54:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 13 Jun 2024 18:54:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Thu, 13 Jun 2024 18:54:09 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 18:54:09 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jun 2024 18:54:09 GMT
ENV JAVA_VERSION=24-ea+2
# Thu, 13 Jun 2024 18:54:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/2/GPL/openjdk-24-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='5219b8df6c8c43be5dab2d1ab5251df85610360ab22789e497ee05c66fa4c7e6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/2/GPL/openjdk-24-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='5632c71df051ca5b6640c3c2a09ca3dd2b3dd131ea632906bd0eef7033323223'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 13 Jun 2024 18:54:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:427bba466fea4df7396a02ec368c5aa24d07ac80d02aa94eb57ba7af7b84b5a3`  
		Last Modified: Fri, 07 Jun 2024 03:50:01 GMT  
		Size: 51.2 MB (51219315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781661864a4116a1d8e527aab7df6d5fd61774ddb50168553d65f23eb554b2f1`  
		Last Modified: Fri, 14 Jun 2024 01:01:52 GMT  
		Size: 15.0 MB (15035469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b57c4871f52de2c1df3752186dd74ee5cd3c5178d322b7fa1bf973611898324a`  
		Last Modified: Fri, 14 Jun 2024 01:01:56 GMT  
		Size: 211.8 MB (211780379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-2-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:1dfe6eb85094b85780543aaf5be1ddc56ac500a48d78c5e7241b8514478d7334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832a1cee2b529c776f51ee6aab1b2fa869d21e04f8644c32ed9e8c9b1615c882`

```dockerfile
```

-	Layers:
	-	`sha256:bb1677d2f760b83bb7de492ee1fda354483ad740a5542869315b5d019014d97f`  
		Last Modified: Fri, 14 Jun 2024 01:01:51 GMT  
		Size: 2.3 MB (2267550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd07a9cb2f7a00e2e6c9d8c24901aa0c88df0ae43868a1b027b619edc2b16c5c`  
		Last Modified: Fri, 14 Jun 2024 01:01:51 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json
