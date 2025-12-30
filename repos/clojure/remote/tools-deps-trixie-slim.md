## `clojure:tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:b8c6ba0778ccaea9a9b402d7bf137222fc5934fe2cd447e12db67eab5bd81eb0
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

### `clojure:tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ddba652c2bc9cdf31b23482c5b4094d59c6d867d6ed7e4a61f29132fffbb185d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193815458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7362d23fb96b993e58feef2d3b609fc0d1c3dc862f4379b846fc24d078d75d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:07:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:07:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:07:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:07:16 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:07:16 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:09:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:09:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:09:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:09:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:09:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43541c44d959b354253abe94ff28ffbd6742f2898191a667479851de61254c1d`  
		Last Modified: Tue, 30 Dec 2025 01:08:13 GMT  
		Size: 92.0 MB (92045289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf117d24e59c9cf4fb6956bbdc4ee7f6c23de417f977f2d36edc2617933f67a`  
		Last Modified: Tue, 30 Dec 2025 01:10:20 GMT  
		Size: 72.0 MB (71992597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589d9a9ae031646fd921f5ef38434be43dbd916169a7ec8d51afbd940960ec0d`  
		Last Modified: Tue, 30 Dec 2025 01:10:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54ef427a95e7699ac91473cad5f85ac4a5d12580e5830d19374b7ce292bf5d3`  
		Last Modified: Tue, 30 Dec 2025 01:10:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a5d04dc9704fb30b1874a5f95f24003022b5feceee361172cc3027bbfb7d9c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5223243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e7e6149da686a60fdb3569ad7c3d37659025a271e160c8ca503a60b4f43450`

```dockerfile
```

-	Layers:
	-	`sha256:13270b96a4cc1a69cb57c4f92ad69597567ec7581fe724c76da3d1ab2239e0ab`  
		Last Modified: Tue, 30 Dec 2025 04:47:40 GMT  
		Size: 5.2 MB (5207549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b5c17cbf64db4f3d52171e7bd3c7a99b47a50e5c959e6af05f9fcb048a76597`  
		Last Modified: Tue, 30 Dec 2025 04:47:41 GMT  
		Size: 15.7 KB (15694 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c147bdef4d44bf7b65e6f50a8a8de223b78702f0c38d055a197415031c0747b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192998725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ad90303b353801498a2d833e74721404410a9a1cbef2caeddd6359ee13e686`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:10:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:10:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:10:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:10:53 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:10:53 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:11:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:11:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:11:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:11:10 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:11:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a63ec0d613db49c5650c29e12454adb17a9c2aa6971ac8b9a14a655dae94a92`  
		Last Modified: Tue, 30 Dec 2025 01:11:57 GMT  
		Size: 91.1 MB (91052481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9e3483e140101ff59d49ac5c0f7b1440e0b363aad837ebef01337775f5a027`  
		Last Modified: Tue, 30 Dec 2025 01:11:46 GMT  
		Size: 71.8 MB (71806568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5232f5da1de736c359b04639de2f96da05bf3062872b571aa714fd44fbccd558`  
		Last Modified: Tue, 30 Dec 2025 01:11:38 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f17f9b64c7bc13c51bfc6c72775a8b2532f5fbcf2fa9d3ca7cb342da9ff88d`  
		Last Modified: Tue, 30 Dec 2025 01:11:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1f28573111b14d7f942cd7ca2b50983d72b4a2b84e72e6135c068ce99c627576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae12bfb8c48a99a3eb597b3c81add5c56f71860ca031120936f2fae51d91ab51`

```dockerfile
```

-	Layers:
	-	`sha256:dd71e27f8cdca74d3620a043e35099efa9b01bbe4c9efa4561c030f9cf177820`  
		Last Modified: Tue, 30 Dec 2025 04:47:46 GMT  
		Size: 5.2 MB (5213339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00638b7f1e0d0c0679b0298b4cf1d2ca2da0156380688fa99418b0d066b194f8`  
		Last Modified: Tue, 30 Dec 2025 04:47:47 GMT  
		Size: 16.6 KB (16634 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:0d45639fd3bc2f3d3767e938fc05533879ced0e648610b6a024c5547ac0f2fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202595565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02af09f8f6e813aa2ba00e3a2a7f5d14824a4c292db295402d20387259cd516e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 19:15:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 19:15:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 19:15:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 19:15:00 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 19:15:01 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 19:15:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 19:15:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 19:15:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 19:15:45 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 19:15:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:34b56ab3c5579c93222f3403d640c7a7f19044e9e46a2d1c6b1da60bde918efc`  
		Last Modified: Tue, 30 Dec 2025 15:11:02 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6641751f0ad442566e7584e41ec87027fbbe61b528d316ccc54fec38b944127`  
		Last Modified: Tue, 30 Dec 2025 19:16:48 GMT  
		Size: 91.6 MB (91610756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bbd6a224bab56cbe0076908828e6356a1065033c8ad7acb2dac55cea26fd57`  
		Last Modified: Tue, 30 Dec 2025 19:16:46 GMT  
		Size: 77.4 MB (77386882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ecf27e95707dc1663f22aefe7b8b5b377106522ffa91ed1e69b0c08a5866c9`  
		Last Modified: Tue, 30 Dec 2025 19:16:40 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c407f2fb947ac4d150e5b3b48f5b7c1fa4a09765cceba01dbbb954309307e50c`  
		Last Modified: Tue, 30 Dec 2025 19:16:40 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:269186f8c5766cd8f1548e6153c13c4875eba6290d515d23ce5d4da053f1d03f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc862e3f210e8e52df0b976d4e35a74f93a01caf20b286c23e33a3976f51c84b`

```dockerfile
```

-	Layers:
	-	`sha256:67336d2189dcab35989b8f80babeb262737a1f2bd708962dfccfc1a6208333fa`  
		Last Modified: Tue, 30 Dec 2025 22:37:42 GMT  
		Size: 5.2 MB (5213230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a1228bbce165c2405a4f8d93463b0e6a33c96342091c0c00912a3e2f5482722`  
		Last Modified: Tue, 30 Dec 2025 22:37:43 GMT  
		Size: 16.6 KB (16552 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:cb8d2b948f52e6dec7da81b45e6110b539cd5bf4ceeffbba8fc356e886cc2f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189905323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd042f98246648ba6e65a2200b4d4bfed74fa68140f54154eebc65893c49fff4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Sat, 13 Dec 2025 19:15:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 13 Dec 2025 19:15:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 13 Dec 2025 19:15:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 19:15:07 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Sat, 13 Dec 2025 19:15:07 GMT
WORKDIR /tmp
# Sun, 14 Dec 2025 16:50:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sun, 14 Dec 2025 16:50:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sun, 14 Dec 2025 16:50:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 14 Dec 2025 16:50:14 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 14 Dec 2025 16:50:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a299023170aa749b8b31ddbccaa883d75e32b7625d16dd55056362d3561393`  
		Last Modified: Sat, 13 Dec 2025 19:20:42 GMT  
		Size: 90.8 MB (90752844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf2a7ed85980bf30e8d5220f61e05ff80e32e32140ef09b8967692323640d37`  
		Last Modified: Sun, 14 Dec 2025 16:54:00 GMT  
		Size: 70.9 MB (70878282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb574d8441b0d6a44eaa032a58e5c5a774bdd7e79266cea2fbb9e4432d6dd448`  
		Last Modified: Sun, 14 Dec 2025 16:53:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3e66b6ae56ff64bfd983d122942e1ee7324fafa3ad5b1d2d2e6cc2852b1e51`  
		Last Modified: Sun, 14 Dec 2025 16:53:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b4934955e06e695c9b2a543e29fd94d48eec460505fe84570372f58630797571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb5d59e2792ab95453325c31bf17ffea964cab18b796ff41830e84c9992a245`

```dockerfile
```

-	Layers:
	-	`sha256:c987685c8245c16ea10e6b7dc27ffd5a4e743a70fb9aba883f1271dbc5fe22c6`  
		Last Modified: Sun, 14 Dec 2025 19:37:28 GMT  
		Size: 5.2 MB (5197022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f650b4835f3e00eddac9b5c6ba006b469c7a50c18fae7622498af61d4037f216`  
		Last Modified: Sun, 14 Dec 2025 19:37:28 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:436874561c7535ca9da1d3d9e45931e008483b0c784ecd9f887324a940bf1ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191000178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343eacd5d376ac57d7f71f95052a68eb8c5e1d52081861e136e71321025dba03`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 02:07:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 02:07:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 02:07:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:07:54 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 02:07:54 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 02:08:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 02:08:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 02:08:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 02:08:10 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 02:08:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74841f1c4a0ebccd933982c8ba11ec13d8e8943d851c7e4f7b9b02683132807c`  
		Last Modified: Tue, 30 Dec 2025 02:08:54 GMT  
		Size: 88.2 MB (88210716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21b6315660b286bfa4561ae5c2795c7535660a38ec9fd75c0f029bef30d4fd2`  
		Last Modified: Tue, 30 Dec 2025 02:08:53 GMT  
		Size: 73.0 MB (72954000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925b0c447031b7ca29d5e59a3cba0ebd7aa6b1abadf803eccd88c2d986cc662`  
		Last Modified: Tue, 30 Dec 2025 02:08:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d6a3dc541b9c8a81c72e312d30c0322243512d61858f40d64ac401bfb9fcf6`  
		Last Modified: Tue, 30 Dec 2025 02:08:48 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:39367f61ccd36599804079c03bcee77eebcf5d9f581657e14650cc2e01b31468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9190b6cce99147a5f35f4d996248d6980842718e98b323fde262d1fae3d0d64`

```dockerfile
```

-	Layers:
	-	`sha256:1e8af6d3cec5f965deb41e2f56b67356dbe7e7629ac44f5105fbabbd4c47e2a6`  
		Last Modified: Tue, 30 Dec 2025 04:48:00 GMT  
		Size: 5.2 MB (5206021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63fc0ef9eaaddf655e65967b498dd8293b24314ef9960af0d4a3211bd746dd0f`  
		Last Modified: Tue, 30 Dec 2025 04:48:00 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json
