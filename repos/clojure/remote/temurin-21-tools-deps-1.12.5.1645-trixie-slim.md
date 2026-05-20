## `clojure:temurin-21-tools-deps-1.12.5.1645-trixie-slim`

```console
$ docker pull clojure@sha256:5132f6476bcf7c53665f7aaf50d12215efcc5a7a2f5841d2dc1f4af3ff004355
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

### `clojure:temurin-21-tools-deps-1.12.5.1645-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:10d6eda8bba5530454766a3ed07af0762a7cbcd56bebd6f6a9589d981912755e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (259995605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a69873c40fbf2a7634054de3c074e6cf6fb94d21a271ab8ff83090dcd5afa2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:25:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:25:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:25:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:25:30 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:00:02 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:00:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:00:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:00:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:00:19 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:00:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb63553a90f0a42fcb01e633c66c4d15b23f88411ac6fc22f2ceb2ede5674e1`  
		Last Modified: Tue, 19 May 2026 23:26:24 GMT  
		Size: 158.2 MB (158166966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ecacab44ed8b9e0caf7a32e3c69dff11451e136a302b7a570f4683e4d9967bc`  
		Last Modified: Wed, 20 May 2026 00:00:39 GMT  
		Size: 72.0 MB (72047671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80df4a12d13c69269fd1598c16d4babef6ef05cf390bf7fa3b3b45f104c07bf4`  
		Last Modified: Wed, 20 May 2026 00:00:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127a05ebe699830fa998d3ae62da26eef438541ff87917b9a49983f3de37fa40`  
		Last Modified: Wed, 20 May 2026 00:00:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1645-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0a4f4e459324947f680d437f7d7f0c8e31bdf8fdd4abd201997cb90da703e68f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c64526e1b65c7750b0d05855b3ac9da7000557d42a5bc750638c848cc4c05b`

```dockerfile
```

-	Layers:
	-	`sha256:a72cd2444533004e216b4ccfb8e1e08b7127c8825519af4a5e0745485003fe3a`  
		Last Modified: Wed, 20 May 2026 00:00:36 GMT  
		Size: 5.3 MB (5261819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:717b13d0a71e7bbf1c594b01d8583c1d929ac5bb7e20b961ba0f399c7bf2097c`  
		Last Modified: Wed, 20 May 2026 00:00:37 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1645-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:75d9792b771befdc6e758e1f35b947122852f052d8de4c73d13a1a4cb6e3d1e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258475858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb231d455dfc9f007cbc0b120ec40cef80286eafd670c01a4c1e33d7d3bc4930`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:07:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:07:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:07:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:07:16 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:07:16 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:07:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:07:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:07:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:07:33 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:07:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39ab163c22f24e64388d964fa367a53cead2b194d358816c341afe406775fea`  
		Last Modified: Wed, 20 May 2026 00:07:56 GMT  
		Size: 156.5 MB (156461324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079d55e061eff1783d3d5a885bf1a1b074a71d758e49f6738a97d6ba4802d48f`  
		Last Modified: Wed, 20 May 2026 00:07:55 GMT  
		Size: 71.9 MB (71871571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd6abb4f161468becc7f93cedbf94d8e19ed34c012644a60191c685062ba0d6`  
		Last Modified: Wed, 20 May 2026 00:07:52 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2f62f33ae235dcb50d54397fba228bdfb560177b6af1b6d0b17949cdd7ebac`  
		Last Modified: Wed, 20 May 2026 00:07:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1645-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5703370dad89e8787d4c2da8479a599326626767386006cb2e05712f4ebbc939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5283664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f91486e5d0cec69938898989597c44ffdee69eff031361a6c9d0f16bb7a38b7`

```dockerfile
```

-	Layers:
	-	`sha256:ecc957054659358b055b5e00ca46ef38d7ad151e182d4feb31d6da67c043bc39`  
		Last Modified: Wed, 20 May 2026 00:07:52 GMT  
		Size: 5.3 MB (5267580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fad40d98d61beb6d45b42af5b26115ac5e803805c0c3c09b68efc0609594c9fe`  
		Last Modified: Wed, 20 May 2026 00:07:52 GMT  
		Size: 16.1 KB (16084 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1645-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e817fac9d32647520c3b52f303bd23dc4abed842090b3bb13fee1a13e92c44e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269398646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56704d898525347cd0ae177dfbb0fa63e395af6ed46109e1c0c51506d94cb561`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:37:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:37:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:37:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:37:56 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:37:56 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:30:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:30:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:30:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:30:51 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:30:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9429fc219825eaf2a233c26bd84cdc3eef77eb70dd8fad888800a28c7609e2e4`  
		Last Modified: Sat, 09 May 2026 02:39:07 GMT  
		Size: 158.3 MB (158343282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afc6c187204cf5615f44697bf9a615145efb166ef57d2343b22f8b8e11090c0`  
		Last Modified: Fri, 15 May 2026 20:31:29 GMT  
		Size: 77.5 MB (77456237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc7eeb9f004b964bfb5864b58e3f312857bd3bbe52ca4757bfb59f8b0ca7e93`  
		Last Modified: Fri, 15 May 2026 20:31:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dee112fe3ca36efed02bcda7209647b7f910a22e3b3d32ddb6e64ac5f92b16c`  
		Last Modified: Fri, 15 May 2026 20:31:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1645-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aeefdcdc2cdcd04e03458bc0c7b461633cea9a2f2c86f24b8a3dc97953c5c9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54218182ea599e96d5b7d495c203451844d1b2ed9ca3b744126a52f591fbfb1e`

```dockerfile
```

-	Layers:
	-	`sha256:e23bbc54757871a4a1e4a2fa8f304820ae59e4ec61c1231c21da5118dfd714fd`  
		Last Modified: Fri, 15 May 2026 20:31:27 GMT  
		Size: 5.3 MB (5266076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b741602841b76c0b4c966002c1e257eacc7dfb99e6b73a7d5e0ee0e1d248a3a4`  
		Last Modified: Fri, 15 May 2026 20:31:27 GMT  
		Size: 15.1 KB (15059 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1645-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c13c8f1a0ac6bca079a51ddebc768819ca05c43009b0f422ce8a6de6f2cad6e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250245012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38414178b2264e9ddb35f598618e383e14e39e9e2b51634d7811dd441b593975`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:29:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:29:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:29:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:29:25 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:29:26 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:32:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:32:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:32:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:32:51 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:32:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d6b2e9210ade672c80e699b87d922bc5ac522046d84e1a1c114ba8bba4ba9b`  
		Last Modified: Fri, 15 May 2026 20:33:58 GMT  
		Size: 147.4 MB (147388338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0f250b19c784ccc4f3a23cc2ebe95ed57132e5946e720eb4d6e15606589e70`  
		Last Modified: Fri, 15 May 2026 20:33:56 GMT  
		Size: 73.0 MB (73015282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0e04e1d54bf0e5b667077684c85ca0088110875248520347cdf096e0a0833a`  
		Last Modified: Fri, 15 May 2026 20:33:51 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff1a672faeeeb99c835924a363c2b3625d72034fc038af297c3c2a2c565cc18`  
		Last Modified: Fri, 15 May 2026 20:33:51 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1645-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:68662129c3962cd1534393f72a871d321e3a59d36c7d584a8a60878a8bc30ed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65b75fb8859b7e10808b52aeef125f84ba8a53e5f97d1b5a34bfcdf08f91b07`

```dockerfile
```

-	Layers:
	-	`sha256:23fab76404bea38cad4191261762e4e6c38574aa47ebc3a9733d924c53affe6c`  
		Last Modified: Fri, 15 May 2026 20:33:51 GMT  
		Size: 5.3 MB (5257629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83688abe2b110d4f53909a08b1ceb757374b175b303924bbaa52f47af2d70e5d`  
		Last Modified: Fri, 15 May 2026 20:33:49 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json
