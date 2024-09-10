## `openjdk:24-oracle`

```console
$ docker pull openjdk@sha256:b7d5d1a004039581ba80fa704d8871ef2de52b350614d254279a3a35c346141e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:838f22543b34fd67795e9637f4ac26a598c1adb5b72e57b15d84e6c276e0d5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 MB (300130979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe6cc2eb5f63eaad2b901c0eb328019fbde3ed6360edf541b2de72b5de28880`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 06 Sep 2024 18:48:13 GMT
ADD file:d8a38112d165940510d5cfd57f316139caf4069546c97dfc10a08f33f3f1ca9f in / 
# Fri, 06 Sep 2024 18:48:13 GMT
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
	-	`sha256:12d7e45337f84111b352ed27b6a21ab109dec7571b23ebc522b6bb6b318d883b`  
		Last Modified: Mon, 09 Sep 2024 22:21:36 GMT  
		Size: 49.2 MB (49237791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48d62797a6a657cc627514abd40304456b8c9e3ff6e10c63f2e19f48bf69bd4`  
		Last Modified: Mon, 09 Sep 2024 23:02:11 GMT  
		Size: 39.1 MB (39060878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3d408aa04717d10c404fb4967df73c20cae4b77bdf8dfe24e9209951e1fc69`  
		Last Modified: Mon, 09 Sep 2024 23:02:14 GMT  
		Size: 211.8 MB (211832310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:73f448f1b035a3f6ecee9ef68074aafe65ff0cf51099109d582337f8c8b50684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3663807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fdcca585882c5ded34996bb8308b442b2d900caa4d16eb378bc77e8cf5b5fdd`

```dockerfile
```

-	Layers:
	-	`sha256:056b21e384a5ebd724271502ab62da272d9911e4685469a084c742988c26c771`  
		Last Modified: Mon, 09 Sep 2024 23:02:10 GMT  
		Size: 3.6 MB (3644279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26b5cb4c339f25c6dca563e26f52bfabcba2e4e750dd386e6c33d2dc82d90b63`  
		Last Modified: Mon, 09 Sep 2024 23:02:09 GMT  
		Size: 19.5 KB (19528 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-oracle` - linux; arm64 variant v8

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

### `openjdk:24-oracle` - unknown; unknown

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
