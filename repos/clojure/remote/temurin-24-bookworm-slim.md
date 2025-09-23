## `clojure:temurin-24-bookworm-slim`

```console
$ docker pull clojure@sha256:61b33824255ddf1b2d35cb831d5b3ffb94ca3e60180900bf95bce52c4c7ac273
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

### `clojure:temurin-24-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:02f0db9ccacb327adea9be92fe0665d2e9d07a9915365e026ee8977eacdd3048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187879606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b4ce39fd8f03d9fbd552791c10edd86f3ab9ec5ab3b23d0be3462de53243f9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4c576fc14be5baa7031453c3b7950999feb0ed185a937cee737385bb5bbe2c`  
		Last Modified: Mon, 22 Sep 2025 23:47:36 GMT  
		Size: 90.0 MB (89975239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa229a62824edeb3cb9177540cdfdf24014a30ee1ac7ed00ce8398217c0c7e06`  
		Last Modified: Mon, 22 Sep 2025 23:47:19 GMT  
		Size: 69.7 MB (69674976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1a3e1ca2d5c7b487940ae370581711ab03265ef24ed0e2ad591e384c1e9ad3`  
		Last Modified: Mon, 22 Sep 2025 23:47:21 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85a1ca07b987fb6a1046fac2ff4bb45041fb04908c88cd0e609b33f7f7790fc`  
		Last Modified: Mon, 22 Sep 2025 23:47:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:81c268ff4cb333ab7de388eb2ddc5bf55eb3c2772b9a03b455e044801c89ffa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5079908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4252a796ecffbdacbce2ce72d007ce1b0f14d1584c5420fa6e87c879bbc1c4d`

```dockerfile
```

-	Layers:
	-	`sha256:7d64b3b2b4abe87494d9b65aaf2a4ad7d810320ebf37d7f58b626a40d9426052`  
		Last Modified: Tue, 23 Sep 2025 00:44:07 GMT  
		Size: 5.1 MB (5064036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a5528d75f059485110a152563996ddcf278e7e40e2e1882061a5b1d05bda2bd`  
		Last Modified: Tue, 23 Sep 2025 00:44:08 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a87e4fb62dd6d9612e471806635e42aca6d7efbc73f793c0a57f0c1e8cc72d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186759191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2961d64f25f3e5f084009c212fdfc3c643d901b5565af0a28fe03c8c802d298`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b82057c86042446af9b30924e9709bd59ada723ea36acd92edd35a1b0430615`  
		Last Modified: Mon, 22 Sep 2025 22:21:01 GMT  
		Size: 89.1 MB (89092491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bb3dd37c494d3766b8a4c96feef2134af8fac2da7d3050db6c3bbc16838da8`  
		Last Modified: Mon, 22 Sep 2025 22:21:08 GMT  
		Size: 69.6 MB (69563559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a42c94fff9950c21fc16150226da94cfe1d346b0f1676e8ef8bd30e22475ca7`  
		Last Modified: Mon, 22 Sep 2025 22:20:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609871cfcbbcc0ae4d6bbe1a239a154c1e2371af4f1a952e853982ae5d843632`  
		Last Modified: Mon, 22 Sep 2025 22:20:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:07cf929587bed7fbc6dc52f15a1dfc9ab50dea25c08c3ffb2fb8229aa441754d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5085784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4861dadb470b480572836b0e8422bd2f25ffa6389d00e31101d71d2faac865`

```dockerfile
```

-	Layers:
	-	`sha256:8a3e911041734cf320fa3e0ddb277e0676463c2846ff69d23622b8acde579f42`  
		Last Modified: Tue, 23 Sep 2025 00:44:13 GMT  
		Size: 5.1 MB (5069794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5f3bbc4a18dd741acbbf7e5df707e41ff8a77c70933156b611bffbbd6513aad`  
		Last Modified: Tue, 23 Sep 2025 00:44:14 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:38cfd1f8581ed1aa214573a119cb98fc755417425f7a7b7b99baa2d7046af781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 MB (197501497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c40b4477dbd978d3de226c522df8591207055fb863b114742447e61e545409`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fd09d5192cc7e3cbe99d4d308da8fdfddb81b3944db144f97d3a1682452e5f`  
		Last Modified: Sat, 13 Sep 2025 03:51:41 GMT  
		Size: 89.9 MB (89918193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8b7acbaa315771dbbaf3c50703a5a7d4bf17e75440d5b74d2ba7bacf9d6cc6`  
		Last Modified: Mon, 22 Sep 2025 23:25:17 GMT  
		Size: 75.5 MB (75513498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf07af94cab0dcfe50bae43db0d684352fd23da950730395bea9a66d41f29cd`  
		Last Modified: Mon, 22 Sep 2025 23:24:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e91ac62c2978eb01a3b7d336472ec83f1a8f67ed73189c17c9396dddb4b2b5`  
		Last Modified: Mon, 22 Sep 2025 23:24:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ebe7085916e04d8caf3418392e5661a8e674eec9faf15b1c89db9e796a480ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14714f3f490d6ddc739ce829a1cb5016878757a636aeebdc3b5e054c495f8afc`

```dockerfile
```

-	Layers:
	-	`sha256:3a45cd92fe29cce3dba97bc0615a94cbf0c631f3a150818526806a4d6b28a617`  
		Last Modified: Tue, 23 Sep 2025 00:44:21 GMT  
		Size: 5.1 MB (5070492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a991bf063fd5d50cf4fc04849ac238180dd564885d02b9f6ca4906cfe91a7c73`  
		Last Modified: Tue, 23 Sep 2025 00:44:22 GMT  
		Size: 15.9 KB (15920 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:9722fe7bfe9fa50c61f35e1a91cbca82883d556b968d0382d2f3974e0f059092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180602417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab32fe91375f74f741bc05998f14877b8c2951d3b2d4a37b6d94c9fe25c7c74`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8062d35212474884f57e135a7c513bcb3237247281dcb5972254c07f21343289`  
		Last Modified: Sat, 13 Sep 2025 03:18:48 GMT  
		Size: 85.2 MB (85226409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff4687ffa539116351f5d0b28a6c2712ea7eb9b4a49664f37aa34a3c66d8461`  
		Last Modified: Mon, 22 Sep 2025 23:21:17 GMT  
		Size: 68.5 MB (68490668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b31ad0bd83b7b378c92fd92579ab5ebc178124e64159d789eac7f0afa55e8f0`  
		Last Modified: Mon, 22 Sep 2025 23:21:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c746c5c1b94d48e440b1714988f4691747c0bcd65226201cf8f665a67fb4878`  
		Last Modified: Mon, 22 Sep 2025 23:20:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2e28a2e9212b883f51a475a0829478b055214e841c9fc01456e71986ef42879d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5073777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72db906e19fd17616cae83c57bfd9c04e98cae30faced90afa60a1d8779d9c88`

```dockerfile
```

-	Layers:
	-	`sha256:70ac889e4117d9662cf54506eb2035faaa6fc75eaf59b68a28ea2521c735ebc6`  
		Last Modified: Tue, 23 Sep 2025 00:44:27 GMT  
		Size: 5.1 MB (5057905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03f2440b444a01f517c3210cfe22d6d6117b5deea17a5cd9e8dfb674a7c757e2`  
		Last Modified: Tue, 23 Sep 2025 00:44:29 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json
