## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:02459fbd182bf761a05f61eff9bef42183c43b09cea61cde5290a71c6737c5fb
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

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4b2ba3714dd4ccc0f942ea051d71f14533881a6d517f2428d122674405919693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255732156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885b1e27961efeec7094e3b554ccff53d0c5bddcae06d416be34011d9524a180`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 22:39:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:39:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:39:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:39:41 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:39:41 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:39:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:39:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:39:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:39:56 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:39:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e4b9304cbb9757d98924240ea3c8f389dcda59f518b09fef4787ada493daba`  
		Last Modified: Thu, 11 Dec 2025 22:40:41 GMT  
		Size: 157.8 MB (157825956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f800fc293891af68688e6125d3cd1c233866e9ec0f10d5ef96b99ec24fa1ef90`  
		Last Modified: Thu, 11 Dec 2025 22:40:32 GMT  
		Size: 69.7 MB (69676744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d014d019af0d57bd9879e9e6217b974ae37dbe6978c04bf5225f8fef21bc208`  
		Last Modified: Thu, 11 Dec 2025 22:40:25 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2577bcbcda771b4e0c93062739370224c30bcff49b27418f48d62e7c48995f6e`  
		Last Modified: Thu, 11 Dec 2025 22:40:25 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e93f498990453520f4de241198e5c2497b1de4a2054c7903bb62f9d8d283a078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b690518769dfbc4884f6de51ae59c81b036d213f4d0b2b208f6bfc6193cb2b7`

```dockerfile
```

-	Layers:
	-	`sha256:80d1cc167c45bc8f89682de2e317ba827982dfa23187b20e2f2fa9d8e97e288e`  
		Last Modified: Fri, 12 Dec 2025 01:41:05 GMT  
		Size: 5.1 MB (5116492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:417a1ffe9567eb8a950ab3ec1cddaa200b07645f356177e861a4d381eac778cf`  
		Last Modified: Fri, 12 Dec 2025 01:41:05 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4b65b1395e6b5f4f744c610343c5cb91b960bed005958b7c1d05286434297191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253769564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0912b063505f9b71357b5a472125a06958336208476f38f50e0ddfe1818f67`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 22:40:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:40:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:40:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:40:03 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:40:03 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:40:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:40:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:40:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:40:18 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:40:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e6a1136234daf33bbf926d89c1acfa8e063bf752f7d111c74cb98ede488bb6`  
		Last Modified: Thu, 11 Dec 2025 22:41:09 GMT  
		Size: 156.1 MB (156107624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a00d32a99abae221e0891bb2e481c32c2f56392c9d4e1022d28a6bd19046948`  
		Last Modified: Thu, 11 Dec 2025 22:40:58 GMT  
		Size: 69.6 MB (69558672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784c59dffa0380a4a12e0383d67f41527266693a3c7fa44f0714d6e7cbdad2bd`  
		Last Modified: Thu, 11 Dec 2025 22:40:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309de2c7fb3bf3fb4d407cdf96de54434e91701c9b3a8cdfaa0917542f2481be`  
		Last Modified: Thu, 11 Dec 2025 22:40:52 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5648a6c2a570fc52f05fe4f5aaabe25f48fc5034ab3338b96f2a8bb3728952d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1712c5e6aca896621085ffe6891716e02d3e53eda72b3ae533af88317ceaae`

```dockerfile
```

-	Layers:
	-	`sha256:17917e39599094787e8337ac6efb98c828b74c0158c0105737f6a5bd0c998c70`  
		Last Modified: Fri, 12 Dec 2025 01:41:10 GMT  
		Size: 5.1 MB (5122253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97aca9f3657bf092a97d94a9edf74155ba322e337dc7cf9f539524ff83c1403b`  
		Last Modified: Fri, 12 Dec 2025 01:41:11 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:61027cff0bac9069d57eea2f1453e8884eb3142fc75f6160ca61f869ade76b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265522731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ebd7d5870bdb27661dbe1a508ff1231806e532d8cec75a9d208389a8f219dc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 16:22:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 16:22:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 16:22:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 16:22:00 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 09 Dec 2025 16:22:00 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 23:00:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 23:00:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 23:00:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 23:00:28 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 23:00:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d170adcd864f030aabc5ba607c417b8b9efd1bdb3b13f20e801de697b8e3a11`  
		Last Modified: Tue, 09 Dec 2025 16:27:29 GMT  
		Size: 157.9 MB (157942949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631dda0b040bb52075559c458fe68a024661ae98cc7a4ccf8a00ea41b89bfa3c`  
		Last Modified: Thu, 11 Dec 2025 23:01:33 GMT  
		Size: 75.5 MB (75509895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ede920fb44d86920c1fa0ea7addcfec5d0ba988fe52faf97fc8157cac56bf7a`  
		Last Modified: Thu, 11 Dec 2025 23:01:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a803c4171914f96843bc94dfd73a85de1c846c117d60c16a7670c3f2fef0887`  
		Last Modified: Thu, 11 Dec 2025 23:01:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b44d6e6fbbaa381ff2b58925cd5674c3c5665eb3c0e3ef6ebaada00771b02266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0164e979b42090ef6870c7dd8e95a805a267e680e5efb6b6033ea0369e86ba1`

```dockerfile
```

-	Layers:
	-	`sha256:b3c17dc75f61e2d0a85a9c99a0089d4ce701cb0f65d623de64c928d0daa18262`  
		Last Modified: Fri, 12 Dec 2025 01:41:16 GMT  
		Size: 5.1 MB (5121650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86ff2d5f27279884ed0f4ae67b5625b8ccf7445748d4aff7167c2377bf8db887`  
		Last Modified: Fri, 12 Dec 2025 01:41:16 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:7bc123d6e5d322ddaf4eb942b71123569bdc431f0a6aedb7e271a71436172a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242442902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf4271f0f9546981135c0e18a83e81d270eb17e9aa364eaadcc21a82ca28ae9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 01:30:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:30:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:30:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:30:42 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 09 Dec 2025 01:30:42 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:35:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:35:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:35:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:35:38 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:35:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89aa0de067223d3ecb4c513f6bcf0d76802a026b7899386bbea2d37a24c9a5ba`  
		Last Modified: Wed, 10 Dec 2025 06:09:05 GMT  
		Size: 147.1 MB (147069831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e6925aaa6e34fc270be4da7c2beb4834519cfff825ebef14c608f4c130dcdb`  
		Last Modified: Thu, 11 Dec 2025 22:36:16 GMT  
		Size: 68.5 MB (68487602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49a2c32b464dd78ea1e501dba157e3e1433cd8919d58deca6e52ecb3dc9a255`  
		Last Modified: Thu, 11 Dec 2025 22:36:09 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fab34bbab3b404d0ceeb3f0c0d693e1e5515ec5ffa8e6676cd75e15634f47c6`  
		Last Modified: Thu, 11 Dec 2025 22:36:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3091ea7f7a0db386e492a89565eb218627a76e7d986da7fafaf8fa329aafb156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8abd990a035a3194957a497a777b2f3485378c49356a55f1bbc0d78e9b0076a`

```dockerfile
```

-	Layers:
	-	`sha256:16ffb87cc5b48534ccdd012445574f583945e1196198c864e3251be4a282dddb`  
		Last Modified: Fri, 12 Dec 2025 01:41:21 GMT  
		Size: 5.1 MB (5107813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32e55fd6c7a8d207260d4a22c43551cd6d9a864e53c637be22499d76ebad8e54`  
		Last Modified: Fri, 12 Dec 2025 01:41:22 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
