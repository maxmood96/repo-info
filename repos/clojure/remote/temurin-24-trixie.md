## `clojure:temurin-24-trixie`

```console
$ docker pull clojure@sha256:decacba698cb01cfad466c78e57e43d2cfb4236c85366bba7e27d2b10f2cf56f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-24-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:5e1dfad9f9f4c4af0c1bef43e0b37d683de8198ed1db41833164913dae9627e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.5 MB (224461590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd021eb3f8df5dca3eb1fb1a80b142678d315a04793f35242f5493adad27f70`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1745798400'
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
	-	`sha256:f8c8542523ef5c08ca9bd5ab7d7265d12930a45ccc7c8364e909fde03c894479`  
		Last Modified: Mon, 28 Apr 2025 21:08:35 GMT  
		Size: 49.2 MB (49248239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543a4cc9777670296712f6a9872398e4d4ea99fbbc7cd6c8fc0c4b43902d72ce`  
		Last Modified: Tue, 13 May 2025 17:53:57 GMT  
		Size: 90.0 MB (89952000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4c43acec6a5a14bcf292c352792edda204cbfef0daed639326286a116e4b6c`  
		Last Modified: Tue, 13 May 2025 17:53:57 GMT  
		Size: 85.3 MB (85260312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7270013e05b5cac053745640ed655b033f02261e8fa2683f2b006c91f73eb18e`  
		Last Modified: Tue, 13 May 2025 17:53:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be32e4c36379a1cb8bd32c0dc6565db5837d4835e62a64254753212717467358`  
		Last Modified: Tue, 13 May 2025 17:53:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:124a9e901c879b014e8e544344ee9fedd861c76ceaeea49c8c2787fe4e45ddc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7235605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543dc3ec3d785bc375b366a22d221de94520ac328dbdab1d9b4e3daa81d9bca2`

```dockerfile
```

-	Layers:
	-	`sha256:e3bf3a8cedabe4cdb2dd07ca0297c94f776df1fb955757263d3b99e3d9d0f8a2`  
		Last Modified: Tue, 13 May 2025 17:53:55 GMT  
		Size: 7.2 MB (7219815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa1f860a64e37173d89d6174d6a6ad1de31ea82b335412e8d94356c7f907a646`  
		Last Modified: Tue, 13 May 2025 17:53:55 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c6f9283832c1d61df310cffec350f24396a16a2001d2b859c65d955a03c2231e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223888708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c33f1ad1a9b21769d2871bf35907f5736ae050ce7a0ec6eb0d352435c5874db`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
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
	-	`sha256:288a1cecb0ea762427d39b072c1ca965d193e927e04da652f7b21eb12e9b2acd`  
		Last Modified: Mon, 28 Apr 2025 21:23:23 GMT  
		Size: 49.6 MB (49624118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd3f46f8509be2e8269dbababafabf79f4ab8c9edb9b2e5e44756fabe24b705`  
		Last Modified: Tue, 13 May 2025 18:08:31 GMT  
		Size: 89.1 MB (89091184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423c8aa892fe9ff225a339615390a338b2061d7647d02f39c6e49756f80f9627`  
		Last Modified: Tue, 13 May 2025 18:10:41 GMT  
		Size: 85.2 MB (85172361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9235a887f968cf63713413b1d005ec7402acab31935306531d5172504b16193c`  
		Last Modified: Tue, 13 May 2025 18:10:39 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8f23d04e9cefce7666521476d866892cd38837a9bb30f867bd6975481ae525`  
		Last Modified: Tue, 13 May 2025 18:10:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9f149abd302d7c820443711f36987af4a10745fb734940db576f6771100094e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7242750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39319440ce21fbe0e698569477489300418fadaa8e2470d528ea52776857c184`

```dockerfile
```

-	Layers:
	-	`sha256:d5cad05005a40077865a1314d75ae147a5030a8e78f9cb20a8419e2b76e72ad2`  
		Last Modified: Tue, 13 May 2025 18:10:39 GMT  
		Size: 7.2 MB (7226842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4b168cbf6f6afdcecd2277de5d15dacbcae1a14020a5422e2d02e378dd0bae6`  
		Last Modified: Tue, 13 May 2025 18:10:38 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:5b09772f0891522601d3baa734770454f648245a46825e3ef105ad681ed41408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233735597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8e928e2f5c30bb6f6d7e8ffa8ba0ceb8a181ee823b5f30567e7d23fd833b44`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
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
	-	`sha256:03ebb30bb37cd398ea8ab1a268c301664089cf5a54d23466e4338782afb5f9cf`  
		Last Modified: Mon, 28 Apr 2025 21:25:28 GMT  
		Size: 53.1 MB (53072552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674c4a3f65801b611fa6629a1a146324b962fe77e75ddd0e9c3fd83f2ba4a1ef`  
		Last Modified: Tue, 13 May 2025 19:35:26 GMT  
		Size: 89.9 MB (89920243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231a0d0b2f6e1e47fabfe89872bcb0dcff48237c5967fc62ecfa5fe53ab4443b`  
		Last Modified: Tue, 13 May 2025 19:42:56 GMT  
		Size: 90.7 MB (90741760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8e9970cda08dc8136e61bfb90f2777eb09595e186891094447a9ba8766cdc2`  
		Last Modified: Tue, 13 May 2025 19:42:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b91ead90f74a033035f062421c02352d9ae129130575edd5830f6a93c575448`  
		Last Modified: Tue, 13 May 2025 19:42:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:23c332d9b5fa51e6e3c6ede4783f1ab458289b02183bf2223b798a8635200155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7241204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa84c7c1438b500f8fe17522cf05cf8395724ccf0fdca54ef589b82e29791e97`

```dockerfile
```

-	Layers:
	-	`sha256:771b6e028b879c57fb05cfcaae23c0cbc65e27f62ac4c4c2cbd68aac324d7767`  
		Last Modified: Tue, 13 May 2025 19:42:54 GMT  
		Size: 7.2 MB (7225366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93fe426c6a4e2d302c2ff2e2c86615dacf19bb6534976099710d0b7ed9803167`  
		Last Modified: Tue, 13 May 2025 19:42:53 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:157d3a8a5edb77db1f480ebbf2dd9b9ed2fac9d8a1ce9523114b94b443759530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219581721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4e9d525a51cf33b38a832562a3322b5b1e047a6bce825481ab3fa5bbb93964`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1745798400'
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
	-	`sha256:3e87a3ef7201dacec1e06fe511cdfaa924c5bf89f4f022c082b59ff14eb11b6f`  
		Last Modified: Mon, 28 Apr 2025 21:16:24 GMT  
		Size: 47.7 MB (47740349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99662c43e3a581efd36df584d38d7972e97cb91f2bf0f9bb2b940995eb26cfe`  
		Last Modified: Tue, 13 May 2025 19:35:31 GMT  
		Size: 87.6 MB (87622197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3d1114d2ee0317735846be0c2dc14c89bc67328f634ea28d7bed89d604e7b0`  
		Last Modified: Tue, 13 May 2025 19:57:07 GMT  
		Size: 84.2 MB (84218135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf9aeb7c81aa03799d982506a104e4481e7121290af781b541c937ca0f651bc`  
		Last Modified: Tue, 13 May 2025 19:56:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5013711b695790b07bae80a6f395073c8ca88de24d35209ce238ab1a81c74bd`  
		Last Modified: Tue, 13 May 2025 19:56:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:eb407adef8421f3fe02726f7b5f8ea9c66a9d982a84038d47c2c2ce9bb4479ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7223677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:091b51fd501b6a72809215a3feb59ff46b10d8ab5ea6753cb83377bd560cc2fa`

```dockerfile
```

-	Layers:
	-	`sha256:1e257f34f802fd065a1b751409aa7201f8358ff14c72bc472205a3156d22886e`  
		Last Modified: Tue, 13 May 2025 19:56:55 GMT  
		Size: 7.2 MB (7207839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2759584605110dd9e929b540fbca724e8c96567e271c09d5890d7dd621948450`  
		Last Modified: Tue, 13 May 2025 19:56:54 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:29e1dbb9dd26db9a2a1a419c2b55f818ce871328d6704d4edadac319906191e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220873766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:340da301641abaaf95fe647165115607457a837875f63bfafa5b4d4b7d821d45`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1745798400'
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
	-	`sha256:e1ec3b1570f7d822c5a6aa013529484429ad99bde8495d827b56c3603992fd3c`  
		Last Modified: Mon, 28 Apr 2025 21:11:06 GMT  
		Size: 49.3 MB (49316646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3caa6d95ac79148cb05f8ba767df9727490450376fab4c523d1cb8c539ceef`  
		Last Modified: Tue, 13 May 2025 18:38:36 GMT  
		Size: 85.2 MB (85216757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f7667d085815f3d53f86c552083618334cd84fbbcfc8a3529c591d5bca5ebd`  
		Last Modified: Tue, 13 May 2025 18:44:25 GMT  
		Size: 86.3 MB (86339323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13173f3c7495e6d1ae7a79b0ec016dc77ee6c4060a1d6d91117e67c1a015b80`  
		Last Modified: Tue, 13 May 2025 18:44:24 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e6e8aab3e416c1d338247fa6a3ed1f7e253644f505f11b0e81acfecd7415ab`  
		Last Modified: Tue, 13 May 2025 18:44:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:763cf4add4d8963f5b32854ba5dda1626d26bb436fcb560f13b1a8422b522a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7234075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45220c1d5d17058064d6f38178eaf8b34eea4d3dee66265c595266a231ad387`

```dockerfile
```

-	Layers:
	-	`sha256:8f055baccd1d9a935109a77c3141e78027be24f5eabddc261f767ed0be12ecc5`  
		Last Modified: Tue, 13 May 2025 18:44:24 GMT  
		Size: 7.2 MB (7218285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c993cebe7486e1747b7aeed36ae4ee5ddd0ccd6afff3fade4629af0050d3f15`  
		Last Modified: Tue, 13 May 2025 18:44:23 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json
