## `clojure:temurin-21-tools-deps-1.12.4.1582-bullseye`

```console
$ docker pull clojure@sha256:02e8ca57b4745800d6f40ef62b59daf72afc49f65dff68673b5da06d38904fad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.4.1582-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4880e378759ce5985c69d57549b284cd0207fc03663c7b1d54434b60864a2020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281140203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0808350373331ea29dd7a4532fed757874f0ab2e959caa5b45ff50becde324ad`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:36:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:36:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:36:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:36:18 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:36:18 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:36:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:36:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:36:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:36:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:36:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:36 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa137c4a0667702f7b5b33d6ea28934725a1e3149623e024799bd8358c48574c`  
		Last Modified: Thu, 15 Jan 2026 04:37:23 GMT  
		Size: 157.8 MB (157825976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f572583d1b2dfef4673f24cbc78b698c40c58bbf7576e37e798df9fff690367`  
		Last Modified: Tue, 13 Jan 2026 03:37:12 GMT  
		Size: 69.6 MB (69556741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cba0d9c5627d79e5b476b0bfbcda96396932d6f726e463d41e18adbfdfffaa`  
		Last Modified: Tue, 13 Jan 2026 03:37:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7771021e271d494538fc2189d08390d5fb5438abd3f7e75bbfdb37611822b9a`  
		Last Modified: Tue, 13 Jan 2026 03:36:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1582-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9ade9ecb825721d9206b582fef94cc09a5fabaf0ea02e21e6f629af3ee0f3894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7414548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980e790890f874b3d6a362426a1c05d4472435e34134605a564e65238ac1af77`

```dockerfile
```

-	Layers:
	-	`sha256:62ff7945ecc9a1252498677c0706b6feba7d31a913da55afa13e7d6b2336e6bd`  
		Last Modified: Tue, 13 Jan 2026 07:42:39 GMT  
		Size: 7.4 MB (7398771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1caf8e4b6d883d161e8caa9d513750bfb3e4bb24e815d0c9b55f16007fa26f1b`  
		Last Modified: Tue, 13 Jan 2026 07:42:40 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1582-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:87fd50d31c5c9ec5eafd64a82766b33820a1158d6388a146dd12497e510ff9b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278053324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d78ea3e7c60a2f4b41f50ed840638e65496f8e808ca2acb20824228b0c5ed0a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:39:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:39:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:39:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:39:29 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:39:29 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:39:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:39:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:39:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:39:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:39:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:52 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b7f87d1e9d3b7b6cf0d892898292f1abefa1e77c829bcf0ae8af4e2b12e238`  
		Last Modified: Thu, 15 Jan 2026 13:10:33 GMT  
		Size: 156.1 MB (156107655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f241fd8b35ee7fb390b2316fbbd945ce69e54e339a2b820e3eaa2a4a56db348e`  
		Last Modified: Tue, 13 Jan 2026 03:40:31 GMT  
		Size: 69.7 MB (69686863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2428e6dbe5f0efc949dd79a6a3adf3cf90167a969f5c48a7655eaf069b6892`  
		Last Modified: Tue, 13 Jan 2026 03:40:26 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7a581f6bbe18f06feea843362b0cdf7b351ed5ccdb1e0047f7576906a38fd7`  
		Last Modified: Tue, 13 Jan 2026 03:40:26 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1582-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1d835cfa7ffeadaadce66d05f5339742b86fd1d415f5dd450a448f3510699d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d54cfa6104a32752c80e454794dd6151d6dc0cf05f741c564c3e2658a37816f`

```dockerfile
```

-	Layers:
	-	`sha256:70c476f68b47338cf6606b37575459a9eb10b3ae25ad0ac2f62a459d03ed9c5b`  
		Last Modified: Tue, 13 Jan 2026 07:42:45 GMT  
		Size: 7.4 MB (7403870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74fe1299853601fe38b30a58228e1ad57f334c0f8f07034e11db29a573aec557`  
		Last Modified: Tue, 13 Jan 2026 07:42:46 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
