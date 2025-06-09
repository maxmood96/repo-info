## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:682c6e67b31a2d12cf5e292d16ca8016183aa0a54e8f26428c2886922fa6be56
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5a47e93c5f24991b595fcc18d5d9d8449a56aa53a6e6de4db53199d4895b788f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255390803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5f46fe19975bb2161de9b9df9bdfcbb9d443e350d68392d539fe234d024f7a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2e01f4f5ca38c2fb1ced1a4d0a4d358d5b444fe65ca5b1311a87b1e5d2b60b`  
		Last Modified: Mon, 09 Jun 2025 19:00:06 GMT  
		Size: 157.6 MB (157634503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c0a53615c7462cfe5fdcf7d9991e1b3710d10beb6028f20617e4c98d921977`  
		Last Modified: Mon, 09 Jun 2025 17:19:05 GMT  
		Size: 69.5 MB (69529931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f235e8a2f1e8a544455af929aa90fc6580209a147221f0cf4de9726e763e6355`  
		Last Modified: Mon, 09 Jun 2025 18:59:58 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60658189b7e15933d486f8e1259e0bf263a35aa4432709962fe0e0a098493e2`  
		Last Modified: Mon, 09 Jun 2025 18:59:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b02dcca69f42a631e558735318accaac0f72537aa94b90f3577023d9ed60d0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5130261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c3c3a28496d7c30d50db53ed106d023d62c84e147fadcbd2d7bb8a6372c887`

```dockerfile
```

-	Layers:
	-	`sha256:4a782c4ffe09fb217e66b2f042e6dac0f5e40461676fa9de635b20d69e1d4c3e`  
		Last Modified: Mon, 09 Jun 2025 18:39:05 GMT  
		Size: 5.1 MB (5113686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26e2c617ec205e511761de92e3b0c534c96a506bbe754196a7fef0fef02a4ca9`  
		Last Modified: Mon, 09 Jun 2025 18:39:06 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:38a66d335df7be3554df3a46757a4ca65c7fcac5ed542c013c71212eec38825e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253387006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51245b163aae234aed0ec7fccac0cc30e85211f5618962f2c8c91c251134ab85`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec03d7eeca89e0760e8dbc23abc005a69970b61d7619400463b7928ff3fe8a3`  
		Last Modified: Wed, 04 Jun 2025 17:10:52 GMT  
		Size: 155.9 MB (155928831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcf2e1809dd898f51c85947a926640f5072ec15e66381436dcc1a2ba4dc5c71`  
		Last Modified: Mon, 09 Jun 2025 17:53:13 GMT  
		Size: 69.4 MB (69391852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f518a34ecf152c8247624dc3ebb9e46af551334001455def14b06d2fc0ffe337`  
		Last Modified: Mon, 09 Jun 2025 17:52:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da160d4233b8a756f494920d167536700225e3fcd5d7d6b51c30bf4a96df593`  
		Last Modified: Mon, 09 Jun 2025 17:52:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:afb8cda7d76552d0fdbd56f305734e9287abc90c6d34eb9e2d7f8ac74213b8dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5136188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c4dd6fc9eeb06dc63a0f1282a7aea041082ba3f7bc41d9597bdf0adf5f5250`

```dockerfile
```

-	Layers:
	-	`sha256:c897fe5056b8c1809b20cd1f8ec6ecc781a4366cc20069623efbc94de5a312d5`  
		Last Modified: Mon, 09 Jun 2025 18:39:12 GMT  
		Size: 5.1 MB (5119471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77203406b9e78f1ec164820cfec25e98b7553ac4abe89cc751de04ade847fd38`  
		Last Modified: Mon, 09 Jun 2025 18:39:13 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:87d2ae968be79a03fb4617b9f0edbc3d69f6752988a77fc8608762125dffe78c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265218697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89aa00f40e55d63e00ae33ca2ebc788a5a440c4e1376effdb0edc7c78dbabf22`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d05da02c9fa2302ce040ac6b740be17fb80e4f4da068aaee1ed947b3588ea4`  
		Last Modified: Tue, 03 Jun 2025 09:05:46 GMT  
		Size: 157.8 MB (157804869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd857bf3690d00e702ae2e2d504cdec90b0864acf84ad20b9b505e8192a8e0b`  
		Last Modified: Tue, 03 Jun 2025 19:01:50 GMT  
		Size: 75.3 MB (75345876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676bdb09cdd739a9cb39c4717b719c0988530350ff883d5173fa1be672c0e658`  
		Last Modified: Tue, 03 Jun 2025 19:01:39 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f608bfe4299702be26936574ef60e49241ef17ed65fede67eba23c7830216e`  
		Last Modified: Tue, 03 Jun 2025 19:01:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1198a36a9e2df3aac430a6492ccb0195f3066bdb716c66c1ca4a1cef70e55909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4987101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b193fa909708ad337df142fe87d89115e01d3eef599b2825ae8f7b039c3627d`

```dockerfile
```

-	Layers:
	-	`sha256:4fb97b77b0f262bee8c24beede5fc91b0105a6122b2b70e143a81397742a8452`  
		Last Modified: Tue, 03 Jun 2025 21:40:09 GMT  
		Size: 5.0 MB (4970466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f3f0b053d22622aa183f911d5746443666484ce8556daf522ab3b29e8ea46cb`  
		Last Modified: Tue, 03 Jun 2025 21:40:09 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c7e031f6345ff3d1de4706034fe27117f321e6030eadbed8b53bc06b92631839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242128992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c9dcbb7291a28fe88cc5ea5077ed2dc9bc7d7e2e13d44bfd332ff5789a86fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833ce0de8cf4c008922a20ce0f4a2e515d9892f114fbc6b544b0dc1f28845f2b`  
		Last Modified: Wed, 04 Jun 2025 11:30:49 GMT  
		Size: 146.9 MB (146910974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b82e86a683cd0bdf96b78a4a00b1aa87ce188e2a92d509c6de018636f38941`  
		Last Modified: Tue, 03 Jun 2025 18:38:40 GMT  
		Size: 68.3 MB (68334171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6a098bf31f4a89c0cb98dbe0d1acdb3625071913bb844c7057bd1f27094c73`  
		Last Modified: Tue, 03 Jun 2025 18:38:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3459ee6af6fac624439d5af670c0f8b9f6ba6eaa78e9cfd9c5bf62f8b734fbb1`  
		Last Modified: Tue, 03 Jun 2025 18:38:38 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:14cfe136b788b3cea1964508306545f5ad5fc1d6b1c77e5c5032a88d2272564b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4976084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95676605271fa9dc215d3845c9306e4b94c19c78ebf7badbac0bbd4aba1c41ef`

```dockerfile
```

-	Layers:
	-	`sha256:a69c208065eb2644e64b3a0b30e69c110f72c0fd35567fde35925a2643eb270e`  
		Last Modified: Tue, 03 Jun 2025 21:40:14 GMT  
		Size: 5.0 MB (4959509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6cf1fe57241ed336afb5bf689d29b6dfb62503d73ed42e2b21c277ce742d4ef`  
		Last Modified: Tue, 03 Jun 2025 21:40:15 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json
