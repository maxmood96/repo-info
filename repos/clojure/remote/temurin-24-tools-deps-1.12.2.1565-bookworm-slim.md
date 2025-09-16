## `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm-slim`

```console
$ docker pull clojure@sha256:d3fd1c211176dbc9953043240c709975a0969dd2320327462442eaf99c14a232
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

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bb9119111fc2a62d936a019ae01c4c1acf4846dadbdc4d32d6936d74f2f7e4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187874055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febf2499283420752bac393829fb3a319ca5b942143679e0e1f43ee439e7a87c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952d824fa62fafca1c35900887ec16fd6238d531702356825c9029d1c2586510`  
		Last Modified: Tue, 16 Sep 2025 00:22:10 GMT  
		Size: 90.0 MB (89975206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e483e2945f9eef54d3c0f2f9d3b41b53ee6721a810841f2078b0091c31ac93`  
		Last Modified: Tue, 16 Sep 2025 00:22:09 GMT  
		Size: 69.7 MB (69669458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a565f65616242b5abfe9d875ccd898608e2742b030150567b6f38b9ce6e4a076`  
		Last Modified: Tue, 16 Sep 2025 00:14:17 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272ae95c2c48982deee0b55dd04b478475f1d7abb6b16adc6a163274c87d1519`  
		Last Modified: Tue, 16 Sep 2025 00:14:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a376da7e600517c00e3090ada7f49033e0bb98f67a0b3c74511166a92030f8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5079908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89554350cf0a854cd568b0d1b0c5d5cb17f412f7bf76ea93847cdc5381848515`

```dockerfile
```

-	Layers:
	-	`sha256:265ebf14a337e1c6d828c47dc6a0d2d0466fa4d1b580c7fe4692148b3736ec04`  
		Last Modified: Tue, 16 Sep 2025 00:44:35 GMT  
		Size: 5.1 MB (5064036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85b867498f3c81253b6a23b86a7371897a6f3cf72c0f560ad518e33d151fcfcf`  
		Last Modified: Tue, 16 Sep 2025 00:44:36 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b000d03abd5adead486f9d64da96020bc8cb508c3017c7b0d79d299f816e8381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186754768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac52c446a0d6a77d3d6a623c4234b64609d02f218ba89a1615b3a4ac4427c517`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d2a03efeeba1e158a24d85add18acef28b55a0b55fe230dac3317d21e802f1`  
		Last Modified: Tue, 16 Sep 2025 00:36:04 GMT  
		Size: 89.1 MB (89092475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eccb4077e45e3b7a3770f4c2b0702d8621844da36906d97ac47941fa25f3c2e`  
		Last Modified: Tue, 16 Sep 2025 00:36:02 GMT  
		Size: 69.6 MB (69559156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1676ebbb419908c9804e1570d3f2d7ae5e0d3ef08eeb5e26a8d0b07860b2dd`  
		Last Modified: Mon, 15 Sep 2025 23:35:06 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2318792cd6cf7527c6ca8c0ea6b8629f47a982b93983aa15f12998acc8a93204`  
		Last Modified: Mon, 15 Sep 2025 23:35:09 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:170511c18efa0884125bf77cf847cb51d3ca51e2043f3e0609553574531a8901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5085784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb6a0bbfd5a7bf110ef814a4c41fbcb7a8eeea241a85383cd602f204421e440`

```dockerfile
```

-	Layers:
	-	`sha256:352d02bf95aa10149c8b50e8d16390d78278bf1a6b3eb28fcd26454ca1481e40`  
		Last Modified: Tue, 16 Sep 2025 00:44:41 GMT  
		Size: 5.1 MB (5069794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9fa39c91c22c81d90f06ad8a5be88aea162d307915060928541890a634bea1`  
		Last Modified: Tue, 16 Sep 2025 00:44:41 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:957565422855d76776cc8debc26c0239fcf3beae3fdc77b6dcbb19b93d459b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 MB (197498513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a17e51612191de01188f1dbf34a84ec3dbede5d582415d1c55a84b9d063b62`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b097b82e87ae83660625cc9b730d6110b249f2172d82d31c165e9cfcabd00bd6`  
		Last Modified: Tue, 09 Sep 2025 12:57:16 GMT  
		Size: 89.9 MB (89918195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f68c9b5e7d1a560586691b1535f4a7468a3e86071ab0607e1e0fea908df2b2f`  
		Last Modified: Tue, 09 Sep 2025 13:05:14 GMT  
		Size: 75.5 MB (75510515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6688501da06f040678954afb0c3b26b31837551be48bc93966dfa962029ece6`  
		Last Modified: Tue, 09 Sep 2025 13:04:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07599b34d96ff271df2d997bdb40403c93e7e4cd412f999d97eaa30c893a125`  
		Last Modified: Tue, 09 Sep 2025 13:04:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e0db1616ca0d3429c6c7c9a9fd7303cdaeb2f4d173b1fa7699ca61331e696f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53dbdfbf05dc1991921edfd7497ea6a08842e346ac839e3f32d4aa20f44c43b4`

```dockerfile
```

-	Layers:
	-	`sha256:29e56887e367d17e8d9742ee3688c4671dee4306ab1592ff19e1ae71767f0885`  
		Last Modified: Tue, 09 Sep 2025 15:39:32 GMT  
		Size: 5.1 MB (5070492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa36e60c09ee7065b371e30a1b9ee48134665c9c97ee85901b6aca39382dc745`  
		Last Modified: Tue, 09 Sep 2025 15:39:33 GMT  
		Size: 15.9 KB (15920 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c5e82b3f11674db4cbbcf40ab194d89233aa8eebe15048a86ec7222bb65c9f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180597052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebfb000ebc9d39ddc5ded28494c084d4d7eeb487024f59169e10e9084e7b012`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0f917e81dc0c2e313b192edcc8a1d89e6f0e5547f2c13abf5f905f60ec1c63`  
		Last Modified: Tue, 09 Sep 2025 06:41:42 GMT  
		Size: 85.2 MB (85226398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f21677e94f8443b5a32204ba0b92fe65d3d5811dd3e5483cb5cd16aa62b54e`  
		Last Modified: Tue, 09 Sep 2025 06:41:32 GMT  
		Size: 68.5 MB (68485319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab9baf691f6ae240ecd6926466966048da8db2b81c97afda57dc21cff5bdb13`  
		Last Modified: Tue, 09 Sep 2025 06:40:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ddd9d203756d7beed84589785bdeedaffdab4cc19f655b808683125c7b13ea0`  
		Last Modified: Tue, 09 Sep 2025 06:40:53 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aef0e207557c3c4fb0a3b8b4ff8ff5d4d619a344987fa5cacfcc1c90c4ea8737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5072978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68abf76769f352c749744bb2fe812a878b85c2442062341c5de98cfc811d80f`

```dockerfile
```

-	Layers:
	-	`sha256:c5e8e0f03bbd2885a9bf8d8ac8b387d3ce2b5d574874d6eb6532b82868e53bb8`  
		Last Modified: Tue, 09 Sep 2025 06:39:52 GMT  
		Size: 5.1 MB (5057905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615595ee6983394c9f14c76a070eb28596e2bd7405358cf44d4a69068035fd40`  
		Last Modified: Tue, 09 Sep 2025 06:39:53 GMT  
		Size: 15.1 KB (15073 bytes)  
		MIME: application/vnd.in-toto+json
