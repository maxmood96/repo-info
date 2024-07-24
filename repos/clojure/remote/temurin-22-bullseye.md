## `clojure:temurin-22-bullseye`

```console
$ docker pull clojure@sha256:68acba1e38744475c0be9320fd7303315b8c7e558652fb4eb1490f1188229f74
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7ead153635a4ef401b9b658605c53d902b100cb21b5660f56c7ebc7b1cc7da6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280588342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b026f4844279200aa4460de89f8169ab049277c9919f54a1a9c44ad85ab705`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3553ca1371a3338a2eb9cb7b149c25ae4c0e11b9bb56ec7bc9de3ea53c824ce6`  
		Last Modified: Wed, 24 Jul 2024 03:04:43 GMT  
		Size: 156.5 MB (156481648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559d5526ce722977e38896141b1f4734bf29fe29f15ac5730b50ae1480a26d69`  
		Last Modified: Wed, 24 Jul 2024 03:04:41 GMT  
		Size: 69.0 MB (69021076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edab1737aa1f1f4d60aaeedf8a59b7c091338c32e972a652f908d1afefc2635`  
		Last Modified: Wed, 24 Jul 2024 03:04:39 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b914b36dc3870ef397a20aca7fb7e7d123d435769ce886777c4a6460c8a04a`  
		Last Modified: Wed, 24 Jul 2024 03:04:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:82a1ea105a3a8db8c098427bcb4e68643d2018635da5b1da76197b5ffa8967af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7055778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:587f667f891ba72f9b3904a6b632b99fe5afc4b8463d43e0efe98a717659e6ea`

```dockerfile
```

-	Layers:
	-	`sha256:11c72f0a5685499dd7453931ef652a684b0d4281a7cf755958143a30740749a6`  
		Last Modified: Wed, 24 Jul 2024 03:04:39 GMT  
		Size: 7.0 MB (7040338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eccf15171c4169d375304478a259e2e4aaf1e934d6c05f1b1d0c14de5abf1ff`  
		Last Modified: Wed, 24 Jul 2024 03:04:38 GMT  
		Size: 15.4 KB (15440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7c21c30e6b172f1eee342f224536298a5a52ff95712de762ed05cfef54e41d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 MB (277602874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924ab462831975a2b03c24548b1a4fa09ff6098aadef702cde22739f2806bc98`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71e59cd424eb028670dad655354139def6754ab2abad36b82fa28bd50a1641c`  
		Last Modified: Tue, 23 Jul 2024 12:55:57 GMT  
		Size: 154.7 MB (154738008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9518a803c3e0ff148f79bcca61312f968e076aa9f2264a60995c42d3d3afec`  
		Last Modified: Tue, 23 Jul 2024 13:02:25 GMT  
		Size: 69.1 MB (69133837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e7158c50660e4c8780a8cc0e23e238b5c434b325af431840f8e3550bd7364e`  
		Last Modified: Tue, 23 Jul 2024 13:02:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b323bf29abb7427f20bddd5a04684e82447acf2c3570887ebe5f9df22c5e93`  
		Last Modified: Tue, 23 Jul 2024 13:02:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c5abc1654786c65b356295ab20db2280433c817c9b95588f3fbd2d5df972937d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7062035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dae8da101328e66597666ec33af271d92eae58e54dbf9b309a671a6cce0bcfc`

```dockerfile
```

-	Layers:
	-	`sha256:508ee49a5ff6f89fa51cd5d4c7939cad4befac0f99a2f0fc75e4b38fcea7ca57`  
		Last Modified: Tue, 23 Jul 2024 13:02:23 GMT  
		Size: 7.0 MB (7046060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e4ce65d725c46f7608ad31ad406003797922485dae4c5a96843ebc07331caf6`  
		Last Modified: Tue, 23 Jul 2024 13:02:22 GMT  
		Size: 16.0 KB (15975 bytes)  
		MIME: application/vnd.in-toto+json
