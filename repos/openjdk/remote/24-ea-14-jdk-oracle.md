## `openjdk:24-ea-14-jdk-oracle`

```console
$ docker pull openjdk@sha256:86ce881543e203c20e9e14b18e989a1982c104b0a9d3f4e1f13135b36a5f16d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-14-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:9e2646a10506915769581188bd581a2629d2a764ae3efa0cbb0ac3f285dbdf07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 MB (300128732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ff6a2f7e8bd143b71464eff5784ef09288f20714e5d8272b46cf583cccd72d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Aug 2024 01:20:24 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Fri, 23 Aug 2024 01:20:24 GMT
CMD ["/bin/bash"]
# Fri, 06 Sep 2024 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 06 Sep 2024 18:48:13 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 06 Sep 2024 18:48:13 GMT
ENV JAVA_VERSION=24-ea+14
# Fri, 06 Sep 2024 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='e3cf94d73e0ca63c536e901858cb97a0053c62606f8bb9d5b2ca20e1cc573d0c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='0d13500ae2e96601c70e90fca2ad928c3bf541afc71c293aed33924a2361d97a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0e226c67c550c556ec0ddf7c89cd3d7842f5b2517b8e837107da1b6b352fa1`  
		Last Modified: Fri, 06 Sep 2024 22:01:13 GMT  
		Size: 39.1 MB (39062693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ad117a471b8fdd12c16493df3979503fe23cce30582dbad716ffdfb441db0d`  
		Last Modified: Fri, 06 Sep 2024 22:01:17 GMT  
		Size: 211.8 MB (211831975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-14-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:c91351e7a905ec99f62cac4fbf58ef7861fb7047af55d78230f6f9231d5b3e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3663779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40582e56b040ff0ab77095d488c7a25d6b03ab69179bc2bf49fd15a9b0a1d6b0`

```dockerfile
```

-	Layers:
	-	`sha256:6d85dcf5ac275ff2d18ce91c9a0cd77959749008c6e3d17c12ad7b0e5524a69b`  
		Last Modified: Fri, 06 Sep 2024 22:01:11 GMT  
		Size: 3.6 MB (3644251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83d35ea326688b7168ceea6b256f60216480a9ac7215cff3ecb4a8a8a74427e8`  
		Last Modified: Fri, 06 Sep 2024 22:01:11 GMT  
		Size: 19.5 KB (19528 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-14-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7e4ac73aafbdceded98958093807e138f3cb2d2e1de041ee687c9bc2b79d2e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297059318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71b53d67a6b28cd6331c14652cf3e908863b758f86ceebbf1627d4598d5d0a2`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Aug 2024 00:40:26 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Fri, 23 Aug 2024 00:40:27 GMT
CMD ["/bin/bash"]
# Fri, 06 Sep 2024 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 06 Sep 2024 18:48:13 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 06 Sep 2024 18:48:13 GMT
ENV JAVA_VERSION=24-ea+14
# Fri, 06 Sep 2024 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='e3cf94d73e0ca63c536e901858cb97a0053c62606f8bb9d5b2ca20e1cc573d0c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='0d13500ae2e96601c70e90fca2ad928c3bf541afc71c293aed33924a2361d97a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d43f5ded4088b46b5f902d592d52c2a52fe637a75fa3f5875e873ef3c66794`  
		Last Modified: Fri, 06 Sep 2024 22:24:26 GMT  
		Size: 39.5 MB (39489040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d7fa6da34451efda3c1a92cd10668e1a134ca1405ab43685514606fba6d5db`  
		Last Modified: Fri, 06 Sep 2024 22:24:31 GMT  
		Size: 209.7 MB (209682487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-14-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:936533b61d2992156efad41e06a4ce1caa66d2d45235602ab318d6a52345e28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3662636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f969693b433324783afb49977e3e26de49933ac60d68deb52e126d716b93ca`

```dockerfile
```

-	Layers:
	-	`sha256:2e0f6396590117672fe8bfd5afb11fef6f159c4f42f4165a83bfc2052b8ffd39`  
		Last Modified: Fri, 06 Sep 2024 22:24:25 GMT  
		Size: 3.6 MB (3642634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8e10d7a56aa517e82008b3b58f731e128e98cc2cd37faecdff4a90b856e896b`  
		Last Modified: Fri, 06 Sep 2024 22:24:25 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.in-toto+json
