## `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim`

```console
$ docker pull clojure@sha256:4712e3d7b3720da6de63a959bc36bda27b9bf4eb7f329066d3efd8a8f6dd913c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dc810ba56476134c5ccf2b40e93f3b41c85070ac99f8a27417541a4c45272613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 MB (247299681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3340a0be99809ef252afe6116d06aaf5322971b8a1fadef68782f6162b9ff11`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 02:40:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:40:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:40:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:40:58 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:59:47 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:00:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:00:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:00:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:00:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:00:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2def39ba61d018877eab029bb49f5312188fcf3f564be382981f921d932f625f`  
		Last Modified: Mon, 16 Mar 2026 21:58:52 GMT  
		Size: 30.3 MB (30257826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a522af86c4d6af502174001996ffcd6e50d100d45cdd64ae3a3f3f4dc843fcca`  
		Last Modified: Tue, 17 Mar 2026 02:41:53 GMT  
		Size: 157.9 MB (157857118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405f977bf0c57a63699574253bd171a1a624dc1726ba72e70a4132f04e162cf9`  
		Last Modified: Tue, 17 Mar 2026 03:00:26 GMT  
		Size: 59.2 MB (59183700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f586c50a8f3c91f824d622e4c4afd3f5681ffbb0eba26534203fd88ddab81a4`  
		Last Modified: Tue, 17 Mar 2026 03:00:24 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351ba226b5088e6c1584c2394e1be4326530c07c4fd74ca561b5e09f8c6cab7e`  
		Last Modified: Tue, 17 Mar 2026 03:00:24 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c7f996fb83099c68a21b8cc6afec4a6650dbe1ba6f13e7e06539438715561bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5337740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ace5ba130a6bbf5b7873949f530c9cbe9da0f7778adb51385c9b1883e0c89e`

```dockerfile
```

-	Layers:
	-	`sha256:7193132c743e189d03792ecd1e7fbfcac69417fcc6c50df70c68791014065cfb`  
		Last Modified: Tue, 17 Mar 2026 03:00:24 GMT  
		Size: 5.3 MB (5321905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdcbe997decfc5627804066f4edc7f6def9c7de8c675be71c5481664a1245edf`  
		Last Modified: Tue, 17 Mar 2026 03:00:24 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1151a8b3db4a985b6d2cb60e79894b6320fa008c910884c116d8adab5cd49021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244202128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080ab975bf175bdb8da8ca3fc360a9dbc56182beaf42b0f4d2f1df2e09091b5f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 03:04:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:04:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:04:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:04:43 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:04:43 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:04:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:04:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:04:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:04:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:04:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:345f33ba283982a717a4e5e736aae0d965b9ea4497df11e15c24675df605ff01`  
		Last Modified: Mon, 16 Mar 2026 21:53:13 GMT  
		Size: 28.7 MB (28744526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb9afbad976eec8ccc6f54f0f62d6bd2a909e473c51530439c82f9bb91865a3`  
		Last Modified: Tue, 17 Mar 2026 03:05:20 GMT  
		Size: 156.1 MB (156133026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29ab7a58975cd625e24c45f3eef88e2b1fb160d31dacb168800fe7c3b32096b`  
		Last Modified: Tue, 17 Mar 2026 03:05:19 GMT  
		Size: 59.3 MB (59323539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459924c2307dbac3dc98e49ae219363f72e4f64395dcaa69430801c312b88e0f`  
		Last Modified: Tue, 17 Mar 2026 03:05:16 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c8cac43322e870fc68adcb5484ca5edb34333b00d1cedc562bc7d4b6450889`  
		Last Modified: Tue, 17 Mar 2026 03:05:16 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d255239544d4abd250396cbf193c960cc98815acccf094ff9675f667c7d64ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5343591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f86da6e523a5421df22649c1a517b491f0c0c597fa00bf1c2b7ebb0b82a14b`

```dockerfile
```

-	Layers:
	-	`sha256:9370b372bd2abbec75053851041e27685fa1b6db689b82a8e81460ed359aaa4d`  
		Last Modified: Tue, 17 Mar 2026 03:05:16 GMT  
		Size: 5.3 MB (5327637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:963627984eb08891245b7cec8acd61165c1127f422b00b37504b1a358bb5f81e`  
		Last Modified: Tue, 17 Mar 2026 03:05:16 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
