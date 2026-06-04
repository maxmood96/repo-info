## `clojure:tools-deps-1.12.5.1654-bullseye`

```console
$ docker pull clojure@sha256:c8a002c74d466397c6bb8e8fa8a5205b09f85b1e7059f229206950805badd95b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.5.1654-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:db0e7509e56e06efd9e97a1e2e90f915afc7cc824238a0b4214b19894854855f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.9 MB (212856207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49435d2ce1fe5cecf19f0de9cab213698bdd57c2338ad25513592f07d03577f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Thu, 04 Jun 2026 17:47:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:47:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:47:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:47:23 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:23 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:47:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:36 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348d0ef944c64a2f080b25bf635db26b7fa54855f7beed816e91919754e5eada`  
		Last Modified: Thu, 04 Jun 2026 17:47:56 GMT  
		Size: 92.6 MB (92574586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddd26d5acc43ecd5bccdd1a9c13a415d38c19c9984d1264ea2513ca4924c8f5`  
		Last Modified: Thu, 04 Jun 2026 17:47:55 GMT  
		Size: 66.5 MB (66511730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a322776e818c4e229d0049026e25a0202d40b2e7b31bafacdb4774934551600c`  
		Last Modified: Thu, 04 Jun 2026 17:47:52 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78179a427f0e3dfe8dd61057d5c95f98c67ab2d82fa1f39aa023a6a0de125cd`  
		Last Modified: Thu, 04 Jun 2026 17:47:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1654-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b310a0c3a6758ed8c28a28ec9e5cc81e00df731a59f4e8b08deed6ccb34b4f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7390114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1ceed7f0301a268c74fd14ec16140a84617005add1bec78408c4a3de713fcd`

```dockerfile
```

-	Layers:
	-	`sha256:a516607532652b819c557e92ec16eb46b254808765840c01c79b8b355a5f5932`  
		Last Modified: Thu, 04 Jun 2026 17:47:53 GMT  
		Size: 7.4 MB (7373515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16f37e7ef7ea4d2b71472e2f518480246bcf8220f8f63b281980990e9aad5b2d`  
		Last Modified: Thu, 04 Jun 2026 17:47:52 GMT  
		Size: 16.6 KB (16599 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1654-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:13494b4e47f6f15681d9c5ccac8801f551cb6a1627da05f5752ca7c46845a983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.5 MB (210477723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4257aed85d13f271975e9d2be19eb0133d7e8edaa60681928764201c6708c548`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Thu, 04 Jun 2026 17:47:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:47:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:47:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:47:14 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:14 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:47:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:28 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6291e17decf47606754b03f5b60becdcba3b813f57a6eefb7707d2537c02d1da`  
		Last Modified: Thu, 04 Jun 2026 17:47:49 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86be094addbe1c697a8246579b0e8495d55e16bf8e91174b6c50647ad558c42`  
		Last Modified: Thu, 04 Jun 2026 17:47:50 GMT  
		Size: 66.7 MB (66677850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd200458f89b157e1adb21decc1159c0f6da28aa494655bd96ac40a345a5cee`  
		Last Modified: Thu, 04 Jun 2026 17:47:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4699c1d248a232daf727aaa08b04d45383da7415c97403c3104f8a49227679`  
		Last Modified: Thu, 04 Jun 2026 17:47:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1654-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:744f51d4c64f10f681efbf3ad71fbc199c74a7be391c33917f1e89183c0e2ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a89eed77c4283b9135a8f16a774acce524aa62d157c35f7cb1f0831803215ae`

```dockerfile
```

-	Layers:
	-	`sha256:7bb1b5371baf127d20fd36e124628ae55cbcc1e46a385e23557d7cfc412eeeca`  
		Last Modified: Thu, 04 Jun 2026 17:47:47 GMT  
		Size: 7.4 MB (7378635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d067c6fc0e5c9162d1a20ceaa3c12a79f646bac21e12b882cfdf0ba4436a2c8d`  
		Last Modified: Thu, 04 Jun 2026 17:47:46 GMT  
		Size: 16.7 KB (16743 bytes)  
		MIME: application/vnd.in-toto+json
