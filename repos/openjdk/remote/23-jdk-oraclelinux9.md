## `openjdk:23-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:d2d212451541856e29f7b2f781f7c22a072a0ab9ad987ba73a2c6f7ba83fe16b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:63e57e77bfd7d4bf44fa538a2a3c053c134bde21df1811d6a0a331ba01a196b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.3 MB (299317501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172de1787bdc8f7003bb9e701ffed52c5235cf552053e93bd9352777baa47cd1`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Aug 2024 00:29:11 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
# Wed, 21 Aug 2024 00:29:12 GMT
CMD ["/bin/bash"]
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Wed, 21 Aug 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='08fea92724127c6fa0f2e5ea0b07ff4951ccb1e2f22db3c21eebbd7347152a67'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='076dcf7078cdf941951587bf92733abacf489a6570f1df97ee35945ffebec5b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c13465a21f41a4b5bdfb062ea9465e42819d7498c1ec6a4b25d4a02d462fde`  
		Last Modified: Wed, 21 Aug 2024 21:03:37 GMT  
		Size: 39.0 MB (39046715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed10dec56bb453c481d60985e18d7e8a22703e5a2ab006040f4e94e6993c579a`  
		Last Modified: Wed, 21 Aug 2024 21:03:39 GMT  
		Size: 211.3 MB (211275965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:466dc45259753af6d1c77307b2c439c6e1750bd869dcc404f68041be73609114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3561709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a6cd20f49d3b752b2e016251c4484c986d65582cf86ffd8d78b7710d845e1f`

```dockerfile
```

-	Layers:
	-	`sha256:0e44704d13ea69ed94fbc05c6f5b07104ec7d256917545f689affdc8a5d65899`  
		Last Modified: Wed, 21 Aug 2024 21:03:36 GMT  
		Size: 3.5 MB (3544045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:696f41bb38c7951f1d981eff0a431d2a4e1915bcf54de87bff18b9342511fc3d`  
		Last Modified: Wed, 21 Aug 2024 21:03:36 GMT  
		Size: 17.7 KB (17664 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:05ba9736cdf9c8f9ab25de2cc81f44980cdfa95383add11b02c7461f9bded9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296302551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ba56307ecbc9153b401ed920c8110fd9f159c65e881f885d4f24bada4dd177`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 20 Aug 2024 23:40:54 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
# Tue, 20 Aug 2024 23:40:55 GMT
CMD ["/bin/bash"]
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Wed, 21 Aug 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='08fea92724127c6fa0f2e5ea0b07ff4951ccb1e2f22db3c21eebbd7347152a67'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='076dcf7078cdf941951587bf92733abacf489a6570f1df97ee35945ffebec5b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64a371a7ad1ff13a4dded4febe3bd91f6ddf3dac8b18dc7feef6e025c2943f3`  
		Last Modified: Wed, 21 Aug 2024 01:11:51 GMT  
		Size: 39.5 MB (39478981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb92939352ea614c84c18258594556ea1bdc6fbf97ae1b52668930276419a82`  
		Last Modified: Wed, 21 Aug 2024 22:02:20 GMT  
		Size: 209.2 MB (209169004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:0071eac65b2915a7253e10914a9a18b060b511641359923e03f83d7c8ab50e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3560423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8224957222c77dabdf1cd747edfddc71c1f32eebd507310add83d0c264e50dae`

```dockerfile
```

-	Layers:
	-	`sha256:be0f925f58123b3fe567ab74b606b39e071503602f25699a22633467dbdde07a`  
		Last Modified: Wed, 21 Aug 2024 22:02:16 GMT  
		Size: 3.5 MB (3542356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:295461e9e5eedb774ac222994fc76a65213b3ffcbfa493a40be4c651c8461e8c`  
		Last Modified: Wed, 21 Aug 2024 22:02:16 GMT  
		Size: 18.1 KB (18067 bytes)  
		MIME: application/vnd.in-toto+json
