## `clojure:temurin-8-lein-2.9.10-bullseye`

```console
$ docker pull clojure@sha256:caac3599df5d9946427c6c28bc54cdf1a2a11ef3497974d6eacdac1500823db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-lein-2.9.10-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:bd7b7603aee41b862074c5128931f54fde462a26c4cfb46fe52f86f0ffe633aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177235775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e1f12381f56b30743b90a6bc976ea02295b2a5955e4a4c4b871fa1bc84a183`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:43 GMT
ADD file:abc6873c98339a3c496cb75ec2528e65ebe1f20d2cea777033f86dcd55d73da5 in / 
# Tue, 15 Nov 2022 04:04:43 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 17:50:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 17:50:31 GMT
COPY dir:53540f2d79f4eef9b2bf8c4b39ecdbbd82fb14bfcf951e14853afffd2efa2ecb in /opt/java/openjdk 
# Tue, 15 Nov 2022 17:50:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 17:51:50 GMT
ENV LEIN_VERSION=2.9.10
# Tue, 15 Nov 2022 17:51:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 15 Nov 2022 17:51:50 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 17:52:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 15 Nov 2022 17:52:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 15 Nov 2022 17:52:31 GMT
ENV LEIN_ROOT=1
# Tue, 15 Nov 2022 17:52:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 15 Nov 2022 17:52:34 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:a8ca11554fce00d9177da2d76307bdc06df7faeb84529755c648ac4886192ed1`  
		Last Modified: Tue, 15 Nov 2022 04:08:24 GMT  
		Size: 55.0 MB (55038615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc3c1232a71c325547fbbeb2b9de7293ab2fac0425f4b1e29f33f7ba72c3686`  
		Last Modified: Tue, 15 Nov 2022 18:06:30 GMT  
		Size: 103.5 MB (103530622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185c73cefea50958b77b56ee96360f3fe7aa9836207a4d68953ecf11dfb51f43`  
		Last Modified: Tue, 15 Nov 2022 18:07:01 GMT  
		Size: 14.3 MB (14267825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805037ce5bbf4e5e099e9b67a3e1099c5b6e11f550af0ee9e596885be9944ebf`  
		Last Modified: Tue, 15 Nov 2022 18:07:01 GMT  
		Size: 4.4 MB (4398713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-lein-2.9.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c8031a3103e76850d0c3951d945a3b3fce7115de84f1739e2cdf8d15991ec758
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.0 MB (174981207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10686903240ce0c0609dae5f8ea6c5edbc3174712185bc8f930381ea3fd0c3c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:12 GMT
ADD file:1f3a7177f64e1adda3e7a541c93dd4322c6ecb4f00f7b015665df2c0c08b59a5 in / 
# Tue, 15 Nov 2022 01:41:12 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:48:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 05:48:27 GMT
COPY dir:8a3fd802e7e57a45d80b19a89e91b421563b952585d39995819354f278317671 in /opt/java/openjdk 
# Tue, 15 Nov 2022 05:48:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 05:50:02 GMT
ENV LEIN_VERSION=2.9.10
# Tue, 15 Nov 2022 05:50:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 15 Nov 2022 05:50:02 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 05:50:17 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 15 Nov 2022 05:50:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 15 Nov 2022 05:50:17 GMT
ENV LEIN_ROOT=1
# Tue, 15 Nov 2022 05:50:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 15 Nov 2022 05:50:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:077c13527d405646e2f6bb426e04716ae4f8dd2fdd8966dcb0194564a2b57896`  
		Last Modified: Tue, 15 Nov 2022 01:44:12 GMT  
		Size: 53.7 MB (53699862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046fabb8a21ba00eac3c1d47151d833a4f75a4a53165082db8407708793358bf`  
		Last Modified: Tue, 15 Nov 2022 06:01:34 GMT  
		Size: 102.6 MB (102626606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cdeb6764322a9682cc82ba45f78d9af399bf1a94a8095b54a6a108f8e54b4f8`  
		Last Modified: Tue, 15 Nov 2022 06:02:05 GMT  
		Size: 14.3 MB (14256034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e393dfbd05715d4f36bb62fe73bac465721067ffa21b064b1bcf6424198389`  
		Last Modified: Tue, 15 Nov 2022 06:02:04 GMT  
		Size: 4.4 MB (4398705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
