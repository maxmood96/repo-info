## `clojure:tools-deps-1.12.4.1602-trixie-slim`

```console
$ docker pull clojure@sha256:3174c51d4705470ee29f15c48f321931b63350e77bdda439abb0b2f71391ae40
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

### `clojure:tools-deps-1.12.4.1602-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7b18a28eb7f59441561bc70d8dd356a05b6efe27b3ffc3f138d1381e0475b1d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193820767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac9c74fc22a0168cde3856a05d4547b1c631853685bfffdcc0c03bc287f5184`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:23:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:23:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:23:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:23:21 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:23:22 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:23:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:23:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:23:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:23:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:23:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b540b3318991f4e54a0471b3f77dce1c1123964264a53d0ae8209e7a2e6a9359`  
		Last Modified: Tue, 03 Feb 2026 03:24:00 GMT  
		Size: 92.0 MB (92045302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f58928dd350de9cfe22f0248a8ece55466cbb8a1aae759a56ab506f8f0a75c`  
		Last Modified: Tue, 03 Feb 2026 03:24:00 GMT  
		Size: 72.0 MB (71995828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad05bb0df7c12faa5d2ec1251b5f466c52331561769232d97cf9880eb7c401e`  
		Last Modified: Tue, 03 Feb 2026 03:23:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3522889447b74cd2e29b06ece1f1b7c925e97a1f52a7dcb66e466b22838644ff`  
		Last Modified: Tue, 03 Feb 2026 03:23:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bf2b05e9ae7b6e204b1264e224eafbc1c1cb4219b674ae3341d66531ebf5fb0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb321fe2eab2a9bc2cca65d485710d1e7bd28b169b3f4138ab9d89da672dfbe6`

```dockerfile
```

-	Layers:
	-	`sha256:8891dc6aa94e3962eabfac3eb26e2cf9603e1ff2b6e1ec978a651bcaf3a5865c`  
		Last Modified: Tue, 03 Feb 2026 03:23:57 GMT  
		Size: 5.2 MB (5207649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c116ef852da9dbc466d6ea0b95028869391302f7db737c12628d89eaac9983ce`  
		Last Modified: Tue, 03 Feb 2026 03:23:57 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:72387029d63fa5b36c97d4ec88f27ff7cea5fb26bd21d11f7a29f804be7543da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (193000202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b7318a5825062b68d69968a01afb6402281fe928678950ddfaafcad21d5e759`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:25:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:25:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:25:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:25:44 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:25:44 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:26:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:26:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:26:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:26:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:26:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9933a2c1c0a153814ddb64b556f62b410322f37479af4eb2a4d1735bf4b2099f`  
		Last Modified: Tue, 03 Feb 2026 03:26:23 GMT  
		Size: 91.1 MB (91052508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612850548fa3d50fc0aa0bf71812cf029232fbf0805e226bad353f3871911d6c`  
		Last Modified: Tue, 03 Feb 2026 03:26:23 GMT  
		Size: 71.8 MB (71806588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6fcef2967b8a40c9b5ceb055f024bb74ac9dbaa8c262ef1ca0bc86fa6658943`  
		Last Modified: Tue, 03 Feb 2026 03:26:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4683204efab797549e4aa087466c7fdc841a33f17a8894f8cb20182b741b0852`  
		Last Modified: Tue, 03 Feb 2026 03:26:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:60610c42a182f0fdfad0539dc199857404d8192d14c97ea4db2f916e1dc3480d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5230074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1abec546f3c3bf87a48e3150a1224f8fb6e02eeda804560a2c42a6ef2f8a53b2`

```dockerfile
```

-	Layers:
	-	`sha256:7689ae261da9e8ef8833d2610b10044a369b239fa5716589592ad50347820a8c`  
		Last Modified: Tue, 03 Feb 2026 03:26:20 GMT  
		Size: 5.2 MB (5213439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2595255174e7c49a7dfa84dce7b324c7fb553608cd6a705037f4d7b640ee776`  
		Last Modified: Tue, 03 Feb 2026 03:26:20 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:0b789dc7d201da8a6c3455cda4749bd46a6e3581df0477fe952edf67e1a235de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202601873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbbef749f9854bae508b87a8528d768c8f2a03b98da842acd4c128f3e7908faf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 09:55:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 09:55:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 09:55:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:55:09 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 09:55:09 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:59:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 09:59:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 09:59:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 09:59:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 09:59:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f10a9e89797e7a2bf9c3797106afccb3e72751ad9db3091c001fdcec0c24eae`  
		Last Modified: Tue, 03 Feb 2026 09:56:27 GMT  
		Size: 91.6 MB (91610788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e3953fd87d2933109ce3dbf33b3fec8b699fa51814532f3317f2b63a6bf68c`  
		Last Modified: Tue, 03 Feb 2026 09:59:45 GMT  
		Size: 77.4 MB (77389855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6621c59f259f708590f9569054455ff68376c8a508166729d6a114445893e603`  
		Last Modified: Tue, 03 Feb 2026 09:59:43 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11dc462e3cb1b038a7886d5d66777fffbe837edc2ff0a3e9360dbad07e4b0755`  
		Last Modified: Tue, 03 Feb 2026 09:59:43 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:387dd95476d52f39996f61811dfdd0c589862b7308616de82d0492a857323494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be717d3f1d568dd0cd0c6291a6c2d6f5a3b41c768ca5a3cff9fb1f3887dc659d`

```dockerfile
```

-	Layers:
	-	`sha256:347e0a46e10829a45cc0f4c44e2bb6cade0781fc88d2370d4b3dd57c5e23829b`  
		Last Modified: Tue, 03 Feb 2026 09:59:43 GMT  
		Size: 5.2 MB (5213330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:069d4a2b03e22861207ab08d6f27302b412b036cbf0cee701460c536782dbdcb`  
		Last Modified: Tue, 03 Feb 2026 09:59:43 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:fb6c6ca8f88b92ccb231f586645ec7b72072c3082d851e4fe01107f3dbb830bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189909492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454d681981248205ad4fd189842d61bcf2a6c17a2cd10b722dd55aab40272817`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 21:18:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 21:18:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 21:18:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 21:18:34 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 21:18:34 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 21:34:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 21:34:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 21:34:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 21:34:38 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 21:34:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929c7ecf56a52879f53fc321620a27e7c3b04a5166da71501974d2aac3a52dc4`  
		Last Modified: Thu, 05 Feb 2026 21:23:57 GMT  
		Size: 90.8 MB (90752874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f3500bf82e850515aaf4047d41e12f3a9ba3003c52b8064edd9241c98d7e22`  
		Last Modified: Thu, 05 Feb 2026 21:38:14 GMT  
		Size: 70.9 MB (70879185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5483642d9e39d2360695a28875d6826e74766e12ba8bf8d704f8ce57d30fe62d`  
		Last Modified: Thu, 05 Feb 2026 21:38:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f253aee1c6681b3fec5608c40c29d78df4af842b8c5d51173cc1ecdc73f1e7`  
		Last Modified: Thu, 05 Feb 2026 21:38:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c03cebc966b1a7925f8364991614cfa0781cc059d754198435be668313d33f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f204806b71becf3015e4b5195631abbf6926e80bb86fba6e1715449e685dfc`

```dockerfile
```

-	Layers:
	-	`sha256:47245c383d018a3d924de085c39c18d6f1f6350d778826fe429080311e2e7c07`  
		Last Modified: Thu, 05 Feb 2026 21:38:04 GMT  
		Size: 5.2 MB (5197122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:823e95cd239b6b1c9929889d0ff2bb74398482ecbd6bc72f265c230080c4ec57`  
		Last Modified: Thu, 05 Feb 2026 21:38:02 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:132210771cc44be11dd446c0b4712297a1bbd908ecd557a74ad5e7f405b3a059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191002946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d93c2c0f5d7649712bc4706e27b69cde7d25261f7da25be165a55e08cc10cf4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:06:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:06:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:06:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:06:27 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 05:06:27 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:07:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 05:07:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 05:07:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:07:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:07:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635f4900007f98e7f67419952a5a5a7cfdb2468fd30b472fb66d39a7f43c9064`  
		Last Modified: Tue, 03 Feb 2026 05:07:05 GMT  
		Size: 88.2 MB (88210676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d30b209aae8bc669b0bd50434d6ee84ea84f787f6df05cae709c30d051049c`  
		Last Modified: Tue, 03 Feb 2026 05:08:02 GMT  
		Size: 73.0 MB (72953079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a486f37d7d2af469188912a9690b840325e5a0764d0c91de82781b4c20977006`  
		Last Modified: Tue, 03 Feb 2026 05:08:00 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08de98eadaf4068385e2da17c6cf8ab68e9e0ad636cee4506ae93ea7a43a839`  
		Last Modified: Tue, 03 Feb 2026 05:08:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aaf0a2e9a57c1ac7fb2b851e5af2b7902d634509e0587df63197591e016c26d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00691f834f99bc6a50af25c515ace731396993a6ddd728131355876b06633866`

```dockerfile
```

-	Layers:
	-	`sha256:225f2c7e702efdb02f2d5e367bbcd1eed2f526c05eb65bde9e53289653515e99`  
		Last Modified: Tue, 03 Feb 2026 05:08:00 GMT  
		Size: 5.2 MB (5206121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67b06be872398bfc61363656079194843ceeafa2a8f4f82b797bb58d6a96ac3f`  
		Last Modified: Tue, 03 Feb 2026 05:08:00 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json
