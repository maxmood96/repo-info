## `clojure:temurin-17-tools-deps-1.12.0.1530-trixie-slim`

```console
$ docker pull clojure@sha256:74b39b62b2cec528ada6781292ff84bc08d317ffad39f2741e8066ca5a13f84e
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

### `clojure:temurin-17-tools-deps-1.12.0.1530-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cb71f717cc3eaf7043241e76af42288bdd0e0c6ed0a34ec1f1de902648a3ca1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246114386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3066cd2e54e6930ab7979ec28acaec9e9ed3828ec4c5210a26e4be87956d5d38`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ced038dea045df288fe9bdbe03117ca66fe2a071217e196ac86ed07f965fe688`  
		Last Modified: Wed, 21 May 2025 22:27:59 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7042036f48aaf7e71f194d437986a954a71d546ebdcab6ad3323363db568fbd1`  
		Last Modified: Wed, 21 May 2025 23:33:16 GMT  
		Size: 144.6 MB (144634958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d641cc90f166d4fed563295b11772f072e9baa5292e9b256d09ae7c64f618c`  
		Last Modified: Wed, 21 May 2025 23:33:15 GMT  
		Size: 71.7 MB (71723005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fcfe5cb7740ca4a14d84916b41e9d23d1f7106e72aaa18842add34c882904c`  
		Last Modified: Wed, 21 May 2025 23:33:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0854c6f7ff79ab492466b0ce4bc552d78d6d9d599a866ec018a385202ee6e19a`  
		Last Modified: Wed, 21 May 2025 23:33:13 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a3a312c0c707b9fb01211e6d5daadc10186d32cd3fffc226c0b13f4b2ab6beed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5127920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa42245080d23902fa782000b85adfe434785726be198561fabde322d2801bf4`

```dockerfile
```

-	Layers:
	-	`sha256:47828aa183255c9434b9175c98718dff65801d2dbd49223def25ed8216036b30`  
		Last Modified: Wed, 21 May 2025 23:33:14 GMT  
		Size: 5.1 MB (5112065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:564904461c696e905861204c3bedf0cee9b1f05a5e21188660511f24b084061b`  
		Last Modified: Wed, 21 May 2025 23:33:13 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f945b1f190c27139ce25d3e3b7b1fbc893463f51768e1f27bacb7129bd89091d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245279456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e9153acbe8fcec53b55322d315fc03ad7fb2e439fae94ea7e77e8102796fcb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6098c2c9fa277c00ab580ce12bf64a9e1edf9e9139ba18ad85f3cc3063834aa6`  
		Last Modified: Wed, 21 May 2025 22:31:23 GMT  
		Size: 30.1 MB (30119455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3620a9bb9726aad3574bf095dbb1621ceffb53ff75a01d73f301f2d39be71947`  
		Last Modified: Thu, 22 May 2025 08:24:18 GMT  
		Size: 143.5 MB (143512634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8538087aba2f28f6b0723151506e88173f537fb6ddd066cb235e84c36b6cc902`  
		Last Modified: Thu, 22 May 2025 08:28:36 GMT  
		Size: 71.6 MB (71646327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f4e14696be97822bbf13f85c7e7aac3d757e8221c77cf857be247d1879983d`  
		Last Modified: Thu, 22 May 2025 08:28:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ca57c90655dde1b3aa4f2adce4f02d29f1f508706f75b9e9bef0dc2603596c`  
		Last Modified: Thu, 22 May 2025 08:28:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cab5e63d526ddeca4a441a2b6dca55745ed06386c94b244a1d4e418aa9e7a2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f8f693a9211d2f92c90cc10a2b8993eb89bbbc0e427998bdd160d0d426bf1b`

```dockerfile
```

-	Layers:
	-	`sha256:c6c13e608887a5a5a94b729bdc836940c999c6359e9de7a67e7491078e507d40`  
		Last Modified: Thu, 22 May 2025 08:28:33 GMT  
		Size: 5.1 MB (5117834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cfae6341fc93624adc0aa81dce061f6995058fdcf16d8144bcf4c0632b310d6`  
		Last Modified: Thu, 22 May 2025 08:28:33 GMT  
		Size: 16.0 KB (15973 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3bbc7a173dfa45ebd45dcf5a4dc3d494069efbefec7a4b71841698a47c257cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255078086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed638a62f438f01bb8e96aef2170ca2232547bb8753bfdd2519fb9eede43aa7c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:62eecea9deba6eaccef3e829ddec51f2c540dbbb668a68816c8ce3c4b8023d93`  
		Last Modified: Wed, 21 May 2025 22:32:27 GMT  
		Size: 33.6 MB (33580565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752aadd727d13bef3a04ff3f73afe267503571039f4c27b12f32587ffea2d872`  
		Last Modified: Thu, 22 May 2025 11:19:40 GMT  
		Size: 144.3 MB (144280527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a31602d38b4bbfc2e0a5d692624bf2bbc5cc86ef97d1bbe6edc7e898fb6cf52`  
		Last Modified: Thu, 22 May 2025 11:26:09 GMT  
		Size: 77.2 MB (77215955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645229f56d1de587c6536f5013093e7c0350934a05d63bacf35b4364f1914b9f`  
		Last Modified: Thu, 22 May 2025 11:26:06 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd8ce081d4a4cb5dee09e2923bc2e21739c72faf2195df7e47d532c47101a84`  
		Last Modified: Thu, 22 May 2025 11:26:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2eece221cb130fe875a77613eaf2983192aee8e0b6ed408cbcc6c1eeb5ebfb2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7d3bda0cf0c6da41e4c49e29c4daa8c0018bad68bd913967ba1b773542a075`

```dockerfile
```

-	Layers:
	-	`sha256:a0d860d471edba0f60e47a2064a9fdb42c07af158de95a6457bb90c766473a68`  
		Last Modified: Thu, 22 May 2025 11:26:07 GMT  
		Size: 5.1 MB (5116436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cacdcfd936838632ce6669f871155fae675e7c854e7596ee686cdfc419d2c9a`  
		Last Modified: Thu, 22 May 2025 11:26:06 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:cbfb636900921cf8e5711b8756fd397eb03c69cf568ba17e90e882d72b490ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237431166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1384f6e265d2062a9d0792647734491bfb5359cdc26f2966a11bce42f788d8ce`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f092cb6a76bde9a7b3c337ea49e8a7adec71062dc5df097be99d3975e92bc53a`  
		Last Modified: Wed, 21 May 2025 22:38:21 GMT  
		Size: 28.2 MB (28245354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52be1428abfc1929d2ac9f71b808537062706c618ab92200260de881b252238b`  
		Last Modified: Wed, 21 May 2025 23:41:14 GMT  
		Size: 138.5 MB (138492687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc0d552f3e5050fd61c9a97ba28264536d6bf7d72548292af15037acda96e4c`  
		Last Modified: Wed, 21 May 2025 23:56:27 GMT  
		Size: 70.7 MB (70692085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2de3b2e39d8fca55f0fcfff40f2ec56749990642ce920d3f6dba7e6f7480a4`  
		Last Modified: Wed, 21 May 2025 23:56:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c82256aea3985acab18e3ddc535d1e2efbd88932e2776ee451b23f9b1ac43a`  
		Last Modified: Wed, 21 May 2025 23:56:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:11e896a65f29a510dc8c9cd1d88326054f51d4fe5ce8096e98889a1cd83a3243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5115513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836189a3fef0584df0d289e500775d8a4ef38e709ab9383c34e7f700c1ce018d`

```dockerfile
```

-	Layers:
	-	`sha256:e4950d337f6d3911fd31568debfb4b941013f36b396efbc768c1fb83d9602ce9`  
		Last Modified: Wed, 21 May 2025 23:56:18 GMT  
		Size: 5.1 MB (5099610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac7ead1e02a296c6ca8b03d74c83995aeccb0af2437c0bb7b791ace531d4e89b`  
		Last Modified: Wed, 21 May 2025 23:56:17 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:345c7ac252a5d9b9f749141d80b936571db1474843326ec66353d4799d1bfd96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237316292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192ff1848ed1b5ebef5f6e0e00eb5641f5c9ac76c10fad679392187bebfa1e5c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7cbda353d6047374e3da60bdf79ae89f8047840010f0964c87a8f2714e146106`  
		Last Modified: Wed, 21 May 2025 22:32:10 GMT  
		Size: 29.8 MB (29829620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f866fbdbc997a98310a85e809fa09dc3d467102d09761b5f6eebb2aeffa51c6d`  
		Last Modified: Thu, 22 May 2025 03:52:43 GMT  
		Size: 134.7 MB (134673609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe58dc7a0632dd800369af251db76b9abdeba3760b61bf693f873160273b7a8`  
		Last Modified: Thu, 22 May 2025 03:56:34 GMT  
		Size: 72.8 MB (72812025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81efc61cdbe815de42cf2d3ed57986b3ffdd99eff2f11a8816064cbd7dca09b`  
		Last Modified: Thu, 22 May 2025 03:56:32 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667dd9c16de47d800cb0c94d074c769c062a996853a2297679f2ad1ec46e7c77`  
		Last Modified: Thu, 22 May 2025 03:56:32 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3261311457f70583fe50227b2428b6982a4a84040982c935d02449ffa562fb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89306e553e1208cd9f723611029cc7e7c35e1a3bba28f3dba719154c6d014e07`

```dockerfile
```

-	Layers:
	-	`sha256:20de558a6168e6338ec8e1260a8196707b2d59e4714707c272c82a4a3fd63710`  
		Last Modified: Thu, 22 May 2025 03:56:32 GMT  
		Size: 5.1 MB (5107989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5f1766f3306faf25345b01304bd6f0e91d5dafbfa680df37a3a1431c129a855`  
		Last Modified: Thu, 22 May 2025 03:56:32 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json
