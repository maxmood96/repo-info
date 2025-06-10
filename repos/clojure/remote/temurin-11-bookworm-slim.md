## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:662791f9986f29db59d8d180844ffa4ef49b1b0319968278d487b60bcaaa0861
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

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:488aba0b7ede0282a7f321e4545a9ff4575739facd1d9b489da689178a77144f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243391424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:841bd65e0963e16d6813db6fa33e7e2821c4319b6689509470d2daa41765bd09`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8feef64b43de6be87bc50e51cc712323da91670b4ed80bf0bcbce3800b2bbf`  
		Last Modified: Mon, 09 Jun 2025 19:56:29 GMT  
		Size: 145.6 MB (145635655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8afcadb9a14aff9c9fb23d9350087f61fb5e52a6e0ecd196237c91e490c5c4`  
		Last Modified: Mon, 09 Jun 2025 19:56:30 GMT  
		Size: 69.5 MB (69529794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e82cdd8905d028a8af44957b39b273760c6815f470da6f8420db5adedf88e1`  
		Last Modified: Mon, 09 Jun 2025 17:22:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7e50bdfb5fbf0079aa527ef387aadd11d1da339a25e4f6f94d3c6dba3a59469a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5144339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae9f77d4693d51beee3914f7ce597d2956b859832602d4ba7277bf903708eb4`

```dockerfile
```

-	Layers:
	-	`sha256:38a0c55d494b83f692f3f926ffcb1e20cd116ff030e32c36c926bf985c5b30ad`  
		Last Modified: Mon, 09 Jun 2025 18:35:00 GMT  
		Size: 5.1 MB (5130029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecb4c11fb8a936765fafaa25a5e021c4508fef01c92464bc4b7a0cf393410350`  
		Last Modified: Mon, 09 Jun 2025 18:35:01 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1be65b8f4eb8a84a089e98c4391388a4f277716fb8c696eb010f235dbd7c9be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239877286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b1a5451a9d9243f5afc3bf2a70978643b83ee87e631c18f036bd0bb42c62e5`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fefc44eaff424442f81822836abca91702f398096a9228568e0ead8c9faa1d`  
		Last Modified: Tue, 03 Jun 2025 13:57:49 GMT  
		Size: 142.4 MB (142420640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bf551b01bbde908093d88703e0e3dd52ba8f1d78d5fd40c18c48b5b98d4f1a`  
		Last Modified: Mon, 09 Jun 2025 17:40:27 GMT  
		Size: 69.4 MB (69390721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c48e177ff6abb3f3ecf318d9564ad018331787b77134836f7263619de68284`  
		Last Modified: Mon, 09 Jun 2025 17:39:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5e87e2b2b0941a630d8d90c0b7ac11a3df9a7c55af11bbe42fab67e561b2c51c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3926e02db485db03b923da8be00cf58cd3205bba5823724fcbe96c42015364f8`

```dockerfile
```

-	Layers:
	-	`sha256:ab8cd8c7fd0dbc2203e83af6fad3719b9d0177f828fbdb50aa2c98145331f0f4`  
		Last Modified: Mon, 09 Jun 2025 18:35:07 GMT  
		Size: 5.1 MB (5136408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aa3f8af0fab8300b09982b611b94154a47945aca760e67d26deca9971947648`  
		Last Modified: Mon, 09 Jun 2025 18:35:08 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:76ac6827658e18b18068a5d147e67edf37a9584049ca7bd88254f03c821c45ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240223816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1895873cf22c6e78943e425efe146ea53b0560bd4887c1bb1d9c7af2c7ca0ff`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb70de7f1ea6e9e8fa70cca464f19bf365abae7dceabc396212b1df21d889e84`  
		Last Modified: Mon, 09 Jun 2025 19:57:17 GMT  
		Size: 132.8 MB (132810522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b008591cc668816df7b9b1458366611f9333a294df6e078c359a9751b55d510`  
		Last Modified: Mon, 09 Jun 2025 17:52:51 GMT  
		Size: 75.3 MB (75345736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3edb69239a815a34f872689ec77182b81ec73bb48377e5e64c020b314df5e0`  
		Last Modified: Mon, 09 Jun 2025 17:52:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5d7a14a02fff5ada9a249008be160f67690f7ce9e5c5f5fcbdd75f432abf37a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5148930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9801cb451d24387728ba6deaf5bb4d95a642e03c3b8f564f213a775e7b73e6fb`

```dockerfile
```

-	Layers:
	-	`sha256:7ef347d42bef884146ce307be07817bd8ed860d2afb1102c6a09df32fb8531aa`  
		Last Modified: Mon, 09 Jun 2025 18:35:17 GMT  
		Size: 5.1 MB (5134572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d42d1347d9e8a32ee3d28321b01c91d18d7de494ca8027799dfeb66dc3c01ed1`  
		Last Modified: Mon, 09 Jun 2025 18:35:18 GMT  
		Size: 14.4 KB (14358 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:91e09dc52cce5ddc5b643aa9ac92bec14f8d9a092352984d884ecfd00dcf20de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220802828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d177724cc2ec02d7e5873f6d568a0fcdafa7b46e1e6da95b15229e8405355a8`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed11ad230f06796b3ae1c13456129099ee497fa349ff5586d1c755ec5be7b03`  
		Last Modified: Tue, 03 Jun 2025 06:01:19 GMT  
		Size: 125.6 MB (125585354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39ce8a54a2e3ae5e7052ca7d4cb50087d92a378888b8babeda1609df3853008`  
		Last Modified: Mon, 09 Jun 2025 18:42:11 GMT  
		Size: 68.3 MB (68334022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32961b909de7b4caed8614181b75ec9585376f14c5d9c670da282560905461a7`  
		Last Modified: Mon, 09 Jun 2025 18:42:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7700f9715d3e38b8084fd4ab4bc2ed36f9ce7ea015dc8b11b514f518abb6a209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83bc70ffb0d491585ff3236741b6a73cbfe1bd19f5ea34cc6a8fbf137d737c3e`

```dockerfile
```

-	Layers:
	-	`sha256:3844a2f6e4050f7d0d721e20e3eb00d4cdedd56d373b67a3421dac6bd46a0dc6`  
		Last Modified: Mon, 09 Jun 2025 21:34:50 GMT  
		Size: 5.1 MB (5121354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81aa0b96c9e7f858734304e7722ab4ed20859823b0cbd8f4e2ef2d22273cc866`  
		Last Modified: Mon, 09 Jun 2025 21:34:51 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json
