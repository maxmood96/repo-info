## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:7ebec4e9614fc5522291e09b198eeaeeb18ab7e813722268a3abfe8981649565
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:b2e73cf87b0439674eaac29304a386d2b0459794493473978f4a3df679f1a3a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184199758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1443da4e55361cb3e67ddf25633ab745d6cb5fddcbcf30c5cf72fd1c165bf4`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c3ce72545bfd8e6e453f99b7722afc852ddc83bdca10c5747540ff9e8d6b1a`  
		Last Modified: Wed, 21 May 2025 23:31:40 GMT  
		Size: 54.7 MB (54716179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180893af4ac7a54c2e59f93ee45bfbd168e4ac1f2b0b146db9fb0e913b2fc1de`  
		Last Modified: Wed, 21 May 2025 23:31:40 GMT  
		Size: 81.0 MB (80994691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124bd76731eec45bdb0e6f7599569a7fdcecf02efeb254557346ee94cf537184`  
		Last Modified: Wed, 21 May 2025 23:31:39 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7ceb74ee4a1e4182e3eb9175fbe6ee4a963bfa86b9775e974fca5585aca6d9bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7354368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2fe99d21f20eb29de1e503397862f99f990811f2dcf5b887b322e6adaaf8365`

```dockerfile
```

-	Layers:
	-	`sha256:a8c90df6ccf62f1b8285372c2eeefe663fce08b8015642cc441919763d502b22`  
		Last Modified: Wed, 21 May 2025 23:31:39 GMT  
		Size: 7.3 MB (7340132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:504b1b41f1e27ac6211f3746d3581b2885dbf28efeae954dfe0859fad59f3c0f`  
		Last Modified: Wed, 21 May 2025 23:31:39 GMT  
		Size: 14.2 KB (14236 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:619ef417675a6c2947797e686c5a4f00357247b006a778c5630e7b3e47147efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (183005038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b205cba981cdc83c0d84437d2e24f2d0b3209365fdae06614cabc5c2967e298a`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977d15a1b69807a4fb0ae4b56169568ecd360221a931a02586a1bc6ee3dcf975`  
		Last Modified: Thu, 22 May 2025 07:59:56 GMT  
		Size: 53.8 MB (53830516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6401572bbc974c2799072ab5c8974da9452bdc633a3c943fdca609e3a5f5f224`  
		Last Modified: Thu, 22 May 2025 08:05:00 GMT  
		Size: 80.8 MB (80846697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131a57fb81af3271080d2b5a0f7dbc4bbf0ec6be777ced60f61474264cd879fc`  
		Last Modified: Thu, 22 May 2025 08:04:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8814815905fb18218185876e480859a2ecb8cd676c98bb68d119b40c2c73ac96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7360948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5448dd613662fa8fbd68899bbb21adcb92ffe6e3735417716a72f4dff2b72e7a`

```dockerfile
```

-	Layers:
	-	`sha256:de0a394690a2b35c3ed3bc76860c4cbada69725bebd3bdbb658882a6f5aec6a3`  
		Last Modified: Thu, 22 May 2025 08:04:58 GMT  
		Size: 7.3 MB (7346593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9526dcdc24d93c6eca0a73316a68429186424c6908a735eae2d3efb30d7b0787`  
		Last Modified: Thu, 22 May 2025 08:04:58 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:9acd2b3de0b46d052de8c39e9f2a0d712342b6dcf8f5796bf5981f493bd44347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191301973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eec9c74c33fab7bf0c4c952b4b35d6e842eb7f154e64bec16075e8cdf7bc17d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Mon, 28 Apr 2025 21:21:34 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1503ed161a535170ec0a94cbb44402f797f949590744faaf54bc98204dbe07`  
		Last Modified: Tue, 13 May 2025 17:57:00 GMT  
		Size: 52.2 MB (52167968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9b93a5bde6601edc1437ec21dd5c715013c23ac3a48dfb8bc349f603bca61a`  
		Last Modified: Tue, 13 May 2025 18:08:22 GMT  
		Size: 86.8 MB (86801231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3481bf2c3ac94b7a20e2b726a64ac6fd632cacd4b200ba0a484a81d0c9dc01`  
		Last Modified: Tue, 13 May 2025 18:08:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f9399e9a9f3b74f578e293d6dc87c4811380955d429081776f50ce7bff344bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7314006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226b5b86ed5d37d0168c674d8a3c98c02d7e5148c50148963f2debc3e1b9dd3b`

```dockerfile
```

-	Layers:
	-	`sha256:8a632dffe9ebb1e7a55313f40ee00bb56a436ce59168ba0d991af146fb9dd0bc`  
		Last Modified: Tue, 13 May 2025 18:08:19 GMT  
		Size: 7.3 MB (7299721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:464f049c38f2105512d4ae161dea57f93c0b5e4da94ad0ed53ef247c1da83248`  
		Last Modified: Tue, 13 May 2025 18:08:19 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json
