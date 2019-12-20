## `clojure:openjdk-14-lein-2.9.1`

```console
$ docker pull clojure@sha256:1e21580271d0fb997a98037a5cb39cd2c18f93197d0b3ad1acd06a7d6cfbc34f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-14-lein-2.9.1` - linux; amd64

```console
$ docker pull clojure@sha256:2651af806f40c1bbdf8a52815857c46c687c398cd42e896e21082e0fa5f0dcf0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.6 MB (251586877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf344fbb671c8f49d5bc6086dfafaa4743d0334043cbfbcb4b881f544d2b50ca`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 22 Nov 2019 14:55:09 GMT
ADD file:bc8179c87c8dbb3d962bed1801f99e7c860ff03797cde6ad19b107d43b973ada in / 
# Fri, 22 Nov 2019 14:55:10 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 19:14:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 19:14:45 GMT
ENV LANG=C.UTF-8
# Fri, 22 Nov 2019 19:14:45 GMT
ENV JAVA_HOME=/usr/java/openjdk-14
# Fri, 22 Nov 2019 19:14:45 GMT
ENV PATH=/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2019 19:14:46 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Dec 2019 23:30:54 GMT
ENV JAVA_VERSION=14-ea+28
# Thu, 19 Dec 2019 23:30:54 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk14/28/GPL/openjdk-14-ea+28_linux-x64_bin.tar.gz
# Thu, 19 Dec 2019 23:30:55 GMT
ENV JAVA_SHA256=ce2e3acf3b20426545a2e835cad33b21351359c67bf30a7722aaa21d97ee5862
# Thu, 19 Dec 2019 23:31:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Thu, 19 Dec 2019 23:31:11 GMT
CMD ["jshell"]
# Fri, 20 Dec 2019 01:04:51 GMT
ENV LEIN_VERSION=2.9.1
# Fri, 20 Dec 2019 01:04:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 20 Dec 2019 01:04:51 GMT
WORKDIR /tmp
# Fri, 20 Dec 2019 01:05:04 GMT
RUN apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha1sum lein-pkg && echo "93be2c23ab4ff2fc4fcf531d7510ca4069b8d24a *lein-pkg" | sha1sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver pool.sks-keyservers.net --recv-key 2B72BF956E23DE5E830D50F6002AF007D1A7CC18 && echo "Verifying Jar file signature ..." && gpg --verify leiningen-$LEIN_VERSION-standalone.zip.asc && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get remove -y --purge gnupg wget
# Fri, 20 Dec 2019 01:05:04 GMT
ENV PATH=/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 20 Dec 2019 01:05:04 GMT
ENV LEIN_ROOT=1
# Fri, 20 Dec 2019 01:05:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 20 Dec 2019 01:05:13 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:000eee12ec04cc914bf96e8f5dee7767510c2aca3816af6078bd9fbe3150920c`  
		Last Modified: Fri, 22 Nov 2019 15:02:49 GMT  
		Size: 27.1 MB (27092654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1dc2bdcfe193ce54affa45170354ca76667c40f8cf536b6282dd379e17e24a`  
		Last Modified: Fri, 22 Nov 2019 19:19:08 GMT  
		Size: 3.2 MB (3249119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646f7263fe2d59eb4bac3860d55c1438acbe162706df09f1f0f89198cdc35119`  
		Last Modified: Fri, 22 Nov 2019 19:19:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a73873182bc693254bdcba9b8cf687fd6889a831d332c3fa2fd8cffc4b05cb7`  
		Last Modified: Thu, 19 Dec 2019 23:36:20 GMT  
		Size: 199.3 MB (199287075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8bc5160a41421906be6cf53e2dfb636350d3d0d5499d05abc0048276fc1ef21`  
		Last Modified: Fri, 20 Dec 2019 01:10:47 GMT  
		Size: 17.8 MB (17789587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9223365d9a5a611ea8d5c3600b5280cfc37e4991630508945685568fd4a9520c`  
		Last Modified: Fri, 20 Dec 2019 01:10:45 GMT  
		Size: 4.2 MB (4168232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
