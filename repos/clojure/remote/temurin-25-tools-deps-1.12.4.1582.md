## `clojure:temurin-25-tools-deps-1.12.4.1582`

```console
$ docker pull clojure@sha256:49e8d965b8ed6d7cfb23c02842b4084b0dc3a5f16b29c9fd1cdd42a7606e75d5
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

### `clojure:temurin-25-tools-deps-1.12.4.1582` - linux; amd64

```console
$ docker pull clojure@sha256:1d8a6956cbab8db1a44cce7423c2dc6b0ee3fc1c1f1c08e1d3c9d3aa0b44488b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221674071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625ec4d3731b6095b43eca889de36bc8a57287d82bc18866154d04fc8576660b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:39:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:39:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:39:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:39:06 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:39:06 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:39:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:39:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:39:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:39:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:39:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044e9e15b2e23160521d10aeafff368884bf828c86ab241a417afc1595f3408d`  
		Last Modified: Tue, 13 Jan 2026 03:39:57 GMT  
		Size: 92.0 MB (92045289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510d93ae5e9b12fa93c6214406945fdff27588678c9ee349dc8f0751e929f279`  
		Last Modified: Tue, 13 Jan 2026 03:39:57 GMT  
		Size: 81.1 MB (81146123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d91b2492fe0e40143f2755f4e362bb1ef9c1ecfb2d74856ac3bd4bdd9a2c449`  
		Last Modified: Tue, 13 Jan 2026 03:39:51 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b709f5ce5867ec68a30f736047340e4af4b5880841af27a1830c0f2f3ba0e9`  
		Last Modified: Tue, 13 Jan 2026 03:39:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1582` - unknown; unknown

```console
$ docker pull clojure@sha256:affe02086d04446c24c4742b34cf31fe6380928aeeb8155b4043fdc84217dcd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7345968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f7f08cc754d0f6fbd78f32d09a50062debcf545987baa425ac455325eeb50b`

```dockerfile
```

-	Layers:
	-	`sha256:e576d7770f8540ce730996c21ed4c85ef8423567b70840ac2e52d69d6873cf5d`  
		Last Modified: Tue, 13 Jan 2026 07:45:23 GMT  
		Size: 7.3 MB (7328197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58db61e92173f20c3f7d1b5ffc0a52508486d17eb81d8f20d47b46c70b75b448`  
		Last Modified: Tue, 13 Jan 2026 07:45:23 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1582` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dec5d8d2bdc9578ab1403fc6a196be6b7417306db6d8f29202249d92a7e69d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220558726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4994219bce4d17da4bf1a8029c5ce076de72a35dfcef042a0c89b225bec1b6f3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:43:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:43:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:43:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:43:01 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:43:01 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:43:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:43:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:43:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:43:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:43:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12c220ac0f0f0f139b5bc22a77f881a01dbf21bd4f608e88cbe7ec65d41c107`  
		Last Modified: Tue, 13 Jan 2026 03:43:54 GMT  
		Size: 91.1 MB (91052514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036c8e629db51d9034b3eadcf652827afd71ff196a7c39c5d97fcaf2cee62c11`  
		Last Modified: Tue, 13 Jan 2026 03:43:53 GMT  
		Size: 81.1 MB (81139097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d3a502e042ce1c061856c002b6989053a23998d133f3dd37473c9e5262985b`  
		Last Modified: Tue, 13 Jan 2026 03:43:47 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b61ee202ae8859925202c625442551eb7f7bf6fb5fb7ff3179ebbf37133db24`  
		Last Modified: Tue, 13 Jan 2026 03:43:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1582` - unknown; unknown

```console
$ docker pull clojure@sha256:d995892375977fba7ed8eae30880449f382e418f080b9ce65609e8d8fa9ef3b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dad5d55b8b8207ad2cdfb5c0735de38822b4a0b838f9061c9d1f70eda5ca168`

```dockerfile
```

-	Layers:
	-	`sha256:70c3c5646342f38dcfe4832292934a40c6961114ea778f26ff536ded0becb338`  
		Last Modified: Tue, 13 Jan 2026 07:45:29 GMT  
		Size: 7.3 MB (7334029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddccb7d35f128f193ae2890d547f5ee0a8a42523f582ac59ba9c76ed6c04ae03`  
		Last Modified: Tue, 13 Jan 2026 07:45:30 GMT  
		Size: 18.0 KB (17961 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1582` - linux; ppc64le

```console
$ docker pull clojure@sha256:6cb6690de0d5bfdacdfbb634dfa46ef5192f6c893d9334a00bdc1e84978cc689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230925780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8271ee2c40b5e35e7e0ee986458d3d976dce79ca9ec1bc270ef81d8ec39bb58e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 05:29:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 05:29:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 05:29:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:29:37 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 05:29:38 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 05:52:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 05:52:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 05:52:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 05:52:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 05:52:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:39 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b170658cc3480535e317472b552956a72545fa3b10ff67eeabf8ec9da0a276`  
		Last Modified: Tue, 13 Jan 2026 05:32:49 GMT  
		Size: 91.6 MB (91610769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5908c3b8f6020adaab940a2424a5d3b748ebc5f68c969e9ccf31529ada26723`  
		Last Modified: Tue, 13 Jan 2026 05:53:25 GMT  
		Size: 87.0 MB (86986593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb825faebafb2f3141402a96c0111229c4237004df42fab48d66416b68f8dbf1`  
		Last Modified: Tue, 13 Jan 2026 05:53:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac46e2668c28164db0403ac2fb14844f698d91a007212f72ce3ca82a84f91f53`  
		Last Modified: Tue, 13 Jan 2026 05:53:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1582` - unknown; unknown

```console
$ docker pull clojure@sha256:e0b56b4fdf314c3a34fdf27173b385446c81bce6101500c914c81b2a312bb710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7352602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f89d9d22499dc7e08adedddb90e4efb24b0c97ff56f149d9326eb1af203ffe93`

```dockerfile
```

-	Layers:
	-	`sha256:0b0e116a918b0ec05cb9688e8b51c533bad39d60c229f35d9ec00be77eedce81`  
		Last Modified: Tue, 13 Jan 2026 07:45:35 GMT  
		Size: 7.3 MB (7334747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1ca37199fea2439fb742dce65edda686f253fe7ff0c13bf891b2e4729df94a`  
		Last Modified: Tue, 13 Jan 2026 07:45:36 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1582` - linux; s390x

```console
$ docker pull clojure@sha256:797ba21161011e0a93906a276e70befbb771cd83a2581a6e24fb333f64934df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215309556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0659a3f82cb3d44f126807a68ed97d4fef26ba68124965bb8a6613900d03358c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:06:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:06:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:06:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:06:49 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:06:49 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:08:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:08:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:08:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:08:50 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:08:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:26 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59357e56c5eabe42db724069fed8dafeb8cd07f5df0a3442d2e90ddf3c2420d6`  
		Last Modified: Tue, 13 Jan 2026 03:07:43 GMT  
		Size: 88.2 MB (88210715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41786a30589d0815854ff9a64285cf634e8877ce4ac3b8227d84c946ba19dce`  
		Last Modified: Tue, 13 Jan 2026 03:09:27 GMT  
		Size: 80.0 MB (79959370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc79e121e3a10224effa5bb717e2c7360461bcd3a26ac7d0b364037c616f28c1`  
		Last Modified: Tue, 13 Jan 2026 03:09:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487dfdcd0b3d00088d3361a8e2e1e49e910566911c7cc5b919d257ed66edceb4`  
		Last Modified: Tue, 13 Jan 2026 03:09:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1582` - unknown; unknown

```console
$ docker pull clojure@sha256:a25db9de46f828747d616989c93745f258f912305e4c876c910a73c72b34c3f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77de6d4db8746952cd8cbde7562ccdce69c5b332e7f9bee8a5ed06b6cb062665`

```dockerfile
```

-	Layers:
	-	`sha256:4969ce3d32e6c9c3e5eaf68c3f4c56457479cb14861e6f21d81e3150a88b781e`  
		Last Modified: Tue, 13 Jan 2026 04:40:18 GMT  
		Size: 7.3 MB (7322064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89e793a25ea2491c63d1b5b4089bc4bd928c8a199c41a67d3b97a168b952ec75`  
		Last Modified: Tue, 13 Jan 2026 04:40:19 GMT  
		Size: 17.8 KB (17769 bytes)  
		MIME: application/vnd.in-toto+json
