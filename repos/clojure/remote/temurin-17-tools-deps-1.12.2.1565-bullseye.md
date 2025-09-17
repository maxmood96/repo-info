## `clojure:temurin-17-tools-deps-1.12.2.1565-bullseye`

```console
$ docker pull clojure@sha256:39e0a3e8f4c34d7fb95369875cf075e9ac2583e4f681d7b61590bfa63da5033f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.2.1565-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5054c5e76db1f3f382e92decd78f60d8af2ab3f142f43fe332072b090ffed6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268006048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3c0b39e7f76f277131a3d4e355c4837f27c5f00fa580bc3e08b32b388c9a7f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eca575a521c17ad1c92bc2c3033f294418b12352aa26df99d8427524538803c`  
		Last Modified: Wed, 17 Sep 2025 13:03:44 GMT  
		Size: 144.7 MB (144693565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b10899f709425b9b303fe86174375fcba2a5c6fea05ee56adce56f2b127fce`  
		Last Modified: Mon, 15 Sep 2025 23:26:58 GMT  
		Size: 69.6 MB (69556043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c26638279ee70860a2f2915cb0681d05996b92fcd5288c985e250cb46992e1`  
		Last Modified: Mon, 15 Sep 2025 23:26:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaec1a2806e90cbc4eecd9c45ec827834f47bff9c0cc50acaaadab8e1f9e44d`  
		Last Modified: Mon, 15 Sep 2025 23:26:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1565-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:099eb2c9fa6e3a5c580c726c532f87546633534d1d8b7bfd3da91ccb61d0a7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7411488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b8127448f44c1ec5e12fae85cde36e7ede29259d5a37edf3127da0e89a51ec`

```dockerfile
```

-	Layers:
	-	`sha256:b58361d8c7cf562d9ad108e4614aed634b21f5a2d1d6ab3a810e24134a197a8b`  
		Last Modified: Tue, 16 Sep 2025 00:38:52 GMT  
		Size: 7.4 MB (7395667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:925de50c741f552208daf6bb38c73f9627e75dca447cf41156c3ab11cdcd8764`  
		Last Modified: Tue, 16 Sep 2025 00:38:53 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.2.1565-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:475b96006ecc404c5977b74299f288af70bc7bcdc639ab9d0b07100645d54c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265475337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8477c05c028dbab18251ef8c25187128df6c48093395d0b34330aa347b7bdf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4435cbc56933d931c16699620c168c24220c5af558c447eead082c60552cd9a5`  
		Last Modified: Mon, 15 Sep 2025 23:26:43 GMT  
		Size: 143.5 MB (143542107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353bc89ef4dcdfce1f01a6a6d043884f806adb8f4b88d039da60e7ad1daedde9`  
		Last Modified: Mon, 15 Sep 2025 23:27:08 GMT  
		Size: 69.7 MB (69683818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c828fd409d686074c5a44ba51140ef984705220283032a8fe9ec82bf60e1631`  
		Last Modified: Mon, 15 Sep 2025 23:27:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24439854a121b5908744aedfadc713c5cdacbb937551fa9cc5710b726b656f28`  
		Last Modified: Mon, 15 Sep 2025 23:27:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1565-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:49f25805faf499105423ae453fa5d3b70b85c6a39a55bd5e4b0a898c3c124fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97e47684cdc1c76de0b16328f07c8645c8cd02f3354626228dd534781b68c8d`

```dockerfile
```

-	Layers:
	-	`sha256:41d63d041155f2bf12a196ec00e7a93b388507ef165cdd20dd3d4116af315ca0`  
		Last Modified: Tue, 16 Sep 2025 00:38:59 GMT  
		Size: 7.4 MB (7400766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66d5d10dc47a788aa5bc0b83645431d03500b097db2d59b0d63a8864475bfcce`  
		Last Modified: Tue, 16 Sep 2025 00:38:59 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
