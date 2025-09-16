## `clojure:temurin-8-tools-deps-1.12.2.1565-trixie-slim`

```console
$ docker pull clojure@sha256:b62efe354c24ffd70ce2bf87cb30c10e069727c860a4d55073f7bdf79f51aef3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d436dc279cbe898c4645fb7391771d18e84bfd3720eddce965c5b5749910ab99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156487641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13130f6cc20b92044caecf58507b0d2271eb625a77adf5be8e7260cf105ee307`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80944def7d21d137666abe7b5f454334c1181d0b1a7f15ee9381e8eafba115b1`  
		Last Modified: Mon, 15 Sep 2025 23:24:46 GMT  
		Size: 54.7 MB (54731324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee3d69766feb30ceae96160e6b17b2a472e207b9b61cc4ba6958160a7251711`  
		Last Modified: Mon, 15 Sep 2025 23:24:37 GMT  
		Size: 72.0 MB (71982177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f215a748c7433dfc049b683f1962c8489d45f1e0c50a01f2aac3628af428f289`  
		Last Modified: Mon, 15 Sep 2025 23:25:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cff79d2f62bbfc4502344a0e681a992313a4f28887cf64fb1365ac351c5c48c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cba8ef971222d84acdf7463a1f7ab84e79c97429d9d54089432a66121d84e96`

```dockerfile
```

-	Layers:
	-	`sha256:f4317a70ab3b9748a90b43f6b829339f4c4376253a20d3d49f67127d8ffe56d6`  
		Last Modified: Tue, 16 Sep 2025 00:49:54 GMT  
		Size: 5.4 MB (5377723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afbb10f7d2b61c410e145821ed235111cc64b009c526a0d2965504d06e3dd63f`  
		Last Modified: Tue, 16 Sep 2025 00:49:55 GMT  
		Size: 14.3 KB (14271 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:90bd13d4af577bec01906d12fe59ca10b4836b6f0a3093fd52404c4dfaf7a100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155776729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b116837cf3bf5b233fd339f2e584070aff221ec6a136aca1841df950509d6d7e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f045457a6b7fcefa9de9378dcdc1772533b6aaf89c78227425a1c3b7009c4ac0`  
		Last Modified: Mon, 15 Sep 2025 23:25:24 GMT  
		Size: 53.8 MB (53835607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08185f53c9ac1157aea70e9464a4d30dd9edee260b7de9bd0975df59c0fe2c2`  
		Last Modified: Mon, 15 Sep 2025 23:25:22 GMT  
		Size: 71.8 MB (71803845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40e2e4aef1661de5ef9e675bb48104f4240b93e2dccae2478d9292c7b1ad891`  
		Last Modified: Mon, 15 Sep 2025 23:25:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:59e0491a0722134fb374eaa289399888a89563f56f1f8de2fa692f574c6f875b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6122ff2d6bef2df7ba7d468ee5bbb8e119867bbc85ab077b4092654747de80`

```dockerfile
```

-	Layers:
	-	`sha256:5f0cd8b5c720adc7358cabb844c6d7ff98c11d55047ebe92dcf7e059fe1ded05`  
		Last Modified: Tue, 16 Sep 2025 00:50:00 GMT  
		Size: 5.4 MB (5384190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73e19dfd71e254ce27d66175188ab63e96d0a362cc25ddaa864a864fda5c9dee`  
		Last Modified: Tue, 16 Sep 2025 00:50:00 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:7ce2e549ae892c36b5cffa1c349a40cddd44cf993a32b5c8ac18a00b009f3262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163158640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed0a48229de9a5ec269c1d9ad88d6b6b9b2acd46954b021f074de1b8c852d33`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262b0555b2bb60c36d7f21b333880d303b345dbd2b24529e7df37706b46c92a3`  
		Last Modified: Tue, 09 Sep 2025 08:54:36 GMT  
		Size: 52.2 MB (52165415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0613f6dc223255f0828aa94ba1e0738de49674efc34c247b4aff10645ef137ac`  
		Last Modified: Tue, 09 Sep 2025 09:01:50 GMT  
		Size: 77.4 MB (77398229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a940643cece891caccc983ad5822a4c0167005e18ca24ce5a0e271ca8fb6af`  
		Last Modified: Tue, 09 Sep 2025 09:01:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3097c4f42b0d70aaeacd10e439822904726034d3b84c283f83c1722fa9831be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af95272c89136839685564ee207aa587c63a0bc438e9e25f375414dd95febd56`

```dockerfile
```

-	Layers:
	-	`sha256:8c58d3b2d6e1196776e1758cbaefa64c814f6d0af170e2b83a44adb1b6ff61a0`  
		Last Modified: Tue, 09 Sep 2025 09:38:16 GMT  
		Size: 5.4 MB (5382687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9a10f2a9ed3ae048a9e47af6092b6483c4789142bb2991bdfe65c992d85753d`  
		Last Modified: Tue, 09 Sep 2025 09:38:17 GMT  
		Size: 14.3 KB (14318 bytes)  
		MIME: application/vnd.in-toto+json
