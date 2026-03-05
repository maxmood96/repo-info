## `clojure:temurin-25-tools-deps-1.12.4.1612-trixie-slim`

```console
$ docker pull clojure@sha256:e268199389f99b532b7f2df2f27f74f6d4fc9d6ef987e4cfb65dae5b008b7f89
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

### `clojure:temurin-25-tools-deps-1.12.4.1612-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:867aeedca5cb644edcafed93a0d84e2063d268a49b677a88d02a9aaa76198c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.1 MB (194051000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99be2a9ed6e1084648607dfbd442ef84b722cde4d999c0c839554e18339add1e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:51:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:51:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:51:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:51:47 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:51:47 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:52:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:52:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:52:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:52:04 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:52:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5504e4efd2cd7139097303a674f12986c062efa18882487c4f427a10cb4adf3`  
		Last Modified: Wed, 04 Mar 2026 17:52:24 GMT  
		Size: 92.3 MB (92256297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5e48cc091b20c855ed5e768c387d7fc3a55a07016a10e8fb1308272f5dc0d6`  
		Last Modified: Wed, 04 Mar 2026 17:52:24 GMT  
		Size: 72.0 MB (72015030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ce0c928a8e7de885de88318cdce2adc6db44732efeb18d86c487e65846cdbf`  
		Last Modified: Wed, 04 Mar 2026 17:52:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68db0eb2018b44df7993c2acc4da641a2a55b1024b3e043808c4d65047f8fcc9`  
		Last Modified: Wed, 04 Mar 2026 17:52:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1612-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:317bba4351769784ddc80acff7180e8e2928c0a448c95b6458308d89f316916a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33617a8ea399b412f9741c1dc94662c4651cc23384ad9232ceb3a063b587b89`

```dockerfile
```

-	Layers:
	-	`sha256:9ae12d093f822cb68342bfb1c2a31bc3b335fe11f49e8c05e04aed172b4472ca`  
		Last Modified: Wed, 04 Mar 2026 17:52:21 GMT  
		Size: 5.2 MB (5227150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:537bb6edc4ddbeb10f6c3ea3501d9f1290addc98456c650627fd0ecd86b686fa`  
		Last Modified: Wed, 04 Mar 2026 17:52:21 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1612-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3b61a780a3f83acaae9a1f0760019eae4428af6ea831971e0c6bc3b4905749c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193260222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec90837b337e4ec6b41304bb49e80c5428e232c7473d40badf503f26d8bed2e3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:51:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:51:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:51:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:51:20 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:51:20 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:51:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:51:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:51:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:51:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:51:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad8ae84a4b842c626d9e7656049d032eb7c9443add8cde34834cb56209ac882`  
		Last Modified: Wed, 04 Mar 2026 17:51:57 GMT  
		Size: 91.3 MB (91288289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30bc7ffcf2151153c348c874f11f78573f6f68d203f7631bdd6daf437e9fcec`  
		Last Modified: Wed, 04 Mar 2026 17:51:57 GMT  
		Size: 71.8 MB (71830798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6a5e0c94406008668f0d70b50cdb02bcdfaa1e5ec621e5d867ea6ef6a9758f`  
		Last Modified: Wed, 04 Mar 2026 17:51:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea3aa4a563bd93d4e476c6e90c96e05fdfbab5d1ea22d03212a1ddc86b7fdeb`  
		Last Modified: Wed, 04 Mar 2026 17:51:54 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1612-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b8637bca5e3d28d270cbbce0fb59b3769b5ce637e25f9dffb598c67f173b1924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d068eede175ecb4573b446737a35451c6b892dac4763856334f175e25db4d155`

```dockerfile
```

-	Layers:
	-	`sha256:ac3ba5f978ad82523a882a1fbdf21bae66f64e6bf2ca57cd29005032a453f69a`  
		Last Modified: Wed, 04 Mar 2026 17:51:55 GMT  
		Size: 5.2 MB (5232940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11ec9655218b8fc9d6a85cedd2d67980bc533fd93a4bcf0eb7d01b1f05fe3477`  
		Last Modified: Wed, 04 Mar 2026 17:51:54 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1612-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:12eac3b046d04ccf4719387d7e9a2c121a28fa2ae5751098a0585c42edf164a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202661938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b129c5766dcf047f33629de922f6a0772658ac93ec70a3e442f324c74c2754a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 18:12:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 18:12:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 18:12:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 18:12:04 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 18:12:04 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 18:12:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 18:12:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 18:12:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 18:12:59 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 18:12:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565bb8389edab3c5cf2d038878a825d2f59a12ac69ef62c2bbad1ee6fe71ef29`  
		Last Modified: Wed, 04 Mar 2026 18:13:43 GMT  
		Size: 91.6 MB (91632867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b95ba125a9d95c7494a62becadf77dcc0a515a087e44bfccdb6f7202908dac7`  
		Last Modified: Wed, 04 Mar 2026 18:13:37 GMT  
		Size: 77.4 MB (77427811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d39ee457381535613b1f8fdc8d454b533a4fd05efd8786d4436c3ed8b18231d`  
		Last Modified: Wed, 04 Mar 2026 18:13:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d55f5c76a40010dbd2eb1d8c485df48aabf2f6ef887f9622e0bd164b9e6c4e`  
		Last Modified: Wed, 04 Mar 2026 18:13:34 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1612-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0325d0afae563c9b0503c6948f23c20122423f232f8723fe40fe15b84cf20428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5231398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db16dc7d25f74fa9ed57366f5b5046f9db3b115cdee5874570f1932e56e9dd7c`

```dockerfile
```

-	Layers:
	-	`sha256:9618aefa772ead81cb283af939caa2bded22d5bc160103cb86087e6e006c1554`  
		Last Modified: Wed, 04 Mar 2026 18:13:34 GMT  
		Size: 5.2 MB (5214845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70d70f48cb1586ca15d03db0ddc90751dc97665fa5c8922bce359abcce2716f1`  
		Last Modified: Wed, 04 Mar 2026 18:13:34 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1612-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:0c57c2bce1b47139ebf69ff57ea025505b24b728a466db38e0208955d186a5e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (189950110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53b11854c1517f9b88b6a9b327f76d9e6a3c9bce2b81924362a64bf7931fe64`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 11:46:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 11:46:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 11:46:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 11:46:26 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 11:46:26 GMT
WORKDIR /tmp
# Thu, 05 Mar 2026 07:05:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Mar 2026 07:05:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Mar 2026 07:05:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Mar 2026 07:05:47 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Mar 2026 07:05:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e473dd55fe7be2200230572f9e970b4d013f0a4eabca3f6f6d67c88b697e1bc`  
		Last Modified: Wed, 04 Mar 2026 11:53:35 GMT  
		Size: 90.8 MB (90773397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738af451d4d1e137f34cfb6adf69b3938d93085f2f0c9a063e3d2a0218e84439`  
		Last Modified: Thu, 05 Mar 2026 07:09:18 GMT  
		Size: 70.9 MB (70899252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18bf1ed37881e0b4b15bc8bb9662370f8b1a82bab58e80037ab450eefb5f190`  
		Last Modified: Thu, 05 Mar 2026 07:09:07 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba5060e26609f10a596646c56d48456ccfe56060e06986da57917b1f0f681fe`  
		Last Modified: Thu, 05 Mar 2026 07:09:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1612-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2369cdb16daae6044aa7d2392d25ec07b0cf1d46c235baf7042ae0b1fe141f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036869a08b58e38015595789daf60c8a98ccdda169ccfb7f3046cd055c843919`

```dockerfile
```

-	Layers:
	-	`sha256:2bdabfa1004791e4e23bcd6f2357ce18fb61c7403a5472bcc8da3c779a5b570a`  
		Last Modified: Thu, 05 Mar 2026 07:09:08 GMT  
		Size: 5.2 MB (5198637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:884b030158c13f4f2915743c9021fb6348e26d04f343d3982e905c0cd2b2238f`  
		Last Modified: Thu, 05 Mar 2026 07:09:07 GMT  
		Size: 16.6 KB (16551 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1612-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:9428acb1975d8f7281e353e516b4fdac9401ba26dbb72d71727c9dde7aa5d888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191056610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e33e24e82d5694e4672e559c71fa08ef8ee75348daecbad9898c688a24381d4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:52:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:52:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:52:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:52:33 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:52:33 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:52:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:52:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:52:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:52:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:52:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf3aba4e6c936cf63494d6195cf7221b5267bbf28184e53c5727bf4e30ae2fe`  
		Last Modified: Wed, 04 Mar 2026 17:53:17 GMT  
		Size: 88.2 MB (88233824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69c39d8731d68492017d0753f79f1fff9cee12ee81784ff779e2a964a9cc431`  
		Last Modified: Wed, 04 Mar 2026 17:53:17 GMT  
		Size: 73.0 MB (72983568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5563211ec623d82d000d655f179dcb23bd4100c8b70f77d44b3065b82cab18b6`  
		Last Modified: Wed, 04 Mar 2026 17:53:14 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36413420a83adfb493af592f51033cae3271adc9f6857c6ea09b767c7b94f3fe`  
		Last Modified: Wed, 04 Mar 2026 17:53:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1612-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a7ccf83b897d85062c123038e9ef542aa36b3e69a129e067b81d2c817376e340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45d34570173e3f25a84ad32243e625bf39b1b923395e237e52c9c25e5c5812c`

```dockerfile
```

-	Layers:
	-	`sha256:8c111193681972bccf733729cb1e07d222390369c388d5c37168d6718cfbc6c1`  
		Last Modified: Wed, 04 Mar 2026 17:53:15 GMT  
		Size: 5.2 MB (5207636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb04302d44c86ace1478f85de80a1d81c41ada293646d7d8fffbbaefad032c49`  
		Last Modified: Wed, 04 Mar 2026 17:53:15 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json
