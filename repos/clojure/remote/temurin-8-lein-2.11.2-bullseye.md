## `clojure:temurin-8-lein-2.11.2-bullseye`

```console
$ docker pull clojure@sha256:0d8c63977c0db4835358dd4681a67f649a0c16de616c54b68c1404eb1432a31c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-2.11.2-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0a97049d161cc5b244c6f2bc14d9fdf4a501aed91e5d8a0157b1cf9fe1e6670e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179245360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb90d7c2de623fa033c3938b0f6d46042d0ec723f4d30b6574052274ef78520`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 15:17:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6d93d01aec3559cdc54e385876f3239a5bbd0afdfd7d431f2b98741fdadf6b`  
		Last Modified: Wed, 29 May 2024 19:56:56 GMT  
		Size: 103.6 MB (103600210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c9463371a4cdbfed7a58da4ae162c5a00e64d44287f6f0bfa21b0895e191f5`  
		Last Modified: Wed, 29 May 2024 19:56:54 GMT  
		Size: 16.1 MB (16147689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a44fd2e0a73b4715912049cbf4d1a8e07377a56f44a545b24d9884db3a849aa`  
		Last Modified: Wed, 29 May 2024 19:56:54 GMT  
		Size: 4.4 MB (4398030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:27338b24891ccf022a2860103a95d0dc26fee25ab669a06047ffe3212ae73607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4189788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f2fc40d52362c9eca0abea8cc720badb1068b56f9502e408ba7dd20990499a`

```dockerfile
```

-	Layers:
	-	`sha256:fcb48282c6b9259a64d183b8257a551c8504ae18b181820583e35fbbbf2a029c`  
		Last Modified: Wed, 29 May 2024 19:56:54 GMT  
		Size: 4.2 MB (4173810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc71d5d8e698c9af5b8993f39af1facb6b44a7af2cd29a008cf6aa01b679dff6`  
		Last Modified: Wed, 29 May 2024 19:56:53 GMT  
		Size: 16.0 KB (15978 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.11.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:268411dedfa5c2d4c3775fe1627ce13d5cf2b1f62146956d33eb78f54ff0d211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176973994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b98f0162beb61f38ccd722d2beeadd5999f64213ea92051cf72d5c352dad76`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:47 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Tue, 14 May 2024 00:39:48 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 15:17:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63911e15f438f0df584fead0a70409ce33f1ce399ac96a51f4a8a5525258392a`  
		Last Modified: Wed, 29 May 2024 20:26:37 GMT  
		Size: 102.7 MB (102700399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b10a741afb61d5748ada4fd6f52d312648b902d1f71283ef314fa22e24a8cc`  
		Last Modified: Wed, 29 May 2024 20:26:35 GMT  
		Size: 16.1 MB (16136471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35245c80c60cd38d9af21b2b407ec10428c72a424d2b136d12ab2f09c308d91`  
		Last Modified: Wed, 29 May 2024 20:26:35 GMT  
		Size: 4.4 MB (4398102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f74b7e910b239fe72e964bf16105e1e8cfdf2f0a44bcb4b11ca8311cf1a58ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4189891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fdcde2a98699750d6b238d3d48c1f1b9547d3f182f545541b4e47a8fb1c276b`

```dockerfile
```

-	Layers:
	-	`sha256:0ada6dd253c6ca694c7ffd31432ac9a83024906d4eda50f03b6f685284f231e9`  
		Last Modified: Wed, 29 May 2024 20:26:34 GMT  
		Size: 4.2 MB (4173390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f2962c4e34c65b5def9253fce01a5d0bcf363bf0fc3d08b83429c822f25f463`  
		Last Modified: Wed, 29 May 2024 20:26:34 GMT  
		Size: 16.5 KB (16501 bytes)  
		MIME: application/vnd.in-toto+json
