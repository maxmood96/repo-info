## `openjdk:24-ea-3-jdk-oracle`

```console
$ docker pull openjdk@sha256:9e83a0ac82e205b53504aac4287a2b6ecff2790fc381331ceee84e58ab6c6005
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-3-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:2fa25c979c45b770ddd81d0957f2532dc19ef28cecc5a68e239e9219ed567b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298185730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf931aa7150a5de7eac2fb99a2a3cd9efa83e39b79a8cb89f4e407fc6d5e7ba`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Jun 2024 18:52:10 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 18:52:10 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 18:52:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 21 Jun 2024 18:52:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 21 Jun 2024 18:52:10 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Jun 2024 18:52:10 GMT
ENV LANG=C.UTF-8
# Fri, 21 Jun 2024 18:52:10 GMT
ENV JAVA_VERSION=24-ea+3
# Fri, 21 Jun 2024 18:52:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/3/GPL/openjdk-24-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='dad750c864049dba95a01fa89ad1c52c3b702ba87c3c865e5e64fa624f9e3de0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/3/GPL/openjdk-24-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='4a5515c226db56008676461bef7443163ccfe369415342136b8d9691ecd5130b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Jun 2024 18:52:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5cc31512be0b59ac7a8b35a6401e68e3f4717b3eed880468e8016e6ca3ee37`  
		Last Modified: Sat, 22 Jun 2024 00:55:56 GMT  
		Size: 37.9 MB (37862427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552b84dd52eb03f2995aedd51e2a0f0262e40d055185228b1f0d6d075b6eb1f1`  
		Last Modified: Sat, 22 Jun 2024 00:55:58 GMT  
		Size: 211.3 MB (211329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-3-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:57d7522bce7d3d22230bdadc0190a4f71571b814fef8b77d4b15ea791f957603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b9605b130e9b28c2e38b09f5f4e05c87d52df96505de5168751bf32f659506`

```dockerfile
```

-	Layers:
	-	`sha256:ab468c89f8337ceceb14efaf9a30fb7a5a7cfc1f1ed2eebda9a33f492707170e`  
		Last Modified: Sat, 22 Jun 2024 00:55:56 GMT  
		Size: 3.3 MB (3333228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14b07633fadf7bace8ae34bc2e94259abc3a2dd2e6e8fedf97f2aa31313fc711`  
		Last Modified: Sat, 22 Jun 2024 00:55:56 GMT  
		Size: 19.5 KB (19502 bytes)  
		MIME: application/vnd.in-toto+json
