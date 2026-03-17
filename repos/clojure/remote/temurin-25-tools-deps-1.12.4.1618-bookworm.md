## `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm`

```console
$ docker pull clojure@sha256:07ed6c7922fa939e961e434633b9780fa0bede3a14703a0dcd3b5e6a9ecae5b4
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

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm` - linux; amd64

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

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

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

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

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

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:aa474b5618d6754a8095590f92c1fa2a8f84907c3025e8b4612f7d0c78e3273e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230970522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5634f2b6422339c13f5d5938c9b4db0e2afea2a2fb8e243ab61ecbdb2d289fec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:03:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:03:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:03:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:03:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:03:56 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:48:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:48:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:48:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:48:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:48:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c072e92b832614e86d956c6381c6b7617944feae3193ea5691e9506870844136`  
		Last Modified: Mon, 16 Mar 2026 21:51:19 GMT  
		Size: 52.3 MB (52336698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81438db6b066b5319caf43fdad1d2cd4324d06132f04193db065dad00c8bc101`  
		Last Modified: Tue, 17 Mar 2026 18:06:02 GMT  
		Size: 91.6 MB (91632940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f167dbcba53acc80d6fd06080209eb579be2e3e166ec940ec6d1b922f4f84b`  
		Last Modified: Tue, 17 Mar 2026 18:48:46 GMT  
		Size: 87.0 MB (86999842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c7f948fcae1f290e78be61d0db05c77df181bf7a890966c63319c49e78cbd5`  
		Last Modified: Tue, 17 Mar 2026 18:48:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1302b136cdb8027be4c862b42c0f35ff66bfd8a5aecd76c3c75778e5c60ae7b5`  
		Last Modified: Tue, 17 Mar 2026 18:48:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3b018df7759638fb6108a25df28b5a812f51647b7e17f292bfd0c4a15178212a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7354118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d394e2c2c20d4ed9e34618528e3124b8a5d0dca1f16925c0616cd094b9d99ba`

```dockerfile
```

-	Layers:
	-	`sha256:a8fbc374c6a0280bb2807ed0d3040ae8b06152c2b20407bbed6d7863357678fd`  
		Last Modified: Tue, 17 Mar 2026 18:48:44 GMT  
		Size: 7.3 MB (7336264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4b7e8dfd598986ac85e931013e91e800bf73374a9b1414a8d7f278ca3c30861`  
		Last Modified: Tue, 17 Mar 2026 18:48:44 GMT  
		Size: 17.9 KB (17854 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm` - linux; s390x

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

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

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
