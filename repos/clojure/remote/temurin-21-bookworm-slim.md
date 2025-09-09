## `clojure:temurin-21-bookworm-slim`

```console
$ docker pull clojure@sha256:cfb32c6662264a1f020e0f1fbe475cea7d580a6505846117ba564f6855ae4678
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

### `clojure:temurin-21-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:664016ace08896f1dc14860a74dd58d1fd861667cb33ef0d1c37391908d97f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255704189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e8c23c8c020c6a788aa368db5f08ecaff55b8b7119e48deb6965fa1d06cd58`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4697fcc43aea84bdd08c0bcc20bc06b0d58b7b532f9709b712f79c06f671ec2`  
		Last Modified: Tue, 09 Sep 2025 05:00:54 GMT  
		Size: 157.8 MB (157804821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6d414712eb88191f293ce65f64225e9107e0e4bc51eed75faee1e866740df8`  
		Last Modified: Tue, 09 Sep 2025 05:00:25 GMT  
		Size: 69.7 MB (69669984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc06154aa223c483db8cd7274d5b9650b11c7c12d0e9eadc3a5333ce6fbb92e`  
		Last Modified: Mon, 08 Sep 2025 22:12:05 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7530f371f7f4a5dffb69b6bd78369b6ee08cac6cee01de79488feb94445a2db9`  
		Last Modified: Mon, 08 Sep 2025 22:12:09 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2937708c3260814e2d3e975c8aadd0d9a0ffc97b4ca006253c8550857aca7204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be783e7141f0a4869cf2c20ea9b398fbdde2659d422599f7abf2454ff7bf57d`

```dockerfile
```

-	Layers:
	-	`sha256:d36921c5801f7c8e0846f8649f10339ab56b7165a492715675c05ae185291582`  
		Last Modified: Tue, 09 Sep 2025 00:39:48 GMT  
		Size: 5.1 MB (5117186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aaaacce53d027d86d213d86616878b3b8875fe99f7c776e2af38bb7b5cdfcb1`  
		Last Modified: Tue, 09 Sep 2025 00:39:49 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5aca6d179f1a0ba124adbc034a7db958dd4cd29fbc6e1b470dbb46c95b6e9d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253743281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c52a2cf63db92e7100a36e3bafb94b20abf70c62c9a6a6a3f3a39883b0c08d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec05fa0c28eac7c363957f9a78ebd6d62d7b0dd10ae5e9e8ad5c56845d86bce`  
		Last Modified: Tue, 09 Sep 2025 00:41:36 GMT  
		Size: 156.1 MB (156081188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec848b71dc587a7386347db9ab9681cbb05e27067f0099891472142f8a66023`  
		Last Modified: Tue, 09 Sep 2025 00:41:34 GMT  
		Size: 69.6 MB (69558957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dea242815006ffcad5886ad92cef5cc852ddc19346fb53fe2332e201f5f9c4`  
		Last Modified: Tue, 09 Sep 2025 01:21:49 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49648be2aa652d6995e443c2a7eec7f47bd159d3f9ae5cf60e12bb4e91b466b9`  
		Last Modified: Tue, 09 Sep 2025 01:21:53 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:04933b918a08ed7ae80c647b5cb1a8b3524f0c733cd8a16f359369ec4319631f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d64de4cd394844c233fe7e112282797837e74c14ed6f12a06b0e52b75638bd7`

```dockerfile
```

-	Layers:
	-	`sha256:147ff0f88ec72132082d34c1d21ebe039e2b96eb6a2749f13f325c93997ac2ea`  
		Last Modified: Tue, 09 Sep 2025 03:39:32 GMT  
		Size: 5.1 MB (5122971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a6ca97d0674c917c4a969af4e2330033acb2f3c53fc71cb47745c0669a31e50`  
		Last Modified: Tue, 09 Sep 2025 03:39:33 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:93c6689d9973ae3946f4bf96e7145cdaf936a988ffd3b8e18bd7375aac189a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265541929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0915e7d375bd9f5c1192126a1465815be2405e9ac5aa3dbb23172e0fd8851dfd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ffd328672fd40878f149855d02f5c91f57260d057b8ee8febb0d0879fefa3b`  
		Last Modified: Tue, 02 Sep 2025 08:52:31 GMT  
		Size: 158.0 MB (157963469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd60fcaf424ed5149916c0da05432fdf9416f6a5e26ec835ce5e42c21f5d742`  
		Last Modified: Tue, 02 Sep 2025 09:04:11 GMT  
		Size: 75.5 MB (75503995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c29a81ea10f3bbbb0bbb623c188e62fcf76e2131307afeabd5d1b51d17186e`  
		Last Modified: Tue, 02 Sep 2025 09:04:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8f260de2b2cfc0d67af70b6a3e2f1471939e44efcb65932c2ea6f92452fa6a`  
		Last Modified: Tue, 02 Sep 2025 09:04:02 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a56ee55f817d7c077a3804ec7cef70460d8b8a98d1b1b17e6e94b007fff895f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5136876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393678ec8d956bc8348135eae3d2b21749119be9dac988471d965928278f4338`

```dockerfile
```

-	Layers:
	-	`sha256:5af1752f5ba4734d4a9988a8e2513fe149901ea5a9caa09bb8041da9369c6c13`  
		Last Modified: Tue, 02 Sep 2025 09:40:42 GMT  
		Size: 5.1 MB (5120241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:583427c53ed8f2f20b0494a6219ca0a03d912c9bdfeb562484ed3343ee675663`  
		Last Modified: Tue, 02 Sep 2025 09:40:43 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:df4345fe3518fd31aa704abe6da11d093303965276c2fd10759087008a52c396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242396964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12740c0553daeea75ff9a39f4562a35e667b12f58f19675eac228ae94336c80`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edea75e075838ed0aa639f17f3b0b7e49fd14ab0f1d51627956073864e0a9c3`  
		Last Modified: Tue, 09 Sep 2025 05:48:16 GMT  
		Size: 147.0 MB (147026941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51c82b960154169deb7d06e83af13c498875280df42ce494a29168aee95d452`  
		Last Modified: Tue, 09 Sep 2025 05:52:32 GMT  
		Size: 68.5 MB (68484684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f4e35f161b0855f704e04069376037687bb5aa8094218db27a7db86ac7d378`  
		Last Modified: Tue, 09 Sep 2025 06:02:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e127eb9da34482c41ddaf943003d7dd7606464b41815a511e4418cd69683e48a`  
		Last Modified: Tue, 09 Sep 2025 06:02:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0d314b9f67198e37459e466e49cfb770b3254bb4cb5d0b702f409dc3712a785a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f4067e0bce13c96d5915a21b24763a3c38e0f07e6bc7e928c8624ea88b5290`

```dockerfile
```

-	Layers:
	-	`sha256:78eae0ad5972ddaca51c5561286bfb73cd8e6274c8f1efaab65e871486da0b7c`  
		Last Modified: Tue, 09 Sep 2025 06:38:22 GMT  
		Size: 5.1 MB (5108507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58695126a00d79a74ce51849df44b2f3e9d0fc8c260e0bc151945168d8a4587a`  
		Last Modified: Tue, 09 Sep 2025 06:38:23 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json
