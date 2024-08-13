## `clojure:lein-2.11.2`

```console
$ docker pull clojure@sha256:eb97e9c00015386aab7e0f327d885b40b5c1a73d6371f365c5ec67432f907df6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-2.11.2` - linux; amd64

```console
$ docker pull clojure@sha256:7ac0814c7b93e0fae975f94d7a197ea8ed2f1cbb62e1bd6d060ab7ec635fada5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274331490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb8c107fa07361f741792c5f07fd32aee30378948c463937847ae6b5899dbc2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
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
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307c0c6acdaf1a4abbb919ade7c77f272099bb073d8dc62966bece7adc037bd3`  
		Last Modified: Tue, 13 Aug 2024 01:11:29 GMT  
		Size: 158.6 MB (158579313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276af3342cdf6d180401adec4d79e9bd1dd557db9ebf1fad3c9a98b4e443782e`  
		Last Modified: Tue, 13 Aug 2024 01:11:27 GMT  
		Size: 61.8 MB (61799583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848fce2bd297b71aff6d17337b816f7ad51c0739526d2cc102c0169bf57b1136`  
		Last Modified: Tue, 13 Aug 2024 01:11:26 GMT  
		Size: 4.4 MB (4398086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1e8c448ebf0b904b6e0d9a5ee01ccc6345d5af3218266b39d31eec5e906e5d`  
		Last Modified: Tue, 13 Aug 2024 01:11:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.11.2` - unknown; unknown

```console
$ docker pull clojure@sha256:45c50aeaad3d9a2db9943324bc03c0d851f623ce194b3207933fb275b8ff94c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6384861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70efdb36c56b3f6e00c53b516e517e83415de7e553cf76f67094cd000e42301b`

```dockerfile
```

-	Layers:
	-	`sha256:7a69850ff6110b73047d8fb952d164d625803632a4ff880e0c9d8fcbc16b8e7d`  
		Last Modified: Tue, 13 Aug 2024 01:11:26 GMT  
		Size: 6.4 MB (6364921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:974cf36f51c1e9853cf616b1f6b88434046806dd877de4f685355a986554edc0`  
		Last Modified: Tue, 13 Aug 2024 01:11:26 GMT  
		Size: 19.9 KB (19940 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.11.2` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:43ca73e575f5fd503843681499770a74493aad26c64a5c8f8476acddc74c4c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272407358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:497e40e984a4e5edcc686bfa6094dd1cfb163425c8e31b285d4ba8d30301a4f3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 20 Jul 2024 21:06:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 20 Jul 2024 21:06:39 GMT
ENV LEIN_ROOT=1
# Sat, 20 Jul 2024 21:06:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cfe8e625b59cbbdce764f2360958da104710a92c5313b85ee3c12b7c861ef8`  
		Last Modified: Thu, 25 Jul 2024 19:06:56 GMT  
		Size: 156.7 MB (156746183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540387b175f8305ff8d2d5b65b742118ae3fb893eeaf8b9e48d7a1961b76c3db`  
		Last Modified: Thu, 25 Jul 2024 19:06:54 GMT  
		Size: 61.7 MB (61674243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f47aa0f4f8032d45051093e6558844bb6df8c50d5e62d927e4ce7cfbceb843`  
		Last Modified: Thu, 25 Jul 2024 19:06:52 GMT  
		Size: 4.4 MB (4398060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db705bc1531745387ba4989acfe9b81697abfc00d877bb7d1e37cf0b91c55d60`  
		Last Modified: Thu, 25 Jul 2024 19:39:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.11.2` - unknown; unknown

```console
$ docker pull clojure@sha256:f2f6b3a4e3f78c0bfc4523d198461f6ea8e8b679a2b3d43d20b7c7c2267a9143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6391026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1615412eeee5accb21d23a46afe274149c77d13d40a03cc739a3124829747b`

```dockerfile
```

-	Layers:
	-	`sha256:3530049ec9d79d6b9df4cf6ef8f2e2bed079bdefd6d892204f5ef252cc3595b6`  
		Last Modified: Thu, 25 Jul 2024 19:39:43 GMT  
		Size: 6.4 MB (6371321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5990d4a7f719a7277c9a59ad4e7c24b1ba9914755beb2b0967a27265b1f18e05`  
		Last Modified: Thu, 25 Jul 2024 19:39:42 GMT  
		Size: 19.7 KB (19705 bytes)  
		MIME: application/vnd.in-toto+json
