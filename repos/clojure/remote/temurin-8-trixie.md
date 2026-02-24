## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:91def8185d868e710b87b3996b4fcea9b04096868a4fc008f378f56b4ee61005
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:9931d6c5edba829d3879ccaf21b18ee1fbf7739f75a8e260e18409e0159093fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190003881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2ef4739ac0740c66bd978e4090e19600410c25e73dceae0bb3166590b0ab42`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:52:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:52:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:52:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:52:23 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:52:23 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b748e78e7b88335045a7938572d023d71fe0f01480d555a0534a19c0f0ba5b`  
		Last Modified: Tue, 24 Feb 2026 19:52:53 GMT  
		Size: 55.2 MB (55170068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1f4f076d7d5698338e0e4ab23199e469d1255df3b33f32be57f9ffe1f2ee45`  
		Last Modified: Tue, 24 Feb 2026 19:53:41 GMT  
		Size: 85.5 MB (85540044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c14137f11425a83d19191736ec7e35df487c976574528c7a3acf4808a72f2a`  
		Last Modified: Tue, 24 Feb 2026 19:53:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b96d5ef3e6c575112664f61efb3bd8f3907a6ccc4141c2629a63a3d87a067b6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7604237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d278617cf9d8d91580c705135496b0cb9a6b82cf238a3381678ce32c49878425`

```dockerfile
```

-	Layers:
	-	`sha256:a55847d8942e75ceacf75c62eff9e27fb4eadd7e4792be18ba0d8bcca4bcfab4`  
		Last Modified: Tue, 24 Feb 2026 19:53:37 GMT  
		Size: 7.6 MB (7590067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c58bba47d2c53220adee7344e664b531099a890dc03c5fe1432541dfbf190a2e`  
		Last Modified: Tue, 24 Feb 2026 19:53:37 GMT  
		Size: 14.2 KB (14170 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:23081d5e7f2696df193ba8d5b5482c9697d20772c833e6b0446c8fe700adf1d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189269237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555b12397e69d9d7ea915a3f860fc30fc18ff288296b2e41c7a8b3b6e38b8a5e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:03:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:03:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:03:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:03:54 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:03:54 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:04:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:04:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:04:14 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffea5bc637380019ebfcf1c2986b05e95a9345882ceef7187b8a6e659a3d421`  
		Last Modified: Tue, 24 Feb 2026 20:04:35 GMT  
		Size: 54.3 MB (54251622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c51f0da78c920ccc7b606244a9873c2d06bf2f9ad888be02b6f2e17ab514a07`  
		Last Modified: Tue, 24 Feb 2026 20:04:35 GMT  
		Size: 85.4 MB (85364804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3df6554104c992dcfd07f78edb745d1709a7d5f2aa21ffca6f3aa51d06c532`  
		Last Modified: Tue, 24 Feb 2026 20:04:32 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:92a6bc4f230253d3c59baa1d67695ccc4ef25fbd134fd9c402c42ec332ae747c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7612085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a3fe78552ffc11fb353ce33217a7b4f87a448e5ff4e38b2670734271b7cb17`

```dockerfile
```

-	Layers:
	-	`sha256:b199765e3ec0a4d129c61daf425f30a9b537e2d241d1c2f058b4b4a7e90c8bae`  
		Last Modified: Tue, 24 Feb 2026 20:04:32 GMT  
		Size: 7.6 MB (7597797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df8b542e985e245ccedc374eb54c9373658d1828f72e45dded230190a36a5d59`  
		Last Modified: Tue, 24 Feb 2026 20:04:32 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:bc8d9c402fee5aeb0cd89035dc8f086b24f8d8eac2d66304ac7f2c2581e3db1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196710226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5eb21aee2d6a7cbe3797c43cb28bb6e983c8492616e403c085714c81586498`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:59:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:59:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:59:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:59:16 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:59:17 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:07:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:07:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:07:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e31da8e0f9e130c166e97ec3b0c716f0ac97a7e8894e13f7961b61b37819485`  
		Last Modified: Fri, 06 Feb 2026 00:01:40 GMT  
		Size: 52.7 MB (52650394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329a4ba3aea40fc559907aed1c8987fe5d99a928d3b0eedfd7b978c4b55dc94e`  
		Last Modified: Fri, 06 Feb 2026 00:08:57 GMT  
		Size: 90.9 MB (90947071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b636d89a0392804a99da1d846f95ac4291d2ae62e0e7425076e2f9a568fbe76f`  
		Last Modified: Fri, 06 Feb 2026 00:08:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c3216c887949bd379b3fddadfcb1595989e1afad85c7187d0ad6577cfb59180b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7609301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22cd7e473a006e20e1bae94f9fcd4d2716a9cb2c75cd6c73488014d2a8a8719a`

```dockerfile
```

-	Layers:
	-	`sha256:0f9ad73fea1435516de7a62f3e7397fb8759d72c77a4b3bc1277530cdfa424e5`  
		Last Modified: Tue, 17 Feb 2026 23:32:41 GMT  
		Size: 7.6 MB (7595083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75aa8b2b3c133c1e502a8b13207e572ff5446cf489f95c6542104e3ffb3abf43`  
		Last Modified: Tue, 17 Feb 2026 23:32:41 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
