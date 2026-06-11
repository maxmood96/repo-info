## `clojure:temurin-21-lein-bullseye`

```console
$ docker pull clojure@sha256:07a513f608dd7926d8eff224a97526b4a75e55393f17c8b11206ac7b7a9e70d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:96167373859432c50ad7236f3f93fe3affceb5b557bb93a2b100ea463443436f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233086513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05af0d06898c36d082ab1e2bb29ec67c4a09692dfd2778f87594d726a87199e1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:19:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:19:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:19:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:19:47 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:19:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:19:47 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:20:01 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:20:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:20:01 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:20:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:20:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:20:02 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:20:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f34896181accd4589406189ed8c89d51569bf8db23b13348b1d3f93e78bc3d`  
		Last Modified: Thu, 11 Jun 2026 01:20:23 GMT  
		Size: 158.2 MB (158166905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05522d94bbe82925ef6a64b8765c9c13f5d5ab5894d9bc9307306907756f8bd1`  
		Last Modified: Thu, 11 Jun 2026 01:20:20 GMT  
		Size: 16.6 MB (16629695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8011293435fcf6e6ae37fabe553a522c46348ff954a85eeea68a65897ae667`  
		Last Modified: Thu, 11 Jun 2026 01:20:20 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f3d6a5ea48c3784a827caccf20c5dc6a68b9a57eb03928ddda2ed7cb8424a4`  
		Last Modified: Thu, 11 Jun 2026 01:20:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3d29a4def997e41defe998519df93f3d035cb29d96594a9b724dd511538d962e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee956d93ca974273d1f3e47862c076d1a9ab7a056b97bee83dca5c486f7c0409`

```dockerfile
```

-	Layers:
	-	`sha256:9884a9defa3b0432adfb6a1512cde1783881cfeac22bee1881db998812e5987f`  
		Last Modified: Thu, 11 Jun 2026 01:20:19 GMT  
		Size: 4.5 MB (4488345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19330040525ca34dcd3f3b780c47b45d5159bbd309dbbc2d3ef60c61cb488e1c`  
		Last Modified: Thu, 11 Jun 2026 01:20:19 GMT  
		Size: 18.5 KB (18522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9678b0602b9a8d8d29367c3023e8d01145e9c224730244277c7a7a026afd8eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229860470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2774e6ebec55b2589e4816e2dcc3d05d01704e343dc8ca1022fb784d7d8e499d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:23:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:23:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:23:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:23:34 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:23:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:23:34 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:23:54 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:23:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:23:54 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:23:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:23:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:23:56 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:23:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32566dda540eccfcd9e4bf7b4419e03bec89a609afedd1221b51539ace358feb`  
		Last Modified: Thu, 11 Jun 2026 01:24:18 GMT  
		Size: 156.5 MB (156461323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13bc0072be587d4b4facff3589f77fea530ec79a175381ca341691ae93085b3b`  
		Last Modified: Thu, 11 Jun 2026 01:24:15 GMT  
		Size: 16.6 MB (16616866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3738b9d343d1372f6087ac36e1d270915272023d90660a4e59fe31f547fb4e87`  
		Last Modified: Thu, 11 Jun 2026 01:24:14 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75927f454a5a344478cb1a6fd657fc740ad4616a802b702757c008bc65504933`  
		Last Modified: Thu, 11 Jun 2026 01:24:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7f210d9398789f68c6d43a0919dfb87572cefd2491cd2116529b0c404426b2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4505962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a8b158b7cc13943d501ad59fcc3777db4e04abdce2d265e0a02fb297987631`

```dockerfile
```

-	Layers:
	-	`sha256:09b73ed6655e0431313ccae1f57496eb8e59d23b86a2a83ce697c624411d30d6`  
		Last Modified: Thu, 11 Jun 2026 01:24:14 GMT  
		Size: 4.5 MB (4487319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a400df0d4a738918e6695f35b097e91d340285224eeb3d51be3d8e0da94bb452`  
		Last Modified: Thu, 11 Jun 2026 01:24:14 GMT  
		Size: 18.6 KB (18643 bytes)  
		MIME: application/vnd.in-toto+json
