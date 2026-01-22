## `clojure:temurin-17-tools-deps-1.12.4.1582-bookworm`

```console
$ docker pull clojure@sha256:fb6a9e6288dac68b0464cd813790d103e8cd28525724715e0c43eb18a49513ac
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

### `clojure:temurin-17-tools-deps-1.12.4.1582-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:860db8dd470880962d48cad165ca134b811fec2fea5363b60ba52a8ac2b6d1e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274475912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc3a6f961c3c8b9ab8cc96e248bf4ea27dda5f23732ecbac289d0c72f40388ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 01:54:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:54:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:54:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:54:26 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:54:26 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:54:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:54:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:54:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 01:54:42 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 01:54:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3a3de769c6c3f72772be58fb98d89eeb34b78e9997149ecc2f83d46978ba2b`  
		Last Modified: Fri, 16 Jan 2026 06:13:16 GMT  
		Size: 144.8 MB (144847946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d3ef3e9c3d17c4748ea6b61c6a1f8b053d42f998ab5712a1a6e06cd7aae054`  
		Last Modified: Fri, 16 Jan 2026 01:55:20 GMT  
		Size: 81.1 MB (81145306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b528fad934b89a627d961a59c0ecfcd1e79d1ecfd9265d5eefedc754e5bcf2`  
		Last Modified: Fri, 16 Jan 2026 01:55:00 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b2ce8a9e90f2e111f4ba12e3b479c0ecd61ff6801a85d443a715f3114af376`  
		Last Modified: Fri, 16 Jan 2026 01:55:10 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:dd1ce072b371766fa3608bcca1b079c65e0ee3b802313694f5efa4fd9784d230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7391313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d52adaab7ccee8e711d2d44de808c248983c105b3099efd4aef69aa324358c`

```dockerfile
```

-	Layers:
	-	`sha256:f2a98eae2e78721054a81db90812bf55fdb994cc0031a8ad39294e85ae6bb6e5`  
		Last Modified: Fri, 16 Jan 2026 04:40:38 GMT  
		Size: 7.4 MB (7375535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44e011d9afabf3a77b228306781b1ad409d1e9c9e5aed958b47bd66d7576a52f`  
		Last Modified: Fri, 16 Jan 2026 01:55:00 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1582-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b1539035185c3ffa7a38e8ebf70dbc3eed3117a8283fa2ae5ad11cae3ea4fd3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.2 MB (273185526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a22a8754401db164c93adedb59fc67a27f793efd3481a6ec43c31cb99273942f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 01:58:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:58:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:58:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:58:20 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:58:20 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:58:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:58:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:58:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 01:58:36 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 01:58:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8076a40dce0e2b88cff100ce251074445349f0cc857434f892eb82bf3135df7e`  
		Last Modified: Fri, 16 Jan 2026 01:59:04 GMT  
		Size: 143.7 MB (143679931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92443a5ce07a51480eb1f72beae83b65c7e2a5e316dde4e6622a3421fd570dc9`  
		Last Modified: Fri, 16 Jan 2026 01:59:03 GMT  
		Size: 81.1 MB (81138480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0f0800bbeb9957ebedae6e21234ef284cbac2c17af55601e9f92d3b58aa181`  
		Last Modified: Fri, 16 Jan 2026 01:59:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4729ea566e86db698afa83677b9aefd5730303bb1c2ed6fb948177af6be3e785`  
		Last Modified: Fri, 16 Jan 2026 01:59:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cf1ef56e2f9a0814e2fac2d447ecffa00a75e545ab6c42cf24fa9c45a145cb96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edca2b6e28acca6dce050c36c34fa454a4e083c8300a00eda9a61053a2f110a9`

```dockerfile
```

-	Layers:
	-	`sha256:ed2b109b857902ac2a818cd82d89e6f2f56e7e8371486102ea69ed3db967210b`  
		Last Modified: Fri, 16 Jan 2026 01:59:00 GMT  
		Size: 7.4 MB (7381298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:666bc72005afc8baf49b408581cfb5410f4c913e4ddfb11e8df156b92bee6496`  
		Last Modified: Fri, 16 Jan 2026 04:40:48 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1582-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:21b4aae28f5605b0df00feb99dfe685885d2ab8e845910c3e2fcd49adce77202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283840039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec4ea5d12f4b4ba5038b4450ba2057d3dcf5c0d1b3879a5497c23fd9b3e518bc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 03:12:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:12:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:12:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:12:06 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 03:12:07 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:20:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 03:20:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 03:20:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:20:08 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:20:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7649ae7dd81da82230511111108bc60a688b861fec794a0460e34e68ea9084`  
		Last Modified: Fri, 16 Jan 2026 03:14:18 GMT  
		Size: 144.5 MB (144524732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1cc496fed1c36f8d66af64156e801ac1737ad6016f464c1f6ba838aa68049d`  
		Last Modified: Fri, 16 Jan 2026 03:21:24 GMT  
		Size: 87.0 MB (86986891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39563d8141d956aaf08bcb6f19529cac0a587dbe0170a366647379f70e36bc16`  
		Last Modified: Fri, 16 Jan 2026 03:21:14 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b93547f483c3aeb06dda5741f18436def48153d1c775941fefff38b18bacd65`  
		Last Modified: Fri, 16 Jan 2026 03:21:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1b61765c81a2478126183ac3cc0308d850310af4398e90249b079001882941cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7396577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903336e6db20f23bbc2d97224f9293abab241afae15215ec38101acbdaa1faf8`

```dockerfile
```

-	Layers:
	-	`sha256:bc65812cc15bb317aa311e72b57a1da30c2edadf80a6bcc0f0f0131320e49a0b`  
		Last Modified: Fri, 16 Jan 2026 04:40:56 GMT  
		Size: 7.4 MB (7380751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9866525218f3bc4bb3e9b44772bd25dee14a94033c8c87125b89327e2917b0e2`  
		Last Modified: Fri, 16 Jan 2026 03:21:06 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1582-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:168ed1e1bb5a9ed76067d1d325853beca3e68d3c1bd16aa9bc487f0df7d34fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (261958515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d866db024a81c97be0e2cbda1c027bf7e91f5f34846ee6ebe87f180476045a5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:15:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:15:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:15:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:15:50 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 15 Jan 2026 23:15:50 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:16:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 15 Jan 2026 23:16:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 15 Jan 2026 23:16:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:16:03 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:16:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:26 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a4e65f91bf8fabfb37d94cb2c3f8147c2abb08a57ec48a145b2bddba56b56d`  
		Last Modified: Thu, 15 Jan 2026 23:17:00 GMT  
		Size: 134.9 MB (134859767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377e17a49b03202ef7a5ba5e9248ec99fe2ad4613f7e0ff512b00dfedc07b8af`  
		Last Modified: Thu, 15 Jan 2026 23:16:49 GMT  
		Size: 80.0 MB (79959275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1855b225fb62fdd93c5384f76dcedeb1dbe44cc82db97777350f5a110b9685f0`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398b7bb38f97c5859ad6d607f908fe8d7a125b01c1e8b3c66f32cae675ce512b`  
		Last Modified: Thu, 15 Jan 2026 23:16:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e86cbc011f2a45038648fd0b668291ae765b9be6f9aa0f717feef5d9aadc461a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7382632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ceb08baaa67ba8f690b6a3f6de76bca67ea307b5ca0f1177bee9ac357d58b0`

```dockerfile
```

-	Layers:
	-	`sha256:3b6764de5e8f4fcd545697bcf38196cad2eb25e06a9c4d773108affe305181ab`  
		Last Modified: Fri, 16 Jan 2026 01:39:03 GMT  
		Size: 7.4 MB (7366854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ee4572293d593f4ab2a8c4269c6ceddf8c1db909d163c15076a1a1c225311a1`  
		Last Modified: Fri, 16 Jan 2026 01:39:04 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json
