## `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim`

```console
$ docker pull clojure@sha256:a68ac68ee1b540a137760199c8f2090b36b35b458a51345b94a65f3fd313e441
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

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2a6dfcf0e88fb4d1d759ddab11f571347c47f74862e6deba04bcbc5a5dada89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242392374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771bda591ca11a87957438539e905fd60917f4334602424faef755b97301bd82`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a90d692b2ea3be47c643ab64b8218fe1c7d551e158a1e76fd0e12f75c3fb20`  
		Last Modified: Wed, 21 May 2025 23:33:07 GMT  
		Size: 144.6 MB (144634958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d690374fd48da307fabb3394727d01ed46842c17ee246aa83edac6eb695c4cdf`  
		Last Modified: Wed, 21 May 2025 23:33:06 GMT  
		Size: 69.5 MB (69531048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665b862e918b95a442b8bfaf1421670db8462383755e7fed62f0f25aac91b966`  
		Last Modified: Wed, 21 May 2025 23:33:05 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9030b2e620a8e88d8253d9328e2d53d943a74cb3c2bcbee1e08876ad44f4945`  
		Last Modified: Wed, 21 May 2025 23:33:05 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8097b7e759e18ce3d8b149f50643e13fab21d52b42d82fc686f956a04b1cb7f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4977377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919233fbae5bd7fe684363d5f80eda67c76975e23454050b26967d5cece36d62`

```dockerfile
```

-	Layers:
	-	`sha256:48b92f924d0b91ea495d39322ab37f977dd1e0ca45f5bb3d4ee329d98fdf0f9f`  
		Last Modified: Wed, 21 May 2025 23:33:05 GMT  
		Size: 5.0 MB (4961498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22a2cd7c31e5898deba026900cf2b799ad53ec2e26a41ca7eac1c5e84d512b3d`  
		Last Modified: Wed, 21 May 2025 23:33:05 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2f2b4803da3131f5267aee9b19a37eca8d9efe929af9ce730486810536649f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240965081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0ed8c699d9cb05fe24e0fedc392441b66dd8447b4362a1468fb500a4e39ae4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b321836524b69ea3544c5efb3ffd84866c65bfdc9bc0020ff7d56a1633cff0d3`  
		Last Modified: Thu, 22 May 2025 08:20:52 GMT  
		Size: 143.5 MB (143512639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3a91216796ce999fae54dcb9b4dc51743e74220e782b62e9ab536dceef9c32`  
		Last Modified: Thu, 22 May 2025 08:25:49 GMT  
		Size: 69.4 MB (69386124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793160d2a51ce79989475e916b3199c3b397272af153c2946008b73e76faebe3`  
		Last Modified: Thu, 22 May 2025 08:25:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ff0642eb278933713b27f4f7cf64a3ab4688d5477ab94cb63b68925c7b68f6`  
		Last Modified: Thu, 22 May 2025 08:25:46 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:99766b418fd681dcc8859b7e580a057027ec718d6822830b842fb8e80e10a959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4983256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd26afe9120f644c2d0ceb2675de1db7a40d9868c3ac3b76cd8643f08c4ddd69`

```dockerfile
```

-	Layers:
	-	`sha256:e94b6e82cdba0cd4f4c6301fa1bf757fa40692006975a03e3dc017ff10f7e402`  
		Last Modified: Thu, 22 May 2025 08:25:47 GMT  
		Size: 5.0 MB (4967259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7578fe2d984bc6d128bb017ae1add68d1349bad71fff9d672b072723f77b1d4`  
		Last Modified: Thu, 22 May 2025 08:25:47 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ccd6dedf9f9936dceb34f56898594aaa76ddb54cc82c4689940a201bf78f953f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.7 MB (251695739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcca312505dc5530a5ffa8c788f91de9ec9d1a6bd8ff242f4ef8b56e9e0ba617`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Wed, 21 May 2025 22:28:16 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc11ef7c3f5380ac924221255625cf91a9c9e7a9f7592fa1d185dcf16a57faf6`  
		Last Modified: Thu, 22 May 2025 11:16:04 GMT  
		Size: 144.3 MB (144280502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7dfa4e98c6074f63f56f7d303fe3283859b9faa58489ce7ea36eed02bfcbf6e`  
		Last Modified: Thu, 22 May 2025 11:22:52 GMT  
		Size: 75.3 MB (75347286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aeaae3734e1c8141e5f41960a74840ea4d9475bd2973a68ea0344a70b46a79`  
		Last Modified: Thu, 22 May 2025 11:22:49 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd4c6b393b7857ed2227e415bf2fd824c27070f2c094d922cd1a9508936f021`  
		Last Modified: Thu, 22 May 2025 11:22:49 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5b2769717bc2f44fec26ab09b59a1ba87fd935880dc7da1fb787a4af4c01a118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4982582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add829d208a1faf295f1da4c19d9efa971bfb24079e4e4492573b6f410977dd0`

```dockerfile
```

-	Layers:
	-	`sha256:65a1b57dfc12515dfc842595e02494b317667277b0cf025b744666ac21ed2004`  
		Last Modified: Thu, 22 May 2025 11:22:50 GMT  
		Size: 5.0 MB (4966656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e9f4345a26c13a8e8c5211abb9e448b389668b5e7481261b23951020cfa3272`  
		Last Modified: Thu, 22 May 2025 11:22:49 GMT  
		Size: 15.9 KB (15926 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:28cb41f290b9cbcc906fe4060cec5f4fe4ec8ad3502ce5d33f5b2c23a12bcaa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229884732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba44742bc29d28a333c800c9677b9cb12968f44e45ba7e7df582effc4ceac07e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93366ebf43b9fe117214d3ac77d0ba774ae0502fb6f9fea20e59c5e22af5a643`  
		Last Modified: Thu, 22 May 2025 03:50:40 GMT  
		Size: 134.7 MB (134673611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e4748ae384287bf80ec41aa8612900579f411344d015b92e213d3bca1b844a`  
		Last Modified: Thu, 22 May 2025 03:54:35 GMT  
		Size: 68.3 MB (68327272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9d93c484b9b14a5529e584e0699bbf7fcd22424bf817a94e13a8f64e2cc91d`  
		Last Modified: Thu, 22 May 2025 03:54:34 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7ae1c10f5797d6ce5bd1376f718af847cd9b3753a97f3da59d23b487edbf1c`  
		Last Modified: Thu, 22 May 2025 03:54:34 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9fc3ca50cac2dee24a61a7efb5584c31f4167afac715d5b7c373921850872c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4971588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b6011b808ab5de1055909ee5ffdf645555acdf81468ec9ebbbdcbfde5c274b`

```dockerfile
```

-	Layers:
	-	`sha256:f803ff454fd295f792009027aeae47b000f388d53b29f2eaf3b20c36db416133`  
		Last Modified: Thu, 22 May 2025 03:54:34 GMT  
		Size: 5.0 MB (4955711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d6c9efa979fc20365f83eb859e62d3f41c6cd41b0ecf0166eb9f27bb181dfd0`  
		Last Modified: Thu, 22 May 2025 03:54:34 GMT  
		Size: 15.9 KB (15877 bytes)  
		MIME: application/vnd.in-toto+json
