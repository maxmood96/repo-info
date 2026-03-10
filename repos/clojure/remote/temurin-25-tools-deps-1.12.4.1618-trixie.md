## `clojure:temurin-25-tools-deps-1.12.4.1618-trixie`

```console
$ docker pull clojure@sha256:59c6df3d8fe9ec1a7d4737e9483ce016353d5442986b130eeb3f2954bf718d06
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

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:c9df8cc74081a3e397854e968c26dbe5b44b2434dd31485048a2d62ceb72ef24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227117956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ff22cad1c108cb01182ac0219ca1dd2072d05455b534dd6f13b32100599480`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:36:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:36:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:36:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:36:41 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:36:41 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:36:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:36:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:36:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:36:58 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:36:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4406970ff6595c598a4e21a88e9474cda722bb063ef518eb1f9517bc6f12df3f`  
		Last Modified: Mon, 09 Mar 2026 20:37:20 GMT  
		Size: 92.3 MB (92256329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab853a65086c0d7111a10fbf19157b7531ee6d350b74b624262bcdada84ae35`  
		Last Modified: Mon, 09 Mar 2026 20:37:20 GMT  
		Size: 85.6 MB (85567463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292a906c0b422fa5e89a116609089843edbe22cf816be566680787a5eacc2e7e`  
		Last Modified: Mon, 09 Mar 2026 20:37:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2a1ff2c6c6a8818af1889e867cffc9bdb9c7f08352002bd835a8c146540572`  
		Last Modified: Mon, 09 Mar 2026 20:37:17 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8fa854822242f055aa89e3917442c5f58063d1ca287179ce31509675dcba83a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7455074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6515190d089322db298abf14b8585b40b171e5a1fb0cf3ed21a2a698b594cbc`

```dockerfile
```

-	Layers:
	-	`sha256:439760117a810c7ad9577a3f7112d7a362d309815abc2e6a8965ed74b770c2ac`  
		Last Modified: Mon, 09 Mar 2026 20:37:17 GMT  
		Size: 7.4 MB (7438659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f7dbe891ac7b93832476a416de260e2d1679d6c89edf02f9375ed4dd747d118`  
		Last Modified: Mon, 09 Mar 2026 20:37:17 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:32294fa3bf395dd71519d163bc6f2138d85982313a8123410f043a2a91427e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226324497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:918b80db91b09759a7332c05fab47d5ea4bc2e3332d512dae55c667813d06d46`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:36:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:36:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:36:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:36:39 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:36:39 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:36:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:36:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:36:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:36:58 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:36:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f32f1f8f75656177835045458ac3248fc9dbfd96819e034daa331619eed12c`  
		Last Modified: Mon, 09 Mar 2026 20:37:21 GMT  
		Size: 91.3 MB (91288290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e45f3c4fd7338dde05127c7f509a3c350bdf7b6eea3f5e1d196fb6191625cca`  
		Last Modified: Mon, 09 Mar 2026 20:37:20 GMT  
		Size: 85.4 MB (85382995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a17c51f822af30c5fac80efeef6868e1df8903cf0f5aecf8cd9d62ef450b2ea`  
		Last Modified: Mon, 09 Mar 2026 20:37:17 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d928c01980003d1a0e2a6430ab1d954b6461e7f594bb698d0706483791771314`  
		Last Modified: Mon, 09 Mar 2026 20:37:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:15d5d20301ee55570379effee264786ac19b027fb2527f4fbbf870c3e1991b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7462267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b062672ea9928ff24577ef941d92938abe2e3a00dc43012fa648ad21aa04fe`

```dockerfile
```

-	Layers:
	-	`sha256:96e3a80245c6e3f50b2fd8463dec977b050536d50263e393e1e5e9a8c698c053`  
		Last Modified: Mon, 09 Mar 2026 20:37:18 GMT  
		Size: 7.4 MB (7445710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34e5375ad4656010e02153f9ef5c74e73b161badf8462d6acbd171d398403620`  
		Last Modified: Mon, 09 Mar 2026 20:37:17 GMT  
		Size: 16.6 KB (16557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:504f4d61b6b0d9456c2e9bd56cbe8b4a2a98f20a90e404f58360b5dc694e96fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235723822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9dbcb8910e09df43b4c9462a2dd853f0e2c002f79e90867453c33835f324c7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 21:09:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 21:09:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 21:09:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 21:09:36 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 21:09:41 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 21:10:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 21:10:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 21:10:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 21:10:55 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 21:10:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6acdff6d79e7690911a08c603866c0b781f4a47b1f3b956653bdc69af9a247`  
		Last Modified: Mon, 09 Mar 2026 21:11:43 GMT  
		Size: 91.6 MB (91632868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5654c105cdb12bcb304a0e12e31df6ca12b61e1e7030daf06cd05e276ea55595`  
		Last Modified: Mon, 09 Mar 2026 21:11:43 GMT  
		Size: 91.0 MB (90977649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e45319e0466bbb9e79b2c129093f40989a8bf17ed05f25faffd5e41334e656c`  
		Last Modified: Mon, 09 Mar 2026 21:11:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b479e0db5839dd50f4b8a97eb0c0505698771997b67b7561dc18ba4568f9f179`  
		Last Modified: Mon, 09 Mar 2026 21:11:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:379363485d09c157817632c9cdd3cb7ceee7123c5871f8c63ea7be38598090b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf18a696f48baa8f8c3920c1cf7fbf3ea3bb44006dc3c40bf4132663cd5663a`

```dockerfile
```

-	Layers:
	-	`sha256:60b02465e82a435fb3988c7c2175578e85d21b4fc6b141d4e8858d07eb5b4547`  
		Last Modified: Mon, 09 Mar 2026 21:11:39 GMT  
		Size: 7.4 MB (7426404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e53bbdd15ea3a1e67b0b2596e8a25078405aa2317a2fea9416912d65ed9e834d`  
		Last Modified: Mon, 09 Mar 2026 21:11:39 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:6bd1ea0a91f7cce14164aaae7c8b57a2a52e08d90fab53a3bb0f9ce9d506f1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (223004034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab41788c4662d26a7edafae2033485d4810699bf9139223f3db0d2b1fe51607a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 11:38:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 11:38:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 11:38:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 11:38:19 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 04 Mar 2026 11:38:19 GMT
WORKDIR /tmp
# Tue, 10 Mar 2026 02:02:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 10 Mar 2026 02:02:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 10 Mar 2026 02:02:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 10 Mar 2026 02:02:56 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 10 Mar 2026 02:02:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3be247472b67578a1d05739722d8adeca41098796e5d6210800176db58046fa7`  
		Last Modified: Tue, 24 Feb 2026 18:57:42 GMT  
		Size: 47.8 MB (47776936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8c80deefa5794092a24432da9b0e8a50fb59fc32467cb68891a413c01800f5`  
		Last Modified: Wed, 04 Mar 2026 11:45:55 GMT  
		Size: 90.8 MB (90773397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fcc77f0adf22568ae26b70577392e278629bda55f55cc024df6e2035661326`  
		Last Modified: Tue, 10 Mar 2026 02:07:56 GMT  
		Size: 84.5 MB (84452655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783ee3ffac8cfb705f508203dd7c61976edfed3105a8e327df47c02968c9a136`  
		Last Modified: Tue, 10 Mar 2026 02:07:40 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb06b8943050b8e9ba1bb56f7901c66db1e42fc7623fb006c188f556c0969c4`  
		Last Modified: Tue, 10 Mar 2026 02:07:41 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4f43c781cc7ac1cb91c36856c4b82c28a72d76d5cd2d6c6c2839abe381b800a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebb376d4bde25ba159e4d1fcef9982c215825ba93b45edad2430c1d9582ad8b`

```dockerfile
```

-	Layers:
	-	`sha256:8e79d7e5857759f6a1e58a2f59939f4520e70b432a155406d96f5003e2686359`  
		Last Modified: Tue, 10 Mar 2026 02:07:43 GMT  
		Size: 7.4 MB (7408597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f20612dafba217a4658333072d2b0e9b915eb9e33bbe22cccf385f0ff16800bd`  
		Last Modified: Tue, 10 Mar 2026 02:07:40 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:fd85333877fa6fdfb8221055b26810e2a009a7ae5060456a730bc90b71c83815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224119325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615228ef79bdc9f246dc935715015dec57b6367b7a1108d3ec1646de204d81fd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:37:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:37:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:37:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:37:48 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:37:48 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:38:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:38:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:38:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:38:04 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:38:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e4ff5064e305cbdd6c66eb4d5ef363945adf4aca10628b0d7f6e8bb31eb62b`  
		Last Modified: Mon, 09 Mar 2026 20:38:43 GMT  
		Size: 88.2 MB (88233822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86a3240916c7d30b4baa0d4f2be0bfd6f666b107e0e852a50eb647312e13d86`  
		Last Modified: Mon, 09 Mar 2026 20:38:43 GMT  
		Size: 86.5 MB (86529927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bafc3398ae4e30698038e66d7f710525520e44535163befbc64201a1c7ffccc`  
		Last Modified: Mon, 09 Mar 2026 20:38:30 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3ffb275d02726f2fee607e5f1fcfffde166d853750019d19f31930fa92782d`  
		Last Modified: Mon, 09 Mar 2026 20:38:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:153de47563c942deba69b504be45ef34011159ede42b39b52bf353d5990b004d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1373c538565cd449c0253133c75d3f2a65ddb9a6f3c2a5279f5fbbfe5c2a8b0`

```dockerfile
```

-	Layers:
	-	`sha256:08148375c4d6c3e44f6584b8df0787afb20e2e2fb3e78bdcf74e390a0dec9de8`  
		Last Modified: Mon, 09 Mar 2026 20:38:32 GMT  
		Size: 7.4 MB (7419143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c9393079190663cb00a69ddc329e7060e544bee17fce1c09a2f9fbd240899ce`  
		Last Modified: Mon, 09 Mar 2026 20:38:30 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json
