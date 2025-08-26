## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:11f95df0d5856c4eb8d7a91c5fb3933cd688fc021feb55069b6beb9cabbdfa70
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5fd10da3839ca51e02372af5e01e94a93b8fdc7a15d390460fcfa8f661e49e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247212851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a940bb3db42b52eee05fd7b70ec7f3b48d8c94b51e53021f112a7955c89a75c0`
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
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfce69ee7f5c7f3c86325c55d7c8ca278b6ff4c0808fe93afd5f3815734fd064`  
		Last Modified: Tue, 26 Aug 2025 18:49:23 GMT  
		Size: 157.8 MB (157804748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9a2dabb0b3a1949a9b33f2c05e2574f89da409e006c84fe9635cf59265c22c`  
		Last Modified: Tue, 26 Aug 2025 18:49:13 GMT  
		Size: 59.2 MB (59150944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36ecdec2a9e0d3e8364ab47f403a325d7f3cab52a16ef94e3e81da8697200e6`  
		Last Modified: Tue, 26 Aug 2025 17:32:24 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5688665a78d63a59b64ebf565b0f9fa8491d2d32b8a625010c3faf913759463a`  
		Last Modified: Tue, 26 Aug 2025 17:32:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f239253822f1053f6b99fbd781115bc6a1a4013802574ef6bbdbc6e3a4712635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5328440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150abafc496f4502daf7a52aba761707921fec44cb4e8981273d7b77729a8a5f`

```dockerfile
```

-	Layers:
	-	`sha256:298c2f7aca10deac19f3642f161a5c973739a5635525f69fd7df97bfe53cbc30`  
		Last Modified: Tue, 26 Aug 2025 18:40:08 GMT  
		Size: 5.3 MB (5311865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68e5ae828573563842024ace651703cba7411af0320101bf827e6187419a4523`  
		Last Modified: Tue, 26 Aug 2025 18:40:09 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ebbf0fafcc6a26ced2f86466a7b2c01b29a8c5122b9d71fbd3a47fc0afa7c2d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244115463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7734e53e4822658322c24d1e1731d94574a50ff15dfa4063c4afeae60b0f80a8`
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
	-	`sha256:2018a747c37989de117c5255ed9b90797d04cc50b7b51efd380710484b6be5df`  
		Last Modified: Tue, 19 Aug 2025 02:32:37 GMT  
		Size: 156.1 MB (156081251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e668e191be6b5e37eaa898607d9debab8e85d1b035855ad75ac9eacdac7d617`  
		Last Modified: Tue, 26 Aug 2025 19:11:17 GMT  
		Size: 59.3 MB (59282677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a2cc1bac12b875dc377b696885dc6189c6ad18649b1a9b98c6ade0deb5c2b9`  
		Last Modified: Tue, 26 Aug 2025 18:39:44 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c351be3ba21ff9a183bfe9bd126247ac7c54d3ac051e3f7e2013e8c0647153`  
		Last Modified: Tue, 26 Aug 2025 18:39:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:80f009ec6e61e47891eb07f87f91b5d7365307026444f792663199e885ff57dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5334337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba8c476a9ea97c1ad74925fb83cf9442b233410315ff270bb8c9321cff4fa25`

```dockerfile
```

-	Layers:
	-	`sha256:7a42fd7e3c49db0255acbf699b5caf4ca7ddf222f5596e983a109c6f4158967d`  
		Last Modified: Tue, 26 Aug 2025 18:40:16 GMT  
		Size: 5.3 MB (5317621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b914be260355af98554f2a206fde68ba5e204ce9f375faf21d032be536b936c`  
		Last Modified: Tue, 26 Aug 2025 18:40:17 GMT  
		Size: 16.7 KB (16716 bytes)  
		MIME: application/vnd.in-toto+json
