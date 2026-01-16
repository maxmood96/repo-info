## `clojure:tools-deps-1.12.4.1582-bookworm`

```console
$ docker pull clojure@sha256:e251002fd4af8d99eeaa4d6c74b860a5bce902a76ee329713575f13dd2bd896a
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

### `clojure:tools-deps-1.12.4.1582-bookworm` - linux; amd64

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

### `clojure:tools-deps-1.12.4.1582-bookworm` - unknown; unknown

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

### `clojure:tools-deps-1.12.4.1582-bookworm` - linux; arm64 variant v8

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

### `clojure:tools-deps-1.12.4.1582-bookworm` - unknown; unknown

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

### `clojure:tools-deps-1.12.4.1582-bookworm` - linux; ppc64le

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

### `clojure:tools-deps-1.12.4.1582-bookworm` - unknown; unknown

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

### `clojure:tools-deps-1.12.4.1582-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:e85590ce45744c9323d8ee36263ac7bc0a37fc2c6d1f2e001e9a9ae5b1ddac9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215309554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a024b6758ad20e1601f6197a648c9be7cbe493c98405c824dd581319307135`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:23:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:23:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:23:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:23:06 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 15 Jan 2026 23:23:06 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:23:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 15 Jan 2026 23:23:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 15 Jan 2026 23:23:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:23:20 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:23:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:26 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d228a424ac43e5b633b49f78829dd5efa41560a237d73954164bfe619c713508`  
		Last Modified: Thu, 15 Jan 2026 23:24:05 GMT  
		Size: 88.2 MB (88210666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b130280ab2fe6f155872cd30a712c99fa16b821d954979a5b2e8066fe175ac4b`  
		Last Modified: Thu, 15 Jan 2026 23:24:00 GMT  
		Size: 80.0 MB (79959419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86684d721bd0702d257b55e52d629b12b4e596389c890f04ca840f9cb2ea2d5e`  
		Last Modified: Thu, 15 Jan 2026 23:23:57 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae28dbb1b65e8b4acbb7652fa12aba496372976091eedab145b4acfbc370966`  
		Last Modified: Thu, 15 Jan 2026 23:23:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1582-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:54268646cdc141f3eb333214095f29b25b0b5091f8bf8ab17ba33c7ad6f181f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543c2c7b7e8002814df4c2aaeefac90d597230bd72578d1d62124040fdd1339b`

```dockerfile
```

-	Layers:
	-	`sha256:a5dd894de48a42ede9463cd70a8418fe946954d2e1464da54537d31971504d95`  
		Last Modified: Fri, 16 Jan 2026 01:43:45 GMT  
		Size: 7.3 MB (7322064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:771c2d8a10bd42e69678775b27c91baa4b9e4a0a912feb0b7d6ff4623e77e81b`  
		Last Modified: Fri, 16 Jan 2026 01:43:46 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json
