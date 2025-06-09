## `clojure:temurin-24-bookworm-slim`

```console
$ docker pull clojure@sha256:074c96b5b79b2a7951b476ca6ba358a1e7d7a531efdaf6da99ea1a3706749d58
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

### `clojure:temurin-24-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e59c7381c6e0f87ca6b3bd073071cb65dbae24ba127625350b341cec52040214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187707918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91af8cce9cb5f8594e167c979b3cdcbeee6fd0e11c41fbb67b5c5c17b5e72870`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a5ffb2ef4f645d303b9feb4c2f74b212f77c2d6d29f80e6b80ea530a8ec80a`  
		Last Modified: Mon, 09 Jun 2025 17:19:11 GMT  
		Size: 90.0 MB (89951996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360b342e76d1f1beff1d4ea8297a51a67219f0920df4546e680e04952efe86c9`  
		Last Modified: Mon, 09 Jun 2025 17:19:12 GMT  
		Size: 69.5 MB (69529550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44db46cb24a1555a8f16b7a2d3a406282752788deeb3ef9c0fd76cbcd3188d3f`  
		Last Modified: Mon, 09 Jun 2025 17:18:59 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc5d454ef1eeaf3396a69a02e01212d2601fcaceedb5a308476382a04dbfa3e`  
		Last Modified: Mon, 09 Jun 2025 17:19:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:116bbe6b57f07ba49e36b4781c3b1c9cae24ecbe6f7ee6b411f71e741f8d3434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8161f351bc0f269806bb1b1bd8dd3ea5f5918a2b09518b7f51a88493b1987a`

```dockerfile
```

-	Layers:
	-	`sha256:888e06e226090bc2871b579eb92ca6661d2b248984578c52fbea3175dfe0b31a`  
		Last Modified: Mon, 09 Jun 2025 18:41:02 GMT  
		Size: 5.1 MB (5060534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d12db7ad77688fabc79a23e66ad17b68f1dbfaec1efb99315ab51e9fa733d8e`  
		Last Modified: Mon, 09 Jun 2025 18:41:02 GMT  
		Size: 15.9 KB (15871 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c385c471b758cab32a1674f3fea72abf85b27541708db19bba2818daef099226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186548156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23dc96fe1f22178d9e06d3d5df7f25113a97f8987975f96e96fe39ee6a7d7e65`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71e656269e61d9fee81d36b750f503dc64c9352c0276d046ba8584c69c03aa4`  
		Last Modified: Fri, 06 Jun 2025 12:21:14 GMT  
		Size: 89.1 MB (89091268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed39db032b6502f266d5a2c686048124ad141fd375b2e841c6359c891b38272`  
		Last Modified: Mon, 09 Jun 2025 17:59:24 GMT  
		Size: 69.4 MB (69390570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2476a47341a27a51b5ff3100842a55205813a0feec089b25c61c55528422663`  
		Last Modified: Mon, 09 Jun 2025 17:59:08 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9984869abecd1e22235a46f9e5fcf81e2c72218c731f1910d9a826a23d03aeb`  
		Last Modified: Mon, 09 Jun 2025 17:59:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0b9caa0953f156ff149f07d13d01641822fdc0dfa22a3556a04e0bdbab097daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd2ea3ddd3a8bdec688099534adfd28f58e4b490f18621050c349407bec07da`

```dockerfile
```

-	Layers:
	-	`sha256:698a675d61335a3ca04839e5cea6df75d29acc8a50f6fc735b240bcbf204bc4e`  
		Last Modified: Mon, 09 Jun 2025 18:41:08 GMT  
		Size: 5.1 MB (5066292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45adfd7e09f62435ee08b3145084354e1c795a85b84e288c1a69105277320ddf`  
		Last Modified: Mon, 09 Jun 2025 18:41:08 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:0ebae82a60fc37292e68145cac5add24851e4919c1f040c5d54fbf6b9dc0a6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 MB (197334122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0adaf21fab3cb6f0464096f689c7209249fba6cdc4294b8435b7bb640c1fa11`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11812ef70a6e51874f7a3e88e70c2ad9b1a21e9929f025712f7e56568a7f3111`  
		Last Modified: Tue, 03 Jun 2025 09:27:03 GMT  
		Size: 89.9 MB (89920260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae07a2865f2723647b6fee9f20365f13e8aa5d4c8ffae0150b9fd9087150b8f8`  
		Last Modified: Tue, 03 Jun 2025 19:12:31 GMT  
		Size: 75.3 MB (75345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddca11ca79da36b897126177347969f070a24a79e912b28d9cd6a790bc5b9c9`  
		Last Modified: Tue, 03 Jun 2025 19:12:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f831dcb8e7cd8a23b410c02f10cadaf9a92359e72fb274f99355b77d15edc4ce`  
		Last Modified: Tue, 03 Jun 2025 19:15:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5c223a4e40208b7f1083d8f13ce7dcb5a160c2a8c7271fc65181807cdbf2dfc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0272d27dab3b4c456b1a8eba63c6bbdad8447b41b91676aefd5af30370a9743c`

```dockerfile
```

-	Layers:
	-	`sha256:fa297017d9d47ba5d33ad5e0c5e27220ad3242d94ac1759c74edae0fa3dbe0b1`  
		Last Modified: Tue, 03 Jun 2025 21:42:39 GMT  
		Size: 4.9 MB (4918600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff0cc9cac9d855e079b3c1d17a940e91efdccb6a59ca70979055f7834f72f74`  
		Last Modified: Tue, 03 Jun 2025 21:42:40 GMT  
		Size: 15.9 KB (15920 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:347bc7864e260b4bdda3df6b01f856b87626ca17f0b4556550b9c2ac3aa14b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180434892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b362773a788784215a397a4d3a5c46f2ea27491d5567fb11f3aad84434970ba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b984f64a36288041a3c614f4a78a8680d1a70349b080261f6d6bd8de5660a8`  
		Last Modified: Tue, 03 Jun 2025 06:36:43 GMT  
		Size: 85.2 MB (85216876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149f3e89f659661184f28ec2ffca2d54f2995ba19d636173287f8fa6e237e5e4`  
		Last Modified: Tue, 03 Jun 2025 18:44:22 GMT  
		Size: 68.3 MB (68334171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15b243dd75693e805b8246534804adf8acc0bd764ff0645ea8d666e66710a9a`  
		Last Modified: Wed, 04 Jun 2025 04:19:16 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ae3c2ef3eb00b58f581b4803c85dda21fe52b2fa59cb5e6a0b85ebe4f3c306`  
		Last Modified: Wed, 04 Jun 2025 04:19:21 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:09d810c19f7c390d1435c62f8c1c6e31aa1ba721ee04a9bcbd1da63104c7ff8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9201478ba68b647f6b787b05f826af8d578e0c5be1e593a5b234d726b37d7c7`

```dockerfile
```

-	Layers:
	-	`sha256:615c41caf93584f3abe35d4d38ca7ff630573e1cbc3473dc45f048d7f213ac24`  
		Last Modified: Tue, 03 Jun 2025 21:42:45 GMT  
		Size: 4.9 MB (4908905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a14ee87b8793c3725ba8ac04f1029bab6f7a9ebaafbdc86987987763bac29e`  
		Last Modified: Tue, 03 Jun 2025 21:42:45 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json
