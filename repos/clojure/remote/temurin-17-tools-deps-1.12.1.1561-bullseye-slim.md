## `clojure:temurin-17-tools-deps-1.12.1.1561-bullseye-slim`

```console
$ docker pull clojure@sha256:28f6747db78e0038a2129a572f92d14c0cfa9577dcb1644a569da3ffae0556c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.1.1561-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:28288e4715cf485244862ddd28985eb8c565a846066f39eb54f5c84879c8e871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (234002397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac8d52b0ec08594f33d26c07b3997c7bd9e55e23e8d57c86bae1d7f29121cf4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9b1953779a7967ef001f7145905e0bf1e35672708bf1a82fcbbe0fdd4013b0`  
		Last Modified: Tue, 19 Aug 2025 03:47:04 GMT  
		Size: 144.7 MB (144693284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb8204ccf49d0a219bde3187493b50dd314e71d90488370b8a4b2b325684924`  
		Last Modified: Tue, 19 Aug 2025 03:47:02 GMT  
		Size: 59.1 MB (59051953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e08e151ae7d7b2f3a251dc1133a788a25ab7e906307b1271ee42b5c441196f1`  
		Last Modified: Mon, 18 Aug 2025 16:57:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5719d571917054fbd6d04cf1440a778aa0124d357b91db2bb1f3baf3e152061`  
		Last Modified: Mon, 18 Aug 2025 16:57:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1561-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:47042cb1c6eb397fddf6fee54f9b691424fef1f6e522aec63791ceee1b2073d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5323946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:671be35547f75dacde6d4de67238bc79f170f57627832982406f775e25ef35b0`

```dockerfile
```

-	Layers:
	-	`sha256:fb36c5fb6c0b1c99f985b7e864514d7342638354ebc9b30e83a4bffa68caa071`  
		Last Modified: Mon, 18 Aug 2025 18:37:44 GMT  
		Size: 5.3 MB (5308067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c87c5edd58ec7364813ca8aeba9d84770042136f226d7e072797235fcb5c2805`  
		Last Modified: Mon, 18 Aug 2025 18:37:45 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1561-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4b55f6e76bb3d28c169fc0e55f2250b1122118ba0ac73b04f2ed078414b10027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231480404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed22cbbc3ec25cf37da654d22b213cbf509ba735dbb643a382612afe4cf597a8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3ae6e888f8d80755e7324ad970040abde4815c597db4a9f05cfdd6ecbe241c`  
		Last Modified: Tue, 19 Aug 2025 03:47:44 GMT  
		Size: 143.5 MB (143542102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b21a86b144ad85fb7e51a2649b904ff5985da334878ef66daa1a394eff51df1`  
		Last Modified: Mon, 18 Aug 2025 17:08:41 GMT  
		Size: 59.2 MB (59186767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60fdd94ab0eba91f5ba20f28a4655a49803fb08fd4953986daf2326333381642`  
		Last Modified: Mon, 18 Aug 2025 17:08:35 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bd7372624b9665ec324e9f8ba0b09f55ee24f42c2a37de63092178268ca664`  
		Last Modified: Mon, 18 Aug 2025 17:08:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1561-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:83d1067d7520b33f88fd620a1fa7c80d0e5ddacd1f5032005dadaf746211ee7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5329795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5453ac40e1f7b87347ccbccf905bad00c2e7158719835b2cf0b91a2c5a4aafeb`

```dockerfile
```

-	Layers:
	-	`sha256:326c816131a13571ba8c1022537a522751c0fb7b9b7a787e05628a6879cd9a50`  
		Last Modified: Mon, 18 Aug 2025 18:37:50 GMT  
		Size: 5.3 MB (5313799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1658adf9e5ee78edf36c9f0d5d1e3d0ec49dc8be46f5054727848b1d0f68442c`  
		Last Modified: Mon, 18 Aug 2025 18:37:51 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
