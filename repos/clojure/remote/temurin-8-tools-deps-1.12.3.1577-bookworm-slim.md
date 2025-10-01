## `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim`

```console
$ docker pull clojure@sha256:ceb4b4e4d39d78d006b21f73d1c09335837e905311581379bcac6102bc7edc4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6a359af1553c8992656baf9b20b2e0441d4b610b00d3b57edadfa066477a178f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152640350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb1ff6fcddf44ec835a8b8f1c453099e9bf6a6504cbb14712e706e7360c8cd7`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7dd7ee128c409f71b2eda529c897b0a6b3ca6f2cfb731c7706c27bbcd69be1`  
		Last Modified: Tue, 30 Sep 2025 00:51:28 GMT  
		Size: 54.7 MB (54731285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3e6f041490d380f7074e7e63e58afb97a97824b6f2e12855902db25dfbc348`  
		Last Modified: Tue, 30 Sep 2025 00:51:29 GMT  
		Size: 69.7 MB (69680086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb34a765260fe3b40e7f0b7f07f2252e6a0b27bd870b6b5ee60674574e94d75`  
		Last Modified: Tue, 30 Sep 2025 00:51:24 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ef61a67099fa4df063b5f5a52252463672abae500acc353323776a1d0b8df9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f7128b482c0d9987ada37873de785d2d74347d037421925714686086f57cf0`

```dockerfile
```

-	Layers:
	-	`sha256:abb7111744eda9f18407ce15e7b714c4d58cf9c0510259417a769f83140917fd`  
		Last Modified: Tue, 30 Sep 2025 00:50:59 GMT  
		Size: 5.2 MB (5234998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c2f1694b7d78b0bdf732d7acb9a061a1e605f7ab146d74b719f2c57b603609c`  
		Last Modified: Tue, 30 Sep 2025 00:50:59 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0416b4730aa2b555861c0548d8e41d4a9fbef3de55bd015c8fd3ddc56354651f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151498783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b61fcb741e35f7e3aaacb2451961dfc5ed6d229b7d8941ee7cfacf2e61f959`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc71ed230687c7182348ac1bbf9f9f3bcfd96064f80293d40cbdb8ae32113ba`  
		Last Modified: Fri, 26 Sep 2025 17:53:32 GMT  
		Size: 53.8 MB (53835607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3aaec1e9756b578a0e0c5d2a9342ca0676962666b711f02c60e2c28666c7f4`  
		Last Modified: Fri, 26 Sep 2025 17:53:47 GMT  
		Size: 69.6 MB (69560432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a6ed61f7768ca40bef98d774af886342855118c4d100414a58d2b3d70a750a`  
		Last Modified: Fri, 26 Sep 2025 17:53:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5bfe9f6ebd00a2c00cad6952126d62ce73009d846eed5099ed3fb2dd43869a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b2ace426530f95e2cd8af104b4c3e6e05bcd3c2133f07377b0fc825327af2f`

```dockerfile
```

-	Layers:
	-	`sha256:d68d7b35e20ab352e9d85f6a23cedb050e0d11591e0c9af0ab5d97ff6bcc2ab1`  
		Last Modified: Fri, 26 Sep 2025 18:46:39 GMT  
		Size: 5.2 MB (5241457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0dabe6600ed88fad0a7657f68ec8451c0c65c67f4c78da612287342551e845f`  
		Last Modified: Fri, 26 Sep 2025 18:46:40 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f8f04a436cb14286398b1c362745438c52ecee641b36812f142c14a9b6a0e300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159748203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e77856003b240742f2eb8ecfb53c534cf43d3f36b91fcf124214c3afa49df21`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0781e62220442f26637c34d0b32044ee4ea07ff003cd3f16b856a1aa3146bb42`  
		Last Modified: Fri, 26 Sep 2025 17:56:15 GMT  
		Size: 52.2 MB (52165456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df73b2e61f8df6ffa064598653f6e9bb73f611652e2f7ceb8a0871d168b70fba`  
		Last Modified: Fri, 26 Sep 2025 17:56:18 GMT  
		Size: 75.5 MB (75513340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcaa430b7bc1d795854ab65d0ab7a58e0e0d0dffdadca04c7f11aad8cee833b`  
		Last Modified: Fri, 26 Sep 2025 17:56:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:257e811802da31c1e8f21cd29bb87ce0b534bcaa2fa630ea6cac47d41560b943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8367a307024127bb64d6f71eedfd761984185732275d02d7c00b7770eee053`

```dockerfile
```

-	Layers:
	-	`sha256:06d9b36c76b926fcb23df8b2519bada3c7950b4b03f0b60779579f8bbb69b8e8`  
		Last Modified: Fri, 26 Sep 2025 18:46:44 GMT  
		Size: 5.2 MB (5240749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35dedd6ea92a8190e4127aacca264b3a2a1380942cdc0d306a3f1529ea516ec7`  
		Last Modified: Fri, 26 Sep 2025 18:46:45 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json
