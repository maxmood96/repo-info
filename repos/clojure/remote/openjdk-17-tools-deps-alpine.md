## `clojure:openjdk-17-tools-deps-alpine`

```console
$ docker pull clojure@sha256:9d2cd6663079c45ddd029da0da70f545cb43d7c016cfe53956a088f3652830ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-17-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:c282b4f97b828fca134a5062241d953ac0e096a2b0c1d91eb8aecde50f796d22
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208947527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2388788a75c0724f67513fc90f2198841ee64377e8ecec069e420cbddaa9da`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 01:15:06 GMT
RUN apk add --no-cache java-cacerts
# Thu, 01 Apr 2021 01:15:07 GMT
ENV JAVA_HOME=/opt/openjdk-17
# Thu, 01 Apr 2021 01:15:07 GMT
ENV PATH=/opt/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Apr 2021 01:15:07 GMT
ENV JAVA_VERSION=17-ea+14
# Thu, 01 Apr 2021 01:15:19 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/14/binaries/openjdk-17-ea+14_linux-x64-musl_bin.tar.gz'; 			downloadSha256='f07a1ac921333dafac1cd886ad49600ce143be7efebd32e1a02599a8a0829dd4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 01 Apr 2021 01:15:20 GMT
CMD ["jshell"]
# Thu, 01 Apr 2021 01:53:43 GMT
ENV CLOJURE_VERSION=1.10.3.814
# Thu, 01 Apr 2021 01:53:43 GMT
WORKDIR /tmp
# Thu, 01 Apr 2021 01:53:55 GMT
RUN apk add --update --no-cache curl bash make && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ea4a943d32496dc2423a529b32a309f2c0365e56ba251d4a56739c5977b906a3 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Thu, 01 Apr 2021 01:53:55 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c0977514f1a113de97ffc6f5e9fd1873b8d77fb352205316fdc4d7696aab84`  
		Last Modified: Thu, 01 Apr 2021 01:21:03 GMT  
		Size: 928.4 KB (928397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563752cd6ffc7ae1632f28e21155f16c5b95902be182e29ba84e415f794f40c1`  
		Last Modified: Thu, 01 Apr 2021 01:21:19 GMT  
		Size: 186.8 MB (186797685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efebbb41b12a2cce9ed7fe5224e2dc3e67c972043b90960bd459f08e2bfa4409`  
		Last Modified: Thu, 01 Apr 2021 02:09:33 GMT  
		Size: 18.4 MB (18409498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
