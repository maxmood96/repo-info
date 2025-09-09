## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:29ac19bc8b5d7c13157ff5138580606ff6f4b0f86016150d23227951600bca6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e2c3878561a5fd080ae8dd4d418c4578bad91324774c6ee5cbae798edf01440f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234101506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63815ff5043df706a7ca3f79c92951a5417a020a755b440bee4081f71ca9dd1d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a186af68327d734fd03edb7106534731bda0fb70ff3ecd40231893d4ec35a0`  
		Last Modified: Mon, 08 Sep 2025 21:43:27 GMT  
		Size: 144.7 MB (144693302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04d6c9af37a98a1272699f6c826a540d3125cde36933996066c40a2ce11ef0d`  
		Last Modified: Mon, 08 Sep 2025 21:43:25 GMT  
		Size: 59.2 MB (59151096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b66c2b28c73b2fbcebead407dd149a478e4eeeed3e071dcbf71fb472edca67`  
		Last Modified: Mon, 08 Sep 2025 22:26:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0586b91a78e6e9bb82949c8ef328e5068e4624745be981e38baed34688ec863c`  
		Last Modified: Mon, 08 Sep 2025 22:26:46 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0fb6ea6c3e93fb24673fbaaa53783ebc108ab306eab1fd6fe29451d71d3f9c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5323945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b215aea63751b4a36954ccdba10fd3c5d598d788d93ca20f0b0daf65cfc993`

```dockerfile
```

-	Layers:
	-	`sha256:408fd0937b034501d0059bd5a6e23ffb1ebcf58c57776e028ac50781589fd2e3`  
		Last Modified: Tue, 09 Sep 2025 00:37:50 GMT  
		Size: 5.3 MB (5308067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d0883a3ac96e368eefbe596679875e233c09cf85b613476ff537128539d7ac0`  
		Last Modified: Tue, 09 Sep 2025 00:37:52 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:59bb354ecb8d33fd8c8198d11ad953ce22ccd5eccfa6f4f8c377f9a5d6224919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231576489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5521eb7d4030d9e38d98814766f686dbff32d1b2e1988de1f2b3dd5921bc690`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e2026aa583480d70d13af9d7d6e721f73d5e7e28ff9c70fa6900ceb26667d1`  
		Last Modified: Tue, 02 Sep 2025 05:44:58 GMT  
		Size: 143.5 MB (143542156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002bff9532adc1f4417224f763153087134d9c135be166b5428cfe2c2ac107ff`  
		Last Modified: Tue, 02 Sep 2025 08:06:04 GMT  
		Size: 59.3 MB (59282800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bede17efeb02ecb0ae71b838c74b9c008cc9c1c9fc8400ee342929f4229fa9f4`  
		Last Modified: Tue, 02 Sep 2025 08:05:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3268dcee26db625594cbe5678d41f95d30f1e8d51ab82be721cc20f0104d016a`  
		Last Modified: Tue, 02 Sep 2025 08:05:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9aeb3d96e8936ae5d812172449306f1b8100dc263738cdc09ff049acb0e88599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5329796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c77054055f9c4b8d13312a8f9488139599f073e9cec66482ce5e31585035e9e`

```dockerfile
```

-	Layers:
	-	`sha256:34eeb63e225571dc1089a7691e75c7caa1d041e8446a9185aea350aab5ef1db5`  
		Last Modified: Tue, 02 Sep 2025 09:38:09 GMT  
		Size: 5.3 MB (5313799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c0c8956b30f374f8be83b6cceb43a842013216f38ecfb83ef2c631674b657bd`  
		Last Modified: Tue, 02 Sep 2025 09:38:09 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
