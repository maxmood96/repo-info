## `clojure:temurin-17-trixie-slim`

```console
$ docker pull clojure@sha256:c8fef21cf6b71ad72cd7d2476d445496c1e88cee5538f44662fb1240a05caca5
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

### `clojure:temurin-17-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:60ca3027ae5c493d05311008c9209c75f53380340e8cd4ee1d295e0f6dee5ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246618415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2c4e136c61b1f3a99913a69123b8297a567ad809aab580dfc34d9defc3d8d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:39:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:39:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:39:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:39:27 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:39:27 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:39:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:39:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:39:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:39:44 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:39:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74baf9d155e1f8530388a48f560b571b4e03d3529678ef97e27fd2c52da7cbbc`  
		Last Modified: Fri, 12 Dec 2025 02:10:04 GMT  
		Size: 144.8 MB (144847921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb360ceb54dcd42d2038472c7ecd9f8e3ceb6924af36e982ec504c51ed98ad4f`  
		Last Modified: Thu, 11 Dec 2025 22:40:19 GMT  
		Size: 72.0 MB (71992959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88a87b274b2d63c784b87fb4e76c1c737dd0ece022fa2f5d22a3f02b2007383`  
		Last Modified: Thu, 11 Dec 2025 22:40:12 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9fd299c195771b549a131cc8b8526709cecddbed3a369938ceda247d6e62d0f`  
		Last Modified: Thu, 11 Dec 2025 22:40:12 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:255f9aafd3c1e1e6cd5feafa50bc92bc41252560ec3f87b3d05d84f49d0dc457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abec35fdabf531ddcade52e9210561e87de533c4b0354cf6bb4f3870ca749d13`

```dockerfile
```

-	Layers:
	-	`sha256:2991b0fefc4e642a3c4f1deaec4bef67d2b34cdcb80828577e37e6151f7d883d`  
		Last Modified: Fri, 12 Dec 2025 01:39:53 GMT  
		Size: 5.3 MB (5256199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b00e0b1bb268f41f6409e831dec902516ab55136ed0b3a3ed89d0cda699e5ce`  
		Last Modified: Fri, 12 Dec 2025 01:39:54 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:40a86e5ab2aa9df1db6f6dc50415003852cf252981392207ca41030e7a27c87f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245626356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df70bce8de961ef17f69d55fce2d5da0ff05fac0403dde9985ccfb88f08acb76`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:38:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:38:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:38:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:38:20 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:38:20 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:38:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:38:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:38:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:38:38 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:38:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f5fb78f89688f223affa3e4a94f56f5128989d11736e0c268974d226a30186`  
		Last Modified: Fri, 12 Dec 2025 02:10:41 GMT  
		Size: 143.7 MB (143679936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2a756f65ee33e92c052dcf258802e056b068fdfeeb791b89a23afb042a2602`  
		Last Modified: Thu, 11 Dec 2025 22:39:14 GMT  
		Size: 71.8 MB (71806752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b9e5873da10e14d158eff967cc567eeb0cf3d4f59e7ad3cd2781af07b4944d`  
		Last Modified: Thu, 11 Dec 2025 22:39:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f7c799d4eeb3fca2aeebeb9febfa91bb0227a558bca3e099fd1bc815b36839`  
		Last Modified: Thu, 11 Dec 2025 22:39:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6c8045b6a8e51d7f14484912e61687ea8b1e3a2550c0b347bf132b581981d5fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329976c1537b25b735cf32bcf1672c530d0c00870f143969523a75289676641d`

```dockerfile
```

-	Layers:
	-	`sha256:dc328eced56ad63e326ff805283a4863607a51b0aa74b1bcab7274df53d7e1a9`  
		Last Modified: Fri, 12 Dec 2025 01:39:59 GMT  
		Size: 5.3 MB (5261968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f479fa99cf5a669745297f2e43d982f005443b7ff88e57a0ca4bc8c4a6812566`  
		Last Modified: Fri, 12 Dec 2025 01:40:00 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:275c0b28ce6bb676a7f7cccb7bc53cd313d54c7fbcdaa893db5f6f15bf1b9be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255510267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932f9c4f8a5b7c21cb4e9647bd93f3177b3e019234dd3f66b625500b98ba92fe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 03:51:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 03:51:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 03:51:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 03:51:36 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 09 Dec 2025 03:51:37 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:58:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:58:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:58:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:58:33 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:58:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bf16378c0060db84f932d737d6c281316c915f7a3a4ce2efa43f2817d95192`  
		Last Modified: Tue, 09 Dec 2025 03:56:09 GMT  
		Size: 144.5 MB (144525257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fed25143abd98e72fc53289d37c2f7e95398d723672b2a4b60a1469bf0bb1c3`  
		Last Modified: Thu, 11 Dec 2025 22:59:32 GMT  
		Size: 77.4 MB (77387078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bffdceb5f3b2f6971b30e56e87453acb803d78e5f03594b02cb2ce686d0a6fe9`  
		Last Modified: Thu, 11 Dec 2025 22:59:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aede364f5c686e1bd89af9da96d60b8c4c6ce9bdbed96941741861c16ed8456f`  
		Last Modified: Thu, 11 Dec 2025 22:59:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:406dc9e3c43d2bea02ee7963ead6295bb7ca7aff6bedb723c40fbda4e6a3c78d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42babb8fa219f653fd2da2866b480108d3d3bc1789a6a5754f7f1304aba1c207`

```dockerfile
```

-	Layers:
	-	`sha256:68b510cf8a15cd755c979cea86df6599cc24cb9b6f2b7fb5df68d3e97d0b2052`  
		Last Modified: Fri, 12 Dec 2025 01:40:07 GMT  
		Size: 5.3 MB (5260570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4be608386f1760b8801ac6c9c37bf13ff23162980a50fe98dca37f25b09ca770`  
		Last Modified: Fri, 12 Dec 2025 01:40:08 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:dab5c1b25506b2b223e1f68d41c84476f98742f067e4c90bd73ea4f5c3684553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241041888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6108397a705ab2300207842728e2dad09e68b3253891debbf0879d7a3f47ba4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Sat, 13 Dec 2025 18:46:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 13 Dec 2025 18:46:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 13 Dec 2025 18:46:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 18:46:20 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Sat, 13 Dec 2025 18:46:20 GMT
WORKDIR /tmp
# Sun, 14 Dec 2025 16:08:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sun, 14 Dec 2025 16:08:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sun, 14 Dec 2025 16:08:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 14 Dec 2025 16:08:29 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 14 Dec 2025 16:08:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48c227efd13f09a34b153f418d7d540a21d31aecdd5fd15ad6529d2a559ad99`  
		Last Modified: Sat, 13 Dec 2025 18:52:43 GMT  
		Size: 141.9 MB (141889553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78efe06b7cfaf4c0a1d7b9cae49a177e3d280a75aaa44ac3c8b5fd7d5010d31`  
		Last Modified: Sun, 14 Dec 2025 16:12:22 GMT  
		Size: 70.9 MB (70878139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c104a843b30739f7bfee3c61a26fff06c88fd670d41404c04df29fa3c324cb7`  
		Last Modified: Sun, 14 Dec 2025 16:12:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90fd04a522bed8828fd409c258f0e239327a5178d734162b6d533cd8dd61989`  
		Last Modified: Sun, 14 Dec 2025 16:12:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:199778d736a9b8c008baef05bea93d6cc220f74e6dc39d74cd2636a95bee020b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:079852dd14e8bd31b88c1fbdb5cb07f9daadd0f8defb211e49e675dc1b0dcb6d`

```dockerfile
```

-	Layers:
	-	`sha256:4e5463f6e7dae0c70304f85de141dd7a87b8f3f68a7f4b98a83af8a4ea00dc72`  
		Last Modified: Sun, 14 Dec 2025 19:35:40 GMT  
		Size: 5.2 MB (5243744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d3b7c246e159c516b3d04a32a3ac0fe44bb9992d493b9ac1316f3471b66e8d0`  
		Last Modified: Sun, 14 Dec 2025 19:35:41 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:1c98bf06dac4e686a9719d900a6bc94e5360b4220ab822b7cada808ec36e27f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237647853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec78f2bb38b0f8a0fe4ed6c34e4dd45ebd3d053e7a94999e6fd27c53d40db7f1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 01:28:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:28:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:28:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:28:50 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 09 Dec 2025 01:28:50 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:35:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:35:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:35:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:35:28 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:35:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3260fdadccc7546154b4e7a7be47bf1049c46ad309ddf771b36f324535df05`  
		Last Modified: Tue, 09 Dec 2025 01:29:54 GMT  
		Size: 134.9 MB (134859033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308a944f5b3c33877cb5bbbdd8c185dd3779455451dafba2fb205b547200b97c`  
		Last Modified: Thu, 11 Dec 2025 22:36:07 GMT  
		Size: 73.0 MB (72953380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f7a2c2874635ede9208635df956ad137d3edde4555c70e29681786faaa629b`  
		Last Modified: Thu, 11 Dec 2025 22:35:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f8158d09340b8ee923b746002e4226c221cdb43ea0e08eaeeb56a74fdb35c1`  
		Last Modified: Thu, 11 Dec 2025 22:35:58 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:40c7cb962c555f344d26c5880fa5abbdcf18e7932f940776d002c3d0ab6ef345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5267935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c665e90a999c783b1c93513410a01d8e60b0bebda2b448ed1981b1391acd3ff8`

```dockerfile
```

-	Layers:
	-	`sha256:c41fa339165882a821c45d27b2a7bed3a21074445d627c26e3e1078dc3bcdb39`  
		Last Modified: Fri, 12 Dec 2025 01:40:13 GMT  
		Size: 5.3 MB (5252123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63adc0f672ef9ea158144f7f0b59d41521d13bf52dd1b8e55ebb91cf547ae27a`  
		Last Modified: Fri, 12 Dec 2025 01:40:14 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
