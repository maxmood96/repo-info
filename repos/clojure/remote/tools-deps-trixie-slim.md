## `clojure:tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:e027e865f1f3e5b84a5840b8e86e51dbf097951bae595921b938fc81da1c8e16
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

### `clojure:tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:87ae54aebe6cff1025a045bf4ae3b05c2034769e37dcbdd01d158e5ec4187723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194401879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad737ca56c73f6bab87816780e3b01c6e210e049818107279b1a0715689421ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:16:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:16:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:16:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:16:13 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:16:13 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:16:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:16:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:16:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:16:29 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:16:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1a535892c33d429684443c5469ea54f368e23ab3f1f61eddab17d076af600a`  
		Last Modified: Fri, 15 May 2026 20:16:51 GMT  
		Size: 92.6 MB (92574564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305254915beb812e48f81550728b63de7cd2b89e4b1830d06ea35212d3662f9b`  
		Last Modified: Fri, 15 May 2026 20:16:51 GMT  
		Size: 72.0 MB (72046045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669624fb8a3612e826cd8b3c31568f89ef09b2dac24f1b32c4d67d7e85cb02af`  
		Last Modified: Fri, 15 May 2026 20:16:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecddf1dcaceb5954de6b1a6ab0baec69ff6ce4f85031275f34a6d4040a5c63a`  
		Last Modified: Fri, 15 May 2026 20:16:48 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:72c64a834ba00cf07edbff972155897bd05cc4d9250378a9525f45322c6fbcc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5244581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b5f2b64dce6f9d167481dc0c8cd491f7bb52d3e9aefff4bda92fab93272568`

```dockerfile
```

-	Layers:
	-	`sha256:d4d74ad40d7d0869c4df61fe10c1ffa050f861276dd2a4f7ca7aa888dc6b34e4`  
		Last Modified: Fri, 15 May 2026 20:16:48 GMT  
		Size: 5.2 MB (5227935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b0e6cdf86d260f326dd4e125e60f843bc56db74ca3e33b508e98d587908d5df`  
		Last Modified: Fri, 15 May 2026 20:16:47 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:169767b29d6d74260caf5a45cd9538af4c507f519efad91377a8c143b32c80ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193541781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421b25cac3ef65e5498af61a55e6dfc3586eabfb588d1a1b048c4f83161f845b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:16:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:16:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:16:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:16:14 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:16:14 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:16:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:16:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:16:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:16:32 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:16:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417c808e65004d4b52c30b70f88571a5c92a3ad98317169d501055711b70baab`  
		Last Modified: Fri, 15 May 2026 20:16:53 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb04b242533c7bfe87d4a43e9460d14df0c68f85455eef8939ce08fde8c059c`  
		Last Modified: Fri, 15 May 2026 20:16:53 GMT  
		Size: 71.9 MB (71854844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdb1a6dbc5d6de119d951a823905898434c9977e14625f6bab48d7e5bbf4098`  
		Last Modified: Fri, 15 May 2026 20:16:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843fa8f64f67cd16ab077dce56e58e6ee84955287e46d4b853822ab9d9fd2704`  
		Last Modified: Fri, 15 May 2026 20:16:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b1b263baf93740a65690947bb306f8d48020bf442654f1bbfbbefa2ad14d0a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5250514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712bac4297995cfdab081ab1f2d88b922c977874ffa76e990b3686e7f486914e`

```dockerfile
```

-	Layers:
	-	`sha256:1676c419ef493a1ebb7bdeb66d20e881d65f2b28a49665878ff1c2d3b3ba2b80`  
		Last Modified: Fri, 15 May 2026 20:16:50 GMT  
		Size: 5.2 MB (5233725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48e5d2a5b5c0218c6b6a4d0bf484e0a3ceae096dc73262b5a55d623cd1aea070`  
		Last Modified: Fri, 15 May 2026 20:16:49 GMT  
		Size: 16.8 KB (16789 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:25f0944fc5188d5a50e748d6a0f796b11927b2641fcd396d9096c262592132a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.0 MB (202970156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583956a49b03b46999795e66e4237f0b6f85c3979df2ab891bf10c6ac7a5ef7d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:43:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:43:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:43:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:43:32 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Sat, 09 May 2026 02:43:32 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:55:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:56:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:56:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:56:02 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:56:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac28bbda9cf605f0d239dc381ad9eec484e7e0bec93b2a70b5e743abff1b6d9`  
		Last Modified: Sat, 09 May 2026 02:44:39 GMT  
		Size: 91.9 MB (91914009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4f47fd9138cd0c2159184fa8a0b930eaf53c1911af579346a8d20641b3e9d4`  
		Last Modified: Thu, 14 May 2026 23:56:38 GMT  
		Size: 77.5 MB (77457016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1689f23c5dcd1ddf846e9db90dc24c9f80e9695e26bafb399a3af76ba63e8763`  
		Last Modified: Thu, 14 May 2026 23:56:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b8d1f358dd6c9808f5c0ae2c45b9a8e6f8959dc52e32ed1325eeb6baf834d9`  
		Last Modified: Thu, 14 May 2026 23:56:35 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eb79d470eace2715118d930a681b53719ea02b08ecfd6987db71e62a9911c8c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5231384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea2c3f9aad2a67c230f4be84a84d02b6bd0aadec835dfa5e91d3c21dcd10a02`

```dockerfile
```

-	Layers:
	-	`sha256:eab8991792f8a95664a41d16745809e19efa39af4c704850a7afaa75041e7b8b`  
		Last Modified: Thu, 14 May 2026 23:56:36 GMT  
		Size: 5.2 MB (5215630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d34c84f4203e30630f832d6e528475442cb5988141245be756827445a4a481`  
		Last Modified: Thu, 14 May 2026 23:56:35 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:0e5ebe1d1dbe9f9635d946d6050ea5a0cebf46ba2d0e2bbf097d1ee6a6de9115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191276555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f99df409d0db4a858d57a850dcad3ebbb7ae3d68fa562f72e7342bf59948142`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:38:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:38:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:38:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:38:16 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:38:16 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:38:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:38:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:38:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:38:31 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:38:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6952bb1d663535da0dd5c38e39c53fd423c23c012766a00ed8340a9bae4ab0a1`  
		Last Modified: Thu, 14 May 2026 23:38:59 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef04e6bb2963610cf361e0348ec67e31ab4cdbf0a169f20e636041e20f4a5314`  
		Last Modified: Thu, 14 May 2026 23:38:59 GMT  
		Size: 73.0 MB (73014843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667592f027f933b0e450888d895639a5f2e797d3cd7635235157f0b39b28cb54`  
		Last Modified: Thu, 14 May 2026 23:38:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5403b9f4daaa1353b0fc3a8cc8f0fa13c2d61170fb23e33238fe2a804baebf9`  
		Last Modified: Thu, 14 May 2026 23:38:56 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d28d55805bd72ce807e7dc9eb5a5040241467459af266cf0f2775b6f4c779ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5225068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6764c32217d63dc1a6e62840a96eab907e3fc57ed1af47c92eb0faf7313e387`

```dockerfile
```

-	Layers:
	-	`sha256:34c2d19c395d0ab528c22dfd83f30e9d45295eff522c5b3c91bd1ca494ea960f`  
		Last Modified: Thu, 14 May 2026 23:38:56 GMT  
		Size: 5.2 MB (5208421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6274c93af5a9c35d01c0c76d98db48de757d2f2964ff5b73af738d05d8e47d93`  
		Last Modified: Thu, 14 May 2026 23:38:56 GMT  
		Size: 16.6 KB (16647 bytes)  
		MIME: application/vnd.in-toto+json
