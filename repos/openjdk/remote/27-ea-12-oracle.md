## `openjdk:27-ea-12-oracle`

```console
$ docker pull openjdk@sha256:12d14c74384f3e918ce5998513881b38dc22cd5a4b4729d4713b3c5a23dc2461
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-12-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:5fa49ed9fe140177e38cb0598252a283c6f07f89d5d14c5a3fa9cd761a300374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314024269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe78506e7e88b5455a3d6b56510f69b574a2a4a4ee01fd426f6b883b1574d594`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Sat, 07 Mar 2026 00:40:23 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 07 Mar 2026 00:40:35 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Sat, 07 Mar 2026 00:40:35 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Mar 2026 00:40:35 GMT
ENV LANG=C.UTF-8
# Sat, 07 Mar 2026 00:40:35 GMT
ENV JAVA_VERSION=27-ea+12
# Sat, 07 Mar 2026 00:40:35 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='952af4c17b753724c0f1e7ac4cd90f73568c2121ac60a1ae05ff804481e2ae48'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='09bc1159ce7ffe4b495d58e30271250015d0d9902e670027e1491bc9f1cf1b52'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Mar 2026 00:40:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb41a59e5e559a42f15aeabd32c6a462c54e0369088e60aca7fc2143a93b2d5`  
		Last Modified: Sat, 07 Mar 2026 00:40:57 GMT  
		Size: 38.3 MB (38298183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d12f82cd3431fa9181c78c26a20a7e8b9033c6ec6714c33e0459c030b319b6`  
		Last Modified: Sat, 07 Mar 2026 00:41:01 GMT  
		Size: 228.4 MB (228417215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-12-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:c5b15b91b5f309d3fac77427fc805fff36ee8429a75d35ccfb40749cb6643887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f35262da8e9fb9603d91be976819e5896745e249aa94558baa1ab278a0bee3`

```dockerfile
```

-	Layers:
	-	`sha256:be0b66c641b15b257e5e95563e760caef9d8c188dfc9c7d6a0cee2e74045d870`  
		Last Modified: Sat, 07 Mar 2026 00:40:56 GMT  
		Size: 3.7 MB (3655437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d25825c73d70ee273b3cd9fe13043d48330a95f82b243c1cb5922e2e2735023`  
		Last Modified: Sat, 07 Mar 2026 00:40:55 GMT  
		Size: 17.8 KB (17838 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-12-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6f2fc6c2332c7405b26712046cd598df9284dcb24621a12a811c9ff8c7f0234e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.0 MB (310962854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08a1b270ea51dc2b556ab57fe3667618d25806184c8b5b32ecea86146814e84`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Sat, 07 Mar 2026 00:41:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 07 Mar 2026 00:41:40 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Sat, 07 Mar 2026 00:41:40 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Mar 2026 00:41:40 GMT
ENV LANG=C.UTF-8
# Sat, 07 Mar 2026 00:41:40 GMT
ENV JAVA_VERSION=27-ea+12
# Sat, 07 Mar 2026 00:41:40 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='952af4c17b753724c0f1e7ac4cd90f73568c2121ac60a1ae05ff804481e2ae48'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='09bc1159ce7ffe4b495d58e30271250015d0d9902e670027e1491bc9f1cf1b52'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Mar 2026 00:41:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0929214c9f6a7b2f3c00ee2603eb15c65b8fd4adb34f8c106c07ea110bea9f33`  
		Last Modified: Sat, 07 Mar 2026 00:42:03 GMT  
		Size: 38.7 MB (38693755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65120397d49ce4edcb0a6affcd9d50b696d0c00b1ee5a48654a77a32330d2493`  
		Last Modified: Sat, 07 Mar 2026 00:42:08 GMT  
		Size: 226.4 MB (226367119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-12-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:4828d53b7606211ff485356d926a68821530f8b656dacb5f84b8130a78780908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:867f8b6d20c45d3c384452b18f106339b319887e99704610eabf33229701ad00`

```dockerfile
```

-	Layers:
	-	`sha256:4599c6813516b2e8a7df3039da8f6000a29418976dbf171717f4d06d33ed74d9`  
		Last Modified: Sat, 07 Mar 2026 00:42:01 GMT  
		Size: 3.7 MB (3653127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ca745f01c9110dcdedbec97b345189bc448c6536b6798a2acd4bdd5a07c84e7`  
		Last Modified: Sat, 07 Mar 2026 00:42:01 GMT  
		Size: 18.1 KB (18051 bytes)  
		MIME: application/vnd.in-toto+json
