## `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim`

```console
$ docker pull clojure@sha256:94a45e79907ed7c6b1e0f2efbf3c9f67212fbac30ae391eb66be1387ed02f152
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

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - linux; amd64

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

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c0d5979f5c818a56f6ee5222ba962f5fb27d5844ad7fa84eadaaa12dbacfb9f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 MB (197333928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245465318d78bdf20b99b0222a29aabc12260c0e28b382cdfbaf2363d6a4cd65`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11812ef70a6e51874f7a3e88e70c2ad9b1a21e9929f025712f7e56568a7f3111`  
		Last Modified: Tue, 10 Jun 2025 11:58:44 GMT  
		Size: 89.9 MB (89920260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d62b68d6acc3d502e908254c8ab8708204bfd6d842ebf4240c55c7a0956d7d`  
		Last Modified: Mon, 09 Jun 2025 18:24:20 GMT  
		Size: 75.3 MB (75345713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395179a4215373598af7dbac43fc586ec87aea277cb0dac5343838e6eac975cb`  
		Last Modified: Mon, 09 Jun 2025 18:24:09 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f066fd8bca1b005a65bea886ba3c2af35744ccbcbf8ff855afe528d2fbf9f6ab`  
		Last Modified: Mon, 09 Jun 2025 18:24:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7f82930e28a3ce847eb601c0b7ccc85f9280d922036a1038ab84d918021ce1a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42645c5c3d1a665a5289dd3afad0bd8a46fc5bbf773fdd308a1e0a36b358a79`

```dockerfile
```

-	Layers:
	-	`sha256:2e2a80a6b6767d984b6477a12d8cb641d5809d2eb016c90276259f8a60b2dfd9`  
		Last Modified: Mon, 09 Jun 2025 21:39:09 GMT  
		Size: 5.1 MB (5066990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03c28704fab8774638e1bd70387e0629bde9f69b5da4bfbe0576ca224ec7d4f3`  
		Last Modified: Mon, 09 Jun 2025 21:39:10 GMT  
		Size: 15.9 KB (15920 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:99cb34a701ca65c1af0d9c9a75869a5e329cdd23e778914b9ea0b8fa7bf1daa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180434752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f4e1fba1b6be8d52fd1a5734296d861d31d29bfc5d2107d3a9eaf33da1e6cc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b984f64a36288041a3c614f4a78a8680d1a70349b080261f6d6bd8de5660a8`  
		Last Modified: Tue, 10 Jun 2025 11:58:41 GMT  
		Size: 85.2 MB (85216876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38635de2492ba2aa935d24c8e19e307536793daea618b097430ef511e65f2da9`  
		Last Modified: Mon, 09 Jun 2025 19:00:09 GMT  
		Size: 68.3 MB (68334023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348d4edf77a26c653c08267549270f5c15d42fb9274a66cbd8c3fe2d03cfec94`  
		Last Modified: Mon, 09 Jun 2025 18:59:53 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3f5d3018987cc87dbe77d47071ee4e7224f17afff0219ad74607ff4f4b8766`  
		Last Modified: Mon, 09 Jun 2025 18:59:53 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f9b3c7fab41811a362d4aecc6725db7d228a9fedd5ebee6684ecb731e9abda57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5070275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e860db1dcb446aefb9ed77ba8e84c385ba83436f48d20b2060fdde4ec940a2`

```dockerfile
```

-	Layers:
	-	`sha256:0cc9aaddd78ad798becbf26ba129cea4d8de1a27584df329df0ba299c6ad11c7`  
		Last Modified: Mon, 09 Jun 2025 21:39:15 GMT  
		Size: 5.1 MB (5054403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:733a3b16a8fcecc806375c277e35d05368783ab2f52de742a7fc39eea14d6c11`  
		Last Modified: Mon, 09 Jun 2025 21:39:16 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json
