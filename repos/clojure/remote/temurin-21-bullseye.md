## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:52b1d1d44b4bce067c3acbf34e886f37153f22b16b3e9ce825e27e104633f5d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:cf48b0fd182922868f7a5f6fa467e578da92b7c1a058e3787d65f7fdcf8979bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281123580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88f0d223da1bf50ef52126bee0c884ffdab8b9e3b5434a3767e0137646abd16`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:55:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:55:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:55:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:55:59 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:55:59 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:56:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:56:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:56:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:56:12 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:56:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99fe79729a6949206b3bdaf7cb4810b92af532cb3812eb4d713eadefb13c550`  
		Last Modified: Thu, 06 Nov 2025 04:29:53 GMT  
		Size: 157.8 MB (157804746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046b2d6e0eb3a1d4aefc5d6faf80afc4c7440287d08bb07e59ca24245d7a0944`  
		Last Modified: Tue, 04 Nov 2025 00:56:50 GMT  
		Size: 69.6 MB (69561101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d4e99e77361b308d1bc87e5f080fd0d15f59a2468bd8001fffa42fe2ca4aa6`  
		Last Modified: Tue, 04 Nov 2025 00:56:42 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b090c29a7885154db2ec78b8981918328264c652364cfc8e132f32d7ac9865f8`  
		Last Modified: Tue, 04 Nov 2025 00:56:42 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:69ed1ee41eb7360efd0d67c1a7275f1d3e4442d1de091448a8d091acbc0d0ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7414547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189944b9b5e04a75a841404fee7d84d4c0930b29be9b6d4856b3eaebd8f1d7e0`

```dockerfile
```

-	Layers:
	-	`sha256:8141900e5523b9bd5528dc42ded37c6b8e63ea3e72c529db5ecbc8dd2ff0c482`  
		Last Modified: Tue, 04 Nov 2025 10:42:32 GMT  
		Size: 7.4 MB (7398769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667faf7ba05db62b92af52665da0c964c4b296a1cb25fb16b423b0510453f846`  
		Last Modified: Tue, 04 Nov 2025 10:42:32 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cc1756277d290a013fc784e563c597bd6351e754ff1f87e94a44e5c65db02497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278028490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b6654fbf14661737d115f86d64a6919f7c80da7508d59a274b74015b5012c6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:56:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:56:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:56:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:56:48 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:56:48 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:57:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:57:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:57:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:57:03 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:57:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272e27e9493fe0f5f47319898252f6dee4d66bcab754adb51612f0bad79369a6`  
		Last Modified: Tue, 04 Nov 2025 00:57:28 GMT  
		Size: 156.1 MB (156081259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc82dfadec8278dfd9aff17d8db727d34698ad191fddfabaccd73b882c80f50`  
		Last Modified: Tue, 04 Nov 2025 00:57:39 GMT  
		Size: 69.7 MB (69688226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4d1caa0e4ba2f8c357eb89aed85fa439d54e429d467c665d5e9c3ae0b9dcca`  
		Last Modified: Tue, 04 Nov 2025 00:57:33 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256f6d97ea002aecbfa3e81d48d3fd5bd6f2e7a113a207022a71126f09a1ae54`  
		Last Modified: Tue, 04 Nov 2025 00:57:33 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2587b840b6b7d9280e1497589c1eb8a7e1c1317242d4ac1ad165f4af7f75e562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d04be585b73b47715b868d5e6b46fec2f12bb1720ebe0a2a6b8b03c2592174`

```dockerfile
```

-	Layers:
	-	`sha256:5b23e7054e8a1c596636900596ba6ffd94032f4d011d88d4809aef47973d6ea6`  
		Last Modified: Tue, 04 Nov 2025 10:44:24 GMT  
		Size: 7.4 MB (7403868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63fdf799a2dfc3478aac35dc9bfcbc5bb7d8d0d3fda4dda9b46b267a0e420a96`  
		Last Modified: Tue, 04 Nov 2025 10:44:25 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
