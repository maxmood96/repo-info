## `clojure:temurin-11-lein-bullseye`

```console
$ docker pull clojure@sha256:0ce855d9933040833c2a66c46e28bd03a30ac45ce3d375d1fd05cf79198e267e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c0a411b9c7ffa410290d76a4bfff71782abef5249124cdf20274955a752e6e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220805492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9398351881b477a0e87b3d6aed1071f24f564cb188958720e39aa2f2a6d439d5`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:17:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:17:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:17:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:17:01 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:17:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:17:01 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:17:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:17:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:17:20 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:17:22 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da14779fa9c1210f080ec291b144ca693ba177618ddd45594088c8964bf6a67`  
		Last Modified: Thu, 11 Jun 2026 01:17:42 GMT  
		Size: 145.9 MB (145886262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1dbd8ee273b47555b47e0b6f8a38b1cf5f44574bedbf13a2c0530ddaaffe90`  
		Last Modified: Thu, 11 Jun 2026 01:17:39 GMT  
		Size: 16.6 MB (16629687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cba651ff40c4d695c671a95a4c0bb458cedd033490b79a49ea6ccfb86616b74`  
		Last Modified: Thu, 11 Jun 2026 01:17:39 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d068cfbfb95f027c04d29549d592652616859e72e0553b7115114b58f1562696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88879852176326e0de0b781a937fa5afe9d1d65635c3ca2e521f6b2abfeb857e`

```dockerfile
```

-	Layers:
	-	`sha256:c716d2843cc76ca042be60e66ba3ce288fc1dd8741b7d08aec65874f6eba6101`  
		Last Modified: Thu, 11 Jun 2026 01:17:39 GMT  
		Size: 4.5 MB (4506009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95a91ee70c3ba12c65eab38abbbf143bd71806eac407b34e294bb656f3715304`  
		Last Modified: Thu, 11 Jun 2026 01:17:39 GMT  
		Size: 16.5 KB (16536 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a1be8b3aa6a53d91d1b32a7a1df1fab0262a6e645d4b2bcbf61c2a763b3d548e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.0 MB (215980984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12cc8c0bafd6eb042265f71d39c163ec34f195a31cfa7c4e825b28e60745c976`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:21:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:21:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:21:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:21:17 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:21:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:21:17 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:21:36 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:21:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:21:36 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:21:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:21:38 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d07b5c599b666163da69486ef36d6f23b79a029cdbff6600de457e356b43ec`  
		Last Modified: Thu, 11 Jun 2026 01:22:01 GMT  
		Size: 142.6 MB (142582228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae369fe3f1aba3f4364dadb0aa581fd0910a8e47a1133521f3db50cac07f2b3`  
		Last Modified: Thu, 11 Jun 2026 01:21:57 GMT  
		Size: 16.6 MB (16616850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d974c5e9fe22af3d43f7f794839ac649286b47084179d3009bf59aaabf7f8341`  
		Last Modified: Thu, 11 Jun 2026 01:21:55 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b09247888b9aba638b9d2a9328f22bda6f05d3e9834c25f4e4eb77365d2a9175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96360e2bb12c46744a792982b10742943c918af41ff842d19a18ffc2488f4e9b`

```dockerfile
```

-	Layers:
	-	`sha256:a119d81c92cbee934eff611eaca6ad6634c29b7f0ac352f2c8993249c56834fe`  
		Last Modified: Thu, 11 Jun 2026 01:21:55 GMT  
		Size: 4.5 MB (4505601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b9c752f0bea3f7d328a06fc088fd9ace5edbd30ec2483f3701cc867f1faa06f`  
		Last Modified: Thu, 11 Jun 2026 01:21:55 GMT  
		Size: 16.7 KB (16657 bytes)  
		MIME: application/vnd.in-toto+json
