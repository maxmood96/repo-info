## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:445da7db31a14831da3bf1b367d9247baf7c61753e6c34a5b5a43fed1012ef9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

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

### `clojure:temurin-8-bookworm` - unknown; unknown

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

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-8-bookworm` - unknown; unknown

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

### `clojure:temurin-8-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:a128fcdff377495b00a2df5f14d0fec6aabc2d172c1585dae664dba41e7e85ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191310838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da12bf45df5325b773bb742866e7510572782e7c8570795bc2539bec6aed00a`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38af18b48c8141a93586323596a3c021221957a6728fb6f0d4cd0cbb115e60e6`  
		Last Modified: Thu, 22 May 2025 10:37:46 GMT  
		Size: 52.2 MB (52167962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b536d7977d58e53464b3fa2f1c37789c7d7336caefd8523ea27954a4459145`  
		Last Modified: Thu, 22 May 2025 10:50:34 GMT  
		Size: 86.8 MB (86810614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7072d6759830867adb42dfa695f1962d6d62cbe7b3b47677b81d86ba0c11dd37`  
		Last Modified: Thu, 22 May 2025 10:50:26 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4e254011df227f9f25029ceab78be8c6d7a2f9677e5a9eb57472c421756d761d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7360214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489427b00a332c1d4344bca61c5e10a555771e75a17115805ef88152d9c002ff`

```dockerfile
```

-	Layers:
	-	`sha256:377da4bcc792ebf55248a0a6c04d058d63cf83d78d9b2338ebb9928b8319bbbf`  
		Last Modified: Thu, 22 May 2025 10:50:26 GMT  
		Size: 7.3 MB (7345929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f63a06684e42cf7b318320a2e19096e1fa6833c0ff62b40263bc45e44adf2872`  
		Last Modified: Thu, 22 May 2025 10:50:26 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json
