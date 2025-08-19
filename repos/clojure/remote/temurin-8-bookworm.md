## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:99100c00612e5a8c65886429dc39ed0991513f294aac96694a8a2ed71b9a2c81
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
$ docker pull clojure@sha256:be155cc23868e8841e9a64ed26c7b1b844a26409fb4bdf2557ef069954504dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184268961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9598610b1b99b8bf05cd9946e5c1bb6f77372826b515c6f804904bb0942ae210`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5b5e12d09730ede38f1aeb53ce804273c03a7bdee8d7f8f56c94bf8761a955`  
		Last Modified: Tue, 19 Aug 2025 02:47:54 GMT  
		Size: 54.7 MB (54731347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87002dd0cd2512b9b46b3f95a895ba7add6d3e9a94a6298671d5eae456b7e94`  
		Last Modified: Tue, 19 Aug 2025 02:47:58 GMT  
		Size: 81.0 MB (81042457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3475e457808287fd2af4bcb667f7cb6a87a730a38e501a71baa2d5000d31e7`  
		Last Modified: Mon, 18 Aug 2025 17:15:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b447ec4965edab1ee6dc935159d6d2b88d686ea97785ee24dec5f6dcf88b4374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7504144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8427e52073165f6bc6abff4a325f37d9d7de913bf1245c9d7e4b34a5b5545c8`

```dockerfile
```

-	Layers:
	-	`sha256:eb1ff479e676df9959ca027abc13479b2257b5d78855b49deee2be78370cbc8b`  
		Last Modified: Mon, 18 Aug 2025 18:44:28 GMT  
		Size: 7.5 MB (7489907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8695d8f1eabbed1342f8970e90b454645e53b48b575e28d6f472513ae589bc97`  
		Last Modified: Mon, 18 Aug 2025 18:44:29 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a50dca425d013b9e711eb3a18986ea0e4c73eb5c981ae3d371518d234df40f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183092167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad99e45113339d8e39a2372459768dfc2df8acc78913e1fcd80a2cba4e3d8cc`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab8e03733fa4cd230f3c654cf2c9de160d54ba2f0b7af6f920b3c8ffe594231`  
		Last Modified: Mon, 18 Aug 2025 16:52:49 GMT  
		Size: 53.8 MB (53835608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1338ae4865b0f08028fbb4624bfc9e33a259423b80ef9b0f6c09bb9ac228cfdf`  
		Last Modified: Mon, 18 Aug 2025 16:52:58 GMT  
		Size: 80.9 MB (80913464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cad8f361b707faf6b9c518ab3b31061e4ecb8b36ed34468dfbe8addaa8b9568`  
		Last Modified: Mon, 18 Aug 2025 16:53:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:60412f091ccbf9e8b73d4b11d3090a8b12fb90481fe87d497beaf696bcfff734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f129a523b17d001019cf40ccd9f06f6660588f0218e044c62365fcba8201687e`

```dockerfile
```

-	Layers:
	-	`sha256:4d64e3504d76413ab64dcbc403a06cb89152d9fcda0159f5b5b35e35b8b44c40`  
		Last Modified: Mon, 18 Aug 2025 18:44:37 GMT  
		Size: 7.5 MB (7496368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d970958d2f7912cf540bec0c044cbea99eb5c32f5bb99b30ee18296a3f1382b7`  
		Last Modified: Mon, 18 Aug 2025 18:44:38 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:09224df8b18383a0dab4f378a3cdfbe448526da889f7644657a8215e53311738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191372964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6364f131ff6507a375039d53080021a98908bdf759573eaccf8c9bafe4be00`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47051cd5c75ec10709ec504d89b39f72c1348ec4054ca49be83a8093cd36b3e5`  
		Last Modified: Mon, 18 Aug 2025 16:58:10 GMT  
		Size: 52.2 MB (52165394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb40713e6441c10e5ffab00f01c504442ae49457eddd269b72336380d2c21fa`  
		Last Modified: Mon, 18 Aug 2025 16:58:16 GMT  
		Size: 86.9 MB (86868845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301aad2d9d26921af9e31c40ac149e6a22bd59dd2cec810a65a13fc42b3fc5bd`  
		Last Modified: Mon, 18 Aug 2025 16:58:00 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:95721c0599acab09237859aff63d89476a12eb278cfc3c2d30df5863142f3583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee018d1b1e1d1b9b0b828ee2d6c58c9ca25a7246464b88774f3460218f4b2ca8`

```dockerfile
```

-	Layers:
	-	`sha256:4c2839d4b81445aa39c8580d388293da0c892cbe62a68b47dba9915c5084f714`  
		Last Modified: Mon, 18 Aug 2025 18:44:46 GMT  
		Size: 7.5 MB (7495704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba9cc6f551c08cd647161b5b70af3be4ec728d73506e5843438e8bf2eee79274`  
		Last Modified: Mon, 18 Aug 2025 18:44:47 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json
