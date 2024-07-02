## `clojure:temurin-22-tools-deps-1.11.3.1456-bookworm-slim`

```console
$ docker pull clojure@sha256:d9ad31fb068e5747a1eb373832924e725b48abdd76fbb91ff4599b5fd02bd109
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-1.11.3.1456-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:401e76153fcc516577901ff8476e648f8d5b0afb84ce8aac9cc55cd97dc49902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254909377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18b84e662b0bf57b41039ffe003e4b151d6222ae057d1675b56238c7fb6ef6d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030a8c7c82d8cfbe3accf9620042d3e1d846062b588726d74c4f9af21cf614bd`  
		Last Modified: Tue, 02 Jul 2024 03:03:07 GMT  
		Size: 156.7 MB (156715525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5143b246cdbaf4f45fb00773e3448819e612e10a8dfb399b0a74d83393c40892`  
		Last Modified: Tue, 02 Jul 2024 03:03:06 GMT  
		Size: 69.1 MB (69066535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25186c86cc9f6b2673cc3224513292f2d115151effc2729e69b0e95bdddba10e`  
		Last Modified: Tue, 02 Jul 2024 03:03:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376fb7bc9f5930cda7b16a757bbecc34d64878b6e75d2d3ef0a7c7f05b44f8c3`  
		Last Modified: Tue, 02 Jul 2024 03:03:05 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d12b71eb8701a9e27396969f1b58ccd8d059d31d24b3b26904e25670ea5cbd2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4720545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0338b7707c6ecb4f5f2f7cd8cb15d532826527ac95f0cb71fc219b962aabed82`

```dockerfile
```

-	Layers:
	-	`sha256:dda39037c9f620d883d64503df769918984cfad23590d1d784b3e77a4fd50e75`  
		Last Modified: Tue, 02 Jul 2024 03:03:05 GMT  
		Size: 4.7 MB (4705033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fafbcb7edda01b6873b3513cb779d3a9d9d0e0bf28edc6f2f0ba3d29c857e7ae`  
		Last Modified: Tue, 02 Jul 2024 03:03:05 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-1.11.3.1456-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:53b4a9a8043ed99b91ae9d22b00b7ef548c4ea12ede3563a0188932580ab8dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252539537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0bbeab9827139a0d0ae61e5eadc41fbab9d043c9d2b0bdd7dccb559013647f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d556f73e4c9f57bac26b955ba103d774358439da4efb0b23e476a44efc2c3977`  
		Last Modified: Thu, 13 Jun 2024 12:00:35 GMT  
		Size: 154.7 MB (154738019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e529a5fc30ace21fcc5c078d0a06ab4e01735289c1ee6ed233e5504db10c737`  
		Last Modified: Thu, 13 Jun 2024 12:04:01 GMT  
		Size: 68.6 MB (68620806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777777e585912395d68d8e630605b625fccec4778a78ee1ee3eb0ac422494198`  
		Last Modified: Thu, 13 Jun 2024 12:03:58 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea98b54c7f6f645c334e1eaaa3dfbd0a826357c6519ee9cedcc0260e8ae6107`  
		Last Modified: Thu, 13 Jun 2024 12:03:59 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4fdb260cd33ead8f5e729ce62b04814083102a2c24b946330cd301262b56358c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4727370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b7fa45ea4666b6a43a5d06ae298fe02f6990ee112b5c46d43b68114bf8664b`

```dockerfile
```

-	Layers:
	-	`sha256:8e4af04f5f86794b7600ff726812b1adc8dd489c253213b87f24cbb6d20fc47d`  
		Last Modified: Thu, 13 Jun 2024 12:03:59 GMT  
		Size: 4.7 MB (4711317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:060b4e760b4d69996107aefa5f2c3763c72f125c44ceae2dcaa5c2839bc418ed`  
		Last Modified: Thu, 13 Jun 2024 12:03:58 GMT  
		Size: 16.1 KB (16053 bytes)  
		MIME: application/vnd.in-toto+json
