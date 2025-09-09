## `clojure:temurin-24-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:d612082d66b18ca157c44ed71b354aeeb596d1992999a80146f9e65a99a8d8de
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

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0e5e7455990bed2ad2e427d6594b74b64e4b95cb8cfd08927f35aab4c3d19baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187874500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087ff08c9b878708c2efcfa376c44c2f424353d2ebf6b4c2673817f55cb66a42`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58ddd4f0c53d59b3c9a751d5af087f84e97d403e9c08938fcad6181571c071e`  
		Last Modified: Tue, 09 Sep 2025 06:41:41 GMT  
		Size: 90.0 MB (89975189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915ce5521027c90dd10fd2d5712896107bb70967a69fedc176100fe664e7a103`  
		Last Modified: Tue, 09 Sep 2025 06:41:34 GMT  
		Size: 69.7 MB (69669924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d67dee7dfb9c2f6f907b8a496c3ad367c7909e501e69a44e69cac468036164e`  
		Last Modified: Tue, 09 Sep 2025 01:58:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1c049e09cc7f51ace4c6829bd1f79247c8493395b705321c95159bfced215a`  
		Last Modified: Tue, 09 Sep 2025 01:57:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7484efb75030322e729650e186e06e7c1b891761371620a6438e213135478644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5079907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3148741bf4748ce4a1780eeb0d86d85c0fb3bc886f0787de47a2a47e81b62ba0`

```dockerfile
```

-	Layers:
	-	`sha256:31dd643a131ca3cf019c9fcc23e54a8d748910d3777039cbce636bb159b8c064`  
		Last Modified: Tue, 09 Sep 2025 00:43:24 GMT  
		Size: 5.1 MB (5064036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e952f8371391e029ee6eb0c98d31a02738c2a6e26cec3d80b3d634873d885f4`  
		Last Modified: Tue, 09 Sep 2025 00:43:25 GMT  
		Size: 15.9 KB (15871 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9e4a2c9c460f2384c5c459908effa54486ec7ca58af59a3c8d81b46958c67da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186755005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feef1706e81fcf5a26a27a1b8e5dce0a27c5a71cece6e9358544c94fb97efddb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83266fc4c9ca511a89f5dae4dd9f7d772e053a361551b8b7eb908d68bfca2b83`  
		Last Modified: Tue, 09 Sep 2025 06:41:33 GMT  
		Size: 89.1 MB (89092536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713b93139811935b0cf451c2c90732e756d5ff2aef762ac059a54b143f1de932`  
		Last Modified: Tue, 09 Sep 2025 06:41:27 GMT  
		Size: 69.6 MB (69559330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94131ec8425bc778c7e29089427cea810ba7c6b8db7ad7bcde6ffcd6f11ccc8`  
		Last Modified: Tue, 09 Sep 2025 01:23:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d38bd43ce807252e5bb39682d6d49e4c72df5a5ac80e29d107eda720f69099`  
		Last Modified: Tue, 09 Sep 2025 01:23:15 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:920ce508760eb135c498070b4d39b661d499f754cbd1e8a0ba5cf710928019a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5085784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5f274ef684d0b6ee16a967c0f19d46941d1f5b5d9829cd006d305d9dbab4daa`

```dockerfile
```

-	Layers:
	-	`sha256:b8c99607a1d36afdc76e72a7ff26884b2ee016d9b913706b45301f843a63fa86`  
		Last Modified: Tue, 09 Sep 2025 03:41:28 GMT  
		Size: 5.1 MB (5069794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80f8c6d688a58f89020e05de58002dd524772f7c11c2f7212a989ed81b926100`  
		Last Modified: Tue, 09 Sep 2025 03:41:29 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; ppc64le

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

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; s390x

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

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

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
