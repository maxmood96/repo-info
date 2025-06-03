## `clojure:tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:0e0ad2e71d4a0569add692b44766c0bd4ca2105a6c5ca1d33a87864e998f9e2e
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

### `clojure:tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2340e3a396678fd47268b1abdb844968b6db85342c7e7153ac9c5653ee70be99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255390313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56feb9c1b307e5c58f5219a0fcd99ef7c1271784eb489e9df6ff12af8f49b33e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e7a4d4234a0b4690c5915a6d5517f2dd6652988554214cc8e8e255691e7cf7`  
		Last Modified: Tue, 03 Jun 2025 19:18:23 GMT  
		Size: 157.6 MB (157634483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76361398bd7a36a4113496f96e680babcaaadaf0128aaeda0723a2831046f917`  
		Last Modified: Tue, 03 Jun 2025 18:25:11 GMT  
		Size: 69.5 MB (69529459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc57f53ae751fd395dfe8c11bbf869d6f8c9c871aec5b28e847814e06b74db2`  
		Last Modified: Tue, 03 Jun 2025 18:24:52 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38261d2c941233d29f343e69dcfdeea536e3e0042bd6c21a0a2026f2ab062ce7`  
		Last Modified: Tue, 03 Jun 2025 18:24:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:60fff831b390d512f8fc89e556d07fd2843b1781abb70d9b3ba180015e7343f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4981869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43cd3d09f4bb1ee80217e6c7ff5b7c158944ea11f826205ebe91dc2a14a2f7d0`

```dockerfile
```

-	Layers:
	-	`sha256:93afaff100dcbd00e10cdc50b80d2e054c435eb744dcd3ca2d467f733bb8b142`  
		Last Modified: Tue, 03 Jun 2025 18:38:37 GMT  
		Size: 5.0 MB (4965296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78dade58da4966836659473d63a5d51dddee854409917efec1ca2fd77a3d12ef`  
		Last Modified: Tue, 03 Jun 2025 18:38:38 GMT  
		Size: 16.6 KB (16573 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:652d94e9014720796996396c48c65d50d64f0b571d2083a25f757740529c7599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253386852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6719c58e514263905099cfb75ac0fec08fee7933e4d538d2a822f3702ee288c8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec03d7eeca89e0760e8dbc23abc005a69970b61d7619400463b7928ff3fe8a3`  
		Last Modified: Tue, 03 Jun 2025 10:53:04 GMT  
		Size: 155.9 MB (155928831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23748e1134ae45e248f8cd98347a8ced03f0b73d4f9e79aecc5f07d1ee2a3c8`  
		Last Modified: Tue, 03 Jun 2025 18:46:01 GMT  
		Size: 69.4 MB (69391700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c175977974e98edf2a8837081141a0c4acce620ea837e762a1ab1665f000f50`  
		Last Modified: Tue, 03 Jun 2025 18:46:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0735920c832a1597a32bd8ed75aea6e69ac7ddb2d15c4f6575068d5a0f5e4ba8`  
		Last Modified: Tue, 03 Jun 2025 18:46:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a837d269d8cf2901f9fc8790ff2c5daede933a86d23a4a0df1c0e333631b8ab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4987798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af18f6e20af4584d7cfb01f28966aa1574ef48cf7279db89fe76d82200c0d184`

```dockerfile
```

-	Layers:
	-	`sha256:3c2e4629244d38f2c6e9428baecdba482d780d2849940737498bbe2f73b06b89`  
		Last Modified: Tue, 03 Jun 2025 21:40:02 GMT  
		Size: 5.0 MB (4971081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:884d4fe9e10327d3ed1b704b49d060c60e1648545f6f5fa4e5446d3d5163aed6`  
		Last Modified: Tue, 03 Jun 2025 21:40:03 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; ppc64le

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

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:tools-deps-bookworm-slim` - linux; s390x

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
		Last Modified: Tue, 03 Jun 2025 06:25:04 GMT  
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

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

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
