## `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm`

```console
$ docker pull clojure@sha256:f2a0c4b7ca0803658fec7c2753fd155c9b10b9c113ffa24d9cf9adcb0a61f962
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:7f1b222bea2aa277f9378594071e8b68c7efbc15f4e8143874aa798610914933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219608932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d154581d7fb1d2d884ccab7c798be929167f5bd3e201d66c382fb0c643ec5e6d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8416f29fca1026c5c7a3c8384a49ce4c6feefccc6be86dab25a49668aefcf36`  
		Last Modified: Tue, 26 Aug 2025 17:28:26 GMT  
		Size: 90.0 MB (89975231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c416c56c3821e4225c15e412c3a7eebb773ded0d06efffa1af2005483cf5fcee`  
		Last Modified: Tue, 26 Aug 2025 17:28:24 GMT  
		Size: 81.1 MB (81138149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26217b35c174da13aef85779b2879a611777a364e7d39a650be6ce32070b9236`  
		Last Modified: Tue, 26 Aug 2025 17:28:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460217683d1721f87bfbacf783ad0a7153cabbed702427ec4cc7e7c200ff3e61`  
		Last Modified: Tue, 26 Aug 2025 18:19:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b1ad727e9819f0ec9551d785c08bf195ac6cd23f62e9454d2a74f87ebba74716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7336126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3998bbcb8777bf4615f0791dd6598089f691c2e8568947e5b49e4f7249b413`

```dockerfile
```

-	Layers:
	-	`sha256:89a0f8f9b5aaee86626e8316480b054f1575d390eef67d9f83eda0d3c413c9b9`  
		Last Modified: Tue, 26 Aug 2025 18:41:50 GMT  
		Size: 7.3 MB (7319629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66ca987a8666f31d7f50cd6026ecb74911592439511ca20f5e464bc47201d9da`  
		Last Modified: Tue, 26 Aug 2025 18:41:51 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e2804e146e7fd96b15154c2a29aa9e25cd9c6da6dfea0058b5b24993ba90cbc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218445270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28654b94c7a258513b1727bc164053c8709e7f578f803dc1d3ce8488df30cbb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46c4617dcda5b8cbce800f96abfaa1b7d06f73a3bf88c2b640e3d1664a828d8`  
		Last Modified: Mon, 18 Aug 2025 17:20:17 GMT  
		Size: 89.1 MB (89092502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f632898ee1f055e57d855581c65deaf37388595362631418f064663b8c93405b`  
		Last Modified: Tue, 26 Aug 2025 17:54:49 GMT  
		Size: 81.0 MB (81009276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca9bbffc5d88d7faf7bfabe7e6186d442ae0d7d9e3741849e01ae36f7fc5daf`  
		Last Modified: Tue, 26 Aug 2025 17:54:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a777dcde13998d0e99ff5a65a6a6526abb35b6bf9635c68eebe8f954c9cfd2e`  
		Last Modified: Tue, 26 Aug 2025 17:59:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7cd7ab3be020ba0ca3fd4cc907b00e3cae29bad2a5d247fd2c008bcf39360c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fee52ea83703afe917fef87b2046448c2685ed499b00f9a4dbbb2b6ef57eb91`

```dockerfile
```

-	Layers:
	-	`sha256:dc125ff55deb7137658c3540f893130ecfc9da80a02c665faf9d1177e51b05da`  
		Last Modified: Tue, 26 Aug 2025 18:41:58 GMT  
		Size: 7.3 MB (7325413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cfaaf5bcae7e706512d2ea39451b4e6626cbeaafb3dd9fca56697cf85321b22`  
		Last Modified: Tue, 26 Aug 2025 18:41:59 GMT  
		Size: 16.6 KB (16640 bytes)  
		MIME: application/vnd.in-toto+json
