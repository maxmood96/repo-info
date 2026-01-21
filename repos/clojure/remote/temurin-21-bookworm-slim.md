## `clojure:temurin-21-bookworm-slim`

```console
$ docker pull clojure@sha256:d10f501dfdbb5e647c79de645f47cc4147cb474a2e7b4730fc5d2b0869a50220
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

### `clojure:temurin-21-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9157af188b7205e69c0e8692328b51d617d2520289c301fc9826fc5ecfbd40a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255732676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f5c7a9925d1261a7dcba4b9039876d3973aa369807e05b25e5d87ca69a04b3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 01:57:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:57:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:57:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:57:31 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:57:31 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:00:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:00:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:00:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:00:22 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:00:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101829ceb6ae1a6d9354db0e5b0710541992e4210099884a21dd18c83c53dc78`  
		Last Modified: Fri, 16 Jan 2026 05:10:26 GMT  
		Size: 157.8 MB (157826055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51d0ce00e6fa8a6f97a38b2844f993622872b6943136791e3fe07f4eade50b6`  
		Last Modified: Fri, 16 Jan 2026 02:00:50 GMT  
		Size: 69.7 MB (69677008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ef57aee6b9bc9618c00df6640059a3e51d2f28f2cf5465775c881e936d6d53`  
		Last Modified: Fri, 16 Jan 2026 02:00:38 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee743f258d595b81fd682498a3b93c6de32be636a38124dd1b09c2654dd93dc`  
		Last Modified: Fri, 16 Jan 2026 02:00:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f293cac9c0eb413f26a7e9f47383054cbf8f63a77741b5329ea5e7cd905480f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8db7b3d7d9e82d62a59cc2cc2b435c0b5a399a69475e77dcf9d3eb1808c764`

```dockerfile
```

-	Layers:
	-	`sha256:759b789bce424196cc209421865377696b5c9d5bd3354085137bb75b4e5bf582`  
		Last Modified: Fri, 16 Jan 2026 04:45:13 GMT  
		Size: 5.1 MB (5116502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:070825ad420c76cca8c963b81c8798fbf32dbe5b6ffffac18f9411e79ec5ccbe`  
		Last Modified: Fri, 16 Jan 2026 02:00:40 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:766105c1721fd5301b4bd6d04542b7cfde00c1c9e0f93fbaae8cf94f57f62f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253889306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6418d632d6bf2ac3d89df6d579939e9296905583a396876aefd2825fc3a807`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 02:04:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:04:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:04:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:04:47 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:04:47 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:05:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:05:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:05:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:05:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:05:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a51816fab832ced69c3beef13d9d3a9e8d87563fc9ca78fde1ff3f0b1336ff1`  
		Last Modified: Fri, 16 Jan 2026 02:05:29 GMT  
		Size: 156.1 MB (156107670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460b448feaaefedec3711d15f4dab898300244917c305d7f6fae7df59d3dfe70`  
		Last Modified: Fri, 16 Jan 2026 02:05:28 GMT  
		Size: 69.7 MB (69672707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d29a4f001c3f8f4bc3d6abdb7d728ec00e4ec4c313c0d9f74f18bc86470831`  
		Last Modified: Fri, 16 Jan 2026 02:05:25 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33508d98602709df1ef89b8d646934a381a151fd11459adcd63329e2739c393`  
		Last Modified: Fri, 16 Jan 2026 02:05:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eb9ae44591c6d46132505d5edce283a5a0ebd4d3628fe84819515f5fa0e9767b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f32a058d49092b242290cd82628f45b5ac93720107a19adf4f90fca6b4a9677`

```dockerfile
```

-	Layers:
	-	`sha256:46675d6e9b18c360ec4ab34c1696796c9ab07f68432901af604191c0a1198d2b`  
		Last Modified: Fri, 16 Jan 2026 04:45:18 GMT  
		Size: 5.1 MB (5122263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58ba556c391334abe756d22e7e341970d55dffafbf2262f0455b0bd6f8cc0293`  
		Last Modified: Fri, 16 Jan 2026 04:45:19 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:cdf98cea490d7543db3936800dfb22a782f4dbb161dd45475fd855e3024accab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265525533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e3355c714194c57977e60941acd91c73cdd37c0ee8bdd0c8ae61f3fc124a7e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 03:27:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:27:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:27:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:27:00 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 03:27:02 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:36:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 03:36:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 03:36:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:36:19 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:36:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:24 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5094bf46310c703a83629a08ef35e481705d22cf663c8418d08e57c629ca01ea`  
		Last Modified: Fri, 16 Jan 2026 03:29:07 GMT  
		Size: 157.9 MB (157942940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df83b4e0c7c410f05aefe8509a5095f65c0513a6926bbf0a5e3fdb665c6185dd`  
		Last Modified: Fri, 16 Jan 2026 03:37:22 GMT  
		Size: 75.5 MB (75512839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c064ace76363500ee893d56933c858892ef07effe370c08ed0b82517927d0987`  
		Last Modified: Fri, 16 Jan 2026 03:37:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec4fce555e452db63cfaf279e32692396690bf55efe81fe5baf30992359ceaf`  
		Last Modified: Fri, 16 Jan 2026 03:37:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f74cb39393c2a68b6bd7f4949b3e0df22565d8122da835ae77b7901e6663e5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05b7963828d41f474cdcf16eb6e15ce07100ba30224208dde8a35d94bdbf457`

```dockerfile
```

-	Layers:
	-	`sha256:8dcf8c4ddac5ec3ce65ea897ce31f70cc2a828abf6062c51361b8b2ab43e2cb3`  
		Last Modified: Fri, 16 Jan 2026 04:45:24 GMT  
		Size: 5.1 MB (5121660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bef8f2cf94441b283a1fb6aa1fefeaf125f4b2525f0cdd8a7673632caf2d0db`  
		Last Modified: Fri, 16 Jan 2026 03:37:03 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:562f1a9cd980336d87da553512759fb315071ffff09730a1994c2b2c370f0c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242443852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52794dc06de5ce427192c236d1b9f67543d6087935bd89822a5f20a8a192f16f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:20:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:20:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:20:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:20:00 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 15 Jan 2026 23:20:00 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:20:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 15 Jan 2026 23:20:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 15 Jan 2026 23:20:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:20:16 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:20:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90cbe2e3b111a17feebbf9e28d72c13e483bd7bdf86d08ab8e10c7c3d5063be4`  
		Last Modified: Thu, 15 Jan 2026 23:20:47 GMT  
		Size: 147.1 MB (147069874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f57447f55b2dc37cce1b87328c91e5e2d618b33d469e2a8ce49600cbba0ccd`  
		Last Modified: Thu, 15 Jan 2026 23:20:58 GMT  
		Size: 68.5 MB (68488524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcedf78be2a47e215e89e70ffae848de1a82b987120af5f4de086b6a0d6ef3b1`  
		Last Modified: Thu, 15 Jan 2026 23:20:53 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16531d62ea508068b0b79bfd6db827028446497bcd9b176258350804cda378a0`  
		Last Modified: Thu, 15 Jan 2026 23:20:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ba9f61d73dc851c26752aa957a69b97e374b4eee6abdffbb9dcd71de1f6498f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d098ccb9004cc5341f074f1568fb35c6cc2dafa645d2e04826c10ac210ac55aa`

```dockerfile
```

-	Layers:
	-	`sha256:70f207512ab48c8c2d39fddec262b7da4948636517d8ac17a87d21becbf0a7a5`  
		Last Modified: Thu, 15 Jan 2026 23:20:43 GMT  
		Size: 5.1 MB (5107823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05837d61269d5076b02d9b4cd1a33c51009afd117c6d18ae87a7fa4a794fc1bf`  
		Last Modified: Fri, 16 Jan 2026 01:41:24 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
