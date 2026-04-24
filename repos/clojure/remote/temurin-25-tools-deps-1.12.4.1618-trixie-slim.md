## `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim`

```console
$ docker pull clojure@sha256:e2083072287c0a5180fbe60ef97837d19b4c47114d4802ab3c68df4eec7223bf
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

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:de92536d9664a0ad4d4584dac20a7cf2f4832c53d42bd49837b03c5e4d8f8273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (194048611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d9f6803469df1e550b0a18747009b5190d7689f9baee78b8e817a782a48000`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:21:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:21:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:21:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:18 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:21:18 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:21:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:21:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:21:33 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:21:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff6df917239d3e913de76112b94d5b95a2e5a9cc4a7aafe4c6d35a814487738`  
		Last Modified: Wed, 22 Apr 2026 02:21:58 GMT  
		Size: 92.3 MB (92256281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfd251b2924617442dbb50ae70486f8146958db6ac70b5cbe9feab3ccde2d88`  
		Last Modified: Wed, 22 Apr 2026 02:21:53 GMT  
		Size: 72.0 MB (72011119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7380de37f0c97fdcc32911bee0448b0cdc3a81b202b3253854a62a07963cb1f7`  
		Last Modified: Wed, 22 Apr 2026 02:21:50 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfcd4f2dec9ffcdfce26d00bd7b1497dd89b073b7c5260b0f91a34380ceb3b3`  
		Last Modified: Wed, 22 Apr 2026 02:21:50 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c7669265bfb333d47bc0c8b4b5e0dc92428045ff6484e7e53647ea501d8a733f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c6205fd0989da962345b1c7faba01028977082e6249b27af7bd7d974dabe302`

```dockerfile
```

-	Layers:
	-	`sha256:dac73ba0d168699ad1c7bffd5916a055049b9808b24b7bec2de1b670b0df28bd`  
		Last Modified: Wed, 22 Apr 2026 02:21:50 GMT  
		Size: 5.2 MB (5227278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bc678704f4b0b12a449bccfad1a74e3f03314dde64ff135d0a3cbae76144e8c`  
		Last Modified: Wed, 22 Apr 2026 02:21:49 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3aec900e7ba2216d5a88dca01400b2fb524bd957bfac0a7639662540e278e248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193264483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4c7b5bcad86d4fb87a19043222361254c530a1ff227102e88d9e845ba9de2d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:45:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 01:45:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 01:45:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:45:06 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:24:21 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:24:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:24:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:24:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:24:39 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:24:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3214779e4c6a83f50c16481d42d1e2a6c2802bcae47f725dd458bbb3493a5ef5`  
		Last Modified: Wed, 22 Apr 2026 01:46:03 GMT  
		Size: 91.3 MB (91288309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1a31425f16cb592661b576e8de7c1419913c85bb0a018c8bf2e05b6f285178`  
		Last Modified: Wed, 22 Apr 2026 02:24:56 GMT  
		Size: 71.8 MB (71831527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb08efa56da6ae06c49e2c0659d914d369ab16cbcad74185d77eb026155ef4c2`  
		Last Modified: Wed, 22 Apr 2026 02:24:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd562fdc0d84039c80f85d6f2c25ad77cea348b4ae074182ef7131a2c4f56c4c`  
		Last Modified: Wed, 22 Apr 2026 02:24:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:164f45b9a9b2744b3e9ea4230c9a49e186c3e3080a5d0b88349b5202d79aa95a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154f3aec3a712bcfbfd1048d935234cebc8b72a5435c9c8ccada7f1072fae48e`

```dockerfile
```

-	Layers:
	-	`sha256:9f7cf8c7a2cc2bcd4902edee10d3d3ab668d9d4fe652b3195412ba3603368756`  
		Last Modified: Wed, 22 Apr 2026 02:24:54 GMT  
		Size: 5.2 MB (5233068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d26b625029b240e3ea4fd3ffa79534778343ae8b678858586f0c7e8f656faeb`  
		Last Modified: Wed, 22 Apr 2026 02:24:54 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:5ec684183c5e3459a734d6af2c10ca9b0e14f33c267f95f701de11fad4982292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202661040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45cb589e35c1d3d1c9a40c2019cc1ea2ec301c1786cf5a66f779d8bf5d5ead9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:46:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:46:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:46:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:46:20 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 08:46:20 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:50:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 08:50:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 08:50:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 08:50:18 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 08:50:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312f205a8d7c7914bf7899d6262e3569c67f279b5ea62e2d0808236bb94eebda`  
		Last Modified: Wed, 22 Apr 2026 08:47:38 GMT  
		Size: 91.6 MB (91633137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8116478c5735bd4ae0a77ceda80ff08a7c8f78c611ab0c75a7ddc11dcfd6749`  
		Last Modified: Wed, 22 Apr 2026 08:50:55 GMT  
		Size: 77.4 MB (77428830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebdd7c150432dbc1cde7d76527f8a8f91c7f6bbde5bf096a9d3736f0b20f3df`  
		Last Modified: Wed, 22 Apr 2026 08:50:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74e2d9e60ac794202c12ce5444a6a27d71c0332076ba91417b7b959a5c8ec29`  
		Last Modified: Wed, 22 Apr 2026 08:50:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9da93b75203e2bda19313855df58553df090713960674c4c845c213283beebbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5231526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e983ac63bc9c5e1dca38311982769936f4c9fa8b4eb8155b6045dc9989ad484`

```dockerfile
```

-	Layers:
	-	`sha256:c207f640f56971ee5c7d8c2b0a9dbd97e91d200d517da12a8611a5a689ef1bac`  
		Last Modified: Wed, 22 Apr 2026 08:50:53 GMT  
		Size: 5.2 MB (5214973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adba1ac55756009008799b2357f36ce4a53da4de5ec12cb8adf1387222d198f0`  
		Last Modified: Wed, 22 Apr 2026 08:50:52 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:a55c41d04e5bd5a2d6923580461333493bf27b8e612bc8ddf98b58dea87fa439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (189955555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbdd81ff3d9bfef1412841fe5a16439d9f9052f4b7dc8215b0d9732f93c0833`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 18:44:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Apr 2026 18:44:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 24 Apr 2026 18:44:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2026 18:44:09 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 24 Apr 2026 18:44:10 GMT
WORKDIR /tmp
# Fri, 24 Apr 2026 18:59:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 24 Apr 2026 18:59:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 24 Apr 2026 18:59:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 24 Apr 2026 18:59:57 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 24 Apr 2026 18:59:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c55f344e90013fb17097b23b2ff66d06fed398d9774321dbab29ea1938b95b`  
		Last Modified: Fri, 24 Apr 2026 18:49:26 GMT  
		Size: 90.8 MB (90773403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa61a53c766de33a0867a6185de4ce1d8da3dcf2761bafbac8e7d0451b2cd37e`  
		Last Modified: Fri, 24 Apr 2026 19:03:32 GMT  
		Size: 70.9 MB (70900914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a734b73ce8b86dc93ae83b70b225b9eec02a611f66f601f3c476ecf3bdd565cc`  
		Last Modified: Fri, 24 Apr 2026 19:03:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eade7adc262bf3e13545ccc82fbe97dd7cfbe6ace0a0b9c510b09aa9ae733960`  
		Last Modified: Fri, 24 Apr 2026 19:03:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1561b5fa644ba05c19de1215c7a59852b0d7ed395d29f735afdd34f50c02df5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebdad67faea6af043b20e84c979271feb4fca1599376e5af3455de2f6311540f`

```dockerfile
```

-	Layers:
	-	`sha256:d40d1c9354ca8603061e9bfde9baf03e71f9c5c37b4038d27d203ac5fe6a81c5`  
		Last Modified: Fri, 24 Apr 2026 19:03:22 GMT  
		Size: 5.2 MB (5198765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c3d11fbc9dae4b3d3971fcbd92a533ae089a0ec51b2ce25d2766592bd6f6775`  
		Last Modified: Fri, 24 Apr 2026 19:03:21 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c98374850b16113575bc5b1316f939746f57a003c368ef1c37e7e9691cebe01b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191061580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a117b37a1a908e215ee393100088fb2e564033fef915dab8de99f8414690236d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 04:05:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:05:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:05:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:05:20 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 04:05:20 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:06:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 04:06:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 04:06:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:06:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:06:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f0dbaae84993a6387f129a1f46e9a7bfde4281bb1a1fab547ea5e34e4b891c`  
		Last Modified: Wed, 22 Apr 2026 04:05:59 GMT  
		Size: 88.2 MB (88233796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c8fe53ced4728480d43651c324efcfef5638d535425652bdca24cdf5c6fb85`  
		Last Modified: Wed, 22 Apr 2026 04:06:59 GMT  
		Size: 73.0 MB (72986445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf91e423d6967352f1aa33239e7c7ba536eb7c3ff0e45061935d83d7cae8398`  
		Last Modified: Wed, 22 Apr 2026 04:06:57 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d504e69a16d5e001f182f5b925623848b08b133bcc5575068890f26f697cb1`  
		Last Modified: Wed, 22 Apr 2026 04:06:57 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:32bda9015eba11cb583ce69315d6daa6af32ee65d4cd348f37221a114c6a7e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3902f7c24269df67b331216d243c03acd3ad5f96d1e623cf5b46d3732d8ae4b5`

```dockerfile
```

-	Layers:
	-	`sha256:8f90500564cb499901d032e722a47bb47678af9624750d463b28cce612638665`  
		Last Modified: Wed, 22 Apr 2026 04:06:57 GMT  
		Size: 5.2 MB (5207764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:200583c6d49fae1f092dba82ee74c1ecef2f924f4d4ff06a157370c45c790b9a`  
		Last Modified: Wed, 22 Apr 2026 04:06:57 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json
