## `openjdk:27-ea-14-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:7279d3f05bff5ad6831027429980ead4b8ebd0f79db7ce2ae37e45240a097a82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-14-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:18bd8f1f7cea049880100eebd29cf01ff412d5bf20b045b717d7b02d6e131f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314077776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed3e9ec224bbfd800a3892d8ceb55f5418500a4062c438685c10b910d1f0277`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Mon, 23 Mar 2026 17:58:53 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 23 Mar 2026 17:59:03 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 23 Mar 2026 17:59:03 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 17:59:03 GMT
ENV LANG=C.UTF-8
# Mon, 23 Mar 2026 17:59:03 GMT
ENV JAVA_VERSION=27-ea+14
# Mon, 23 Mar 2026 17:59:03 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='64b478b9973d8d04e1680cdfaf11a8e93f8a17f962af3ddb1c61b76a62c0d699'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='c99686ed0406f05a113b6467b6a57699864922c476481609a703c6dd91534f45'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 23 Mar 2026 17:59:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ff99b8958b7cc179ebcb27985bc05b20d4861068f3132199e50ae5e80aa604`  
		Last Modified: Mon, 23 Mar 2026 17:59:26 GMT  
		Size: 38.3 MB (38297615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2593e44df1ea120c2cde562ac60fd89a0d9f6c072e57c99efc172686b4cd1a84`  
		Last Modified: Mon, 23 Mar 2026 17:59:30 GMT  
		Size: 228.5 MB (228469892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-14-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:be5059439b67feb0efa2509ecdc4718527d8b0487f6508ff17f5e0658e86fa2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3668290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3b2c6bd0697c8056f354651f4096427d90a7047a9b74770c223b787895e0c7`

```dockerfile
```

-	Layers:
	-	`sha256:528afba1706cefcb11a554b1bdd757d17d7df296319287516dd2666d9077f51e`  
		Last Modified: Mon, 23 Mar 2026 17:59:24 GMT  
		Size: 3.7 MB (3652947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8239ae320f234ac2e39541d65e65b7d320d36b604152efc11c96247df310e310`  
		Last Modified: Mon, 23 Mar 2026 17:59:24 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-14-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:052921d5232a65e618e10abf349b070122c7b642d3ed04e22f9a4663e80e75e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.0 MB (311031262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4473836145300cd6e4d00b343684eeea5c5771c35a64a35ad32f4051b57a2447`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Mon, 23 Mar 2026 17:58:29 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 23 Mar 2026 17:58:39 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 23 Mar 2026 17:58:39 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 17:58:39 GMT
ENV LANG=C.UTF-8
# Mon, 23 Mar 2026 17:58:39 GMT
ENV JAVA_VERSION=27-ea+14
# Mon, 23 Mar 2026 17:58:39 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='64b478b9973d8d04e1680cdfaf11a8e93f8a17f962af3ddb1c61b76a62c0d699'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='c99686ed0406f05a113b6467b6a57699864922c476481609a703c6dd91534f45'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 23 Mar 2026 17:58:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14f2d7a5fefa04f09c8732a6043661b9b1e8117227e2389b548f9360613f97c`  
		Last Modified: Mon, 23 Mar 2026 17:59:02 GMT  
		Size: 38.7 MB (38692008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5115c7e3d54ea777159c4d31e769e01049d1f8ef32b72d5110d03ffdcbb37e9d`  
		Last Modified: Mon, 23 Mar 2026 17:59:06 GMT  
		Size: 226.4 MB (226441272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-14-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:4b762eafb022b612a53d54b394cf563de9ae737327c4ef5eadf428a381b64f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3666003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab521e4c20791a241a88e2149f63563c1266fcf8b8fba73b7ace0530db50741`

```dockerfile
```

-	Layers:
	-	`sha256:48d927a77576f85af1cd989149544fdca534bf75e563eb52ef2db2936fd1e5c0`  
		Last Modified: Mon, 23 Mar 2026 17:59:01 GMT  
		Size: 3.7 MB (3650541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a8353c4733d7005f5fbaf93173e32ab807eb0c95f363f65cca1822253aa7786`  
		Last Modified: Mon, 23 Mar 2026 17:59:00 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
