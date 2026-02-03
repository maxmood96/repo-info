## `clojure:temurin-25-bullseye-slim`

```console
$ docker pull clojure@sha256:0d3d53fcf8dc30e0a50e99717b7c8f9bbfccac1a2bf8d3b9a5abdd72a7529ea3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3e2278072fb96a945012e018b944c46911270258a9eab80d4de0e9086e0cc7dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181441100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374c6ca79e950cd309a19461f767f9a78f0bff94784657b7374bbe3ad69aaf54`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:23:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:23:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:23:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:23:03 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:23:03 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:23:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:23:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:23:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:23:16 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:23:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123b987242f9011d1bb55586248e372f067755e13078d0638640d600818fdc9f`  
		Last Modified: Tue, 03 Feb 2026 03:23:38 GMT  
		Size: 92.0 MB (92045302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b78ceb72bf13762a9cd31ae30b6078afb131fc0061f433ad8a3223fdbbb546`  
		Last Modified: Tue, 03 Feb 2026 03:23:37 GMT  
		Size: 59.1 MB (59136470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4698cbf1351e6bbfa26be70c9be17384fdd860750ce5d57cb5b6e1d9cf9d0fd`  
		Last Modified: Tue, 03 Feb 2026 03:23:34 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb16568603aeea38cc10d408f751ea1833d5247e1d49a7ac2a6a56e242f9b13f`  
		Last Modified: Tue, 03 Feb 2026 03:23:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:81f8f4df3acb35466f4dac2d433b6d18f50a9565ddc21a692341dec22c990b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84065bd47ebd8614616469ecfe93041870403d922656ac8ebf4c21491b0d97f`

```dockerfile
```

-	Layers:
	-	`sha256:338da976e4ead7615b1fa609bbb6fac451b1032122a762646659924b8e20be73`  
		Last Modified: Tue, 03 Feb 2026 03:23:35 GMT  
		Size: 5.3 MB (5260226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:732c3b2f606f3c7be01de763edede47927885e8ceb9cab54f81f90e441db9459`  
		Last Modified: Tue, 03 Feb 2026 03:23:34 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0f408e3e6e069a99895aa330d4777ae36e64a66a7a1baa834a262b619694b8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179090138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a8955c26e184e57a8b836bd2ff4758182498b5c035b41f34328244a42a4561`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Wed, 28 Jan 2026 18:06:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:06:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:06:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:06:43 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:06:43 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:06:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:06:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:06:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:06:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:06:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cfc08f2b59c0e6c654e0e1aa09038fe7f300ebcc162c3bc588a67942ba352f`  
		Last Modified: Wed, 28 Jan 2026 18:07:18 GMT  
		Size: 91.1 MB (91052475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec30c440e253e0247ac667e029d0f766f76eed6b2023a521635e683c7e69035`  
		Last Modified: Wed, 28 Jan 2026 18:07:17 GMT  
		Size: 59.3 MB (59288103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbb740314e2e4c00147ea780fef32a631df60f5f54536c055f78ff742959253`  
		Last Modified: Wed, 28 Jan 2026 18:07:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338f1ac47e3e4bff4bccf20304d11753ed024410c90f9a330196450a97cfd753`  
		Last Modified: Wed, 28 Jan 2026 18:07:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9e8b4b6c05fdfc29db66733662d1160cba51fcee4cb975005b507bf447956a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5282646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484f40cf6a15f2ac9c52df7037444aa93b5a96b7026c84d2f6bdadf691551ba8`

```dockerfile
```

-	Layers:
	-	`sha256:99a29df85cffd61be09b0d5a641750b1e19f84d40b47fd4445544e8ff121c8a5`  
		Last Modified: Wed, 28 Jan 2026 18:07:14 GMT  
		Size: 5.3 MB (5265979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a26a77e7b010a5615d01c384a8df5349a4bdc8d8d70e055dcbf042ac2bba05e5`  
		Last Modified: Wed, 28 Jan 2026 18:07:14 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json
