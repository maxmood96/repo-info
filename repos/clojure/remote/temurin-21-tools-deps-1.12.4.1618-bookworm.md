## `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm`

```console
$ docker pull clojure@sha256:f5e5062723d18e8946e05284a888ee0818fa4a0eca74859f151ccacf2e2bb0cb
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

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:7f55fcf78e588b73c52b97855e0c5f73be0eb5bb7d66d9dd12755558788d30b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.8 MB (287823089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b7b0fc2ae507188e1861d2c0da4802f057e5229689efe93b3da1621e3a583a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:18:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:18:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:18:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:18:07 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:18:07 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:18:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:18:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:18:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:18:22 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:18:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a03dfd688d4f2b1b4ab04df87974290e6a16fd57a1cef2f4623c1dc441b78b0`  
		Last Modified: Fri, 08 May 2026 20:18:46 GMT  
		Size: 158.2 MB (158166923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818dd1f033257e08370e4aa8e91ca6428de7c000a773158c1b12ad306dce13b8`  
		Last Modified: Fri, 08 May 2026 20:18:45 GMT  
		Size: 81.2 MB (81166447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae8c432c89504c51aa68e118771216500d89501aa0fb394377f1558b5811342`  
		Last Modified: Fri, 08 May 2026 20:18:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcde42e8ef945ba3fb243c9f2fb961ce703bd6a7c32c04ef60a97e455c0d580c`  
		Last Modified: Fri, 08 May 2026 20:18:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:38a17e095afe154b4066a7e97801afe8841dcde5c9470f80c902fd02585aec5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7398079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:819f3b4d696f3ae1ef7ee665ed7d8f7713697fb16f7675b4e9956fa8b582dab4`

```dockerfile
```

-	Layers:
	-	`sha256:fcd34f31968bc28161ea0d37b551629cc5e3eeb86c7358782610d46735b3fded`  
		Last Modified: Fri, 08 May 2026 20:18:42 GMT  
		Size: 7.4 MB (7381465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c6578c3f36b352a87b99e4c88dac288ebfbb300d592f24d0e3115f18712a918`  
		Last Modified: Fri, 08 May 2026 20:18:42 GMT  
		Size: 16.6 KB (16614 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:74b21df33a8b27f3dc969896923cd3c74fecf82c6b7d7fe0c109b8f5e695c707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (286010207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32b31d8f3d30626c5b68b0a77a9596fbdce03dea9933b37b658daf32f26582b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:22:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:22:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:22:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:22:23 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:22:23 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:22:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:22:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:22:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:22:38 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:22:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358e50697d6c0f754bc33c2ab7fbe8a9f8fc94156b4253b207a886ee0318b564`  
		Last Modified: Fri, 08 May 2026 20:23:05 GMT  
		Size: 156.5 MB (156461289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1e8c20d2a7d255afc200ef0031cc61be89592c904a1cc84e4fead2906b3ca2`  
		Last Modified: Fri, 08 May 2026 20:23:04 GMT  
		Size: 81.2 MB (81174722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fab3b8d31ecc99d89d521372c47cd66903ce853ca7faf3d7c7f70fb3ae5c2d5`  
		Last Modified: Fri, 08 May 2026 20:23:00 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e878c587756c1bae954374c9ebcea29731377c98eb903e6d777ad00eb42687`  
		Last Modified: Fri, 08 May 2026 20:23:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d39c31b25faa6dd1d5061fed000bab04e5c5a65d278b81a9a3d961c48ced4569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7404010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09de8d18c76ece475f0b4d1470650013f1e1170ae3ef83a91a06dba721bc6ec5`

```dockerfile
```

-	Layers:
	-	`sha256:a9379dee5c8bfffe5088ebeb1fc79954fabac6a4cddd5bf56e7bf92f73d15a1a`  
		Last Modified: Fri, 08 May 2026 20:23:01 GMT  
		Size: 7.4 MB (7387252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aaaad7ad6cb2313f7022aa462ace5442f776e6fdd212d332ec6e76eca1a8193`  
		Last Modified: Fri, 08 May 2026 20:23:00 GMT  
		Size: 16.8 KB (16758 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:9d1c66697ec608f07ea28dcced3045b4e24468a5feba842de0ab2546b20dd58c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297685170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14f542482474e69fbd70c6af86a045b26cefce486e81d67d0b62423a405da85`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 01:35:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:35:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:35:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:35:27 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 01:35:27 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:40:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 01:40:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 01:40:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:40:06 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:40:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0398f5f2459bce57485cbf20c7c00c0cc4acd23743ed54d0ac36f4b1a739a3a`  
		Last Modified: Fri, 08 May 2026 01:36:55 GMT  
		Size: 158.3 MB (158343239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8e0b4789351557860694b46272535c93117f7a4691328b094ce2686e9cf5a4`  
		Last Modified: Fri, 08 May 2026 01:40:43 GMT  
		Size: 87.0 MB (87004156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaba1804922b140c687efd6ac4549912e9bd9bc330683f54b12c24909bb597d`  
		Last Modified: Fri, 08 May 2026 01:40:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d0ecef2f15021651346f5987602abf46f737c2ec4425f7706698f9b793427e`  
		Last Modified: Fri, 08 May 2026 01:40:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:227679f74ffb57a162228e77838bb7c4b11215233033c07053046c5c2f9ca280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651970740fc77dfc0ac1c0090a9d4f5d185e143094a1444327c233b0d4e00902`

```dockerfile
```

-	Layers:
	-	`sha256:d0c209e45ae75c7b9991561c4472184b0cd6a9fd0946437638689394730fd0a1`  
		Last Modified: Fri, 08 May 2026 01:40:41 GMT  
		Size: 7.4 MB (7386693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e361a8246910435e103755fa5cbf2158ee2c284078498cbef639e138d42b3a20`  
		Last Modified: Fri, 08 May 2026 01:40:40 GMT  
		Size: 16.7 KB (16676 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:3851199d4617ed09bd3294d93e4af2e11cdc733be50ab1b4a2ffa39fe6683444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274517364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b65245007dea289ea00782e524173484b70b7f6089162243fd894c02e907ff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:16:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:16:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:16:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:16:57 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 22:16:57 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:18:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 22:18:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 22:18:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:18:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:18:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9927e4ebf9213259a4ef5a3246c16010c9dc3952f2cdaf14171591311e8b7dc5`  
		Last Modified: Fri, 08 May 2026 22:17:39 GMT  
		Size: 147.4 MB (147388334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08ee6f4862093670ad6a814dad57d34d8c299d1f9e275fa5c2638043120593d`  
		Last Modified: Fri, 08 May 2026 22:18:38 GMT  
		Size: 80.0 MB (79979965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5476e9e170c7b47cc8d18376c70c8562aadd02b557d479abfab544c9fe5fc1a1`  
		Last Modified: Fri, 08 May 2026 22:18:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a4bd538b55e4c702816611e8eb792a8c43ff0ca85b702698508be114bad336`  
		Last Modified: Fri, 08 May 2026 22:18:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:173fced78b9baeb03bb74726227359fc32d6667565f8eca4c83d9b27d9bc1025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8bb355be47bf6b831e18216a52223d95c2a081de51a172a7c3416849c81cf98`

```dockerfile
```

-	Layers:
	-	`sha256:b81d2bdb6ac08a80c2f4b1917421b68f9f80bd2c9fc45586075e1c29c0f73066`  
		Last Modified: Fri, 08 May 2026 22:18:36 GMT  
		Size: 7.4 MB (7372784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65d549508a37063bbc98f4cc9d8cb0d93aaad42ad0b0e6bd9212ed1da3e8a1fe`  
		Last Modified: Fri, 08 May 2026 22:18:36 GMT  
		Size: 15.7 KB (15661 bytes)  
		MIME: application/vnd.in-toto+json
