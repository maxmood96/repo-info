## `clojure:temurin-25-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:e0d4d0c2c66deaef865c6d79817bb498aae2c07e84f81dba8154e51d5ec0988f
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

### `clojure:temurin-25-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:60b707a31f3168f891270f11ea6bac8951d774720f1a343380dd7a92d712ae2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221924654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6adfd16cd3cc84bfeff67fd93370396a12035840f3098181efa5a1b8c6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:55:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:55:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:55:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:55:18 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:55:18 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:01:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:01:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:01:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:01:24 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:01:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc21d77b997e18aeecc3475421bc8a1eb6cea352b157313ec2aefe45e8757bac`  
		Last Modified: Tue, 17 Mar 2026 02:56:10 GMT  
		Size: 92.3 MB (92256299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80746bca700a5d59188c5a48e17a2b6dd2fad34ba8e52e494b34b2d05a2b9910`  
		Last Modified: Tue, 17 Mar 2026 03:01:42 GMT  
		Size: 81.2 MB (81178732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f70a579dae491eb5672478c6f138963dec60a6c4d1ca4af199254d18cfb494`  
		Last Modified: Tue, 17 Mar 2026 03:01:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303d5ae6eb4c9ce336183870efd60234cbf5d715072747bae39f6a1a923a826d`  
		Last Modified: Tue, 17 Mar 2026 03:01:40 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:abcdf623a58ba76a383b286d3594ce4c90752e9c15996cdc36d8c13e6fd74474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7364672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e209824d1872257b8bc170953246f47fb65cbea5a56219f4ca608d1c6251b7e`

```dockerfile
```

-	Layers:
	-	`sha256:0afe56a0117d2ddd4fa694b40ad118df4ebb94527476618e2a89e2012fda00fb`  
		Last Modified: Tue, 17 Mar 2026 03:01:40 GMT  
		Size: 7.3 MB (7347700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c79fefe9b2409b91bd5d32cb846d93769c13af6c44519feebefbfd1f4b8c8768`  
		Last Modified: Tue, 17 Mar 2026 03:01:40 GMT  
		Size: 17.0 KB (16972 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b173321a8afec6a011d4ce57d97516d80758775f314f424c4b4ded9e661df9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220820689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbce931a2259f43824d7869b465e71c349f8177cda5262d5a1f3957915f6eebe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 03:05:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:05:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:05:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:05:29 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:05:29 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:05:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:05:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:05:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:05:45 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:05:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeae329513ba2056ab9833802db15281e988afba41cfe0447418f7f93d26491`  
		Last Modified: Tue, 17 Mar 2026 03:06:09 GMT  
		Size: 91.3 MB (91288273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313db449c8035a47f1f6bc403de383245ae8b90334874ca29a60175a8273fa1c`  
		Last Modified: Tue, 17 Mar 2026 03:06:08 GMT  
		Size: 81.2 MB (81158343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc39868e13a63f208fd63321de0edb014c644ff8eb7721ad4c2011a57625544e`  
		Last Modified: Tue, 17 Mar 2026 03:06:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e084084eeb10e5cfd810871d2eb5379ddc4fd8d74a6b3a05644b64c16d934444`  
		Last Modified: Tue, 17 Mar 2026 03:06:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:40bb41a5632b54be115f290ffcf94b8c80b56d05d6dccce4855dac0dfc0870a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7371493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c18d0505f898ba207efa72ca4137230d2fe4a757c2ceeb1ee50f9f1dcf99459`

```dockerfile
```

-	Layers:
	-	`sha256:1ffe0ad3ba45452f3b381baf488b9bb3a652c29734d8cce8c1cf3330701945bc`  
		Last Modified: Tue, 17 Mar 2026 03:06:05 GMT  
		Size: 7.4 MB (7353532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43120392f610263f74a33e908296aa2dfca259a27cb4474050e27c74c1972348`  
		Last Modified: Tue, 17 Mar 2026 03:06:05 GMT  
		Size: 18.0 KB (17961 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:b7beffc34bfe40cc153a4e4cc2d9a072b7001ba0dce35f5841dc9660b041b7d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230971108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c124f6cd051a9cc23cc1bbc0f29a4e2588fc69ad6a3c3f237cdaaaf48dc82f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:39:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:39:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:39:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:39:48 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:39:48 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 21:07:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 21:07:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 21:07:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 21:07:37 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 21:07:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375aa8eacf526a2bf938fbc2d4fee75e90900d45e6476502c1338fa7b89cf807`  
		Last Modified: Mon, 09 Mar 2026 20:41:55 GMT  
		Size: 91.6 MB (91632879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7b74684bf768b85dd03b2869338cf265c00fe52c2802044a317223ccf95415`  
		Last Modified: Mon, 09 Mar 2026 21:08:35 GMT  
		Size: 87.0 MB (87000387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27af2fe9a8693464f1749e9cffb5797698e2cebd0280fe8626cbbc3ff2c7f6d9`  
		Last Modified: Mon, 09 Mar 2026 21:08:33 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1695a85255f1960a495b9651b168179b99d25e95e7bce9cc63ea93d17f77837c`  
		Last Modified: Mon, 09 Mar 2026 21:08:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:608872de3d3c76f3429a5523bc09c90deee5563e8c9d648482122451fa6e57f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7353320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989e5d9fc90f87c30e41e0a4ab70c7f5106216d1ace61308dda80eb965fc805e`

```dockerfile
```

-	Layers:
	-	`sha256:615c84c2f8401a1d933a8d3cf270ebe889751db9804bdf5f1d421b0045f381c3`  
		Last Modified: Mon, 09 Mar 2026 21:08:33 GMT  
		Size: 7.3 MB (7336264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e25ce4234c1fe1865f967b9ccc63606b675ad43aad06e9551698a1ebe073ca9`  
		Last Modified: Mon, 09 Mar 2026 21:08:33 GMT  
		Size: 17.1 KB (17056 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:e124b369f76a7940d2535ee113ebe87ce48dbc55f9fa979a1c36a4fdbca742aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215370785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f679a2fa391d159a1fd916ec1b4bcb3be6413a1ee9801ebf0d3bbcffc6f638a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:44:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:44:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:44:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:44:36 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 11:44:36 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 11:45:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 11:45:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 11:45:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 11:45:19 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 11:45:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7dbc3949555449666cc7651209b926019d3fc7f1511f7ebcd8979762b12d59c1`  
		Last Modified: Mon, 16 Mar 2026 21:51:27 GMT  
		Size: 47.1 MB (47147919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb62fc097eaac184da503b941c60f97ec5e455a5301ecef6716aa9c41ac21b33`  
		Last Modified: Tue, 17 Mar 2026 11:46:01 GMT  
		Size: 88.2 MB (88233795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6510f57949c9c8fbced078aac2101f9d9f18a196c82875c7a3fa61bfe121f90`  
		Last Modified: Tue, 17 Mar 2026 11:46:05 GMT  
		Size: 80.0 MB (79988029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec4af12a718341067d14a790190ab5000ba4af16f6c0d908a1200a103d24f62`  
		Last Modified: Tue, 17 Mar 2026 11:46:03 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37be1ce5eda7b8a05210f783bd3cdfe77a3a270f73522beeac78c92c424cc812`  
		Last Modified: Tue, 17 Mar 2026 11:46:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:288ee8c32236467548b4685db80abd9e1d671e14548586c96320cb66fdea5400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7341352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072c639a1e06a38face184d10e1faff8a904d810a2b4b86dcf9ab6af12add735`

```dockerfile
```

-	Layers:
	-	`sha256:a7572f8eb8e0a0c1f2143c5d6751e59e50b5332892bea49d734dc69574146119`  
		Last Modified: Tue, 17 Mar 2026 11:46:03 GMT  
		Size: 7.3 MB (7323581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b6270a6c2d94f4517b820084fe9d76fa311573042dfcac0db2fedd702db633d`  
		Last Modified: Tue, 17 Mar 2026 11:46:02 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json
