## `clojure:tools-deps-1.12.4.1618-bullseye-slim`

```console
$ docker pull clojure@sha256:efab4bb503f7ab43fa1a5baced120b77c701afe21e8f5a94ce1ca67b6ec19127
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.4.1618-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cb0f2c181b39d3a17f28cb7e7a9949543315de72b52cabf333affe814556c2bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.7 MB (181698826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ac9664b053e47c3c77b14f7ebc69060077752121d6526cf3e835c4b386f650`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 03:01:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:01:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:01:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:01:30 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:01:30 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:01:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:01:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:01:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:01:45 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:01:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2def39ba61d018877eab029bb49f5312188fcf3f564be382981f921d932f625f`  
		Last Modified: Mon, 16 Mar 2026 21:58:52 GMT  
		Size: 30.3 MB (30257826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887b1883591b98cffba4f9992de81d34cfdad14c7c5e1aaa14782fc0706adbe1`  
		Last Modified: Tue, 17 Mar 2026 03:02:09 GMT  
		Size: 92.3 MB (92256289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88ea061b1f835d69e7a04119b443276536ee92a23a560efae03b90ff87709c3`  
		Last Modified: Tue, 17 Mar 2026 03:02:09 GMT  
		Size: 59.2 MB (59183668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d837d32eb3f967a91bb76d695a5802ee69ae3127b2dc7ef4f70c1d1e4003b9b7`  
		Last Modified: Tue, 17 Mar 2026 03:02:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92a36974bf240c31dcbe3599fc4b01eee40ccd6da295ea5724786f1269c6452`  
		Last Modified: Tue, 17 Mar 2026 03:02:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f4249d779b5cd1172974511993ef94ccb9aa3c04706796951b8397a9521a558c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5304672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a006f8563bd8b0be1f6b6f6c1df601d4b0ac69d474090e44f5c3298b8f71be1f`

```dockerfile
```

-	Layers:
	-	`sha256:aa2d7a7f4a55d56406ecc20c7ed33f029bcb8c45b5351244b2015efadb8549d0`  
		Last Modified: Tue, 17 Mar 2026 03:02:06 GMT  
		Size: 5.3 MB (5288147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67a2fa52009ab61b4d0102765d05feeabfbae4bffdd386314839e210d52c225c`  
		Last Modified: Tue, 17 Mar 2026 03:02:06 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:520fc32d4d5eff59870984064b04761d14b304cb4d68fcbef281b04af896b0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179357408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec9211eeb759df12850525741b874a7ec7c8a8cb6c8b5a8b231fc7af1dabf28`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 03:06:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:06:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:06:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:06:05 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:06:05 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:06:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:06:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:06:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:06:19 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:06:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:345f33ba283982a717a4e5e736aae0d965b9ea4497df11e15c24675df605ff01`  
		Last Modified: Mon, 16 Mar 2026 21:53:13 GMT  
		Size: 28.7 MB (28744526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21354101ca9267107aacb707f22ae6c57d6c6032cf97fa0e1d12bfbb029aba3f`  
		Last Modified: Tue, 17 Mar 2026 03:06:40 GMT  
		Size: 91.3 MB (91288272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf823e096d012915fe01a351c0892841fb088ee82cab296ed4754d28314cb5e`  
		Last Modified: Tue, 17 Mar 2026 03:06:39 GMT  
		Size: 59.3 MB (59323570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debc8e744e926b9119e47afb03abd93c8b91cd0bb96b12001bb813518508b5c0`  
		Last Modified: Tue, 17 Mar 2026 03:06:37 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e336e560303f26f5aef141624efe3ba06f5338491b117589eb07f538c1afe60f`  
		Last Modified: Tue, 17 Mar 2026 03:06:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5f81e33c6ade9bfcaca4058bb32c1f9f0ea6490207799429414fa098d335d9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5310567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4193bd23a19d9344fd278f90debe182b094a9bfa38f7d87129992e47b94202c6`

```dockerfile
```

-	Layers:
	-	`sha256:e783cf505a623ba4c7d296acf3f3869517358e068f6220c12824284630f4cf3f`  
		Last Modified: Tue, 17 Mar 2026 03:06:37 GMT  
		Size: 5.3 MB (5293900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13f80c125a7d5e6e3aea219db00259c63d6c5b7e9e5be9a24d6005d6734a86eb`  
		Last Modified: Tue, 17 Mar 2026 03:06:37 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json
