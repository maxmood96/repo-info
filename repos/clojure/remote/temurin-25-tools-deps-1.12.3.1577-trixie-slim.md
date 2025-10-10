## `clojure:temurin-25-tools-deps-1.12.3.1577-trixie-slim`

```console
$ docker pull clojure@sha256:5f3285f9ddca924005c9b3baa190e2baad4be86cabc4fdaab1bcf680dfb3b13f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fbf5520ba33f07ff9dcaa6aa73b53a864d948b6dd162a75b278bb4b5bd93c223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196753105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc4147a3e4a92da6bbc1ad0553eb779e5cb31f2fdfacc4566e204c1a3127d03`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fbb6c97dd097e2c95217b8ab1f57d74095d28a9695bc7a058f867e1549b063`  
		Last Modified: Fri, 10 Oct 2025 03:41:28 GMT  
		Size: 92.0 MB (92036030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690c65b18668cda6f3ce30c7ec67839ed728bf30619d344abc134a46803f2e16`  
		Last Modified: Fri, 10 Oct 2025 03:41:27 GMT  
		Size: 74.9 MB (74938264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39147206585e09d541d4c18cd9f8d00e28655b6ba608d94fd4655217eba2802a`  
		Last Modified: Thu, 09 Oct 2025 23:15:12 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b9bcc05d31a22afee6f9adbf75eea0e3474903c1e277ac705ee4a45bc8595a`  
		Last Modified: Thu, 09 Oct 2025 23:15:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8603dbae71db497e91f1936d45e3d093a87cb831e58da3318ddcdea412a0c1f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025f272dc5748d5a0746fdddba5220303f9f89c92ce8019f264eff1de285be36`

```dockerfile
```

-	Layers:
	-	`sha256:7129766d2d3e6541a7da73f61394105d0a9d9cfeca9820cb542448948c0008a5`  
		Last Modified: Fri, 10 Oct 2025 06:49:20 GMT  
		Size: 5.2 MB (5207505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2af3db30520e5f51b1296bf9cc388f85ef50ef075bbf9e12c467a2bed0575e5`  
		Last Modified: Fri, 10 Oct 2025 06:49:20 GMT  
		Size: 16.5 KB (16536 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2d95c524eebea9d47ea35e34369aec62544babb4d88a6b9ab314bc54a2096955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196312020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:398df06c61a1f52dceb61a29225decce7a375f8538ebb6c56cdf83b3c7d77531`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3228d42ce0e696497e1044d76bf6a482bd8f4f5ab3160e7347b293c7cb7e8921`  
		Last Modified: Thu, 09 Oct 2025 22:31:33 GMT  
		Size: 91.0 MB (91045227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db00122923663993d5a552d5fb6dbcdb8c3e2d0a32602890e1790e2d563cc3b9`  
		Last Modified: Thu, 09 Oct 2025 22:31:31 GMT  
		Size: 75.1 MB (75124910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fa08e37a8a8721843ad33a254ad0f0364eaa810fba0aadebb572f88245364d`  
		Last Modified: Thu, 09 Oct 2025 22:31:22 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1814c52cef4d4f6fc5c18ddc00341b8aad7dfa35ddf68b741376704e1fd80f69`  
		Last Modified: Thu, 09 Oct 2025 22:31:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1fcccba565e95f31e18533f092312976552b9bfc677c044a86184ed4dafcdedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e022dbd615f3e9a85253c10c74529c6b542f66a249b7989a6d7b7bb74f38c8f9`

```dockerfile
```

-	Layers:
	-	`sha256:7d10fac50e2a8b7b4c4a2ebe6e0679f42c49e3e46fbb92451ffe459462834b8b`  
		Last Modified: Fri, 10 Oct 2025 06:49:25 GMT  
		Size: 5.2 MB (5213295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de94bc9114cd369cfd82d47af05871f538b275c446e8e540596431d30642ba81`  
		Last Modified: Fri, 10 Oct 2025 06:49:26 GMT  
		Size: 16.7 KB (16677 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:63d1871128bcd1c65b5bd9f5552adc6a572e74efa24c4e02a8a6549e4a68c98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.8 MB (205789166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e260fb3495d0f86e31195f40adda093e838cbf831488451140d159c4885d00`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1e674fe5a0381f7eb3e47c5b778e5d22f245341257fe87e3ea3323a7be54a3`  
		Last Modified: Fri, 10 Oct 2025 05:57:18 GMT  
		Size: 91.6 MB (91601717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae25075db93e637dbcc37fec2412dd1bde25a458c26d2784f171732ff12f0f43`  
		Last Modified: Fri, 10 Oct 2025 06:07:16 GMT  
		Size: 80.6 MB (80587954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4159332fbb2177bda9f45d3646c7c9cb1f58cea00ba11c9f39a8a1e5988cc8ad`  
		Last Modified: Fri, 10 Oct 2025 06:07:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882f546738e7526aa0f0759ede820cd660f36575b1c0b697dbf9b487de4f7031`  
		Last Modified: Fri, 10 Oct 2025 06:07:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:15196d93e576caa4c23e74818dbb320001b4b8dde1b44cf36417ff623bb448da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490aac39dc969dee200f036879286ce9f490aa82f2b2306f97f58901df3d2bc8`

```dockerfile
```

-	Layers:
	-	`sha256:221b41a88c69ddfd2f14b8286c806f97acdf62d031fd43f2aab20dbb729460f5`  
		Last Modified: Fri, 10 Oct 2025 06:49:31 GMT  
		Size: 5.2 MB (5213186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdd76d990585c45a3d77467d804e3224e864871fb5bf9585194358d127767489`  
		Last Modified: Fri, 10 Oct 2025 06:49:32 GMT  
		Size: 16.6 KB (16595 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:387804d3d26037c5cec35e495592fb0a341dc2a1ef528f733c9aea24030bcd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192517408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c2cd4762369b2a8e137141ea6be982a1d646ffadae948e26cbb1e9b7f77c53`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c14210b2e55dc8f2234b49ef3d00fb3fb7050255e8655721e57688e1998fbe2`  
		Last Modified: Sat, 04 Oct 2025 15:14:08 GMT  
		Size: 90.8 MB (90752390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4438d0f363f4565da6530f109ef302236815051d87464be61ffde4cfb72ac549`  
		Last Modified: Sat, 04 Oct 2025 15:34:19 GMT  
		Size: 73.5 MB (73488471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab18a0cb8769f03320f1e3f5277d1e49ba37f13d11cf63e41ae22d291becc89`  
		Last Modified: Sat, 04 Oct 2025 15:34:14 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ca9046d86ebf60ffb21d5efe45960e286772373845da239482012a40582b3d`  
		Last Modified: Sat, 04 Oct 2025 15:34:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a053f21f1476f0fe8e9f3daa40da051898eb772beb07b6a58968f0942c2a57af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814a2ad9cbcf637200799cbc9dc7e6f63a8f7b4ad19f5b3db845c719952bdfc5`

```dockerfile
```

-	Layers:
	-	`sha256:f63483b7f5a293c1e4afd9ec7f02f9ee66796335fd85511232a8a9fc5fa9ec6a`  
		Last Modified: Sat, 04 Oct 2025 18:37:02 GMT  
		Size: 5.2 MB (5196978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3a24526c1cea1b9eb63268bc03b64f199ec64b94079115b13be081dfc78cd1`  
		Last Modified: Sat, 04 Oct 2025 18:37:02 GMT  
		Size: 16.6 KB (16596 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:10f7cf12e5d818b933048b68cafb4d2b2b66bde7821c0ef56cbcab7ce390b4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193607758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb193da4bebcab2471ce8f2c19bc9384558aa2f36b62f199d28150b1b74ed56`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45633c98cf590db510fe792f98e984f11aff9efb115fc0d1b5e71e02600b5f4`  
		Last Modified: Thu, 09 Oct 2025 23:47:18 GMT  
		Size: 88.2 MB (88206429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3694bffa6521f60add0b72a0286e5fcd08f1f4989d9a38826f29bdb96c84e6a3`  
		Last Modified: Thu, 09 Oct 2025 23:52:25 GMT  
		Size: 75.6 MB (75563056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcfbcb8e45b031e8478f71112fd2381de6d6ab041c81aa222b7f23cc78a0c4f`  
		Last Modified: Thu, 09 Oct 2025 23:52:20 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8e2371c29ac54d9f5e9d39d681e73dc9908b91495802e656bc403bf3715fda`  
		Last Modified: Thu, 09 Oct 2025 23:52:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:854d90d3728765df6719890ad5adb8fe962aeb0186b0f5a848ea3c0e6bd3ccce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b83d10e891c53b4e33d86c9940c614d3de205de3756773fc22ae31e0ba60687`

```dockerfile
```

-	Layers:
	-	`sha256:720ec1eac4d6a1449a6359761ff146006ecbf88bdcb487bb1bcaa67722f53af3`  
		Last Modified: Fri, 10 Oct 2025 03:39:54 GMT  
		Size: 5.2 MB (5205977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a6b7908400f1cbdae72b3f415f59b37cece763d099dcb4e196501f703258a14`  
		Last Modified: Fri, 10 Oct 2025 03:39:55 GMT  
		Size: 16.5 KB (16536 bytes)  
		MIME: application/vnd.in-toto+json
