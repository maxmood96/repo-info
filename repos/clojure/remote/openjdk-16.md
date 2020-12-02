## `clojure:openjdk-16`

```console
$ docker pull clojure@sha256:b94444a2cf30eab4a02bee4f8086cba07e7ab7bbda6fe8a6135454f72dcd4c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-16` - linux; amd64

```console
$ docker pull clojure@sha256:1b32bb648cc76df0c74a510a33c95f16148ad93d3b10ac1b08679d375b313f23
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232909563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4109867d75780dc5a2a0033ffdf9c32949e5a63bea1b84c0f5860e48728dddc0`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:14:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:14:56 GMT
ENV LANG=C.UTF-8
# Wed, 18 Nov 2020 00:14:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-16
# Wed, 18 Nov 2020 00:14:57 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Nov 2020 00:14:59 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 01 Dec 2020 23:54:51 GMT
ENV JAVA_VERSION=16-ea+26
# Tue, 01 Dec 2020 23:55:20 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/26/GPL/openjdk-16-ea+26_linux-aarch64_bin.tar.gz; 			downloadSha256=1e2fefe414a16aceeae6816b4e48b426e79bb647927a44bbfe4d692156096e74; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/26/GPL/openjdk-16-ea+26_linux-x64_bin.tar.gz; 			downloadSha256=e74300f3f770122358d768d45e181d29c710e8d41bbc4ab8e492929f2867347c; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 01 Dec 2020 23:55:21 GMT
CMD ["jshell"]
# Wed, 02 Dec 2020 00:32:43 GMT
ENV LEIN_VERSION=2.9.3
# Wed, 02 Dec 2020 00:32:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 02 Dec 2020 00:32:44 GMT
WORKDIR /tmp
# Wed, 02 Dec 2020 00:32:54 GMT
RUN apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "42e18e8a833b863ddfba1c5565bd5d78b54bcee661ec86e94a8bdc67b1733e63 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver keys.openpgp.org --recv-key 20242BACBBE95ADA22D0AFD7808A33D379C806C3 && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.zip.asc leiningen-$LEIN_VERSION-standalone.zip && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 02 Dec 2020 00:32:54 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 02 Dec 2020 00:32:54 GMT
ENV LEIN_ROOT=1
# Wed, 02 Dec 2020 00:32:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 02 Dec 2020 00:32:59 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef17c1a944643971956760785cd2fdb1ae360b47af01d997bd7580f32b8b3512`  
		Last Modified: Wed, 18 Nov 2020 00:22:53 GMT  
		Size: 3.2 MB (3248467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f372ea5b91612afd4a4eedf6685a7aca438c668a5c19bc23dcb12519c861fb2`  
		Last Modified: Wed, 18 Nov 2020 00:22:51 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f3aefa653b4bee9ff46884a0e9cadb3f3c2dc1fdfd6694512decf0f9efcd39`  
		Last Modified: Wed, 02 Dec 2020 00:01:09 GMT  
		Size: 184.9 MB (184923919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93cd28b38ec91c86e5995bb39f9d05f8ec7bfe309bc53903df5c3c6ccec29991`  
		Last Modified: Wed, 02 Dec 2020 00:36:31 GMT  
		Size: 13.5 MB (13463320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f87d26874ac4498eef0e63f726cd498ee1e8833f750f2865821293ba547d7ce`  
		Last Modified: Wed, 02 Dec 2020 00:36:30 GMT  
		Size: 4.2 MB (4168162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
