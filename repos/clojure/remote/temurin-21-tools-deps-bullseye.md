## `clojure:temurin-21-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:bb26a579187d058a8a0aabf86562e1a5e0af9a0185e6421a9e4a95ac2f65dc75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:52e92631acd3247de8d58977ea0e6f2a91d82600acdc095501cbf8897e56c634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281117491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae4cc19ff6b516a47622b3c75fd96ebb83cc39fb6e4d6809c1f08364f60cb3a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
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
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c3c1b4121392e275dbee917d5749ac6f16cb022cb5c59e50ea8fa170c481f3`  
		Last Modified: Tue, 26 Aug 2025 19:11:52 GMT  
		Size: 157.8 MB (157804778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d457feafcc5a7c10a18a36603604ffecbd2b36caf95060002f4c2cd8d71aeea6`  
		Last Modified: Tue, 26 Aug 2025 19:11:36 GMT  
		Size: 69.6 MB (69556328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048cf0cae8f47750766ded01e2d4109536cdccda551af786eb827ceedfe7b1fb`  
		Last Modified: Tue, 26 Aug 2025 18:58:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8af27b71c6503a541afb780a7e7ca12d9f7e8a350aac769db561b1b821eed6e`  
		Last Modified: Tue, 26 Aug 2025 18:58:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:015045733c8f544e4c08f2f3df9e20583364d42a2591d61ca92866ad9318fa1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e93231539f70c3851376cca249562fb8994c60979b4628ab59643522779ed9`

```dockerfile
```

-	Layers:
	-	`sha256:7f5b9a52d2c0557c3e71927527b55e36fbb04346863484f768bdd2a8a74ab259`  
		Last Modified: Tue, 26 Aug 2025 18:40:02 GMT  
		Size: 7.4 MB (7399445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51dd2b33e77bcf20b77de0f100ecd8eadf1a84dd1c802b5e3ea051f95c168de7`  
		Last Modified: Tue, 26 Aug 2025 18:40:03 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1b42c375e80a0d78e95fd8f827438cef08afecc8f11235b157968892ae5292ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278014559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb6ce745e0ac019f8746dd66e40028004d8c5567711e7ecf6f716b7b6e4fa25`
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
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5040edb8c8b4b578b900bd5351ad845bff5b8df176e4185b63c2ceb4a65cad`  
		Last Modified: Tue, 19 Aug 2025 02:34:17 GMT  
		Size: 156.1 MB (156081250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787b764611284aab1f26f857665be99bed269efaef0ec0f327ff0ccba79fae53`  
		Last Modified: Tue, 26 Aug 2025 19:12:11 GMT  
		Size: 69.7 MB (69683855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f674dc16c129ee99c9fdc2f79c5740603018dffdd4e9c71cf83ecffd89a7196`  
		Last Modified: Tue, 26 Aug 2025 17:59:22 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6608851d7210d06d891472169914945c6609f9a6cf314d8fa454b0b3de120f05`  
		Last Modified: Tue, 26 Aug 2025 17:59:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2947debadfc1bf781f9ad992045af1ff2ef165541094a57cdb6b74900c7623c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7421207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314eab224d514961d5ccbf4e67250e2289a004edc51e6ac4a099d2859ecc9e87`

```dockerfile
```

-	Layers:
	-	`sha256:b633ad8ac09b1d92955bf46b4224d17b0b44288d11a3bc18831f6a137f116b3e`  
		Last Modified: Tue, 26 Aug 2025 18:40:10 GMT  
		Size: 7.4 MB (7404568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f42b08dbee680cdace2e004ab1bb2a329e22494e80cd4c210e78cdf8a24a2727`  
		Last Modified: Tue, 26 Aug 2025 18:40:11 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
