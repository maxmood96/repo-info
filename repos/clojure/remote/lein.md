## `clojure:lein`

```console
$ docker pull clojure@sha256:bae227140916276734b81574390d3d60390f446dc91f99f02ebdc6d23925addb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein` - linux; amd64

```console
$ docker pull clojure@sha256:df0c36ec43689488a46324f45aa0501289786159f4aa0bbf2bc8a8420807f069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.4 MB (274351119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe9328d2060f8c94bec7d95b4263aa6fca9d8627071a1b7a2251ddf3682e984`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_ROOT=1
# Wed, 07 Aug 2024 18:04:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7843ea5cb26af010e120e843c94765dbd806b1ea6a5656dda6034dfa9166efd`  
		Last Modified: Wed, 04 Sep 2024 23:07:55 GMT  
		Size: 158.6 MB (158579212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6d433528698dd5941474b6b0a9ac0d7c1d282c7add773deee2b5dc50160a51`  
		Last Modified: Wed, 04 Sep 2024 23:07:53 GMT  
		Size: 61.8 MB (61816735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd85bb87eefc633e9eac9edc4af4c11816c6578777ed83ad9bbc0da830134ae`  
		Last Modified: Wed, 04 Sep 2024 23:07:52 GMT  
		Size: 4.4 MB (4398041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdf99d4d55bea72713df6ff53ac7e78bdba3451a2da1eb3c2fc456c9c5a6cd7`  
		Last Modified: Wed, 04 Sep 2024 23:07:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein` - unknown; unknown

```console
$ docker pull clojure@sha256:ae3cdc4ce955504467aa33440e9acd22f648b33aea71588d43fbf78100af81a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6384245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a34711e7209469cccd09136d18d277d23fa2c3f75ef7aa5b32a08d926639bece`

```dockerfile
```

-	Layers:
	-	`sha256:706d8f394f0321366bd2ebf3516d37ffd444a5cef4538f08c6ad5332f9df2544`  
		Last Modified: Wed, 04 Sep 2024 23:07:52 GMT  
		Size: 6.4 MB (6364306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eb08dc3faba3d924d73f849cb5fa9eaeaa78bb1529cfee1962c3fbc8cbbc1e9`  
		Last Modified: Wed, 04 Sep 2024 23:07:52 GMT  
		Size: 19.9 KB (19939 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5a3a9558165cc66655580788ef5dd967b6d4316c554734425749b1c7a895a822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272407670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f975160f4617499431cf5c94469ccbbdd1a179efed33e78a5e11c37d92b5e27e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_ROOT=1
# Wed, 07 Aug 2024 18:04:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432a3dfe48f41ad044efed0a39ddc56c9ff96bfad23f28032c6b72e9206318e9`  
		Last Modified: Sat, 17 Aug 2024 05:49:36 GMT  
		Size: 156.7 MB (156746222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d21b9bfb0f49476d4075e8fc28ebe6171e52aaedb4359db625073aacd0350e`  
		Last Modified: Sat, 17 Aug 2024 05:49:33 GMT  
		Size: 61.7 MB (61674391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c5b004f4fb7adf4a102207e5b14c4c61644d8c55db59703565111cfd0d8d64`  
		Last Modified: Sat, 17 Aug 2024 05:49:32 GMT  
		Size: 4.4 MB (4398036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a184167e25562cddebac6f11f68a60d4a316f100c2aa304c4df2613f36aef5f5`  
		Last Modified: Sat, 17 Aug 2024 06:20:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein` - unknown; unknown

```console
$ docker pull clojure@sha256:92a8cfa826e59593c2861cf2bfcae177e95eac18fdd3c5274c00bd3c4d5beef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6391846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66da00c9f70b43fe2a0872641557b9bb642bea2b18283677f8f82cbeda883be4`

```dockerfile
```

-	Layers:
	-	`sha256:0548241e3d771535150ee1c6a773f5aa5d76d56bbc171243befa37439ba953ba`  
		Last Modified: Sat, 24 Aug 2024 00:04:22 GMT  
		Size: 6.4 MB (6371311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac7980dd0b6387cd133e7f59149b846ccbcb213e4e8efc6f9e1bdbfbafd7e2c6`  
		Last Modified: Sat, 24 Aug 2024 00:04:21 GMT  
		Size: 20.5 KB (20535 bytes)  
		MIME: application/vnd.in-toto+json
